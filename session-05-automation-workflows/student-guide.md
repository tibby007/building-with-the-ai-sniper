# Session 5 Student Guide: Automation & Workflows — Putting Your AI OS on Autopilot

**Course:** Building with The AI Sniper
**Session:** 5 of 6
**Your Instructor:** Cheryl Tibbs (The AI Sniper)
**Platform:** AI Junkies University

Keep this guide. Everything we cover in class is here in writing so you can reference it later, build at your own pace, and come back to it any time you want to automate something new.

---

## Quick Catch-Up: Where We Are in the Series

If Session 4 gave Claude a brain, Session 5 gives Claude a schedule. This is where your AI OS stops waiting on you and starts running on its own.

Here is where we are in the build:

| Session | Topic | What It Gives Claude |
|---------|-------|---------------------|
| 1 | Foundation Setup | A home base (your project folder + Cowork) |
| 2 | MCPs & Connectors | Hands (ability to take action in the real world) |
| 3 | Skills & Agents | A skillset (repeatable jobs, done your way) |
| 4 | Memory & Context | A brain (permanent knowledge about you) |
| **5** | **Automation & Workflows** | **A schedule (working while you sleep)** |
| 6 | Putting It All Together | A full AI operating system |

---

## Prerequisites

Before this session, you should have:

- [ ] Claude Desktop installed and connected to your project folder (Session 1)
- [ ] At least one MCP or connector set up (Session 2)
- [ ] At least one skill in your project (Session 3)
- [ ] A CLAUDE.md Brain File in your project folder (Session 4)

If you are missing any of these, grab the student guides from Sessions 1-4 in the AIJU classroom. Automation works best when the brain, skills, and hands are already in place.

---

## Part 1: The Big Shift — From Asking to Automating

Here is what has been happening up to now. You open Claude. You type a request. Claude responds. That is a one-time task. Nothing happens until you make it happen. You are the trigger.

Automation flips that. You set something up once, and it runs on its own from then on. The trigger is no longer you sitting at the keyboard. It might be a time (every morning at 6am), an event (a new lead comes in), or another task finishing.

This is the whole reason we call it an AI operating system. An operating system runs in the background. Your phone does not wait for you to manually check for new messages. It checks for you and tells you when something shows up. That is what we are setting up for your business.

### The Three Words That Make Automation Click

| Word | Plain English | Example |
|------|--------------|---------|
| **Trigger** | What kicks the work off | A time, a new email, a form submission |
| **Action** | What actually gets done | A summary is written, a message is sent, a row is added |
| **Routine** | A chain of actions, one after another | Pull the data, write the summary, email it to me, log it |

### You Do Not Need to Code

To automate something, you only need to answer two questions:

1. What do I keep repeating?
2. What should kick it off?

If you can answer those, you can automate it. The tool is just the how.

---

## Part 2: Scheduled Tasks — The Automation You Can Set Up Today

A scheduled task is something you ask Claude to run automatically, on a schedule you set, without you being there to start it.

Think of it like setting an alarm. You set it once. It goes off on its own. Except instead of just making noise, it does real work for your business.

### Things Worth Scheduling

- A morning briefing every day (your calendar, top priorities, anything urgent)
- A weekly content recap every Friday
- A daily check for leads that have gone quiet
- A month-end reminder with your numbers to review
- A Monday rundown of what is due that week

### How to Create a Scheduled Task

You do not need any special code or syntax. You just describe what you want and when.

**Step 1:** Open Cowork.

**Step 2:** Type your request in plain English. Include WHAT you want and WHEN it should run.

Example:
> "Every weekday morning at 7am, give me a briefing of my calendar for the day, my top three priorities, and anything urgent in my email. Keep it short."

**Step 3:** Claude sets up the schedule and confirms the timing.

**Step 4:** That is it. It now runs on its own at the time you set, whether or not you have Claude open.

### How to Build a Routine (Chaining Steps)

A routine is when one trigger kicks off several actions in a row. This is where it stops feeling like a reminder and starts feeling like an assistant.

Example:
> "Every Friday at 4pm, pull my LinkedIn engagement for the week, summarize what performed best, and draft three post ideas for next week based on what worked."

That is three actions from one trigger: pull the data, summarize it, then create something new from it. A to-do list reminds you to do the work. A routine does the work and hands you the result.

### How to Manage Your Scheduled Tasks

