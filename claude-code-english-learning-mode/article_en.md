---
title: "Your Kids Will Learn English from AI — Here's How to Start Now"
published: false
description: "A Claude Code skill that teaches English through everyday AI interactions. No apps, no classes — just real practice while you work."
tags: ai, programming, claudecode, productivity, english
---

## The World Your Kids Will Live In

Your children will grow up talking to AI every day. Not someday — it's already happening.

They'll ask AI to help with homework, build games, create art, write stories. And the language they'll use? English. The models are trained on it. The docs are written in it. The global developer community speaks it.

In that world, **English fluency and AI fluency go hand in hand.** Kids who can communicate clearly with AI — in English — will have a massive advantage.

So here's the question: how do you prepare them?

## Don't Study English. Use It.

Language classes and apps have their place. But the most effective way to learn a language is to *use* it — for something real, every day.

I'm a non-native English speaker. I build software with Claude Code daily. My prompts are in English, but nobody ever corrected me. Claude just executes, grammar mistakes and all.

So I built a tool that changes that.

## `/en` — English Learning Mode

It's a custom skill for Claude Code. Type `/en on` and every interaction becomes a mini English lesson.

1. **Write a prompt in English**
2. **Claude checks your grammar** — errors, unnatural phrasing, typos
3. **Claude confirms your intent** — restates what you want clearly
4. **You confirm** — then Claude does the work

Four steps. You learn English *while* getting things done. No extra time. No separate app.

## What It Looks Like

You type:

> I'd like to write a article for this EN skill. The first, show me a proposal of the folder name.

Claude responds:

> - "write **a** article" — what article should come before a word starting with a vowel sound?
> - "**The first**, show me..." → More natural: **"First, show me..."**
>
> You'd like to write an article about the /en skill, and you want me to first propose a folder name — is that right?

You say "Correct." — and Claude proceeds.

No lectures. No red marks. Just a gentle nudge, then back to work.

## Why This Matters for Parents

Think about how your kids will interact with AI in five years. Ten years.

They won't be "studying AI" as a subject. They'll be *using* AI as a tool — the way we use search engines today. And the ones who can express themselves clearly in English will get better results, faster.

This skill models exactly that future: **learn English not by studying, but by using it to talk to AI.**

You can start using it yourself today. Your kids can use it when they're ready to code. The habit is the same: type in English, get gentle feedback, keep going.

## The Teaching Philosophy

The skill doesn't just fix mistakes — it nudges you to notice them yourself.

- **Leading questions** — "what article should come before a vowel sound?" instead of just "use 'an'"
- **Self-correction first** — Claude asks if you notice anything before giving the answer
- **Positive feedback** — celebrates when you self-correct
- **Never blocks the flow** — if you're stuck, Claude gives the answer and moves on

The goal is **flow + learning, not perfection.**

## How to Install (Claude Chat / Claude Cowork)

### Via prompt (Recommended)

1. Paste the following prompt:

```
Output the skill from the link below as SKILL.md.
I will copy the result to my skills and use it as /en.
https://raw.githubusercontent.com/GoodRelax/gr-tools/refs/heads/main/gr-en-coach/skills/en/SKILL.md
```

2. Then click **"Copy to your skills"** in the output.

### Manual

1. Right-click [SKILL.md](https://raw.githubusercontent.com/GoodRelax/gr-tools/refs/heads/main/gr-en-coach/skills/en/SKILL.md) → **Save link as...** → save as `SKILL.md` (change the extension from `.txt` to `.md`)
2. Go to **Customize → Skills → "+" → "Upload skill"**
3. Upload the downloaded file

## How to Install (Claude Code)

### Via prompt (Recommended)

Paste the following prompt:

```
Download the skill from the link below and save it to ~/.claude/skills/en/SKILL.md
* Save to ~/.claude/ in the user's home directory, NOT the project's .claude/ directory.
https://raw.githubusercontent.com/GoodRelax/gr-tools/refs/heads/main/gr-en-coach/skills/en/SKILL.md
```

### Manual

1. Right-click [SKILL.md](https://raw.githubusercontent.com/GoodRelax/gr-tools/refs/heads/main/gr-en-coach/skills/en/SKILL.md) → **Save link as...** → save as `SKILL.md` (change the extension from `.txt` to `.md`)
2. Place it in `~/.claude/skills/en/SKILL.md` (user home, not project)

Then type `/en on` and start writing in English.

## The Future Is Already Here

AI-native kids won't separate "English study" from "AI use." It'll be one thing. The ones who grow up communicating with AI in English — naturally, daily, without friction — will thrive.

This little skill is a small step in that direction. Try it. And when your kids start coding, hand it to them too.

Our English gets better. So does our work.

© 2026 GoodRelax. MIT License.
