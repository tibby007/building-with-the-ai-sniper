# Session 5 Lesson Plan: Automation & Workflows — Putting Your AI OS on Autopilot

**Course:** Building with The AI Sniper
**Session:** 5 of 6
**Duration:** 60-75 minutes
**Instructor:** Cheryl Tibbs (The AI Sniper)
**Platform:** AI Junkies University (AIJU)

---

## Pre-Session Checklist

Before you go live, make sure:

- [ ] Claude Desktop is open and connected to your AIJU project folder
- [ ] Cowork mode is active
- [ ] You have at least one scheduled task already set up to demo live (a morning briefing works great)
- [ ] Your n8n account is open in a browser tab (even a free workspace is fine for the visual)
- [ ] A Zapier account is open in another tab so students can see the interface
- [ ] GitHub repo is open: github.com/tibby007/building-with-the-ai-sniper
- [ ] Session 5 folder is pushed to GitHub before class
- [ ] Slide deck is loaded and tested in Gamma

---

## Session Overview

By the end of this session, students will understand the difference between asking Claude to do something and setting up a system that does it on its own. They will know how to create scheduled tasks inside Claude, how to think about routines, and where bigger tools like n8n, Zapier, and cron jobs fit when they outgrow what Claude can do alone.

This is the session where the AI OS stops waiting for you to push the button. The work starts happening in the background while you sleep, while you are on a sales call, while you are at the gym.

### What Students Will Be Able to Do After This Session

- Explain the difference between a one-time task and an automated, recurring system
- Create a scheduled task inside Claude that runs on its own (daily, weekly, or at a set time)
- Understand what a routine is and how to chain steps so one action triggers the next
- Know what n8n, Zapier, and cron jobs are, in plain English, and when each one is worth reaching for
- Understand what a Claude managed agent is and how it runs work without you babysitting it
- Walk away with a clear "automate this next" list for their own business

---

## Session Outline with Timing

| Block | Topic | Time |
|-------|-------|------|
| 1 | Session 4 Recap + Hook | 10 min |
| 2 | The Big Idea: From Asking to Automating | 8 min |
| 3 | Scheduled Tasks & Routines (Live Demo) | 15 min |
| 4 | The Bigger Toolbox: n8n, Zapier, Cron Jobs | 12 min |
| 5 | Claude Managed Agents | 10 min |
| 6 | Choosing the Right Tool for the Job | 5 min |
| 7 | Hands-On Exercise | 10 min |
| 8 | Wrap-Up + Preview of Session 6 | 5 min |

---

## Block 1: Session 4 Recap + Hook (10 min)

### Part A: Session 4 Recap — Memory & Context (5 min)

**What we built:** A CLAUDE.md Brain File that gives Claude permanent context about you, plus an understanding of how the auto-memory system learns and stores things over time.

**Talk through this on screen:**
- "Last session we gave Claude a brain. It now knows who you are, what your businesses do, and how you like to work. It does not start every conversation with amnesia anymore."
- Pull up your CLAUDE.md and the memory folder. Remind them this is the foundation everything else sits on.
- Ask the room: "Who finished their Brain File? Who caught Claude using something it remembered about you on its own?"

**Quick live check:**
"Drop in the chat: one thing you put in your CLAUDE.md that changed how Claude responds to you. Even one line counts."

**Key thing to reinforce:**
"Here is where we are. Claude has a home base (Session 1). It has hands (Session 2). It has a playbook of skills (Session 3). It has a brain that remembers you (Session 4). Today we give it a schedule. Today the system starts working without you asking."

---

### Part B: Hook into Today's Session (5 min)

Bridge from memory into automation:

"Let me ask you something. How many times a week do you do the exact same task? You open Claude, you ask for the same kind of summary, the same check, the same report. Monday morning you want to know what is on your plate. Friday afternoon you want a recap of the week. Every single day you want to know which leads went cold."

(Pause for nods)

"Right now you are the trigger. Nothing happens until you sit down and ask. That is fine for some things. But the whole point of building an AI operating system is that an operating system runs on its own. Your phone does not wait for you to manually check for new email every five minutes. It checks for you and tells you when something shows up."

"That is what today is about. We are going to take the tasks you keep repeating and set them up to run on their own. Some of that happens right inside Claude. Some of it happens with bigger tools you connect to. By the end of today you will know exactly what to automate first and which tool to use to do it."

