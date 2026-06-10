# Session 4 Lesson Plan: Memory & Context — Giving Claude a Brain That Never Forgets

**Course:** Building with The AI Sniper
**Session:** 4 of 6
**Duration:** 60-75 minutes
**Instructor:** Cheryl Tibbs (The AI Sniper)
**Platform:** AI Junkies University (AIJU)

---

## Pre-Session Checklist

Before you go live, make sure:

- [ ] Claude Desktop is open and connected to your AIJU project folder
- [ ] Cowork mode is active
- [ ] Your own CLAUDE.md file is open and ready to show on screen
- [ ] A sample memory folder is visible in your project to demo the memory system
- [ ] GitHub repo is open: github.com/tibby007/building-with-the-ai-sniper
- [ ] Session 4 folder is pushed to GitHub before class
- [ ] Slide deck is loaded and tested in Gamma

---

## Session Overview

By the end of this session, students will understand exactly how Claude holds information across conversations. They will know how to write a CLAUDE.md Brain File, how the auto-memory system works, and how to keep Claude's context clean and accurate over time.

This is the session where Claude stops feeling like a tool you manage and starts feeling like a team member who already knows you.

### What Students Will Be Able to Do After This Session

- Explain what CLAUDE.md is and why it is the foundation of a working AI OS
- Write their own Brain File (CLAUDE.md) with their business context, voice, and preferences
- Understand how Claude's auto-memory system creates and stores memories across sessions
- Identify the four types of memories Claude saves and know when each one matters
- Maintain and update their memory system as their business evolves

---

## Session Outline with Timing

| Block | Topic | Time |
|-------|-------|------|
| 1 | Session 3 Recap + Hook | 10 min |
| 2 | What Is CLAUDE.md? | 10 min |
| 3 | Live Demo: Building a Brain File | 15 min |
| 4 | The Auto-Memory System | 10 min |
| 5 | Live Demo: Memory in Action | 10 min |
| 6 | Maintaining Your Memory Over Time | 5 min |
| 7 | Hands-On Exercise | 10 min |
| 8 | Wrap-Up + Preview of Session 5 | 5 min |

---

## Block 1: Session 3 Recap + Hook (10 min)

### Part A: Session 3 Recap — Skills & Agents (5 min)

**What we built:** Custom skills using the Skills Generator, installed into the project folder, and triggered with natural language.

**Talk through this on screen:**
- "Last session we talked about teaching Claude what to do. Skills are the job descriptions. You write them once, Claude follows them forever."
- Pull up the skills folder in your project and show a skill or two that are installed
- Ask the room: "Did anyone use their skill this week? What did you build?"

**Quick live check:**
"Drop in the chat: what skill did you build, or what task are you thinking about turning into a skill? Even if you haven't built one yet, tell me what task you're tired of repeating."

**Key thing to reinforce:**
"Skills handle the HOW. They tell Claude how to do the job. Today we're covering the WHO. Who are you? What are your businesses? How do you like to work? That's what memory is for."

---

### Part B: Hook into Today's Session (5 min)

Bridge from skills into memory:

"Okay, so here's the problem. You have your skills set up. Claude knows how to write a LinkedIn post for your brand, how to qualify a deal, how to chase a document. But every time you start a new conversation, Claude has amnesia. It has no idea who you are, what your businesses do, or that you hate em dashes and never say the word 'y'all' in your content."

Ask the room: "Has anyone had Claude give them advice that was technically correct but completely off for their actual situation? Like it gave you a response designed for a Fortune 500 company when you're running a boutique operation out of Douglasville?"

(Pause for responses)

"That's the memory gap. Claude is smart. But without context, it's giving you generic answers. Today we close that gap. We're going to build the file that tells Claude everything it needs to know about you, your businesses, and your preferences, permanently. And then we're going to set up a system so Claude keeps learning and adding to that memory on its own."

---

## Block 2: What Is CLAUDE.md? (10 min)

### Talking Points

**The plain-English definition:**
CLAUDE.md is a file you place in your project folder that Claude reads at the start of every session. It's your Brain File. Your AI OS instruction manual. Everything Claude needs to know about you, your businesses, your voice, and your preferences lives here.

Think of it like the employee handbook you give a new hire on day one. Except Claude actually reads it. Every time.

**What belongs in CLAUDE.md:**
- Your name, title, and businesses (what each one does, who it serves)
- Your tone and writing style preferences
- Things you never want Claude to do (em dashes, certain phrases, certain formats)
- Your target audience for each business
- Key personnel, tools, and workflows Claude needs to know about
- Any standing instructions for how you like Claude to respond

**What CLAUDE.md is NOT:**
- It is not a skill. It does not trigger a specific task.
- It is not a memory file. It is the permanent baseline, not a log of past conversations.
- It is not optional if you want Claude to actually perform at a high level.

