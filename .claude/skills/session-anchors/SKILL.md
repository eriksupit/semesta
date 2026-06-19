---
name: session-anchors
description: Invoke this skill EVERY TIME a session opens or closes, whenever the user says "update memory", "pipeline memory", "update lessons", "update context", "update scope", "catat ini", "simpan insight", "apa yang kamu ingat", "baca memory", or any variant asking Claude to read or write project memory. Also invoke proactively when any significant decision, validated preference, constraint, or lesson emerges mid-session — do not wait until session close. This skill governs ALL reads and writes to context.md, lessons.md, scope.md, and handoff documents in the Semesta Digital vault. It runs with /confidence, /anti-sycophancy, /brave, and /research-before-dispatch — never shortcuts, never hedges, always Priority 1 evidence from actual file reads. Output in formal Bahasa Indonesia saya–Anda.
---

# session-anchors

## Purpose

This skill is the single authoritative interface between the Claude session and the project's persistent memory layer. It governs:

1. **Reading** — loading the four anchor files into working context at session start
2. **Writing** — updating those files with validated decisions, new insights, and scope changes
3. **Auditing** — verifying that what is written matches what actually occurred (no confabulation, no memory-from-chat)

The four anchor files are:
- `/Users/eriksupit/Desktop/superapps/context.md` — active project state, phase by phase
- `/Users/eriksupit/Desktop/superapps/scope.md` — session scope limits, in/out, change history
- `/Users/eriksupit/Desktop/superapps/lessons.md` — validated preferences, anti-patterns, production insights
- `/Users/eriksupit/Desktop/superapps/handoff/HANDOFF-<date>.md` — session state for successor session

These files ARE the project's memory. Nothing that matters may exist only in chat history.

---

## Companion Skills — Always Active

This skill NEVER runs in isolation. The four companions are **co-mandatory**:

| Companion | Role in this skill |
|---|---|
| `/research-before-dispatch` | Every write is a dispatch. Read the actual file before writing any update. Never write from memory of what the file contains. |
| `/anti-sycophancy` | No insight gets written unless it is Priority 1 evidence from this session — not because it sounds right, not because the user seemed to validate it loosely, not because it "probably" happened. |
| `/confidence` | Aggregate confidence >95% required before any write is committed. Sub-95% = loop: re-read the source file, re-examine the conversation, identify the specific gap. |
| `/brave` | No shortcut exits. If updating all four anchor files is the correct action, update all four. Do not stop at two because "the rest probably don't need it." Loop until the work is complete. |

Violation: running any update step without all four companions active is a process failure.

---

## Trigger Matrix

| Trigger phrase / condition | Action |
|---|---|
| Session opens (any sesi) | READ protocol — load all four files before first substantive response |
| "pipeline memory", "update memory", "update dokumen" | WRITE protocol — full audit + update all four files |
| "update context" / "update scope" / "update lessons" | WRITE protocol — targeted file + audit for cross-file consistency |
| "catat ini", "simpan insight", "remember this" | WRITE protocol — capture specific item to lessons.md + cross-reference |
| "apa yang kamu ingat", "baca memory" | READ protocol — report from actual file reads, not from recall |
| Significant decision validated by user ("approve", "kunci", "go") | WRITE protocol — capture decision to relevant anchor file immediately, not at session end |
| Session close / "buat handoff" | FULL CLOSE protocol — all four files + handoff document + initial-prompt |
| Mid-session: new constraint, new preference, new anti-pattern observed | WRITE protocol — targeted entry to lessons.md, cross-reference context.md if phase changed |

---

## Protocol A — READ (Session Open or Memory Query)

Run in this order. Do not reorder. Do not skip.

