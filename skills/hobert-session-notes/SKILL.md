# Hobert Method — Session Notes Skill

## Trigger
Use this skill when a mentor pastes raw session notes and wants observations categorized and saved to a student's Hobert Method files. Triggers include phrases like "here are my notes from today", "log this session", "update [student]'s files", or any block of raw session notes pasted into the conversation.

---

## What This Skill Does

1. On first use, asks the mentor where they want to store student files on their computer and remembers that location as the base path for all future sessions
2. Identifies the student by their anonymized label (e.g., 8th Grade Mentee #1) — asks the mentor if unclear
3. Checks whether the student folder exists at the base path; if not, asks permission to create it before proceeding
4. Reads all eight category files for that student
5. References the three exemplar mentee profiles to understand the expected quality, depth, and format of observations
6. Analyzes the raw session notes and categorizes each meaningful observation
7. Appends new observations as bullet points under the `## Observations` section of the relevant files — never overwrites existing content
8. Reports a clear summary of what was added, which categories were updated, and recommended next outings or activities based on observed patterns

---

## Base Path Setup (First Use)

On first use, the skill does not assume any file location. Instead it asks:

*"Where would you like to store your student files? Please paste the full folder path on your computer (e.g., C:\Users\YourName\Documents\Hobert Method\Students or /Users/YourName/Documents/Hobert-Method/Students). This will be used as the base path for all student folders going forward."*

Once the mentor provides a path, use it as the base path for all subsequent steps in this session. If the mentor uses this skill again in a future session and the base path is not already known, ask again.

If the mentor is unsure where to store files, suggest: *"You can create a folder called 'Hobert Method' anywhere on your computer — your Desktop or Documents folder works well. Inside it, create a folder called 'Students'. Paste that full path here and we will take it from there."*

---

## Anonymization Protocol

All students in this system are anonymized. Student folders follow this naming format:

`{Grade} Mentee #{Number}` — for example, `7th Grade Mentee #1`, `8th Grade Mentee #2`

- Never use a student's real name in any file, folder, or output
- If a mentor provides real names in their session notes, convert them to the anonymized format before categorizing
- If a new student is being added, ask the mentor to confirm the grade and assign the next available number before creating the folder

---

## Exemplar Student Profiles

Three anonymized exemplar mentee profiles are stored in the Students folder of the GitHub repository:

- `Example - 7th Grade Mentee #1`
- `Example - 7th Grade Mentee #2`
- `Example - 8th Grade Mentee #1`

Exemplar folders are prefixed with "Example -" to distinguish them from real active mentee folders. Never confuse an exemplar folder with a real mentee folder. Before categorizing new session notes, read the relevant category files from at least one exemplar profile to understand the expected format, specificity, and depth of observations. These exemplars represent the gold standard for how observations should be written and categorized. When in doubt about quality or format, match the exemplar.

Note: Exemplar files are available in the GitHub repository. If they are not present in the mentor's local folder, the skill will proceed without them and rely on the category definitions below for guidance.

---

## Eight Categories — Definitions

Use these definitions to decide which file each observation belongs to. An observation may apply to more than one category — if so, add it to each relevant file.

| Category | File | What belongs here |
|---|---|---|
| **Trust-Building** | `Trust-Building.md` | Rapport, honesty, openness, vulnerability, moments of connection or disconnection between student and mentor |
| **Anxiety-Reduction** | `Anxiety-Reduction.md` | Signs of stress, worry, avoidance, nervousness; also moments of calm, successful coping, or de-escalation |
| **Engagement** | `Engagement.md` | Participation, focus, curiosity, responsiveness, willingness to try activities or conversations |
| **Humor** | `Humor.md` | Jokes, laughter, playfulness, sarcasm, teasing — and what role humor plays for the student |
| **Exposure** | `Exposure.md` | New experiences, places, situations, or topics the student encountered; reactions to novelty or unfamiliarity |
| **Identity-Development** | `Identity-Development.md` | How the student describes themselves, interests tied to self-image, cultural or family identity, self-perception shifts |
| **Behavioral-Signals** | `Behavioral-Signals.md` | Body language, mood shifts, avoidance behaviors, emotional outbursts, patterns that signal underlying needs |
| **Family-Context** | `Family-Context.md` | Family dynamics, parental involvement, home environment, sibling relationships, cultural background, family stressors or support systems. Note: observations from this category may also belong in Trust-Building, Anxiety-Reduction, or Behavioral-Signals — cross-post when relevant |

---

## Step-by-Step Instructions

### Step 1 — Establish base path
- If the base path is not already known from this session, ask the mentor for it using the prompt in the Base Path Setup section above
- Confirm the path before proceeding

### Step 2 — Identify the student
- Look for the student's anonymized label in the session notes (e.g., "8th Grade Mentee #1")
- If the mentor provides a real name, convert it to the anonymized format before proceeding
- If the student identity is unclear, ask: *"Which student are these notes for? Please use their anonymized label (e.g., 7th Grade Mentee #1). If this is a new student, let me know their grade and I will assign the next available number."*

### Step 3 — Locate or create the student folder
- Check whether the student's folder exists at: `{BasePath}\{StudentFolder}\`
- If it exists, proceed
- If it does not exist, ask: *"I don't see a folder for [student label] yet. Would you like me to create one now?"*
- If yes, create the folder and generate all eight empty category files inside it using the standard template
- If no, stop and ask the mentor how they would like to proceed

### Step 4 — Read the exemplar profiles
- If exemplar folders are present in the base path, read the category files of at least one exemplar student to calibrate the expected format and depth
- Use the exemplar as the quality benchmark for all observations you write
- If exemplars are not present locally, proceed using the category definitions above as your guide

### Step 5 — Read all eight files for the current student
- Use the Read tool to read all eight category files for the student being updated
- Note what observations already exist under `## Observations` so you do not duplicate them

### Step 6 — Parse the raw session notes
- Read through the notes carefully
- Extract every discrete observation — a sentence or short phrase describing something the student said, did, felt, or reacted to
- Ignore purely logistical details (e.g., "we met at 3pm", "session was 45 minutes") unless they are behaviorally significant

### Step 7 — Categorize each observation
- Assign each observation to one or more of the eight categories using the definitions above
- When in doubt, lean toward including rather than excluding — it is better to over-capture
- Write each bullet point in past tense, e.g.:
  `- [2026-05-25] Laughed at mentor's joke about basketball and made one back — first time initiating humor.`
- If you know the session date from the notes, prepend it in YYYY-MM-DD format. If not, use `[Date unknown]`
- For Family-Context observations that also belong in another category, add the bullet to both files

### Step 8 — Append to the correct files
- Use the Edit tool to append each new bullet under the `## Observations` section in the correct file
- Place the new bullet after the last existing bullet (or right after `## Observations` if the section is empty)
- Do NOT delete or modify any existing bullets
- Do NOT change any headings or other sections of the file

### Step 9 — Output a summary and outing recommendations
After all edits are complete, report back to the mentor with:

```
## Session Notes — Update Summary

**Student:** [Anonymized label]
**Session date:** [Date or "not specified"]

### Categories Updated
- **[Category]** — [1-sentence description of what was added]
- **[Category]** — [1-sentence description of what was added]

### Categories with No New Observations
[List any of the 8 that had nothing to add this session]

### Patterns Worth Noting
[Flag any recurring themes across multiple sessions, emerging interests, behavioral shifts, or anything the mentor should watch closely going forward]

### Recommended Next Outings or Activities
Based on the observations categorized in this session and across the student's full profile, suggest 2-3 specific outing ideas or activity types that could:
- Build on an emerging interest or curiosity observed in this session
- Deepen trust or address anxiety signals that appeared
- Create a meaningful exposure experience aligned with the student's developing identity
- Reinforce skills or behaviors that showed positive development

For each recommendation, briefly explain why it fits this student's current profile.

### Notes
[Flag anything ambiguous, any observation you weren't sure how to categorize, or any concern worth raising with the mentor]
```

---

## Rules

- **Never overwrite.** Only append. Existing observations are permanent.
- **Never use real names.** Always use the anonymized label format.
- **Always ask before creating folders.** Do not silently create a new student's file structure without confirming with the mentor first.
- **Always ask for the base path if unknown.** Never assume or hardcode a file location.
- **One bullet per observation.** Do not combine multiple distinct events into one bullet.
- **Be specific.** Bullets should describe what actually happened, not vague impressions.
- **Keep bullets concise.** One to two sentences max per bullet.
- **Match exemplar quality when available.** If an observation feels too vague compared to the exemplar profiles, rewrite it to be more specific before appending.
- **If a category file is missing,** flag it to the mentor rather than skipping silently.
- **Cross-post Family-Context observations** to other relevant categories when appropriate.
