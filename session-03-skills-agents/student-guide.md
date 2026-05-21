# Session 3 Student Guide: Skills & Agents — Teaching Claude What to Do

**Course:** Building with The AI Sniper
**Session:** 3 of 6
**Your Instructor:** Cheryl Tibbs (The AI Sniper)
**Platform:** AI Junkies University

Keep this guide. Everything we cover in class is here in writing so you can reference it later, repeat the steps on your own, and build as many skills as you want.

---

## Prerequisites

Before this session, you should have:

- [ ] Claude Desktop installed and connected to your project folder (Session 1)
- [ ] At least one MCP or connector set up (Session 2)
- [ ] Access to the Skills Generator tool: https://skill-generator-zeta.vercel.app

If you're missing any of these, check the student guides from Sessions 1 and 2 first.

---

## Part 1: What Is a Skill?

### The Simple Version

A skill is a file that tells Claude how to handle a specific type of task, every time, the same way. Instead of explaining what you need from scratch every session, you write it down once and Claude follows it automatically.

Think of it like a job description. You hire someone and give them a document that says here's your role, here's what you do every day, here's how you communicate. Skills work the same way.

### The Technical Version (still simple, we promise)

- Skills are saved as SKILL.md files inside your Claude project
- When you type a trigger phrase, Claude reads the skill and executes it
- You don't see this happening. It just works.
- You can have as many skills as you need

### Skills vs. Regular Prompts

| Regular Prompt | Skill |
|----------------|-------|
| You explain the task every time | Claude already knows the task |
| Output varies each time | Output follows a consistent format |
| You do the thinking | Claude handles it the way you designed |
| One time use | Repeatable, forever |

### Real Examples from The AI Sniper's Setup