You are always in control. Nothing runs that you did not set up.

| What You Want | What to Say |
|---------------|-------------|
| See everything you have scheduled | "Show me my scheduled tasks." |
| Change a time | "Change my morning briefing to 6:30am." |
| Stop one | "Stop the Friday recap task." |
| Add a new one | Just describe the new task and when it should run. |

---

## Part 3: The Bigger Toolbox — When Claude Alone Is Not Enough

Scheduled tasks are powerful, but they live inside Claude. Sometimes you need to connect a bunch of different apps that do not naturally talk to each other. That is where these tools come in.

You do not need to master these today. You need to know they exist and what each one is for, so you reach for the right one when the time comes (or know what to ask for when you delegate it).

### Zapier — The Easy Connector

**What it is:** Zapier links apps you already use so that when something happens in one app, something automatically happens in another. No code.

Think of Zapier as the middleman that passes notes between your apps. When a new lead fills out your form, Zapier can automatically add them to your CRM, text you, and drop them into an email sequence. Set it up once and it just runs.

**The vocabulary:**
- A "Zap" is one automation (a trigger plus one or more actions)
- The trigger is the "when this happens"
- The action is the "do this"

**Reach for Zapier when:**
- You want to connect two or three popular apps quickly
- You want the simplest possible setup with no code
- The automation is fairly simple (when X happens, do Y)

### n8n — The Power Tool

**What it is:** n8n does the same kind of thing as Zapier (connecting apps and automating steps) but it is more powerful and flexible. You build your workflow visually by connecting boxes (called nodes) on a canvas. It handles more complicated logic and can be self-hosted.

If Zapier is the easy connector, n8n is the power tool. It does everything Zapier does plus the complicated stuff. The tradeoff is a steeper learning curve. You grow into this one.

**Reach for n8n when:**
- Your automation has many steps or branching logic ("if this, do A, otherwise do B")
- You want more control, or you are managing costs at larger scale
- You have someone technical helping, or you are ready to learn a more advanced tool

**Important:** You do not have to be the one who builds the n8n workflow. The reason to understand what it is, is so you know what to ask for when you need it. This is a great thing to delegate.

### Cron Jobs — The Schedule Keeper Behind the Curtain

**What it is:** A cron job is the original "run this on a schedule" tool. It is a developer-level way to say "run this exact thing at this exact time, automatically, forever." Cron is the engine that sits underneath a lot of scheduling, including the scheduled tasks you set up in Claude.

Here is all you need to know. Cron is just a schedule keeper. When you set a scheduled task in Claude in plain English, something cron-like is doing the timing behind the scenes. The difference is you did not have to learn the cron code to do it.

**Do not let the format scare you.** A raw cron schedule looks like this:

```
0 6 * * 1-5
```

That means "6:00am, every weekday." Five values that stand for minute, hour, day, month, and weekday. That is the whole thing. A clock with a job.

**When it matters to you:**
- Mostly when a developer or a tool asks you to set a schedule in that format
- You will rarely write raw cron yourself. Claude, Zapier, and n8n all let you set schedules in plain language or with a calendar picker instead

The only reason this is in your guide is so the word never intimidates you again.

---

## Part 4: Claude Managed Agents

**What it is:** A managed agent is Claude running a whole job mostly on its own, start to finish, without you guiding every single step. You give it the goal and the boundaries. It figures out the steps, does the work, and comes back with the result.

A regular prompt is like texting an employee one instruction at a time. A managed agent is like handing a trusted employee a project and saying "handle this, come find me when it is done or if you get stuck."

### Why Everything in This Course Was Building Toward This

A managed agent is only as good as the foundation you gave it. Look at how the pieces stack:

| Course Piece | What It Gives the Agent |
|--------------|------------------------|
| Connectors (Session 2) | The hands to take action in real apps |
| Skills (Session 3) | The specific playbooks for how you do things |
| CLAUDE.md (Session 4) | The context about you, your business, and your rules |
| Scheduled tasks (Session 5) | The trigger to start on its own |

This is why we built in this order. By now you have laid the groundwork for an agent that can actually run.

### What a Managed Agent Can Do for You

- Run a multi-step project (research, draft, organize, deliver) without you steering each move
- Operate on a schedule so it kicks off on its own
- Use your skills and your context so the output sounds like you and follows your rules
- Know when to stop and ask you instead of guessing on something important

### The Guardrails

