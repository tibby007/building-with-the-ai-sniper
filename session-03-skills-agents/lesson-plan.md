# Session 3 Lesson Plan: Skills & Agents — Teaching Claude What to Do

**Course:** Building with The AI Sniper
**Session:** 3 of 6
**Duration:** 60-75 minutes
**Instructor:** Cheryl Tibbs (The AI Sniper)
**Platform:** AI Junkies University (AIJU)

---

## Pre-Session Checklist

Before you go live, make sure:

- [ ] Claude Desktop is open and connected to your AIJU project folder
- [ ] Cowork mode is active
- [ ] You have the Skills Generator tool open in your browser (Vercel link — see resources section)
- [ ] At least 2-3 skills are installed in your setup for live demo
- [ ] GitHub repo is open: github.com/tibby007/building-with-the-ai-sniper
- [ ] Session 3 folder is pushed to GitHub before class
- [ ] Slide deck is loaded and tested in Gamma

---

## Session Overview

By the end of this session, students will know what skills are, how to trigger them, how to use the ones that already exist, AND how to build their own. We're going from "I follow instructions" to "I have a whole team."

This is where Claude stops being a chatbot and starts being an operator.

### What Students Will Be Able to Do After This Session

- Explain what a skill is and how it differs from a regular prompt
- Browse, install, and trigger skills in Cowork
- Use the Skills Generator tool to create a custom skill from scratch
- Add a skill file to their Claude project
- Understand what an agent is and how it relates to skills

---

## Session Outline with Timing

| Block | Topic | Time |
|-------|-------|------|
| 1 | Recap + Hook | 5 min |
| 2 | What Are Skills? | 10 min |
| 3 | Live Demo: Using Built-In Skills | 15 min |
| 4 | The Skills Generator Tool | 15 min |
| 5 | Live Demo: Building a Custom Skill | 10 min |
| 6 | Agents: The Next Level | 5 min |
| 7 | Hands-On Exercise | 10 min |
| 8 | Wrap-Up + Preview of Session 4 | 5 min |

---

## Block 1: Recap + Hook (5 min)

### Quick Recap
- Session 1: We got Claude set up and configured with a project folder and CLAUDE.md
- Session 2: We gave Claude hands by connecting MCPs and external apps
- Today: We're giving Claude a skillset. Like hiring a specialist for every job.

### Hook
Ask the room: "How many of you have typed the same kind of prompt more than once this week?"

That's the problem skills solve. You stop repeating yourself. Claude already knows exactly what to do, how to do it, and in your voice.

---

## Block 2: What Are Skills? (10 min)

### Talking Points

**The plain-English definition:**
A skill is a pre-built set of instructions that tells Claude how to handle a specific type of task. When you trigger a skill, Claude loads those instructions and executes them without you having to explain everything from scratch every time.

Think of it this way: instead of hiring a generalist who needs a new briefing every day, you have a specialist who already knows your workflow cold.

**How skills work technically (keep it simple):**
- Skills are stored as SKILL.md files inside your Cowork project
- When you type a trigger phrase (like "Betsy write a post"), Claude recognizes it and loads that skill
- The skill file tells Claude who it is, what it does, what to ask you, and how to deliver the output
- It's like a job description that Claude reads and follows every single time

**The difference between a prompt and a skill:**
- A prompt is a one-time instruction
- A skill is a repeatable, reliable system

**What makes a good skill:**
- A clear name and persona (optional but powerful)
- Trigger phrases that make it easy to activate
- A defined output format
- Context about who it's for and what "done" looks like

**Real examples from Cheryl's setup:**
- Betsy handles LinkedIn posts for CCC, AI Marvels, and EmergeStack
- Lisa qualifies deals and packages them for lenders
- Winston builds and manages GHL workflows
- The Skills Generator helps you create new skills on demand

---

## Block 3: Live Demo — Using Built-In Skills (15 min)

### Demo Flow

**Step 1: Show the skills list**
In Cowork, show students how to see what skills are available. Type a natural phrase like "write a LinkedIn post about..." and show how Betsy activates automatically based on the trigger.

**Step 2: Walk through a skill trigger**
Use Betsy or a simple built-in skill. Show:
- The trigger phrase you used
- How Claude responds differently with the skill active versus without
- The structured output it produces

**Step 3: Show a second skill**
Pick something different — a deal qualifier, a document chaser, anything with a clear output format. This demonstrates that skills can cover any function, not just content.

**Talking Points During Demo:**
- "Notice how I didn't explain anything. I just said the trigger and Claude knew the job."
- "This is the difference between a trained team member and someone you hired off the street today."
- "Skills have memory of their own context. They know the persona, the format, the goal."

**Pause for Questions here.**

---

## Block 4: The Skills Generator Tool (15 min)