- **Betsy** — writes LinkedIn posts for CCC, AI Marvels, and EmergeStack in Cheryl's voice
- **Lisa** — qualifies deals, matches lenders, packages submissions for CCC
- **Winston** — builds and manages GoHighLevel workflows automatically
- **Mya** — produces videos using HeyGen
- **The Skills Generator** — builds new skills on demand (you'll use this today)

---

## Part 2: Using Skills You Already Have

### How to Trigger a Skill

Triggering a skill is as simple as typing the right phrase. Each skill has trigger phrases built into it. When Claude sees one of those phrases, it activates the skill automatically.

**Examples:**
- Type "write a LinkedIn post about..." and Betsy activates
- Type "qualify this deal" and Lisa activates
- Type "chase documents for [client name]" and a document chaser skill activates

### How to Know What Skills You Have

In Cowork, you can ask Claude directly:

> "What skills do I have available?"

Claude will list what's in your project and how to trigger each one.

You can also look inside your project folder. Skills are typically in a `skills/` directory and each one is its own `.md` file.

### Tips for Using Skills Effectively

- Use natural language. You don't need to remember an exact phrase, just something close to the trigger.
- If a skill doesn't activate, try rephrasing or being more specific.
- Skills are designed for your context. The more your project folder knows about your business (from your CLAUDE.md), the better the output.

---

## Part 3: Building Your Own Skill

You don't need to write code or know anything technical to build a skill. You need to be able to describe what you want. That's it.

### Step 1: Decide What the Skill Should Do

Ask yourself: What task do I repeat over and over? What do I explain to Claude every week?

Some examples to get you thinking:
- Writing follow-up emails after client calls
- Drafting proposals for a specific type of project
- Creating social media content for a particular platform
- Summarizing meetings or call notes
- Qualifying new leads before you spend time on them

Pick ONE task to start. Specific is better than broad.

### Step 2: Open the Skills Generator

Go to: **https://skill-generator-zeta.vercel.app**

This tool was built by Cheryl specifically for AIJU students. It asks you a series of questions about the skill you want to create and generates the SKILL.md file for you.

### Step 3: Fill In the Generator

The Skills Generator will ask you things like:

- **What does this skill do?** Describe the task in plain English.
- **Who is this skill for?** (You, your clients, your team?)
- **What should Claude ask you before it starts?** (Any inputs it needs upfront)
- **What does the output look like?** (Email, bullet list, document, social post, etc.)
- **What's the trigger phrase?** What will you type to activate it?
- **Does this skill have a persona?** (Optional — you can give it a name and personality)

Take your time. The more specific your answers, the better the skill performs.

### Step 4: Copy the Generated Output

When the generator finishes, it will give you a complete SKILL.md file. Copy the entire thing.

### Step 5: Save the Skill to Your Project

1. Open your Claude project folder on your computer
2. Find the `skills/` folder inside it (or create one if it doesn't exist)
3. Create a new file. Name it something descriptive like `followup-email.md` or `lead-qualifier.md`
4. Paste the content from the Skills Generator
5. Save the file

That's it. No restarts. No technical setup. The skill is now live.

### Step 6: Test Your Skill

Go back to Claude in Cowork and type your trigger phrase. Claude should activate the skill and walk through it exactly as designed.

If it doesn't work right away:
- Check that the file is saved in the right folder
- Make sure the trigger phrase in the file matches what you typed (or something close to it)
- Ask Claude: "Do you see a skill for [task name]?" and see what it says

---

## Part 4: Anatomy of a SKILL.md File

You don't have to write these from scratch (that's what the generator is for), but it helps to understand what's inside.

Here's a simplified example:

```
---
name: followup-emailer
description: Drafts a professional follow-up email after a client or sales call
triggers: ["write a follow-up", "draft a follow-up email", "follow up on my call"]
---

You are a professional email writer for [Your Name/Business].

When activated, ask the user:
1. Who was the call with?
2. What were the main points discussed?
3. What are the next steps or action items?

Then draft a follow-up email that is warm, professional, and concise.
Format: Subject line + 3-4 paragraph email body.
Sign off with [Your Name].
```

### What Each Part Does

| Section | What It Does |
|---------|-------------|
| `name` | Internal identifier for the skill |
| `description` | What Claude shows when listing your skills |
| `triggers` | The phrases that activate it |
| The body | The actual instructions Claude follows |

---

## Part 5: Skills vs. Agents

You'll hear both terms. Here's the difference:

**Skills** are single, specialized functions. One job, done well. A skill that writes emails just writes emails. A skill that qualifies leads just qualifies leads.

**Agents** are skills with more autonomy and complexity. They often have a stronger persona, can handle multi-step tasks, and sometimes chain actions together. Betsy isn't just a skill — she's an agent with a personality, a business context, and the ability to adapt her output depending on which of Cheryl's three businesses she's writing for.

The line between skill and agent is fuzzy at the top end. What matters for you right now:

- Start with skills. Build one. Use it. Get comfortable.
- As your needs grow, your skills will grow with them.
- In Session 5, we'll connect agents to automation workflows so things can trigger without you even asking.

---

## Part 6: Quick Reference

### Triggering a Skill
Just type naturally. Use the trigger phrase or something close to it.

### Finding Your Skills
Ask Claude: "What skills do I have available?"
Or look in your project `skills/` folder.

### Building a Skill
Go to the Skills Generator: **https://skill-generator-zeta.vercel.app**
Fill in the fields. Copy the output. Save to your skills folder.

### Troubleshooting

| Problem | What to Check |
|---------|--------------|
| Skill doesn't activate | Is the file saved in the right folder? Does your trigger match? |
| Output isn't right | Edit the skill file — adjust the instructions in the body |
| Claude says it doesn't know the skill | Try restarting Cowork, or ask Claude to list your skills |
| Generator output looks off | Re-answer the questions with more specifics |

---

## Your Homework Before Session 4

1. Build at least one custom skill using the Skills Generator
2. Use it at least 3 times this week
3. Take notes: Did it perform the way you expected? What would you tweak?
4. Bring one example of your skill's output to share with the group in Session 4

---

## What's Coming in Session 4: Memory & Context

Next session is all about giving Claude long-term memory. We're covering:
- CLAUDE.md — your AI operating system's brain file
- Memory banks — how Claude holds context across sessions
- Making sure Claude always knows your businesses, your voice, and your preferences without you having to repeat yourself

If Session 3 was about teaching Claude what to do, Session 4 is about teaching Claude who you are.

---

## Resources

| Resource | Link |
|----------|------|
| Skills Generator Tool | https://skill-generator-zeta.vercel.app |
| GitHub Repo (all course materials) | github.com/tibby007/building-with-the-ai-sniper |
| AIJU Room | aijunkiesuniversity.com |
| Session 1 Student Guide | In your AIJU classroom |
| Session 2 Student Guide | In your AIJU classroom |