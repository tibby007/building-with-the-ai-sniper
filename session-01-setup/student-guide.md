# Setting Up Claude Desktop & Cowork Like a Pro
## Session 1 Student Guide | Building with The AI Sniper

**Instructor:** Cheryl Tibbs
**Series:** Building with The AI Sniper | AI Junkies University
**Date:** May 8, 2026

---

## What You'll Walk Away With

By the end of this session, you'll have a properly configured Claude Desktop setup with your own CLAUDE.md file, your first custom skill, and a memory system that makes Claude actually remember who you are. No more starting from scratch every conversation.

---

## Part 1: Understanding the Landscape

### Claude Desktop vs. Cowork: What's the Difference?

Think of it this way:

**Claude Desktop** is the application you download and install on your computer. It's the building.

**Cowork** is a mode INSIDE that application. It's the office inside the building where the real work happens.

| Feature | Claude Desktop (Chat) | Cowork Mode |
|---|---|---|
| What it does | Conversation. You ask, Claude answers | Autonomous work. Claude does tasks on your computer |
| File access | Can read files you upload to the chat | Can read AND write files in your selected folder |
| App connections | Limited | Connects to your apps via MCP (Slack, Gmail, GHL, etc.) |
| Best for | Quick questions, brainstorming, advice | Building docs, research reports, automations, multi-step tasks |
| How it feels | Talking to a smart friend | Having an employee who can actually execute |

**Bottom line:** If you just need to chat, use Desktop. If you need something DONE, switch to Cowork.

---

## Part 2: The Files That Power Everything

There are four key components that turn Claude from a generic AI into YOUR AI:

### 1. CLAUDE.md (Your Project Instructions File)

**What:** A markdown file that Claude reads automatically at the start of every conversation in your project.

**Why it matters:** Without this, Claude has amnesia. Every conversation starts from zero. With it, Claude knows who you are, what you do, how you like things, and what tools you have connected.

**Where it goes:** Root of your project folder.

```
my-project/
  CLAUDE.md          <-- RIGHT HERE
  skills/
  memory/
```

### 2. Skills (Your AI Specialists)

**What:** A skill is a folder containing a SKILL.md file that teaches Claude HOW to do a specific type of task.

**Why it matters:** Instead of explaining what you want every single time, you teach Claude once. Then it executes the same way every time. Consistency. Quality. Speed.

**Example:** Cheryl has a skill called "Betsy" that writes LinkedIn posts. Every time she says "write a LinkedIn post," Claude loads Betsy's instructions, which include her brand voice, formatting rules, content pillars, and hashtag strategy. The post comes out sounding like Cheryl, not like a robot.

**Where they go:**

```
my-project/
  CLAUDE.md
  skills/
    email-drafter/
      SKILL.md       <-- Each skill gets its own folder
    social-poster/
      SKILL.md
    meeting-prepper/
      SKILL.md
```

### 3. Memory System (Long-Term Knowledge)

**What:** Markdown files that store persistent knowledge about you, your business, your team, your preferences, and your terminology.

**Why it matters:** Memory is what turns "some AI" into "MY AI." When Claude knows that "CCC" means your finance company, that you don't use em dashes, that your brand colors are specific hex codes... that's memory at work.

**Where it goes:**

```
my-project/
  CLAUDE.md
  memory/
    business-context.md
    team.md
    terminology.md
    preferences.md
  skills/
```

### 4. MCP Servers (Your App Connections)

**What:** MCP stands for Model Context Protocol. It's the technology that lets Claude connect to external apps and services.

**Why it matters:** Without MCP connections, Claude can only TALK about doing things. With them, Claude can actually DO things in your apps: send Slack messages, create calendar events, update your CRM, post to LinkedIn.

**How to connect them:**

- Open Claude Desktop
- Go to Settings > Integrations (or Settings > Extensions for one-click installs)
- Browse available extensions and click Install
- Configure any required API keys or credentials

**Popular MCP connections:** Google Calendar, Gmail, Slack, Notion, GoHighLevel, LinkedIn, Supabase, Google Drive

*We'll go deeper on MCP setup in a future session.*

---

## Part 3: Step-by-Step Setup Guide

### Step 1: Set Up Your Project Folder

1. Open Claude Desktop
2. Switch to Cowork mode
3. Select a folder on your computer (or create a new one)
   - Example: `Documents/Claude/Projects/MyBusiness`
4. This folder is now your workspace. Everything you build lives here.

