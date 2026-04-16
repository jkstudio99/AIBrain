---
type: prompt
created: "2026-04-16"
tags:
  - type/prompt
  - prompt/ideation
  - status/evergreen
related:
  - "[[07 - Prompt Library/Idea Generation/Idea Generation.md]]"
  - "[[MOCs/Prompt Library MOC]]"
  - "[[07 - Prompt Library/Thinking Tools/Thinking Tools.md]]"
aliases:
  - What If Prompt
  - Hypothetical Exploration
---

# What If

A prompt for exploring hypothetical scenarios and counterfactuals. Use this when you want to challenge an assumption, plan for a future state, stress-test a decision, or unlock creative possibilities by removing a constraint you've taken for granted.

> [!info] Purpose
> "What if" thinking is one of the most powerful cognitive tools available — it's how scientists design experiments, how strategists plan for uncertainty, and how writers generate plot. This prompt makes it structured and generative rather than vague and anxious.

---

## When to Use This Prompt

- You're about to make a significant decision and want to examine edge cases
- A project keeps hitting the same wall — you suspect a hidden assumption is the cause
- You're doing scenario planning or future-mapping for a project
- You want to generate creative alternatives to a path you've already started down
- A note or belief feels too settled and you want to pressure-test it speculatively
- You're prototyping ideas and want to explore the full consequence space

---

## Full Prompt Template

```text
I want to explore a "what if" scenario to expand my thinking. Here is the situation:

SITUATION: [describe the current state, decision, or assumption]

WHAT IF: [state the hypothetical change — invert an assumption, change a variable, 
           remove a constraint, project a trend forward, or ask "what if the opposite were true?"]

Please explore this through the following structure:

1. SCENARIO SETUP
   - What exactly changes in this hypothetical world compared to the real one?
   - What are the first-order effects — what happens immediately?
   - What are the second-order effects — what happens as a result of those?

2. THREE PLAUSIBLE OUTCOMES
   For each outcome, describe:
   - What it looks like in practice
   - Who benefits and who is disadvantaged
   - What new problems it creates
   - What it makes possible that wasn't before

3. NEW RISKS AND OPPORTUNITIES
   - What risks emerge in this hypothetical that don't exist in the current situation?
   - What opportunities become available that are currently blocked?
   - What would you need to change, build, or abandon to navigate this scenario?

4. WHAT THIS REVEALS ABOUT THE ORIGINAL SITUATION
   - What does this hypothetical expose about assumptions in the current state?
   - What is the current situation optimizing for — and is that still the right thing?
   - What would a person who believed this "what if" were true do differently today?

5. EXPERIMENTS WORTH RUNNING
   - Name one small, low-risk experiment you could run in the real world to test 
     whether elements of this scenario are already becoming true.
   - What signal would confirm or deny this hypothetical is relevant?
   - If this scenario had a 20% chance of being true, what would you do differently?
```

---

## Example Usage

> **Situation:** *I structure my knowledge work around long focus blocks (90+ minutes).*
>
> **What If:** *What if deep focus is not actually necessary for high-quality knowledge work, and short, frequent bursts of engaged attention are just as effective?*
>
> **Expected outputs include:**
> - Scenario Setup: The constraint of "I need long blocks" disappears; calendar becomes more fluid
> - Outcome 1: Interleaved work style — high-value work becomes accessible in 20-min windows
> - Outcome 2: Cognitive switching cost dominates — quality degrades despite more flexibility
> - Outcome 3: A hybrid model — certain tasks (writing) need depth, others (connections) don't
> - Reveals: Current system may be designed around fear of interruption, not actual output quality
> - Experiment: Track actual output quality and quantity for one week of 25-min blocks vs. 90-min blocks

---

## Variations and Prompt Modifiers

| Goal | Modification to the prompt |
|------|---------------------------|
| Strategic planning | Add "Think 5 years ahead" to Scenario Setup |
| Inversion exercise | "What if the exact opposite of [belief] were true?" |
| Pre-mortem | "What if this project failed completely — what caused it?" |
| Opportunity scan | "What if this constraint didn't exist?" |
| Risk analysis | "What if the worst-case assumption became reality?" |
| Creative writing | "What if this character made the opposite choice?" |
| Business model | "What if our main revenue assumption were wrong?" |

---

## Chaining This Prompt

"What If" works best as part of a thinking sequence:

```
Explore Concept → build foundation
What If         → introduce productive destabilization  
Challenge       → stress-test the scenario itself
Reframe         → see the scenario from other stakeholder angles
Synthesize      → integrate into actionable insight
```

> [!example] Research Chain Example
> 1. `/explore-concept` "network effects" — map the terrain
> 2. `/what-if` "What if network effects reversed after a platform reaches 1B users?" — speculative exploration
> 3. `/challenge` the scenario — is this just Metcalfe's Law inverted? What's the evidence?
> 4. `/reframe` from regulator, user, and competitor perspectives
> 5. `/synthesize` → evergreen note: *"Network Diseconomies: When Scale Becomes a Liability"*

---

> [!warning] Common Mistake
> Don't confuse "What If" with wishful thinking. The prompt is designed to explore a space, including uncomfortable implications. Resist the urge to run it only on optimistic scenarios — the most valuable hypotheticals are the ones where your assumptions fail.

---

## Output Processing

After running this prompt:

1. Save the output as a fleeting note tagged `#type/fleeting` and `#prompt/ideation`
2. If an outcome or insight resonates, run `/create-evergreen` on that section
3. If the revealed assumption is important, add it as a **claim** in the relevant project or research note
4. Log the experiment suggestion in your task system with `status:: todo`

---

## Related Prompts

- [[07 - Prompt Library/Idea Generation/Idea Generation.md]] — Overview of all ideation prompts
- [[07 - Prompt Library/Idea Generation/Explore Concept.md]] — Build foundational understanding first
- [[07 - Prompt Library/Idea Generation/Brainstorm.md]] — Generate options; use before narrowing
- [[07 - Prompt Library/Thinking Tools/Thinking Tools.md]] — Deepen and test ideas generated here
- [[07 - Prompt Library/Reflection/Reflection & Synthesis.md]] — Integrate insights into your review cycle