### Introduction
This is a tool Cheryl built using Claude.ai that lets anyone create a custom skill without knowing how to code or write SKILL.md files from scratch.

**Tool URL:** https://skill-generator-zeta.vercel.app

### How It Works — Walk Through with Students

1. Open the Skills Generator in your browser
2. Answer the prompts — what does this skill do, who does it serve, what's the trigger phrase, what's the output format
3. The tool generates a complete SKILL.md file for you
4. You copy it, save it to your project folder, and it's live

### Demo Flow

- Pull up the Skills Generator on screen
- Pick a simple, relatable use case (example: a skill that drafts follow-up emails after sales calls)
- Walk through each field in the generator
- Show the generated SKILL.md output
- Discuss what each section means

### Talking Points
- "You don't need to be technical to build this. If you can describe what you want, you can build it."
- "This is exactly how I built my entire team of agents. I described the job. The generator wrote the instructions."
- "One skill can save you 20-30 minutes every time you use it. Think about how many times a week you need that same output."

---

## Block 5: Live Demo — Building and Installing a Custom Skill (10 min)

### Demo Flow

Using the output from the Skills Generator demo above:

1. Copy the generated SKILL.md content
2. Open the AIJU project folder in Cowork
3. Create a new file inside the skills folder and paste the content
4. Show students the file structure so they understand where it lives
5. Trigger the new skill in Claude
6. Show the output

**Key Points to Reinforce:**
- Skills are just files. There's nothing magical or complicated under the hood.
- Once the file is there, it's active. No restarts, no technical steps.
- You can edit the file anytime to update how the skill behaves.

**Common Questions to Get Ahead Of:**
- "Does it have to be in a specific folder?" — Yes, inside your project skills directory. Show them the path.
- "Can I have too many skills?" — Not really, but keep them organized. Name them clearly.
- "What if the skill doesn't trigger?" — Check the trigger phrases. Claude is looking for those specific words.

---

## Block 6: Agents — The Next Level (5 min)

### Talking Points

Skills and agents are related but different:

- A **skill** is a single specialized function. One job, done well.
- An **agent** is a skill or a set of skills that can act more autonomously, sometimes making decisions or chaining multiple steps together.

In the Cowork world, your named agents (Betsy, Lisa, Winston, Mya) are skills with a stronger persona and often more complex workflows. The line between skill and agent gets blurry at the top end.

What matters for students right now:
- Start with skills. Build one, use it, get comfortable.
- As your needs get more complex, you layer in agent behavior.
- Session 5 (Automation Workflows) is where we'll connect agents to trigger automatically and chain them together.

**Leave them with this thought:**
"Every skill you build is a team member you never have to train again. They show up every day, ready to work, already knowing the job."

---

## Block 7: Hands-On Exercise (10 min)

### Exercise Instructions

Have students open the Skills Generator tool and build their first custom skill. Give them this prompt:

"Think of one task you repeat every week. Something you explain to Claude over and over. That's your skill. Build it."

Walk around (or monitor the room) and help troubleshoot. Common places people get stuck:
- Not knowing what to name the skill
- Trigger phrase being too long or vague
- Not knowing where to save the file

If they finish early, have them trigger the skill and share what it produced.

### Debrief (last 2 min of this block)
Ask 1-2 students to share what skill they built and what problem it solves for them. This builds community and shows the range of what's possible.

---

## Block 8: Wrap-Up + Preview of Session 4 (5 min)

### What We Covered Today
- What skills are and how they work
- How to use built-in skills with trigger phrases
- How to use the Skills Generator to build your own
- How to install a custom skill in your project
- The difference between skills and agents

### Your Homework Before Session 4
1. Build at least one custom skill using the Skills Generator
2. Use it at least 3 times before next session
3. Come back with notes on: did it work the way you expected? What would you change?

### Preview: Session 4 — Memory & Context
Next session we go deep on how to give Claude long-term memory. We're talking CLAUDE.md, memory banks, and how to make sure Claude always knows who you are, what your businesses do, and how you like to work — without you having to explain it every time.

---

## Resources for This Session

| Resource | Link |
|----------|------|
| GitHub Repo | github.com/tibby007/building-with-the-ai-sniper |
| Skills Generator Tool | https://skill-generator-zeta.vercel.app |
| AIJU Room | aijunkiesuniversity.com |
| Session 3 Student Guide | Linked in AIJU classroom |

---

## Instructor Notes

- This session has the most live demo time of any session so far. Practice the Skills Generator demo before class so it's smooth.
- The Hands-On block is the one where students light up. Give it the full 10 minutes — don't rush wrap-up.
- If students are struggling with the concept, use this analogy: "A skill is like a recipe. Once it's written down, anyone (including Claude) can follow it exactly the same way every time."
- Cheryl's real-world examples (Betsy, Lisa, Winston) are powerful. Students want to see what's possible at scale, not just the basics.