# AIJU Session 1: Setting Up Claude Desktop & Cowork Like a Pro

**Instructor:** Cheryl Tibbs, The AI Sniper
**Date:** May 8, 2026 | 2:00 PM
**Series:** Building with The AI Sniper
**Session:** 1 of [Series] | Foundation Setup

---

## Pre-Session Checklist

- [ ] Claude Desktop app open and visible for screen share
- [ ] Student Handout link ready to drop in chat
- [ ] AIJU room open for questions
- [ ] Have your Jordan project folder visible as a reference example

---

## Session Flow (Estimated 60-75 minutes)

### OPENING (5 min)

**Talking Points:**

- Welcome to Session 1. This is the foundation. Everything we build in future sessions sits on top of what we set up today.
- Quick context: I run 22 AI agents as skills in my setup. I have a Chief of Staff project called Jordan that manages three businesses. That's where we're HEADED. Today we're building the foundation to get there.
- What we're covering: the difference between Claude Desktop and Cowork, the key files you need, and how to structure your workspace so everything plays nice together.
- "You don't need to be technical to do this. If you can create a folder and type in a text file, you can set this up."

---

### SECTION 1: Claude Desktop vs. Cowork (10 min)

**Key Distinction to Drive Home:**

Claude Desktop is the APP. Cowork is a MODE inside that app.

**Talking Points:**

- **Claude Desktop** = the container. It's the application you download and install. Think of it as the building.
- **Cowork** = a feature INSIDE Desktop. It's the autonomous mode where Claude can actually DO things on your computer. Think of it as the office inside the building where work gets done.
- In regular Desktop mode, you're chatting. You ask, Claude answers. It's a conversation.
- In Cowork mode, Claude has hands. It can read your files, write documents, run code, control your browser, connect to your apps. You give it a goal and it works.

**When to use what:**

- Desktop (regular chat): Quick questions, brainstorming, getting advice, having a conversation
- Cowork: "Build me a spreadsheet," "Write a proposal," "Research this company and create a report," "Set up a workflow"

**Show them:**

- Open Claude Desktop
- Show the regular chat interface
- Show how to switch to Cowork mode
- Point out that Cowork lets you select a folder (this is important for later)

---

### SECTION 2: The Files That Make It All Work (15 min)

**Transition:** "Now that you know the difference, let's talk about the files that turn Claude from a generic assistant into YOUR assistant."

#### 2A. CLAUDE.md (5 min)

**What it is:** Your project's instruction manual for Claude. Every time Claude starts a conversation in a project folder, it reads this file FIRST. It's like giving a new employee their onboarding docs on day one.

**Talking Points:**

- Lives in the root of your project folder
- Gets read automatically at the start of every conversation
- This is where you put: who you are, what this project is about, how you want Claude to behave, what tools and systems are connected, any rules or preferences
- Keep it focused. Don't write a novel. If Claude already does something correctly without you telling it, don't waste space repeating it.

**What goes in CLAUDE.md:**

- Project overview (1-2 sentences max)
- Your role and context
- Key rules and preferences (tone, formatting, do's and don'ts)
- Connected tools and systems
- File structure overview
- Common commands or workflows