### Step 2: Create Your CLAUDE.md

Create a new file called `CLAUDE.md` in your project folder. Copy this template and fill in your own info:

```markdown
# [Your Project Name]

## About
[1-2 sentences about what this project/workspace is for]

## About Me
- Name: [Your name]
- Business: [What you do]
- Role: [Your title/role]

## How I Want Claude to Work
- Tone: [e.g., professional but conversational, laid back, formal]
- Format: [e.g., concise responses, use bullet points, no jargon]
- Avoid: [e.g., em dashes, overly academic language, unnecessary apologies]

## My Tools & Systems
- [List any tools you use: GHL, Notion, Google Workspace, etc.]
- [Note which ones are connected via MCP]

## Key Context
- [Anything else Claude should always know about you/your business]
- [Industry terminology, client types, service offerings]
```

**Pro tips:**

- Keep it focused. One page is plenty to start.
- If Claude already does something right without being told, don't clutter your CLAUDE.md with it.
- You'll update this over time. Start simple, refine as you go.

### Step 3: Build Your First Skill

Let's create a simple email drafting skill to get you started.

**1. Create the folder structure:**

```
my-project/
  skills/
    email-drafter/
      SKILL.md
```

**2. Create the SKILL.md file with this content:**

```yaml
---
name: email-drafter
description: "Draft professional emails in my voice and style.
  Use this skill when I say 'write an email', 'draft a message',
  'email [someone]', 'reply to this email', or 'compose an email'."
---

# Email Drafter

## My Voice & Style
- Professional but warm
- Direct and to the point
- [Add your own style notes here]

## Email Format
1. Start with a clear subject line
2. Open with a personal but professional greeting
3. Get to the point in the first 1-2 sentences
4. Keep paragraphs short (2-3 sentences max)
5. End with a clear call to action or next step
6. Sign off with: [Your preferred sign-off]

## Things to Avoid
- Overly formal or stiff language
- Long paragraphs
- Passive voice
- [Add your own "don'ts" here]

## Context
- My business: [Brief description]
- Common recipients: [Clients, partners, vendors, etc.]
- Typical email types: [Follow-ups, proposals, introductions, etc.]
```

**3. Test it out:**

Open a Cowork conversation in your project folder and say: "Write an email to a potential client introducing my services."

Claude should now use your email-drafter skill automatically.

### Step 4: Set Up Basic Memory

**1. Create the memory folder:**

```
my-project/
  memory/
```

**2. Create your first memory file** called `business-context.md`:

```markdown
# Business Context

## Company
- Name: [Your business name]
- Industry: [Your industry]
- Location: [City, State]
- Founded: [Year]

## What We Do
[2-3 sentences about your core offering]

## Target Market
- [Who you serve]
- [Industry focus]
- [Size of businesses you work with]

## Products/Services
- [Service 1]: [Brief description]
- [Service 2]: [Brief description]

## Competitive Advantage
- [What makes you different]

## Key Terminology
- [Term 1]: [What it means in your business]
- [Term 2]: [What it means in your business]
```

**3. Reference it in your CLAUDE.md** by adding this line:

```markdown
## Reference Files
- For detailed business context, see memory/business-context.md
```

### Step 5: Connect Your First MCP Server (Optional Today)

1. Open Claude Desktop
2. Go to **Settings** (gear icon)
3. Navigate to **Extensions** or **Integrations**
4. Browse the available extensions
5. Install one that's relevant to you (Google Calendar is a great first one)
6. Follow the authentication prompts

*Don't feel pressured to do this today. We'll cover MCP setup in depth in a future session.*

---

## Part 4: Your Complete Folder Structure

Here's what your project should look like when you're done today:

```
my-project/
|
|-- CLAUDE.md                    (Your project instructions)
|
|-- skills/
|   |-- email-drafter/
|       |-- SKILL.md             (Your first skill)
|
|-- memory/
    |-- business-context.md      (Your business info)
```

And here's where it CAN go (Cheryl's setup as inspiration):

