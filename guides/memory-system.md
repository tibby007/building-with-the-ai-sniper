# Memory System Guide

How Claude's memory works, what to store, and what to skip.

## The Problem Memory Solves

Every time you start a new conversation with Claude, it starts fresh. No memory of who you are, what you do, or what you've told it before. That's fine for one-off questions, but terrible for ongoing work.

The memory system fixes this. It gives Claude a place to store and retrieve important information about you, your business, your preferences, and your projects. So instead of re-explaining everything every session, Claude already knows the context.

## How Memory Works in Practice

Claude's memory in Cowork and Code uses files. Specifically:

1. **CLAUDE.md** - Your project configuration file. Claude reads this FIRST every session. This is your "working memory."
2. **Memory directory** - A folder (usually `.auto-memory/` or `memory/`) where Claude stores additional context. This is your "long-term memory."

When you start a session, Claude reads CLAUDE.md to understand who you are and what you're working on. When it needs more detail, it checks the memory directory.

## What to Store in Memory

**Store these (high value):**
- Your name, role, and business details
- Communication preferences (tone, format, things to avoid)
- Key contacts and their roles
- Business rules that never change
- Industry terminology and acronyms you use
- Current projects and their status
- Tools and systems you use daily

**Think twice about these (medium value):**
- Meeting notes (better as separate files in your project)
- Full documents (reference them by file path instead)
- Temporary information (put it in CLAUDE.md with a date, remove when outdated)

**Don't store these (low value or risky):**
- Passwords, API keys, or sensitive credentials (use environment variables)
- Information that changes daily (it'll be wrong more than it's right)
- Entire conversation histories (too much noise)
- Other people's personal information (privacy matters)

## Setting Up Your Memory System

### Step 1: Create the CLAUDE.md

This file goes in the root of your project folder. See the [project template](../project-template/CLAUDE.md) for a complete annotated version.

At minimum, include:
- Who you are
- What your business does
- How you want Claude to communicate
- Your current priorities

### Step 2: Create the Memory Directory

```
your-project/
  .auto-memory/
    MEMORY.md       <-- Index file
```

The `MEMORY.md` file is your memory index. See the [template](../project-template/.auto-memory/MEMORY.md) for a starter structure.

### Step 3: Tell Claude to Remember Things

During a conversation, when something important comes up:

- "Remember that Marcus is my business partner and handles all vendor relationships."
- "Store this: our standard payment terms are Net 30 for all clients."
- "Add to memory: when I say 'LOC' I mean Line of Credit."

Claude will add this to your memory files.

### Step 4: Keep It Updated

Memory only works if it's current. Set a routine:

- **Weekly:** Update CLAUDE.md with current priorities and projects
- **Monthly:** Review memory files and remove outdated information
- **As needed:** Correct anything Claude gets wrong ("Update memory: Marcus left the company, our new partner is Diana")

## How Claude Uses Memory

When you start a session, here's what happens behind the scenes:

1. Claude reads `CLAUDE.md` to get your core context
2. If Claude needs more detail, it checks files in the memory directory
3. Claude uses this context to inform all its responses
4. If you tell Claude to remember something new, it updates the appropriate file

You don't have to tell Claude to check memory. It does this automatically in Cowork and Code.

## Common Mistakes

**Storing too much.** If your memory files are thousands of lines long, they lose their value. Claude has to read all of it, and important details get buried. Keep it tight.

**Never updating.** Stale memory is worse than no memory. If Claude keeps referencing a project you finished three months ago, it's time to clean house.

**Storing sensitive data.** Memory files are plain text. Anyone with access to your project folder can read them. Don't put passwords, financial details, or confidential client information in memory.

**Duplicating information.** If it's already in CLAUDE.md, it doesn't need to also be in memory. CLAUDE.md is the primary source. Memory is for the overflow.

## Tips

- Start with CLAUDE.md only. Add the memory directory when you find yourself needing more context than CLAUDE.md can hold.
- Use clear, simple language in your memory files. Write like you're briefing a new employee on their first day.
- Organize memory by category (people, rules, terms, projects) not by date.
- When in doubt, ask Claude: "What do you know about [topic]?" to see if it has the context already.

## Next Steps

Check the [project template](../project-template/) for ready-to-use CLAUDE.md and MEMORY.md files. Copy them into your own project and fill in your details.
