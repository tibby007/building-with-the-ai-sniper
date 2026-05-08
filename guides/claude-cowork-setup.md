# Claude Cowork Setup Guide

How to set up Cowork mode, run your first session, and start working with Claude on real files.

## What Is Cowork?

Cowork is a mode inside Claude Desktop that turns Claude from a chatbot into a real working partner. In regular Claude Desktop, you're just having a conversation. In Cowork, Claude can:

- Read and write files on your computer (in a folder you choose)
- Run code and scripts
- Create documents, spreadsheets, and presentations
- Connect to your tools through MCP servers
- Use skills (specialized instructions for specific tasks)
- Remember things about you and your business

Think of it this way: regular Claude is like texting someone smart. Cowork is like having that smart person sitting at a desk in your office with access to your files.

## How to Access Cowork

1. Open Claude Desktop
2. Look for the **Cowork** option in the left sidebar or mode selector
3. Click it to enter Cowork mode

If you don't see Cowork, make sure:
- Your app is updated to the latest version
- You're on a Pro or Team plan (Cowork is not available on free plans)

## Selecting Your Working Folder

This is the most important step. When you start a Cowork session, Claude will ask you to select a folder. This is the folder Claude can read from and write to.

**Best practices for choosing a folder:**

- Create a dedicated folder like `Documents/Claude/Projects/` or `Desktop/AI-Workspace/`
- Don't point Claude at your entire home directory or Documents folder. Keep it scoped.
- You can organize subfolders however you want inside it
- You can change folders between sessions

**What Claude can do with your folder:**
- Read any file in it
- Create new files
- Edit existing files
- Organize and move files around

**What Claude cannot do:**
- Access files outside your selected folder (unless you grant additional access)
- Delete files permanently without your confirmation
- Access system files or other applications' data

## Your First Cowork Session

Once you've selected a folder:

1. **Tell Claude about yourself.** Start with something like: "I'm [name], I run [business]. I'm going to be using this workspace for [purpose]."
2. **Ask Claude to create a CLAUDE.md file.** This is your project configuration file. Say: "Create a CLAUDE.md file with my basic info and preferences."
3. **Test it out.** Ask Claude to create a simple document. "Write me a one-page overview of my business and save it as a markdown file."
4. **Check the output.** Look in your selected folder. The file should be there.

## Setting Up Your Project Structure

A good project folder structure makes everything easier. Here's a simple starting point:

```
Your-Folder/
  CLAUDE.md          (Your project config - Claude reads this first)
  skills/            (Custom skills you build)
  brand/             (Your brand assets, logos, colors, voice guide)
  outputs/           (Where Claude puts finished work)
  drafts/            (Work in progress)
```

You don't have to create all of this manually. You can literally tell Claude: "Set up my project folder with a skills directory, brand directory, outputs directory, and drafts directory." Claude will create them for you.

## Installing Plugins and Skills

Plugins add superpowers to Cowork. They're bundles of skills and MCP connections.

To see what's available:
- Ask Claude: "What plugins do I have installed?"
- Ask Claude: "What skills are available?"
- Ask Claude: "Search for plugins related to [what you need]"

To install a plugin:
- Ask Claude to recommend plugins for your use case
- Claude will walk you through the installation

## Tips

- **Keep CLAUDE.md updated.** This is Claude's first read every session. If your priorities change, update it.
- **Use skills for repetitive tasks.** If you find yourself giving Claude the same instructions over and over, that's a skill waiting to be created.
- **Save important context to memory.** Tell Claude "Remember that [fact]" and it'll store it for future sessions.
- **Don't overthink the folder structure.** Start simple. You can always reorganize later.

## Troubleshooting

**Claude says it can't access my files:** Make sure you've selected the right folder. Try reselecting it.

**Files aren't showing up where I expect:** Claude saves files to your selected workspace folder. Check there first.

**Cowork mode isn't available:** Update Claude Desktop to the latest version. Check that your plan supports it.

## Next Steps

Once Cowork is running, check out the [Skills Explained](skills-explained.md) guide to learn how to build custom skills, or the [Memory System](memory-system.md) guide to set up persistent context.