```
Step 1: Read scope.md
        -- Understand: what is in scope this session, what is explicitly out.
        -- If scope.md is stale (references a completed session), flag it before proceeding.

Step 2: Read context.md
        -- Understand: current active phase, state of each work stream, open questions.
        -- Note any Context blocks marked Active vs Completed.

Step 3: Read lessons.md
        -- Load: validated preferences, anti-patterns, production insights.
        -- These are standing constraints that apply without the user needing to re-state them.

Step 4: Read the most recent handoff document
        -- Path: /Users/eriksupit/Desktop/superapps/handoff/HANDOFF-<most-recent-date>.md
        -- List directory if date is unknown: list handoff/ and pick the latest by filename date.
        -- Load: session goal, decisions, current state, acceptance criteria, anti-pitfalls.

Step 5: Synthesize
        -- Form a one-paragraph internal summary: what is the mandate, what are the active constraints,
           what decisions are locked, what is the next step.
        -- Confidence gate: if any anchor file was missing or unreadable, report the gap explicitly
           before proceeding. Do not invent a substitute from memory.
```

**Output to user after READ:**
One sentence confirming bootstrap is complete: "Bootstrap selesai. [One-line mandate summary]."
Do not narrate which files were read — that is noise. Confirm + mandate only.

---

## Protocol B — WRITE (Memory Update)

Run in this order. Invoke `/research-before-dispatch` at Step 1. Invoke `/confidence` at Step 4.

```
Step 1: Invoke /research-before-dispatch
        -- Read the actual current content of every file to be updated.
        -- Do NOT write from memory of what these files contain.
        -- Memory of file contents is Priority 5 (model recall) -- not sufficient for any write.

Step 2: Audit the session conversation
        -- Identify every item that qualifies for memory capture:
           (a) Decisions explicitly validated by user (words: "approve", "kunci", "go", "oke", "update")
           (b) Preferences stated or confirmed (positive or negative)
           (c) Constraints added or lifted
           (d) Anti-patterns observed (Claude error that user corrected)
           (e) Production insights that would change behavior in a future session
           (f) Phase changes (new context block needed)
           (g) Scope changes (in/out scope list modified)
        -- DO NOT capture: things that seem like they should be remembered but were not
           explicitly validated. Speculation about user preference is Priority 5.

Step 3: Draft updates per file
        -- context.md: update the relevant Context block. If phase changed, add new Context block.
          Mark completed phases as Completed -- do not delete.
        -- scope.md: update the Scope Aktif section and append to Riwayat Scope table.
        -- lessons.md: append new entries to the correct subsection. Add to Update Log.
          Do NOT overwrite existing entries -- only append or correct with explicit evidence.
        -- handoff/: create HANDOFF-<date>.md if session is closing. See FULL CLOSE protocol.

Step 4: Confidence gate (/confidence)
        -- For each drafted update, ask: is this grounded in Priority 1 evidence
          (actual conversation events, actual file content read this step)?
        -- If any update rests on Priority 4 (user claim not verified) or Priority 5 (model recall):
          downgrade to "working hypothesis" and flag it as unconfirmed in the written entry.
        -- Aggregate confidence >95% required before writing. Sub-95%: identify the specific gap,
          re-read the source, re-examine the conversation. Loop until >95% or escalate with
          named gap + provisional entry.

Step 5: Write files via Filesystem connector
        -- Write each updated file. Do not batch silently -- confirm each write with file path.
        -- After writing, read the file back (head 10 lines) to verify the write succeeded.

Step 6: Cross-check consistency
        -- context.md phase state must be consistent with scope.md Riwayat Scope table.
        -- lessons.md Update Log must reflect this session's date.
        -- If inconsistency found: fix the lagging file before reporting done.

Step 7: Report to user
        -- List each file updated with one-line summary of what changed.
        -- Flag any items that were captured as "working hypothesis" (not yet Priority 1 confirmed).
```

---

## Protocol C — FULL CLOSE (Session End)

Run at every session close. This is non-negotiable — session is not closed until all items pass.