An agent is powerful but it is not a free-for-all. You set the boundaries. You decide what it is allowed to touch, what it should never do without asking, and when it should check in with you.

The good news: everything you put in your Brain File and your skills is already setting those guardrails. The stronger your foundation, the more you can trust the agent to run on its own.

### What This Looks Like in a Real Business

In Cheryl's businesses, the work is split across agents named for the jobs they do. Betsy writes LinkedIn content. Lisa qualifies deals for CCC. Winston builds the follow-up automations. Each one has its lane, its skills, and its context. That is a managed agent setup, and you are building toward the same thing for your business, one piece at a time.

---

## Part 5: Choosing the Right Tool for the Job

This is the table that keeps you from overbuilding. Match the tool to the size of the job.

| If you want to... | Use this | Why |
|-------------------|----------|-----|
| Run a recurring task inside Claude (briefings, recaps, checks) | A scheduled task in Claude | Fastest. No extra tools. Set it in plain English today. |
| Connect two or three popular apps simply (form to CRM to text) | Zapier | Easiest connector. Readable. No code. |
| Build a complex, multi-step or branching workflow across many apps | n8n | Most powerful and flexible. Worth growing into or delegating. |
| Run something on a precise schedule at the developer level | Cron (usually behind the scenes) | You rarely touch it directly. Tools handle it for you. |
| Hand off a whole multi-step job for Claude to run on its own | A managed agent | Combines your brain, skills, and hands into autonomous work. |

**The rule to live by:** Start with the simplest tool that does the job. Do not build an n8n workflow when a scheduled task would do it. Do not hand a managed agent a job you have not even turned into a skill yet. A working scheduled task beats an abandoned complicated workflow every time.

---

## Part 6: Quick Reference

### Create a Scheduled Task
Open Cowork and describe what you want and when, in plain English. Example: "Every morning at 7am, give me my top three priorities for the day."

### Build a Routine
Chain steps in one request. Example: "Every Friday at 4pm, pull my week's engagement, summarize it, and draft three post ideas."

### See What Is Scheduled
Ask Claude: "Show me my scheduled tasks."

### Change or Stop a Task
Just say it: "Change my briefing to 6:30am." / "Stop the Friday recap."

### The Tool Cheat Sheet
- Inside Claude, recurring = scheduled task
- Connect a few apps simply = Zapier
- Complex multi-app workflow = n8n
- Schedule format under the hood = cron
- Hand off a whole job = managed agent

### Troubleshooting

| Problem | What to Check |
|---------|--------------|
| Your scheduled task did not run | Did you confirm the time and time zone when you set it up? Ask: "Show me my scheduled tasks" to verify it is active. |
| You are not sure if a task is still scheduled | Ask Claude: "Show me my scheduled tasks." |
| The automation feels too complicated to build | You may be reaching for the wrong tool. Check the cheat sheet. A scheduled task may do what you need. |
| You want to connect apps Claude is not connected to | That is a Zapier or n8n job, not a scheduled task. Pick the connector tool. |
| Cron format showed up and you froze | Five values: minute, hour, day, month, weekday. You almost never write it by hand. Use plain language in Claude instead. |
| You want an agent to run a job but it keeps asking you questions | That is the guardrails working. Tighten your CLAUDE.md and skills so it has the context to act with less hand-holding. |

---

## Your Homework Before Session 6

1. Set up at least one scheduled task and let it run at least once before next session.
2. Write down three things you do repeatedly in your business that are good automation candidates.
3. Bonus: spend ten minutes inside the Zapier or n8n interface just to see what a workflow looks like. You are building familiarity, not mastery.

---

## What's Coming in Session 6: Putting It All Together

Session 6 is the finale. We take everything from the whole course and assemble it into one complete AI operating system:

- Your home base (the project folder and Cowork)
- Your connectors (the hands)
- Your skills (the playbooks)
- Your Brain File (the memory)
- Your automations (the schedule)

You will leave with a working command center that knows you, takes action for you, and runs in the background. This is where every piece we built clicks into one system.

---

## Resources

| Resource | Link |
|----------|------|
| GitHub Repo (all course materials) | github.com/tibby007/building-with-the-ai-sniper |
| Zapier | zapier.com |
| n8n | n8n.io |
| AIJU Room | aijunkiesuniversity.com |
| Session 1-4 Student Guides | In your AIJU classroom |
