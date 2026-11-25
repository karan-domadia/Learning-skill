---
name: "learn-concept"
description: "Teach a new concept from first principles: check the learner's level, map building blocks, teach with examples and analogies, test at milestones. Use when the user wants to learn a topic."
---

# Learn a Concept

**Goal:** the user understands a new concept. They can explain it, reason with it, spot it in a new situation, and tell it apart from nearby ideas. The goal is not to implement or build something.

**Check metric: time to understanding (TAT).** Every step below either cuts TAT or protects it, by catching gaps before they compound. If a step adds time without doing either, drop it.

## TAT rules (apply throughout)

- Never teach what the user already knows. Skip any building block they showed they know in the level check.
- Ask setup questions together in one turn, never one at a time. If the user's request already answers a setup question, don't ask it.
- One idea per block. Explanations stay short (roughly 100–250 words), followed by a check.
- Use an example or analogy only when it gets to understanding faster. One good one beats three.
- A check during teaching is 1 question. A milestone test is 3–6 questions.
- No preamble, recaps of what you just said, encouragement filler, or restating the plan.
- If the user says "I know this" or "faster", offer a 1–2 question test-out and skip the block if they pass.
- Before each message, ask yourself whether it moves understanding forward or is just ceremony. Cut the ceremony.

## Flow

### 1. Setup (one turn)

Ask up to 3 questions at once, using a multiple-choice question tool if one is available:

1. **Current level**, as 4–5 levels written for this specific topic, not a generic "beginner/intermediate/advanced". Each level should describe what the person can already do with the topic.
   *Example (Bayesian inference):* "Haven't met it" / "Know Bayes' theorem as a formula" / "Can update a probability by hand" / "Understand priors, likelihoods and posteriors as distributions" / "Comfortable with conjugate priors".
2. **Scope and context:** which parts they care about, and why they're learning it (for example, a work context or reading papers). This decides which blocks are in or out.
3. **Target depth:**
   - *Intuition:* can explain it plainly and recognize it.
   - *Working:* can reason through conceptual problems and new cases with it.
   - *Deep:* can derive it, handle edge cases, and compare it with alternatives.

If a progress record exists (see step 7), skip setup and resume from it.

### 2. Map and level check (one message)

**Build the map:** break the topic into first-principles building blocks, meaning units that can't usefully be broken down further at the target depth. For each block, note its one-line essence and which blocks it depends on. Order the blocks so every prerequisite comes first. Group them into milestones of 2–4 blocks, where each milestone is a coherent capability ("you can now reason about X").

Also list **outside prerequisites**: concepts from other topics that a block depends on (for example, conditional probability for Bayesian inference). Tag each one on the block it feeds. Don't break them down yet.

Show the map as a compact numbered list grouped by milestone. Don't explain the blocks yet.

**Level check:** in the same message, ask 3–5 diagnostic questions aimed at the blocks around the level the user picked. Use reasoning questions ("what happens if…", "why…"), not definitions. Include 1 question per outside prerequisite, inside the same round. Skip the topic questions if the user picked the lowest level, but still check the outside prerequisites.

Mark each block as known, shaky or unknown. Tell the user in one line which blocks you're skipping, then start at the first shaky or unknown block. Use one round of diagnostic questions only.

For fast-moving, niche or factual-current topics, verify facts with search before teaching. Don't teach from memory.

### 3. Teach each block

Use this order, and leave out any part the block doesn't need:

1. **Why it exists:** the problem it solves or the question it answers, in 1–2 sentences. This is the first-principles anchor.
2. **Core idea** in plain language.
3. **An example and/or analogy**, if it passes the test below.
4. **The precise version** (formal definition, notation, conditions), only if the target depth needs it.
5. **A check question:** 1 question that needs reasoning, such as predict, explain why, pick the case that fits, or spot the error.

