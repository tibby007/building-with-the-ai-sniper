# Example Skill: Meeting Notes Formatter

<!--
  THIS IS AN EXAMPLE SKILL. 
  
  A skill is just a markdown file (SKILL.md) that tells Claude how to do 
  a specific task really well. Think of it like a recipe card. Claude reads 
  the instructions every time it runs the skill, so it performs consistently.
  
  Skills live in folders inside your project's skills/ directory.
  The folder name becomes the skill name.
  
  Structure:
    skills/
      meeting-notes/        <-- This folder name = skill name
        SKILL.md            <-- The instructions (required)
        templates/          <-- Optional supporting files
        examples/           <-- Optional examples
  
  Below is a real, working skill you can use as a starting point.
  Modify it or delete it and create your own.
-->

## Purpose

Format raw meeting notes into a clean, actionable summary.

## When to Use This Skill

Use this skill when the user provides meeting notes, call recordings transcripts, or rough notes from any meeting or conversation that needs to be organized.

## Input

The user will provide one of:
- Raw typed notes from a meeting
- A transcript from a call recording
- Voice memo transcription
- Bullet points or scattered thoughts from a conversation

## Output Format

Always produce the summary in this exact structure:

### Meeting Summary

**Date:** [Extract or ask]
**Attendees:** [Extract from notes or ask]
**Topic:** [One line summary]

### Key Discussion Points

[3-5 bullet points capturing the main things discussed. Each bullet should be 1-2 sentences max.]

### Decisions Made

[List any decisions that were finalized. If none, write "No final decisions were made."]

### Action Items

| Task | Owner | Deadline |
|------|-------|----------|
| [What needs to be done] | [Who's doing it] | [By when] |

### Follow-Up Needed

[Anything that was left unresolved or needs a future conversation.]

## Rules

1. Keep the summary under 500 words total
2. Use the person's actual names, not "the team" or "participants"
3. If the notes are messy or unclear, make your best interpretation and flag anything you're unsure about
4. Action items MUST have an owner. If one isn't clear from the notes, flag it as "TBD"
5. Don't add information that wasn't in the original notes
6. Write in plain language. No corporate jargon.

## Example

**Input:**
"talked to marcus about the website redesign. he wants new homepage done by end of month. i said we need content first. agreed sarah will get copy to us by the 15th. also need to pick a color scheme. marcus likes blue but im pushing for green. will decide next week. oh and the old blog posts need to migrate over too."

**Output:**

### Meeting Summary

**Date:** [Not specified]
**Attendees:** Marcus, Sarah, [Note taker]
**Topic:** Website Redesign Planning

### Key Discussion Points

- Homepage redesign is the priority, with an end-of-month target
- Content dependency identified: can't build the homepage without copy
- Color scheme is undecided between blue (Marcus) and green (note taker)
- Blog post migration needs to be included in the project scope

### Decisions Made

- Sarah will provide homepage copy by the 15th
- Color scheme decision pushed to next week

### Action Items

| Task | Owner | Deadline |
|------|-------|----------|
| Deliver homepage copy | Sarah | 15th |
| Decide on color scheme | Marcus + [Note taker] | Next week |
| Plan blog post migration | TBD | TBD |

### Follow-Up Needed

- Blog migration needs an owner and timeline
- Color scheme meeting needs to be scheduled