---

## Block 2: The Big Idea — From Asking to Automating (8 min)

### Talking Points

**The core shift:**
Up to now, you have been the one who starts every task. You type a prompt, Claude responds. That is a one-time task. It is reactive. It only happens when you make it happen.

Automation flips that. You set the system up once, and it runs on a trigger that is not you sitting at the keyboard. The trigger might be a time (every morning at 6am), an event (a new lead comes in), or another task finishing (the report is done, now send it).

**Three words to put on the screen:**

| Word | Plain English | Example |
|------|--------------|---------|
| **Trigger** | What kicks the work off | A time, a new email, a form submission |
| **Action** | What actually gets done | A summary is written, a message is sent, a row is added |
| **Routine** | A series of actions chained together | Pull the data, write the summary, email it to me, log it |

**The mindset for non-developers:**
"You do not need to know how to code to automate. You need to know two things. What do I keep repeating? And what should kick it off? If you can answer those two questions, you can automate it. The tool is just the how."

**Set expectations honestly:**
"Some of what we cover today you can do today, inside Claude, by yourself, in two minutes. Some of it (n8n, Zapier, cron jobs) is bigger and you grow into it. I am not going to make you build a complicated workflow on a live call. I am going to show you what each tool is, what it is good for, and when it is worth your time. That way you never overbuild and you never reach for a sledgehammer when you need a thumbtack."

---

## Block 3: Scheduled Tasks & Routines — Live Demo (15 min)

### Setup

This is the hands-on heart of the session. Tell students to follow along in their own Cowork window. This is the automation they can set up today with zero extra tools.

### Step 1: Explain What a Scheduled Task Is (2 min)

A scheduled task is something you ask Claude to run automatically, on a schedule you set, without you being there to start it.

"Think of it like setting an alarm. You set it once. It goes off on its own. Except instead of just making noise, it does actual work for your business."

Examples that land with this audience:
- A morning briefing every day at 6am (calendar, priorities, anything urgent)
- A weekly content recap every Friday
- A daily check for leads that have gone quiet
- A month-end reminder with your numbers to review

### Step 2: Create a Scheduled Task Live (6 min)

In Cowork, type a natural-language request. Show them you do not need special syntax, you just describe what you want and when.

Example to type on screen:

> "Every weekday morning at 7am, give me a briefing of my calendar for the day, my top three priorities, and anything urgent in my email. Keep it short."

Talk through what happens:
- "Notice I did not write any code. I described what I want and when. Claude sets up the schedule."
- Show the scheduled task getting created and confirm the timing.
- "This will now run every weekday at 7am whether I open Claude or not. It is in the system."

### Step 3: Show a Routine (Chaining) (4 min)

Now level it up. A routine is when one task does several steps in a row.

Example to type on screen:

> "Every Friday at 4pm, pull my LinkedIn engagement for the week, summarize what performed best, and draft three post ideas for next week based on what worked."

Talk through it:
- "See how that is three actions in one trigger? Pull the data, summarize it, then create something new from it. That is a routine. One trigger, a chain of actions."
- "This is the difference between a to-do list and an assistant. A to-do list reminds you to do the work. This does the work and hands you the result."

### Step 4: Show How to Manage Scheduled Tasks (3 min)

- Show students how to view what is currently scheduled. ("Show me my scheduled tasks.")
- Show how to change or cancel one. ("Change my morning briefing to 6:30am instead of 7." / "Stop the Friday recap task.")
- "You are always in control. Nothing runs that you did not set up, and you can change or kill any of it any time."

**Pause for Questions here.**

---

## Block 4: The Bigger Toolbox — n8n, Zapier, Cron Jobs (12 min)

### Framing (1 min)

"Scheduled tasks inside Claude are powerful, but they live inside Claude. Sometimes you need to connect a bunch of different apps that do not naturally talk to each other. That is where these next three tools come in. I am going to show you what each one is and when you would actually reach for it. You do not need to master these today. You just need to know they exist and what they are for."

### Zapier (4 min)

**Plain-English definition:**
Zapier is a connector service. It links apps you already use so that when something happens in one app, something automatically happens in another. No code.

"Think of Zapier as the middleman that passes notes between your apps. When a new lead fills out your form, Zapier can automatically add them to your CRM, send you a text, and add them to an email sequence. You set it up once and it just runs."

