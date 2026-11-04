# Part 1 of 6: From Prompts to Skills

*Series: Skills, Plugins, and Governance in the Enterprise*

## Brief

Most people start with Claude by writing better prompts, and most hit the same wall: good prompts live in one person's chat history and die there. This post argues that the real unlock is packaging know-how into skills, reusable instructions Claude loads when a task calls for them. Skills are SOPs written for an AI: the same discipline that makes a human procedure reliable makes a skill reliable. Close by noting that a skill alone is still just instructions, which sets up Part 2.

## Thesis

Prompts are personal and disposable. Skills are shared and durable. The shift from one to the other is the same shift organizations made from tribal knowledge to documented procedure.

## Outline

1. **Hook**
   - The prompt that worked perfectly once and that nobody (including you) could reproduce a month later.

2. **The limits of prompting**
   - Prompts live in individual chats, not in the organization.
   - Quality depends on who wrote it and how they phrased it that day.
   - No versioning, no ownership, no way to improve it for everyone at once.

3. **What a skill is**
   - A folder of instructions (and optionally scripts and reference files) Claude loads when relevant.
   - Loaded on demand, so it doesn't crowd every conversation.
   - Plain-language explanation for non-technical readers.

4. **Skills as SOPs for AI**
   - Parallels: clear trigger, defined steps, expected output, edge cases.
   - What good SOP writing teaches about good skill writing.
   - What's different: the reader is a model, so ambiguity is interpreted, not questioned.

5. **Before and after (personal example)**
   - A prompt you used repeatedly.
   - The skill you turned it into.
   - What changed: consistency, onboarding, time saved, fewer corrections.

6. **What makes a skill good**
   - Specific trigger description.
   - Concrete steps and examples.
   - Scoped narrowly enough to be reliable.

7. **Bridge to Part 2**
   - A skill is still just instructions. It can tell Claude what to do, but not connect to your tools or act at the right moment. That's where plugins come in.

## Personal angle to fill in

- [ ] A specific prompt-to-skill conversion from your work
- [ ] A metric or observable change (time, error rate, adoption)
- [ ] One lesson from writing SOPs that carried over directly

## LinkedIn hook ideas

- "Your best prompt is a single point of failure."
- "I've written SOPs for years. Skills are the same job with a different reader."

Prologe
Skills, Plugins, and Governance in the Enterprise

We went through a rapid development cycle the last few years that took us from chating with a model to building skills and plugins that let the model act in the world. This series of posts is about what I learned along the way, and how to apply it in your organization. My plan is to write six posts, each one a chapter in the story of how we got from prompts to skills to plugins to governance. I dug deep into my educational history and outlined the whole series before writing this first post. I very much felt reminded of the old day's writing 10 page papers about crutial topics like Lincolns Getisburg Address. I hope tht this series will find more real life application than those papers did, and that it will be useful to you in your work. I also hope it will be a fun read, and that you will enjoy the journey as much as I enjoy writing it.