**The difference between CLAUDE.md and memory files:**

| CLAUDE.md | Memory Files |
|-----------|-------------|
| You write it manually | Claude creates them automatically |
| Permanent baseline info | Specific things Claude learned over time |
| Your business context, voice, preferences | Past decisions, feedback, project details |
| Does not change often | Updates as your work evolves |

**Show your own CLAUDE.md on screen and walk through what's in it.**

---

## Block 3: Live Demo — Building a Brain File (15 min)

### Setup

Tell students you are going to build a CLAUDE.md together in real time. Have them follow along in their own project folder.

### Step 1: Open the Project Folder

Go to your Claude project folder. Show them where CLAUDE.md lives (at the root of the project, not inside a subfolder).

If you already have one, open it. If not, create a new file called CLAUDE.md.

### Step 2: Build the Brain File Together

Walk through each section live. Use your own real information so students see a complete, functional example — not a generic template.

**Section 1: Who You Are**

```markdown
# About Me

My name is Cheryl Tibbs. I am an international speaker and AI automation trainer based in Douglasville, GA.

I run three businesses:
- **Commercial Capital Connect (CCC):** A business finance marketplace offering equipment financing and working capital (term loans, lines of credit, revenue advances) to businesses throughout the US, including Puerto Rico.
- **AI Marvels:** An AI automation agency specializing in creating and deploying chatbots and AI-powered business tools.
- **EmergeStack Development Company:** A custom AI automation agency where I serve as CEO.

I am the President of CCC and Chief Strategist of AI Marvels.
```

**Section 2: My Voice and Writing Style**

```markdown
# My Voice and Style

- Conversational, confident, and direct. No academic tone.
- I am African American and my style blends street-smart with book-smart.
- I have a bit of sass and sarcasm but always deliver top-quality information.
- I am an ENFP. Energetic, creative, big-picture thinker.

NEVER use em dashes in anything you write for me. Use commas, periods, or parentheses instead.
NEVER say "y'all" in posts or content I will publish.
NEVER use filler phrases like "straightforward," "genuinely," or "honestly."
Always use Unicode text formatting for any output I will share publicly.
```

**Section 3: Organizations and Credentials**

```markdown
# Affiliations and Credentials

- BWAI (Black Women in AI)
- ABWA (American Business Women's Association)
- BEFN (Black Equipment Finance Network)
- AACFB (American Association of Commercial Finance Brokers)
- Google AI and Machine Learning certified
- Amazon Machine Learning certified
```

**Section 4: Standing Instructions**

```markdown
# How I Like to Work

- Keep responses concise. I do not need long explanations unless I ask for them.
- When creating content, always make it sound like it came from me, not a corporate account.
- My content is always ad-free. Do not suggest sponsored or paid content strategies.
- When in doubt about which business a task is for, ask me.
```

### Step 3: Save and Test

Save the CLAUDE.md file. Then open a fresh Cowork session and ask Claude a question that requires business context, something like:

"What's a good topic for a LinkedIn post this week?"

Show how Claude now responds with context from the Brain File versus how it would have responded without it.

**Talking Points:**
- "See how it already knows which businesses I have? I did not tell it in this conversation. It read CLAUDE.md."
- "This is the difference between a generic AI response and a response that's actually built for your situation."
- "Once your Brain File is solid, every interaction gets better automatically."

---

## Block 4: The Auto-Memory System (10 min)

### Talking Points

Beyond CLAUDE.md (which you write manually), Claude also has an auto-memory system. This is Claude learning from your conversations and storing that knowledge for future sessions.

**How it works:**
- As you work together, Claude notices things worth remembering: how you like things done, decisions you've made, project details, feedback you've given.
- Claude saves those as memory files inside a `memory/` folder in your project.
- The next time you open a session, Claude reads those memory files and already knows what you told it before.

**The four types of memories Claude creates:**

| Memory Type | What It Contains |
|-------------|-----------------|
| **User** | Information about you — your role, expertise level, preferences |
| **Feedback** | Corrections and confirmations — what to do more of, what to never do again |
| **Project** | Active work details — who is doing what, deadlines, decisions made |
| **Reference** | Where to find things — which tool tracks what, which Slack channel covers which topic |

**Why this matters for your workflow:**
- You stop repeating yourself. Claude already knows the corrections you gave it two weeks ago.
- Your context builds over time. The longer you work with Claude, the better it knows you.
- You can also tell Claude to remember something directly: "Remember that I want all proposals sent to clients as PDFs, not Word docs." Claude will save that.

**What you should NOT expect from auto-memory:**
- It will not remember things you discussed in a completely separate project or workspace.
- Memories can become outdated. If something about your business changes, update or delete the old memory.
- Auto-memory is not a replacement for CLAUDE.md. CLAUDE.md is your permanent baseline. Auto-memory is the living layer on top.

---

