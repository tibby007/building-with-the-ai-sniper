# Session 4 Student Guide: Memory & Context — Giving Claude a Brain That Never Forgets

**Course:** Building with The AI Sniper
**Session:** 4 of 6
**Your Instructor:** Cheryl Tibbs (The AI Sniper)
**Platform:** AI Junkies University

Keep this guide. Everything we cover in class is here in writing so you can reference it later, build at your own pace, and come back to it any time your AI OS needs a tune-up.

---

## Quick Catch-Up: Where We Are in the Series

If Session 3 was about teaching Claude what to do, Session 4 is about teaching Claude who you are.

Here is where we are in the build:

| Session | Topic | What It Gives Claude |
|---------|-------|---------------------|
| 1 | Foundation Setup | A home base (your project folder + Cowork) |
| 2 | MCPs & Connectors | Hands (ability to take action in the real world) |
| 3 | Skills & Agents | A skillset (repeatable jobs, done your way) |
| **4** | **Memory & Context** | **A brain (permanent knowledge about you)** |
| 5 | Automation Workflows | A schedule (working while you sleep) |
| 6 | Putting It All Together | A full AI operating system |

---

## Prerequisites

Before this session, you should have:

- [ ] Claude Desktop installed and connected to your project folder (Session 1)
- [ ] At least one MCP or connector set up (Session 2)
- [ ] At least one skill in your project (Session 3, even if it's basic)
- [ ] Access to your project folder on your computer

If you are missing any of these, grab the student guides from Sessions 1-3 in the AIJU classroom.

---

## Part 1: The Problem That Memory Solves

Here is what was happening before this session. You open Claude. You start a task. Claude does not know:

- Which of your businesses this is for
- How you like things formatted
- What tone you use
- What phrases you absolutely cannot stand
- That you have been over this same correction four times already

So Claude gives you a technically correct but completely off-target answer. You sigh. You re-explain your context. Again.

That is the memory gap. And this session closes it.

### Two Layers of Memory

There are two tools that work together to give Claude permanent context about you:

**Layer 1: CLAUDE.md (your Brain File)**
A file you write once and keep updated. It holds your permanent baseline: your businesses, your voice, your preferences, your rules. Claude reads this at the start of every single session.

**Layer 2: The Auto-Memory System**
Claude learns from your conversations and saves specific things it has noticed over time. Past decisions, corrections you gave it, project details, where things live. This layer builds on top of Layer 1 automatically.

Together, these two tools mean Claude wakes up knowing you every time.

---

## Part 2: CLAUDE.md — Your Brain File

### What It Is

CLAUDE.md is a Markdown file that lives at the root of your Claude project folder (not inside any subfolder, right at the top level). Claude reads it every time a session starts.

Think of it like the employee handbook you hand a new hire on day one. Except this handbook is about YOU, and Claude actually reads the whole thing before it ever says a word.

### What Goes In It

A solid Brain File has four sections:

**1. Who You Are**
Your name, your role, your businesses, who you serve, where you operate. The basics that should inform every single response Claude gives you.

**2. Your Voice and Style**
How you sound. What kind of language you use. What you never want to see in your content. What your personality is like. Be specific here. Generic style notes produce generic content.

**3. Affiliations and Credentials**
Organizations you belong to, certifications you hold, anything that should show up in your bios or speaker introductions.

**4. Standing Instructions**
Your non-negotiables. Things Claude should always do. Things Claude should never do. Format preferences. Tone rules. Business-specific instructions.

### What It Looks Like

Here is a simplified example based on the instructor's actual Brain File:

```markdown
# About Me

My name is Cheryl Tibbs. I am an international speaker and AI automation trainer
based in Douglasville, GA.

I run three businesses:
- Commercial Capital Connect (CCC): business finance marketplace serving US businesses
- AI Marvels: AI automation agency specializing in chatbots
- EmergeStack Development Company: custom AI automation agency (I am CEO)

---

# My Voice and Style

- Conversational, confident, and direct. No academic tone.
- Blend of street-smart and book-smart. A little sass is fine.
- NEVER use em dashes. Use commas, periods, or parentheses instead.
- NEVER say "y'all" in anything I will publish.
- NEVER use filler words like "straightforward," "genuinely," or "honestly."
- Always use Unicode formatting for public-facing output.

---

# My Affiliations

- BWAI (Black Women in AI)
- ABWA (American Business Women's Association)
- BEFN (Black Equipment Finance Network)
- AACFB (American Association of Commercial Finance Brokers)
- Google AI and Machine Learning certified
- Amazon Machine Learning certified

---

# Standing Instructions

- Keep responses concise unless I ask for detail.
- When I give you content to write, make it sound like me, not a corporate brand.
- If you are unsure which business a task is for, ask me before assuming.
- I am always looking for ways to generate revenue. Keep that lens on.
```

### How to Create Your Brain File

**Step 1:** Open your project folder on your computer.

**Step 2:** Create a new file at the top level of the folder. Name it exactly: `CLAUDE.md` (capital letters, no spaces).

**Step 3:** Write your four sections. Do not overthink this. Write it like you would explain yourself to a new assistant on their first day.

**Step 4:** Save the file.

**Step 5:** Open a new Cowork session and test it. Ask Claude something that requires your business context and see if it uses what you wrote.

### Quick Tips

- Specific beats general. "Never use em dashes" is more useful than "keep it professional."
- You do not have to get it perfect the first time. CLAUDE.md is a living document. Update it when something is not working.
- If Claude gives you an answer that shows it does not know something basic about you, add that information to your Brain File.

---

## Part 3: The Auto-Memory System

Beyond what you write in CLAUDE.md, Claude also creates its own memory files as you work together. This is the auto-memory system.

### How It Works

As you use Claude in Cowork, it notices things worth saving for later:

- You give it feedback. It saves a memory about that feedback.
- You mention a project detail. It saves a memory about that project.
- You reference a resource or tool. It saves a memory about where things live.
- You correct an output. It saves what you corrected and why.

These memories are stored as Markdown files inside a `memory/` folder in your project. The next time you open a session, Claude reads those files and comes in already knowing what it learned before.

### You Can Also Tell Claude to Remember Something Directly

Anytime you want to guarantee something gets saved, just tell Claude:

> "Remember that I always want proposals delivered as PDFs, not Word docs."

> "Remember that Lisa handles all deal intake for CCC and she always leads with the cross-sell check."

> "Remember that I do not say 'customers' in my content. I say 'clients.'"

Claude will create a memory file for anything you explicitly ask it to save.

### You Can Check What Claude Has Remembered

At any point, ask:

> "What do you have in your memory system about me and how I like to work?"

Claude will walk you through what it has stored. This is a good monthly habit.

---

## Part 4: The Four Types of Memory

Claude's auto-memory system has four categories. Knowing the categories helps you understand what Claude is saving and why.

| Memory Type | What It Holds | Example |
|-------------|--------------|---------|
| **User** | Information about you: your role, expertise, preferences, and perspective | "Cheryl is an ENFP who prefers concise responses and thinks in terms of revenue and systems." |
| **Feedback** | Corrections you gave and approaches that worked well | "Never start a LinkedIn post with a question. Cheryl finds it annoying. Confirmed by correction on 5/10." |
| **Project** | Active work details: who is doing what, deadlines, decisions | "The AIJU course is a 6-session series. Session 4 is scheduled for late May 2026." |
| **Reference** | Where things live: tools, channels, trackers, resources | "CCC deal pipeline is tracked in GHL. Lisa handles intake. Cross-sell check always runs after intake." |

### What Claude Does NOT Save

Claude will not automatically save:
- Code patterns, file structures, or technical architecture (those live in the code itself)
- Temporary details from a single conversation that have no future value
- Sensitive personal information like passwords, SSNs, or financial account numbers

---

## Part 5: Keeping Your Memory System Healthy

Your memory system is only powerful if it is accurate. Here is how to maintain it.

### Correct and Confirm in Real Time

Every time Claude gets something wrong, do two things:
1. Give the correction
2. Tell it to remember the correction

Do not just fix the one output. Make the lesson stick.

**Instead of:** Just rephrasing or re-running the prompt

**Do this:**
> "That's not right. I never describe my audience as 'small businesses.' I say 'growth-minded business owners.' Remember that for all future content."

### Update Your Brain File When Things Change

If you launch a new service, change your positioning, bring on a new team member, or shift how you operate, update your CLAUDE.md. An outdated Brain File produces confidently wrong answers. That is worse than no Brain File at all.

### Do a Monthly Memory Check

Once a month, ask Claude:
> "What do you remember about me, my businesses, and how I like to work?"

Review what it says. Correct anything that is outdated. Delete anything that is no longer true:
> "Remove the memory about [specific thing]. That's changed."

### Signs Your Memory System Needs Attention

| If Claude Is Doing This | The Fix |
|------------------------|---------|
| Giving generic answers that ignore your business context | Update your CLAUDE.md |
| Repeating a mistake you already corrected | Tell it to remember the correction explicitly |
| Using information that was true six months ago but isn't now | Update or delete the outdated memory |
| Not knowing about a key person or tool in your workflow | Add a Reference memory |

---

## Part 6: Anatomy of a Memory File

You do not need to create memory files manually. Claude does it automatically. But it helps to know what they look like so you can read and edit them if needed.

Here is what a Feedback memory file looks like:

```markdown
---
name: feedback-em-dash-rule
description: Never use em dashes in any content for Cheryl — confirmed correction
metadata:
  type: feedback
---

Never use em dashes in any content written for Cheryl or her businesses.
Use commas, periods, or parentheses instead.

**Why:** Cheryl corrected this multiple times. Em dashes are inconsistent with her 
conversational, direct writing style.

**How to apply:** This applies to all content across CCC, AI Marvels, and EmergeStack, 
including posts, emails, proposals, and course materials.
```

### What Each Part Does

| Section | Purpose |
|---------|---------|
| `name` | The file identifier (kebab-case, no spaces) |
| `description` | One-line summary Claude uses to decide if this memory is relevant |
| `type` | Which category this memory falls into (user, feedback, project, reference) |
| The body | The actual content Claude reads and applies |

---

## Part 7: Quick Reference

### Creating Your Brain File
Create `CLAUDE.md` at the root of your project folder. Four sections: Who You Are, Your Voice and Style, Affiliations and Credentials, Standing Instructions.

### Telling Claude to Remember Something
Just say it directly: "Remember that..." Claude will save a memory file automatically.

### Checking Your Memories
Ask Claude: "What do you remember about how I like to work?"

### Deleting a Memory
Tell Claude: "Remove the memory about [specific thing]."

### Updating Your Brain File
Open CLAUDE.md in your project folder and edit it directly. Changes take effect in the next session.

### Troubleshooting

| Problem | What to Check |
|---------|--------------|
| Claude doesn't seem to know your businesses | Is CLAUDE.md saved at the root of the project folder? (Not inside a subfolder.) |
| Claude keeps repeating a mistake | Tell it explicitly to remember the correction, not just accept the fix |
| Claude seems to have outdated information | Check your memory files and CLAUDE.md for anything no longer accurate |
| You cannot find your memory folder | Ask Claude: "Where is my memory folder?" and it will show you the path |
| Memory file content looks off | Open the file directly in your project folder and edit the body text |

---

## Your Homework Before Session 5

1. Complete your CLAUDE.md if you did not finish it in class. All four sections.
2. Have at least one conversation with Claude where you give a correction and ask it to save the correction as a memory.
3. Do a memory check. Ask Claude what it remembers about you. Screenshot it and bring it to Session 5.
4. Bonus: Find one thing in your CLAUDE.md that is vague and make it more specific.

---

## What's Coming in Session 5: Automation Workflows

Session 5 is where your AI OS starts running things without you asking. We are covering:

- Scheduled tasks that run automatically (daily briefings, weekly reports, recurring workflows)
- n8n workflow integration (connecting Claude to multi-step automations)
- Chaining agents together so one action triggers the next
- Building a morning briefing that lands in your inbox before you start your day

If Session 4 gave Claude a brain, Session 5 gives it a schedule. The system starts working for you even when you're not at the keyboard.

---

## Resources

| Resource | Link |
|----------|------|
| GitHub Repo (all course materials) | github.com/tibby007/building-with-the-ai-sniper |
| Skills Generator Tool | https://skill-generator-zeta.vercel.app |
| AIJU Room | aijunkiesuniversity.com |
| Session 1 Student Guide | In your AIJU classroom |
| Session 2 Student Guide | In your AIJU classroom |
| Session 3 Student Guide | In your AIJU classroom |