**Show example from your setup (paraphrase, don't show private info):**

- "My CLAUDE.md tells Claude that I'm Cheryl Tibbs, I run three businesses, here are my agents, here's my tone preference, here are the tools connected."

#### 2B. Skills Folder (5 min)

**What they are:** Skills are like job descriptions for Claude. Each skill tells Claude HOW to do a specific type of task.

**Talking Points:**

- A skill = a folder with a SKILL.md file inside it
- The SKILL.md has two parts: a header (YAML frontmatter) that says WHEN to use it, and instructions (markdown body) that say HOW to do the job
- Claude reads the name and description of every installed skill at startup. When it recognizes a task that matches, it loads the full instructions.
- Think of it like hiring specialists. Instead of one generalist, you have a LinkedIn expert, a document chaser, a deal qualifier, etc.

**Folder structure:**

```
your-project/
  skills/
    my-first-skill/
      SKILL.md
      (optional reference files)
    another-skill/
      SKILL.md
```

**SKILL.md format (show the skeleton):**

```yaml
---
name: skill-name
description: "When to trigger this skill. Be specific."
---

# Skill Title

## Instructions
[What Claude should do when this skill runs]
```

**Real example from your setup:**

- "I have a skill called Betsy that writes my LinkedIn posts. When I say 'write a LinkedIn post,' Claude loads Betsy's SKILL.md which has my brand voice, formatting rules, hashtag strategy, and content pillars. That's why every post sounds like ME, not like a robot."

#### 2C. Memory System (5 min)

**What it is:** Claude's long-term memory across conversations.

**Talking Points:**

- Without memory, every conversation starts fresh. Claude forgets everything.
- The memory system gives Claude persistent knowledge about you, your business, your preferences, your team, your terminology.
- Memory files are markdown files that Claude can read and update.
- Two levels: CLAUDE.md (project-level memory) and a dedicated memory folder for deeper context.

**Structure:**

```
your-project/
  CLAUDE.md              (working memory, high-level)
  memory/
    business-context.md   (who you are, what you do)
    team.md              (your people, their roles)
    terminology.md       (your internal lingo)
    preferences.md       (how you like things done)
```

**Key point:** "The memory system is what turns Claude from 'some AI' into 'my AI.' When Claude knows that 'CCC' means Commercial Capital Connect, that Lisa handles deal intake, that I don't use em dashes... that's the memory system at work."

---

### SECTION 3: Step-by-Step Setup (20 min)

**Transition:** "Alright, let's actually BUILD this. Open your computers. We're doing this together."

#### Step 1: Create Your Project Folder (2 min)

- Open Claude Desktop
- Create or select a folder for your project
- "This is your workspace. Everything lives here."

#### Step 2: Create Your CLAUDE.md (8 min)

Walk them through creating the file:

1. Create a new file called `CLAUDE.md` in the project folder
2. Start with the basics:

```markdown
# [Your Project Name]

## About Me
[Who you are, what you do, 2-3 sentences]

## Businesses / Context
[What this project covers]

## Preferences
- Tone: [how you want Claude to communicate]
- Formatting: [any rules]
- Things to avoid: [what you don't want]

## Connected Tools
[List any MCP servers or integrations]
```

3. Have them fill it in with their own info
4. "Don't overthink this. Start simple. You'll add to it over time."

#### Step 3: Create Your First Skill (5 min)

Walk them through:

1. Create a `skills/` folder
2. Inside it, create a folder for a simple skill (e.g., `email-drafter/`)
3. Create the SKILL.md:

```yaml
---
name: email-drafter
description: "Draft professional emails in my voice. Use when I say 'write an email', 'draft a message', or 'email [someone]'."
---

# Email Drafter

## Voice & Tone
- Professional but warm
- [Their style notes]

## Format
- Subject line first
- Keep it concise
- Sign off with [their preferred sign-off]
```

4. "Congratulations, you just built your first AI skill."

#### Step 4: Set Up Basic Memory (3 min)

1. Create a `memory/` folder
2. Create `business-context.md` with basic info about their business
3. Reference it in CLAUDE.md: "For detailed business context, see memory/business-context.md"

#### Step 5: Understanding MCP Connections (2 min)

**Talking Points:**

- MCP = Model Context Protocol. It's how Claude connects to external tools and services.
- In Claude Desktop, you add MCP servers through Settings > Integrations or through Desktop Extensions (one-click installs).
- Examples: Google Calendar, Slack, Gmail, LinkedIn, GoHighLevel, Notion
- "In Cowork mode, these connections let Claude actually DO things in your apps. Without them, Claude can only talk about doing things."
- Don't overwhelm them here. "We'll go deeper on MCP servers in a future session."

---

### SECTION 4: The Big Picture (10 min)

**Transition:** "Now let me show you where this all goes when you commit to it."

**Show your ecosystem (high level):**

- "I have 22 agents running as skills: Betsy writes my LinkedIn content, Jorge manages my LinkedIn connections, Lisa qualifies deals, Winston builds GHL workflows, Felix runs my Facebook ads, Mya creates videos, Pixel generates images..."
- "I have a Chief of Staff project called Jordan that coordinates everything across my three businesses."
- "I have scheduled tasks that run automatically. Morning briefings, engagement reports, newsletter generation."
- "None of this happened overnight. It started exactly where you are right now. One CLAUDE.md. One skill. Then I kept building."

**The progression (where this series is going):**

- Session 1 (today): Foundation setup
- Future sessions: Building custom agents/skills, creating scheduled tasks, connecting MCP servers, building plugins, advanced automation

---

### SECTION 5: Q&A + WRAP (10 min)

**Talking Points for Close:**

- "The handout has everything we covered today plus the exact file structures and templates. Download it, bookmark it, use it."
- "Your homework: Get your CLAUDE.md created and your first skill built before next session. Just ONE skill. Start small."
- "Drop questions in the room. I'm here."
- Tease next session topic

**Common questions to anticipate:**

- "Do I need Claude Pro/Max?" - Yes, Cowork is available on paid plans.
- "Can I use this with ChatGPT?" - No, this is Claude-specific. Skills, CLAUDE.md, MCP are all Claude's architecture.
- "How many skills can I have?" - As many as you need. Start with 1-2, build from there.
- "Where do plugins fit in?" - Plugins are bundles of skills, MCPs, and tools packaged together. We'll cover those in a future session.
- "Is this the same as Claude Code?" - Cowork is built on Claude Code's technology but designed for non-developers. Same engine, friendlier interface.

---

## Post-Session Tasks

- [ ] Drop the student handout PDF/link in the AIJU room
- [ ] Post a "show your CLAUDE.md" challenge for the community
- [ ] Announce next session date and topic
- [ ] Save any good Q&A for future content
