# Skills Explained

The anatomy of a skill, how they work, and how to create your own.

## What Is a Skill?

A skill is a set of instructions that tells Claude exactly how to do a specific task. It's a markdown file (always named `SKILL.md`) that Claude reads before executing the task.

Without a skill, you'd have to explain what you want every single time. With a skill, you explain it once, and Claude follows those instructions consistently every time you trigger it.

Real-world analogy: a skill is like a recipe card for your best employee. You wrote down exactly how you want something done, and they follow it step by step without you having to stand over their shoulder.

## Where Skills Live

Skills live in folders inside your project:

```
your-project/
  skills/
    meeting-notes/
      SKILL.md        <-- The instructions
    email-drafter/
      SKILL.md
    social-posts/
      SKILL.md
```

Each skill gets its own folder. The folder name is the skill name. Inside the folder, the `SKILL.md` file contains all the instructions.

You can also include supporting files in the skill folder:
- Templates
- Examples
- Reference documents
- Data files

Claude reads all of them when the skill runs.

## Anatomy of a SKILL.md

Every good skill has these sections:

### 1. Purpose
What does this skill do? One or two sentences.

### 2. When to Use
What triggers this skill? What phrases or situations should activate it?

### 3. Input
What does the user provide? What format should it be in?

### 4. Output
What does Claude produce? Be specific about the format, structure, and length.

### 5. Rules
Hard requirements Claude must follow. Things it should always do, never do, and edge cases to handle.

### 6. Examples (Optional but Recommended)
Show a sample input and the expected output. This is the single most powerful thing you can include. Claude learns from examples better than from rules alone.

## Creating Your First Skill

Let's say you write LinkedIn posts every week and you're tired of explaining your style to Claude each time.

**Step 1:** Create the folder structure
```
skills/
  linkedin-posts/
    SKILL.md
```

**Step 2:** Write the SKILL.md

```markdown
# LinkedIn Post Writer

## Purpose
Write LinkedIn posts that match my brand voice and drive engagement.

## When to Use
Use when I ask for a LinkedIn post, social content, or say "write a post about [topic]."

## Input
A topic, idea, news item, or experience I want to post about.

## Output
A LinkedIn post that is:
- 150-300 words
- Written in first person
- Opens with a hook (question, bold statement, or short story)
- Uses short paragraphs (1-2 sentences each)
- Ends with a question or call to action
- Includes 3-5 relevant hashtags at the bottom

## Rules
- Write like I talk: professional but not corporate
- No emojis in the main text (hashtags are fine)
- No em dashes
- Don't start with "I'm excited to announce" or "I'm thrilled"
- Include a personal angle or opinion, not just information
- Every post should teach something or challenge a common assumption

## Example

**Input:** "Write a post about why small businesses should stop waiting to adopt AI"

**Output:**
Most small business owners I talk to say the same thing about AI:

"I'll get to it when things slow down."

Things never slow down. That's the whole point.

The businesses winning right now aren't the ones with the biggest budgets. They're the ones who stopped waiting for the "right time" and started experimenting.

You don't need a developer. You don't need a PhD. You need 30 minutes and a willingness to try something new.

I set up an AI system last week that saves me 4 hours of admin work every day. Took me one afternoon.

What's one task in your business you wish someone else could handle?

#AI #SmallBusiness #Automation #BusinessGrowth #AITools
```

**Step 3:** Test it. Ask Claude to write a LinkedIn post and see if it follows your skill instructions.

## Tips for Better Skills

- **Be specific.** "Write well" is useless. "Write in short paragraphs, no more than 2 sentences each, using conversational language" is useful.
- **Include examples.** One good example is worth 20 lines of rules.
- **Start simple.** Your first version doesn't have to be perfect. Use it, see what needs adjusting, then refine.
- **Test edge cases.** What happens when the input is vague? What if the topic is sensitive? Add rules to handle those situations.
- **Keep it focused.** One skill should do one thing well. Don't make a skill that writes posts AND creates images AND schedules them. That's three skills.

## Advanced: Skills with Supporting Files

For complex skills, you can include additional files:

```
skills/
  proposal-writer/
    SKILL.md
    templates/
      proposal-template.md
    examples/
      sample-proposal-1.md
      sample-proposal-2.md
    reference/
      pricing-guide.md
```

Claude reads everything in the skill folder, so your SKILL.md can reference these files: "Use the template in templates/proposal-template.md as the starting structure" or "Follow the pricing guidelines in reference/pricing-guide.md."

## Next Steps

Check out the [example skill](../project-template/skills/example-skill/SKILL.md) in the project template for a complete, working skill you can modify. Then check the [Memory System](memory-system.md) guide to learn how to give Claude persistent context about you and your business.