## Block 5: Live Demo — Memory in Action (10 min)

### Demo Flow

**Step 1: Show the memory folder**
Open your project folder and navigate to the `memory/` directory. Show students the files that are there. Open one or two so they can see what a memory file looks like.

**Step 2: Create a memory live**
Tell Claude something worth remembering during the demo. Example:

"Remember that for CCC, all deal submissions should be packaged as a single PDF, not as separate documents. Lisa should always default to this format."

Then show the memory file that gets created.

**Step 3: Show memory working across sessions**
Open a fresh Cowork session. Ask Claude about deal packaging. Show that it already knows your preference without you repeating it.

**Talking Points:**
- "This is not magic. It's a file system. But the result feels like magic because Claude actually remembers you."
- "Every correction you give Claude can become a memory. That is how you train your AI OS to work exactly the way you want."
- "If you ever want to see what Claude has remembered about you, ask: 'What do you remember about how I like to work?' It will tell you."

**Pause for Questions here.**

---

## Block 6: Maintaining Your Memory Over Time (5 min)

### Talking Points

Your memory system is only as good as how well you maintain it. Here is what to do on an ongoing basis:

**Add memories proactively:**
Anytime you correct Claude, tell it to remember the correction. Do not just fix the one output. Make it stick.

"I always say 'clients' not 'customers' when I'm talking about CCC. Remember that."

**Update memories when things change:**
If your business pivots, if you launch a new service, if your preferences change, update your Brain File. Outdated context is worse than no context because it will produce confidently wrong answers.

**Review memories periodically:**
Every month or so, ask Claude: "What do you have in your memory system about me?" Go through it and prune anything that's no longer accurate.

**Delete memories that are no longer true:**
Tell Claude: "Remove the memory about [specific thing]. That's changed." Claude will delete the file.

**The big picture:**
Your AI OS gets smarter the more you use it, BUT only if you maintain it. A Brain File you wrote 6 months ago and never updated is a problem. Treat your memory system like you'd treat your CRM. Keep it current and it will serve you well.

---

## Block 7: Hands-On Exercise (10 min)

### Exercise Instructions

Have students start building their own CLAUDE.md right now in class. Give them this prompt:

"Open your project folder and create a new file called CLAUDE.md. Start with three sections: Who You Are, Your Voice and Style, and Standing Instructions. You have 8 minutes. Go."

Walk around (or monitor the room). Common places people get stuck:
- Not knowing what to put in the voice section (have them think about what they hate seeing in AI output)
- Overthinking the standing instructions (keep it simple: what do you never want Claude to do?)
- Not knowing where to save the file (root of the project folder, not in a subfolder)

If they finish early, have them ask Claude a question that requires business context and see if it uses the Brain File correctly.

### Debrief (last 2 min of this block)
Ask 1-2 students to share what they put in their standing instructions. This sparks ideas for everyone and builds community around a shared challenge: getting Claude to actually know you.

---

## Block 8: Wrap-Up + Preview of Session 5 (5 min)

### What We Covered Today
- What CLAUDE.md is and why it is the foundation of your AI OS
- How to write a Brain File with your business context, voice, and preferences
- How the auto-memory system works and why it matters
- The four types of memory Claude creates automatically
- How to maintain your memory system over time

### Your Homework Before Session 5
1. Complete your CLAUDE.md if you did not finish it in class
2. Have at least one conversation with Claude where you give a correction and tell it to remember the correction
3. Come back with a screenshot of a memory Claude created on its own

### Preview: Session 5 — Automation Workflows
Next session we connect everything. CLAUDE.md gives Claude your brain. Skills give Claude your playbook. Now we build the systems that make Claude run without you asking. Scheduled tasks, n8n workflows, chaining agents together. This is where your AI OS starts doing real work in the background while you focus on what only you can do.

---

## Resources for This Session

| Resource | Link |
|----------|------|
| GitHub Repo | github.com/tibby007/building-with-the-ai-sniper |
| Skills Generator Tool | https://skill-generator-zeta.vercel.app |
| AIJU Room | aijunkiesuniversity.com |
| Session 4 Student Guide | Linked in AIJU classroom |

---

## Instructor Notes

- This session has more live build time than any session so far. Your CLAUDE.md should be polished and real before class. Students need to see a completed Brain File, not a half-built draft.
- The memory demo is the moment students usually have the "oh wow" reaction. Give it room. Let them ask questions during Block 5.
- The common mistake students make is trying to put EVERYTHING in CLAUDE.md on day one. Coach them toward clarity over completeness. A focused Brain File is better than a bloated one.
- If students ask how much memory is too much: there is no hard cap, but quality matters more than quantity. One accurate, specific memory beats five vague ones.
- Cheryl's real examples (her three businesses, her voice preferences, her never-do-this rules) are the most compelling part of this session. Be specific and personal. Generic examples do not land the same way.
