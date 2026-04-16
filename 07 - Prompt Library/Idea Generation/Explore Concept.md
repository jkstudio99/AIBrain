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
  - "[[07 - Prompt Library/Note Processing/Create Evergreen.md]]"
aliases:
  - Explore Concept Prompt
---

# Explore Concept

A prompt for deep-diving into a single concept from multiple angles. Use this when a term or idea keeps appearing in your reading and you want to map it thoroughly before committing it to your knowledge base.

> [!info] Purpose
> This prompt turns a single word or phrase into a rich, multi-dimensional understanding. It is the difference between knowing a definition and understanding a concept well enough to teach it, apply it, and connect it to your existing knowledge.

---

## When to Use This Prompt

- You encountered a concept in reading and want to go deeper before creating a note
- You're starting research on an unfamiliar domain and need orientation
- You have a literature note but it feels thin — you want to understand the full context
- You're preparing to write an evergreen note and need material from multiple angles
- A concept keeps appearing across different sources and you want to consolidate your understanding

---

## Full Prompt Template

```text
I want to deeply explore the following concept:

CONCEPT: [insert concept here]

Please structure your exploration across these six dimensions:

1. HISTORICAL ORIGINS
   - When and where did this concept originate?
   - Who first articulated it, and in what context?
   - How has its meaning evolved over time?
   - What was it originally a response to or solution for?

2. TECHNICAL / MECHANICAL DEFINITION
   - What is the most precise definition in its home discipline?
   - What are the core components or moving parts?
   - What are the boundary conditions — when does this concept apply vs. not apply?
   - What does it get confused with, and why?

3. PHILOSOPHICAL / CONCEPTUAL DIMENSIONS
   - What assumptions does this concept depend on?
   - What questions does it leave open or refuse to answer?
   - What worldview or framework does it belong to?
   - What would be lost if this concept didn't exist?

4. PRACTICAL APPLICATIONS
   - Where is this concept applied in the real world?
   - What does using this concept well look like in practice?
   - What are the most common misapplications?
   - Who benefits most from understanding this concept?

5. ADJACENT CONCEPTS
   - What concepts does this one build on?
   - What concepts build on this one?
   - What is the strongest counterargument or rival concept?
   - Name 3–5 related concepts I should study next.

6. SYNTHESIS & NOTE SUGGESTION
   - In one sentence, what is the core insight this concept encapsulates?
   - Suggest one evergreen note title that captures the essence of what I should remember.
   - What is the most surprising or non-obvious thing about this concept?
```

---

## Example Usage

> **Input:** `CONCEPT: Cognitive Load`
>
> **Expected outputs include:**
> - Historical: John Sweller's 1988 cognitive load theory, rooted in working memory research
> - Technical: Intrinsic, extraneous, and germane load types; working memory as 4 ± 1 items
> - Philosophical: Assumes a bottleneck model of cognition; contested by embodied cognition theorists
> - Practical: Instructional design, UI design, writing clarity, code readability
> - Adjacent: Working memory, chunking, flow state, desirable difficulty, split-attention effect
> - Evergreen note: *"Cognitive Load as a Design Constraint"*

---

## Output Processing

After running this prompt, process the output into your vault:

1. **Capture the six sections** as a literature note in `06 - Knowledge/`
2. **Run `/find-connections`** to identify existing notes that link to this concept
3. **Pick the core insight** from section 6 and use `/create-evergreen` to create the evergreen note
4. **Add wikilinks** to every adjacent concept mentioned in section 5

> [!tip] Pair with Trace
> If section 2 (Technical Definition) produces something complex, run [[.claude/commands/trace.md|/trace]] on just that section to map the mechanism in detail.

---

## Variations

| Goal | Modification |
|------|-------------|
| Quick orientation only | Ask for sections 2 and 5 only |
| Writing an explainer | Expand section 4 (Practical Applications) |
| Philosophical essay prep | Expand sections 3 and 5 |
| Building a MOC | Focus on section 5 (Adjacent Concepts) to map the neighborhood |
| Historical research | Expand section 1 and add "key figures and texts" |

---

## Related Prompts

- [[07 - Prompt Library/Idea Generation/Idea Generation.md]] — Overview of all ideation prompts
- [[07 - Prompt Library/Idea Generation/Brainstorm.md]] — For generating options, not depth
- [[07 - Prompt Library/Idea Generation/What If.md]] — For hypotheticals after you understand the concept
- [[07 - Prompt Library/Note Processing/Create Evergreen.md]] — Next step after exploring
- [[07 - Prompt Library/Thinking Tools/Thinking Tools.md]] — For deeper analysis once you have a note
