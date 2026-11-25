# learn-concept

A Claude skill for learning any new concept from first principles, as fast as possible.

## What it does

1. **Setup (one turn):** asks for your current level (levels written for the topic), your scope and context, and how deep you want to go (intuition, working or deep).
2. **Map and level check:** breaks the topic into building blocks ordered by what depends on what, groups them into milestones, and runs a short quiz to check your level, so it can skip what you already know.
3. **Teaching:** for each block, why it exists, the core idea, an example or analogy only where it speeds things up, then one reasoning check.
4. **Wrong answers:** works out the specific misconception behind a wrong answer and fixes it, rather than re-teaching the block.
5. **Branching:** if a part of the topic relies on a concept you are missing, it takes a short detour through just the slice you need (same flow, 1–3 blocks), then returns.
6. **Milestone tests:** questions that go beyond recall (understand, apply, analyze, evaluate), with spaced recall of earlier milestones.
7. **Progress record:** a small file per topic so you can resume in a later session.

**Check metric:** time to understanding. Any step that doesn't cut it or protect it is dropped.

## Install

**Claude Code:**

```
/plugin marketplace add karan-domadia/Learning-skill
/plugin install learn-concept@learn-concept
```

**Claude.ai (web or desktop):** download `skills/learn-concept/SKILL.md`, put it in a folder named `learn-concept`, zip the folder, and upload it under Settings → Capabilities → Skills.

## Use

Just ask: "Help me learn Bayesian inference" or "I want to understand how TCP congestion control works."

## License

MIT