```
Jordan/                          (Cheryl's Chief of Staff project)
|
|-- CLAUDE.md                    (Project-level instructions)
|
|-- skills/
|   |-- betsy-post-creator/      (LinkedIn content agent)
|   |-- jorge-prospect-hunter/   (LinkedIn prospecting agent)
|   |-- jorge-connection-manager/ (LinkedIn connection agent)
|   |-- jorge-messenger/         (LinkedIn messaging agent)
|   |-- lisa-deal-qualifier/     (Deal intake agent)
|   |-- lisa-lender-match/       (Lender matching agent)
|   |-- winston-ghl-workflow/    (GHL automation agent)
|   |-- felix-fb-ads/            (Facebook ads agent)
|   |-- mya-video/               (HeyGen video agent)
|   |-- pixel-image-gen/         (Image generation agent)
|   |-- vince-hyperframes/       (Motion graphics agent)
|   |-- scott-client-intake/     (Client intake agent)
|   |-- nova-data-ops/           (Data operations agent)
|   |-- marco-n8n/               (n8n workflow agent)
|   |-- ... and more (22 total)
|
|-- memory/
|   |-- business-context.md
|   |-- team.md
|   |-- terminology.md
|   |-- preferences.md
|
|-- briefings/                   (Auto-generated morning briefings)
|-- linkedin_drafts/             (Queued LinkedIn content)
|-- campaigns/                   (Campaign materials)
```

That's 22 agents, a full memory system, scheduled tasks, and automations across three businesses. All built on the same foundation you just set up today.

---

## Part 5: The SKILL.md Anatomy (Reference)

Every skill follows the same two-part format:

```yaml
---
name: your-skill-name
description: "A clear description of WHEN Claude should use this skill.
  Include trigger phrases the user might say. Be specific. The more
  precise this is, the more reliably Claude activates the right skill."
---

# Skill Title

## Purpose
What this skill does in 1-2 sentences.

## Instructions
Step-by-step instructions for how Claude should execute this task.

## Rules & Constraints
- Any guardrails or requirements
- Formatting rules
- Things to avoid

## Reference Files
- Link to any supporting files if needed
- Example: "See templates/email-template.md for formatting"

## Output Format
What the final output should look like.
```

**Key rules for SKILL.md files:**

- The `name` and `description` in the YAML header are what Claude sees at startup. Make the description clear and specific.
- Include trigger phrases in the description so Claude knows when to activate it.
- Keep instructions actionable. Tell Claude what to DO, not what to think about.
- If your instructions get too long, split them into separate reference files and link to them.

---

## Part 6: Quick Reference Card

### File Types You Need to Know

| File | Purpose | Format |
|---|---|---|
| CLAUDE.md | Project instructions, read at every conversation start | Markdown |
| SKILL.md | Skill instructions, read when skill is triggered | YAML frontmatter + Markdown |
| Memory files | Persistent knowledge about you/your business | Markdown |
| .mcp.json | MCP server configuration (advanced) | JSON |

### Where Things Live

| What | Where |
|---|---|
| Project instructions | `CLAUDE.md` (project root) |
| Skills | `skills/[skill-name]/SKILL.md` |
| Memory | `memory/[topic].md` |
| MCP config | Settings > Integrations (or `.mcp.json` for advanced) |

### Common Commands to Try

| Say This | What Happens |
|---|---|
| "Write an email to [name]" | Triggers your email-drafter skill |
| "What do you know about my business?" | Tests your memory setup |
| "List my skills" | Shows available skills |
| "Read my CLAUDE.md" | Confirms Claude can see your instructions |

---

## Homework Before Session 2

1. **Create your CLAUDE.md** with your real business info
2. **Build one custom skill** (email drafter, meeting prepper, social post writer, whatever fits your workflow)
3. **Set up at least one memory file** with your business context
4. **Test it** by running a conversation in Cowork mode and seeing if Claude uses your instructions and skill correctly
5. **Drop your results** in the Building with The AI Sniper room. Show us your CLAUDE.md!

---

## Coming Up Next

Future sessions in this series will cover:

- **Session 2:** Building Custom Agents (turning skills into real AI employees)
- **Session 3:** MCP Deep Dive (connecting Claude to all your apps)
- **Session 4:** Scheduled Tasks & Automation (making Claude work while you sleep)
- **Session 5:** Plugins & Advanced Architecture (packaging and scaling your setup)

---

## Resources

- [Claude Desktop Download](https://claude.ai/download)
- [Claude Skills Documentation](https://docs.claude.com/en/docs/claude-code/skills)
- [MCP Setup Guide](https://docs.claude.com/en/docs/claude-code/mcp)
- [Claude Code Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices)
- [Desktop Extensions](https://www.anthropic.com/engineering/desktop-extensions)

---

*Built by The AI Sniper | AI Junkies University | Building with The AI Sniper Room*
*Questions? Drop them in the room. Cheryl's got you.*