**When to use an example:** the idea is abstract, procedural, easily confused with something nearby, or only makes sense seen in action. Skip it when the idea is clear from the statement alone. A concrete case with real numbers or names beats a vague one.

**When to use an analogy:** something familiar shares the concept's *structure*, not just its surface. Always say in one line where the analogy breaks. Never force one.

**Diagrams:** if the concept has spatial, flow or structural shape, draw a small inline diagram when the session can. Otherwise skip it.

### 4. Wrong answers

1. Work out the specific misconception: what mental model would produce that answer?
2. Name it, and correct it by contrasting it with the right model. Don't re-teach the whole block.
3. Re-check with a *new* question, not the same one.
4. If the error shows a prerequisite gap, go back to that block, then return. If the gap is a concept outside this topic, branch into it (step 4a).

### 4a. Branch into an outside prerequisite

A branch happens when a block depends on a concept the user doesn't have, found in the level check, through a wrong answer, or because the user asks. A branch is the same flow as this skill, scaled down to only what the block needs.

1. **Announce it in one line:** "Quick detour: <concept>, because <block> relies on it. Back in ~N steps."
2. **No setup.** Use the main topic's target depth, and limit the scope to what the parent block actually uses.
3. **Mini map:** 1–3 blocks, shown in one line. Skip any the user knows. If one question settles whether they know the concept, ask it first.
4. **Teach** each block as in step 3. Use the 1-question check, and handle wrong answers as in step 4.
5. **Exit check:** 1–2 questions that use the prerequisite *the way the parent block needs it*. Pass, then return.
6. **Return in one line**, linking back: "Now, with <concept>, <parent block> works like this: …". Then resume the parent block where it stopped.

**Limits (TAT):**
- If a branch needs its own branch, allow it once, to a depth of 2 at most. Beyond that, or if a branch needs more than 3 blocks, tell the user it's a topic in its own right, teach only the one fact the parent block needs, and add the concept to "next concepts".
- No milestone test inside a branch. Its blocks join the spaced-recall pool for later milestones.
- Teach only the slice of the concept that's needed, never the full concept.

### 5. Milestone tests

Use 3–6 questions across these levels. Recall can be at most 1 question.

- **Understand:** explain it in your own words, or say why it works.
- **Apply:** use the concept on a case that wasn't taught.
- **Analyze:** compare it with a nearby concept, find the flaw in an argument, or tell apart two similar cases.
- **Evaluate:** judge whether a claim or a use of the concept is right, and why.

From the second milestone on, include 1–2 questions from earlier milestones (spaced recall).

Wrong options in multiple-choice questions should be the real common misconceptions. Use a quiz widget for multiple-choice questions when one is available. Answer open-ended questions in chat.

**Pass:** at least 80% and no misconception left on a core block. **Fail:** fix only the failed blocks (step 4), then retest only those. Report the result in 1–2 lines (score and weak spots) and move on.

### 6. Finish

1. Give a final test of 5–8 questions across all milestones at the target depth, mostly apply, analyze and evaluate questions.
2. Give a **cheat sheet** of 5–10 lines: each block's essence, in dependency order.
3. List remaining weak spots, and 1–3 natural next concepts. Then stop.

### 7. Progress record

Update the record after each milestone and at the end of each session. If file tools are available, save it to `learning/<topic-slug>.md`. Otherwise, output it at the end of the session and tell the user to paste it to resume. On resume, read it, run a 2-question recall check on the last milestone, and continue.

```markdown
# Learning: <topic>
Target depth: <intuition|working|deep> | Scope: <one line> | Context: <one line>

## Map
- M1 <name>: [x] block A, [x] block B
- M2 <name>: [~] block C (shaky: <misconception>), [ ] block D

## Weak spots
- <block>: <specific misconception>

## Open branches
- <prereq concept> (for <parent block>): at <branch block>, then return to <parent block>

## Next
Resume at <block>. Milestone tests passed: M1 (5/6)
```