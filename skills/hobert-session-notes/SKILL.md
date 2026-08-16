# Hobert Method — Session Notes Skill

## Trigger
Use this skill when a mentor pastes raw session notes and wants observations categorized and saved to a student's Hobert Method files. Triggers include phrases like "here are my notes from today", "log this session", "update [student]'s files", or any block of raw session notes pasted into the conversation.

---

## What This Skill Does

1. Identifies the student name (ask if not clear from the notes)
2. Locates the student's folder inside `C:\Hobert Method\Students\{StudentName}\`
3. Reads all seven category files for that student
4. Analyzes the raw session notes and categorizes each meaningful observation
5. Appends new observations as bullet points under the `## Observations` section of the relevant files — never overwrites existing content
6. Reports a clear summary of what was added and which categories were updated

---

## Seven Categories — Definitions

Use these definitions to decide which file each observation belongs to. An observation may apply to more than one category — if so, add it to each relevant file.

| Category | File | What belongs here |
|---|---|---|
| **Trust-Building** | `Trust-Building.md` | Rapport, honesty, openness, vulnerability, moments of connection or disconnection between student and mentor |
| **Anxiety-Reduction** | `Anxiety-Reduction.md` | Signs of stress, worry, avoidance, nervousness; also moments of calm, successful coping, or de-escalation |
| **Engagement** | `Engagement.md` | Participation, focus, curiosity, responsiveness, willingness to try activities or conversations |
| **Humor** | `Humor.md` | Jokes, laughter, playfulness, sarcasm, teasing — and what role humor plays for the student |
| **Exposure** | `Exposure.md` | New experiences, places, situations, or topics the student encountered; reactions to novelty or unfamiliarity |
| **Identity-Development** | `Identity-Development.md` | How the student describes themselves, interests tied to self-image, cultural/family identity, self-perception shifts |
| **Behavioral-Signals** | `Behavioral-Signals.md` | Body language, mood shifts, avoidance behaviors, emotional outbursts, patterns that signal underlying needs |

---

## Step-by-Step Instructions

### Step 1 — Identify the student
- Look for the student's name in the session notes (e.g., "Session with Adrian", "Adrian today", etc.)
- If the name is not clear, ask: *"Which student are these notes for?"*

### Step 2 — Locate the student folder
- The folder path is: `C:\Hobert Method\Students\{StudentName}\`
- Use the Read tool to verify the student's folder exists and contains the seven .md files
- If the folder does not exist, ask the mentor whether to create it before proceeding

### Step 3 — Read all seven files
- Use the Read tool to read all seven category files for the student
- Note what observations already exist under `## Observations` so you do not duplicate them

### Step 4 — Parse the raw session notes
- Read through the notes carefully
- Extract every discrete observation — a sentence or short phrase describing something the student said, did, felt, or reacted to
- Ignore logistical details (e.g., "we met at 3pm", "session was 45 minutes") unless they are behaviorally significant

### Step 5 — Categorize each observation
- Assign each observation to one or more of the seven categories using the definitions above
- When in doubt, lean toward including rather than excluding — it is better to over-capture
- Write each bullet point in past tense, e.g.:
  `- [2026-05-25] Laughed at mentor's joke about basketball and made one back — first time initiating humor.`
- If you know the session date from the notes, prepend it in YYYY-MM-DD format. If not, use `[Date unknown]`

### Step 6 — Append to the correct files
- Use the Edit tool to append each new bullet under the `## Observations` section in the correct file
- Place the new bullet after the last existing bullet (or right after `## Observations` if the section is empty)
- Do NOT delete or modify any existing bullets
- Do NOT change any headings or other sections of the file

### Step 7 — Output a summary
After all edits are complete, report back to the mentor with:

```
## Session Notes — Update Summary

**Student:** [Name]
**Session date:** [Date or "not specified"]

### Categories Updated
- **[Category]** — [1-sentence description of what was added]
- **[Category]** — [1-sentence description of what was added]

### Categories with No New Observations
[List any of the 7 that had nothing to add this session]

### Notes
[Flag anything ambiguous, any observation you weren't sure how to categorize, or any notable pattern worth highlighting for the mentor]
```

---

## Rules

- **Never overwrite.** Only append. Existing observations are permanent.
- **One bullet per observation.** Do not combine multiple distinct events into one bullet.
- **Be specific.** Bullets should describe what actually happened, not vague impressions.
- **Keep bullets concise.** One to two sentences max per bullet.
- **Ask before creating new student folders.** Do not silently create a new student's file structure without confirming with the mentor first.
- **If a category file is missing,** flag it to the mentor rather than skipping silently.
- **The base path is always** `C:\Hobert Method\Students\{StudentName}\` — never guess or infer a different location.