```
Step 1: Run Protocol B (WRITE) for context.md, scope.md, lessons.md

Step 2: Update Superapp -- Home.md
        -- Add any new files created this session to the navigation table.
        -- Update the Status Proyek table.

Step 3: Produce HANDOFF-<date>.md
        -- Save to: /Users/eriksupit/Desktop/superapps/handoff/
        -- Required sections (all mandatory, none optional):
           ## Goal (Session Goal + Ultimate Goal + Linkage)
           ## TL;DR (3-5 sentences: what was done, what is complete, what is the gap)
           ## Context & Decisions (every significant decision + evidence source)
           ## Current State (per-file status, open questions)
           ## Next Steps (mandate for next session + explicit NOT-in-scope list)
           ## Anti-Pitfalls (constraints the next session must not violate)
           ## Acceptance Criteria (verifiable checklist for next session's goal)

Step 4: Produce INITIAL-PROMPT-<date>.txt
        -- Save to: /Users/eriksupit/Desktop/superapps/handoff/
        -- Required sections (all mandatory):
           Mandatory -- Read FIRST (skill invocations)
           Session identity + mandate
           Goal (Session + Ultimate + Linkage)
           Working Rules / Truth Source
           Bootstrap Reading (ordered file list)
           After Bootstrap -- STANDBY
           Special Concerns / Pre-Execute (all active constraints)
           Communication Rules
           Vault Connection
           End-of-Session Closure Deliverables (this section, recursively)
           Anti-Flailing Reminder

Step 5: Confirm both file paths to user
        -- "Sesi ditutup. Handoff: [path]. Initial prompt: [path]."
        -- Session is NOT closed until this confirmation is delivered.
```

---

## Write Quality Rules

These rules apply to every write operation across all anchor files.

**Rule 1 — No confabulation.**
Every written entry must trace to a specific event in the current session conversation. If the trace cannot be named, do not write the entry.

**Rule 2 -- Append, do not overwrite.**
Existing entries in lessons.md are not overwritten unless there is explicit Priority 1 evidence that the entry is wrong. Add new entries; mark corrections as "(corrected YYYY-MM-DD: [reason])".

**Rule 3 -- Specificity over generality.**
"User prefers short answers" is useless. "User answered 'approve' to a 3-sentence recommendation after rejecting a 12-sentence one on the same topic (2026-06-08)" is actionable. Write the specific event, not the abstraction.

**Rule 4 -- Negative lessons are first-class.**
Anti-patterns and mistakes Claude made (and the user corrected) are the most valuable entries. Capture them explicitly: "Claude used 'Nahdliyin' in a Midjourney prompt — user corrected: not recognized by model, replace with concrete facial features. Evidence: Session 2 revision."

**Rule 5 -- No implicit scope expansion.**
Writing a new item to context.md as an "Active" phase without the user having confirmed that mandate is a scope violation. New context blocks are written as "Pending — confirmed by user on [date]" until the mandate is explicit.

**Rule 6 -- Confidence annotation.**
Any entry that is less than Priority 1 confirmed must be annotated: `[UNCONFIRMED — working hypothesis, verify next session]`. This prevents stale hypotheses from accumulating as if they were facts.

---

## Common Failure Modes to Refuse

| Failure mode | Why refused |
|---|---|
| Writing lessons from memory of the conversation without re-reading conversation | Memory is Priority 5. Re-read the actual messages. |
| Updating context.md without reading its current content first | Produces overwrites or duplicates. Always read before write. |
| Capturing "probably validated" preferences | Only explicitly validated entries are written. "Approve", "kunci", "go" = validated. "Seems like" = not written. |
| Skipping lessons.md update because "nothing significant happened" | Run the audit (Protocol B Step 2) before concluding nothing qualifies. |
| Writing the handoff from memory of what was done | Read the actual vault files. State what files actually exist at path. |
| Marking session closed before both handoff + initial-prompt are confirmed | Session is not closed. Produce them first. |
| Updating only one or two files when all four need updating | /brave: loop until all four are done. Partial update = incomplete. |

---

## Output Language

All user-facing output from this skill: formal Bahasa Indonesia, saya--Anda register.
All file content written to vault: English (per project instruction standard).
Exception: lessons.md entries may be in Bahasa Indonesia if the insight is better captured in that language — annotate with `[BI]` tag.