**The Zapier vocabulary (put on screen):**
- A "Zap" is one automation (a trigger plus one or more actions)
- The trigger is the "when this happens"
- The action is the "do this"

**When to reach for it:**
- You want to connect two or more popular apps quickly
- You are not technical and you want the simplest possible setup
- The automation is fairly simple (when X happens, do Y)

Show the Zapier interface briefly. Point out how readable it is: "When this, do that."

### n8n (4 min)

**Plain-English definition:**
n8n does the same kind of thing as Zapier (connecting apps and automating steps) but it is more powerful and more flexible. You build your workflow visually by connecting boxes on a canvas. It can handle more complicated logic and you can self-host it.

"If Zapier is the easy connector, n8n is the power tool. It can do everything Zapier does plus the complicated stuff. The tradeoff is it has a steeper learning curve. You will grow into this one."

**When to reach for it:**
- Your automation has many steps or branching logic ("if this, do A, otherwise do B")
- You want more control or you are watching costs at scale
- You have someone technical helping, or you are ready to learn a more advanced tool

Show the n8n canvas briefly. Point out the visual node-to-node flow: "Each box is a step. You connect them like a flowchart that actually runs."

**Important for this audience:**
"You have a whole team member for this. If you are in my world, Marco is the n8n specialist. The point of knowing what n8n is, is so you know what to ask for when you need it. You do not have to be the one building it."

### Cron Jobs (3 min)

**Plain-English definition:**
A cron job is the original "run this on a schedule" tool. It is a developer-level way to say "run this exact thing at this exact time, automatically, forever." Cron is the engine that sits underneath a lot of scheduling, including the scheduled tasks you set up in Claude.

"You will hear the word cron thrown around. Here is all you need to know. Cron is just a schedule keeper. It is the part that says 'run at 6am every day.' When you set a scheduled task in Claude in plain English, something cron-like is doing the timing for you behind the scenes. The difference is you did not have to learn the cron code to do it."

**Put this on screen so it is not scary:**
A raw cron schedule looks like this: `0 6 * * 1-5`
That means "6:00am, every weekday." That is it. Five numbers that mean minute, hour, day, month, weekday.

**When it matters to you:**
- Mostly when a developer or a tool asks you to set a schedule and shows you that format
- You will rarely write raw cron yourself. Claude and tools like Zapier and n8n let you set schedules in plain language or with a calendar picker instead

"The reason I am even showing you this is so the word never intimidates you again. Cron is just a clock with a job."

---

## Block 5: Claude Managed Agents (10 min)

### Talking Points

**The plain-English definition:**
A managed agent is Claude running a job mostly on its own, start to finish, without you guiding every single step. You give it the goal and the boundaries. It figures out the steps and does the work, then comes back with the result.

"A regular prompt is like texting an employee one instruction at a time. A managed agent is like handing a trusted employee a project and saying 'handle this, come find me when it is done or if you get stuck.'"

**How this connects to everything we have built:**
- CLAUDE.md (Session 4) gives the agent context about you and your business
- Skills (Session 3) give the agent the specific playbooks for how you do things
- Connectors (Session 2) give the agent the hands to take action
- Scheduled tasks (today) give the agent the trigger to start on its own

"This is why we built in the order we did. A managed agent is only as good as the brain, the skills, and the hands you gave it. You have been building the foundation for this the whole course."

**What a managed agent can do for a non-developer:**
- Run a multi-step project (research, draft, organize, deliver) without you steering each move
- Operate on a schedule so it kicks off on its own
- Use your skills and your context so the output sounds like you and follows your rules
- Know when to stop and ask you instead of guessing on something important

**The boundaries (be honest here):**
"An agent is powerful but it is not a free-for-all. You set the guardrails. You decide what it is allowed to touch, what it should never do without asking, and when it should check in with you. The good news is everything you put in your Brain File and your skills is already setting those guardrails. The better your foundation, the more you can trust the agent to run."

**Real-world example for Cheryl's world:**
"In my businesses, I do not do everything by hand. I have agents named for the jobs they do. Betsy writes LinkedIn content. Lisa qualifies deals for CCC. Winston builds out the follow-up automations. Each one has its lane, its skills, and its context. That is a managed agent setup. You are building toward the same thing for your business, one piece at a time."

**Pause for Questions here.**

---

## Block 6: Choosing the Right Tool for the Job (5 min)

### Talking Points

Put this decision guide on screen. This is the takeaway that keeps students from overbuilding.

| If you want to... | Use this | Why |
|-------------------|----------|-----|
| Run a recurring task that lives inside Claude (briefings, recaps, checks) | A scheduled task in Claude | Fastest. No extra tools. Set it in plain English today. |
| Connect two or three popular apps simply (form to CRM to text) | Zapier | Easiest connector. Readable. No code. |
| Build a complex, multi-step or branching workflow across many apps | n8n | Most powerful and flexible. Worth growing into or delegating. |
| Run something on a precise schedule at the developer level | Cron (usually behind the scenes) | You rarely touch it directly. Tools handle it for you. |
| Hand off a whole multi-step job for Claude to run on its own | A managed agent | Combines your brain, skills, and hands into autonomous work. |

**The rule to repeat out loud:**
"Start with the simplest tool that does the job. Do not build an n8n workflow when a scheduled task would do it. Do not hand a managed agent a job you have not even turned into a skill yet. Match the tool to the size of the job. That is how you stay efficient instead of busy."

---

## Block 7: Hands-On Exercise (10 min)

### Exercise Instructions

Have students set up one real scheduled task right now in class. Give them this prompt:

"Open Cowork. Think of one thing you want to know or have done at the same time every day or every week. Then ask Claude to set it up as a scheduled task. Describe what you want and when. You have 7 minutes. Go."

Walk around (or monitor the room). Common places people get stuck:
- Picking something too big for a first automation (coach them toward something simple: a daily briefing, a weekly recap)
- Not specifying a time (remind them the trigger needs a "when")
- Overthinking the wording (remind them it is plain English, not code)

Starter ideas to offer the room if they are stuck:
- "Every morning at 7am, tell me my top three priorities for the day."
- "Every Friday at 3pm, recap what I got done this week."
- "Every Monday at 8am, remind me what is due this week and flag anything overdue."

### Debrief (last 2 min of this block)
Ask 1-2 students to share the scheduled task they set up. Then ask the whole room: "What is one thing you do every week that you are now going to automate?" This builds the "automate this next" mindset that carries into Session 6.

---

## Block 8: Wrap-Up + Preview of Session 6 (5 min)

### What We Covered Today
- The shift from asking Claude to do something to building systems that run on their own
- Triggers, actions, and routines in plain English
- How to create and manage scheduled tasks inside Claude
- What n8n, Zapier, and cron jobs are, and when to reach for each
- What a Claude managed agent is and how it builds on everything in the course
- How to choose the simplest tool for the job

### Your Homework Before Session 6
1. Set up at least one scheduled task and let it run at least once before next session
2. Write down three things you do repeatedly in your business that are good automation candidates
3. Bonus: explore the Zapier or n8n interface for ten minutes just to get familiar with what a workflow looks like

### Preview: Session 6 — Putting It All Together
Next session is the finale. We take everything from the whole course (your home base, your connectors, your skills, your brain, and your automations) and assemble it into one complete AI operating system. You will leave with a working command center that knows you, takes action for you, and runs in the background. This is where it all clicks into one system.

---

## Resources for This Session

| Resource | Link |
|----------|------|
| GitHub Repo | github.com/tibby007/building-with-the-ai-sniper |
| Zapier | zapier.com |
| n8n | n8n.io |
| AIJU Room | aijunkiesuniversity.com |
| Session 5 Student Guide | Linked in AIJU classroom |

---

## Instructor Notes

- The live scheduled-task demo is the moment that lands hardest this session. Have a real, working task ready to show before class so students see automation actually firing, not just described.
- Do NOT try to build a live n8n or Zapier workflow on the call. The goal this session is recognition and confidence, not mastery. Show the interfaces, explain the use cases, move on. Building those is a session of its own and a job you can delegate.
- The cron block is where you defuse intimidation. Keep it light. The whole point is that students stop being scared of the word. Five numbers and a clock. That is it.
- The managed agents block is where you tie the whole course together. Slow down and connect it back to Sessions 2, 3, and 4 explicitly. Students should feel the payoff of the order we built things in.
- The biggest mistake students make after this session is overbuilding. Hammer the "simplest tool for the job" rule. A working scheduled task beats an abandoned n8n workflow every time.
- Use your real agents (Betsy, Lisa, Winston) as the managed-agent example. Naming them makes the concept concrete and it is the most memorable part of this session.
