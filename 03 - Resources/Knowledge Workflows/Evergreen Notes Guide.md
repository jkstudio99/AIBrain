---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/knowledge-management
  - topic/evergreen-notes
  - status/evergreen
related:
  - "[[MOCs/Knowledge MOC]]"
  - "[[Templates/Evergreen Note]]"
  - "[[03 - Resources/Knowledge Workflows/Literature Notes Guide]]"
  - "[[03 - Resources/Knowledge Workflows/Capture Process Connect]]"
  - "[[07 - Prompt Library/Note Processing/Note Processing Prompts]]"
aliases:
  - How to Write Evergreen Notes
  - Evergreen Note Guide
---

# Evergreen Notes Guide

An evergreen note is the atom of your knowledge system — a single, complete, reusable idea expressed in your own words and connected to everything it touches. Unlike project notes that become stale or literature notes that belong to a source, evergreen notes grow *more* useful over time as you build more connections to them.

> [!abstract] Why "Evergreen"?
> The metaphor is intentional. Evergreen trees retain their value through all seasons. An evergreen note retains its value across all projects, questions, and years — because it captures an idea in a timeless, reusable form rather than tied to a specific context.

---

## What Makes a Note "Evergreen"?

Not every note deserves to be evergreen. The designation has specific meaning. A note is evergreen when it meets all four criteria:

### The 4 Principles of Evergreen Notes

#### 1. Atomic — One Idea Per Note

An evergreen note captures exactly one idea, complete in itself. If you find yourself writing "and also..." or "related to this is...", that's a signal you're writing two notes.

**Atomic:** "Feedback loops accelerate learning by reducing the gap between action and consequence."
**Not atomic:** "Feedback loops and deliberate practice together explain skill acquisition, and this relates to motivation theory..."

The atomic constraint feels limiting but is actually liberating: it forces you to identify the *single* insight worth preserving.

#### 2. Concept-Oriented — Ideas, Not Topics

The title and content should be about a *concept* or *claim*, not a broad topic. Topics are categories; concepts are ideas.

**Concept-oriented:** "Constraints drive creativity by forcing novel solutions within defined boundaries"
**Topic-oriented:** "Creativity" or "Notes on Creativity"

A topic note becomes a dumping ground. A concept note has a clear thesis that can be linked to, agreed with, disagreed with, or extended.

#### 3. Own Words — No Paraphrasing, No Copying

Every sentence in an evergreen note should be something only you could have written — because it reflects your understanding, your angle, your connections. If you can Google the text and find it verbatim, it doesn't belong in an evergreen note.

Writing in your own words serves two purposes:
1. It tests whether you genuinely understand the idea
2. It makes the note useful when you return to it — it reads like your thinking, not a textbook

> [!warning] The Paraphrase Test
> Reading your evergreen note back, ask: does this sound like me thinking, or like me transcribing? If the latter, rewrite it.

#### 4. Densely Linked — Connected to Everything It Touches

An isolated evergreen note is a missed opportunity. Every claim in an evergreen note should link outward to evidence (literature notes), supporting concepts (other evergreen notes), applications (project notes), and contradictions (notes that challenge it).

The density of links is a proxy for the depth of understanding. A well-understood idea has many relationships.

---

## How to Write Good Evergreen Note Titles

The title of an evergreen note is not a label — it is a complete declarative statement of the idea. This is one of the most important and most overlooked practices.

### The Declarative Title Principle

The title should be a sentence (or near-sentence) that can stand alone as a claim. When someone reads only the title, they should understand the idea.

> [!example] Good Titles vs. Bad Titles

| Bad Title (Topic Label) | Good Title (Declarative Statement) |
|-------------------------|-------------------------------------|
| Spaced Repetition | Spaced repetition produces durable memory by exploiting the spacing effect |
| Deep Work | Deep work requires eliminating micro-interruptions, not just major ones |
| Motivation | Intrinsic motivation is undermined when external rewards are made contingent on performance |
| Sleep | Sleep consolidates memories by replaying neural activation patterns |
| Creativity | Creative breakthroughs often follow periods of incubation rather than direct effort |
| Note-taking | The act of writing forces comprehension in a way that highlighting does not |

**Why this matters:** When you link `[[Spaced repetition produces durable memory by exploiting the spacing effect]]` in another note, the link itself communicates meaning. The reader (future you) understands the relationship without clicking through.

### Title Formats That Work

- **Causal claims:** "X causes Y because Z"
- **Contrasts:** "X is more effective than Y when [condition]"
- **Mechanisms:** "X works by [mechanism]"
- **Conditions:** "X only applies when Y is true"
- **Definitions:** "X is Y in the context of Z" (use sparingly)

---

## Status Progression: Seedling → Growing → Evergreen

Every note starts as a seedling and evolves. Don't try to write a perfect evergreen note on the first attempt — let it grow.

### Seedling (`#status/seedling`)

A seedling is a note with a good title and a rough first draft. It captures the core idea but may be missing links, may have incomplete reasoning, or may be a direct extract from a literature note that hasn't fully been transformed into your own voice.

**Characteristics:**
- Title may still be a topic label (needs refinement)
- Content may contain some paraphrasing from sources
- Has 0-2 outgoing links
- Has not yet been reviewed after initial creation

### Growing (`#status/growing`)

A growing note has been reviewed and revised at least once. The idea has been tested against your experience and other notes in the vault.

**Characteristics:**
- Title is a clear declarative statement
- Content is fully in your own words
- Has 3-5 outgoing wikilinks to related notes
- Has been linked to from at least one other note (has inbound links)
- May have been updated to incorporate new understanding

**Promotion trigger:** When you find yourself linking to a seedling note from 2+ other notes, it's ready to review and promote to growing.

### Evergreen (`#status/evergreen`)

A fully mature evergreen note. It has proven its usefulness by appearing in many contexts and has been refined through multiple revisions.

**Characteristics:**
- Title is precise and expresses exactly one complete idea
- Content is polished, compressed, and entirely in your own voice
- Has 5+ outgoing wikilinks
- Has multiple inbound links (other notes link to it)
- Has survived at least one "stress test" — you've tried to disprove or complicate it
- May have a `related` section and a list of open questions

**Promotion trigger:** When a growing note has been revised at least twice and has proven useful across multiple contexts.

---

## How to Connect Evergreen Notes to Build a Knowledge Graph

Connection is not just linking — it is mapping the *type* of relationship between ideas. Rich connections make your knowledge graph a tool for reasoning, not just retrieval.

### Types of Connections

| Relationship | Wikilink Annotation | Example |
|---|---|---|
| Supports/Evidence | "Evidence for this: [[Note]]" | Literature note as evidence |
| Contradicts | "This is challenged by [[Note]]" | Competing claim |
| Specializes | "A specific case of [[Note]]" | Application of general principle |
| Generalizes | "A more general version: [[Note]]" | Abstraction of a specific idea |
| Requires | "This presupposes [[Note]]" | Prerequisite concept |
| Enables | "This unlocks [[Note]]" | Downstream application |
| Analogous | "Similar structure to [[Note]]" | Structural parallel across domains |

### Building Clusters

Clusters emerge naturally when many evergreen notes share themes. Signs of a healthy cluster:
- 5+ notes on a topic all link to each other
- Certain notes act as "hubs" with many inbound links
- The cluster has a natural entry point (a note that explains the theme and links to the others)

When a cluster reaches this density, create a dedicated MOC for it and add it to `[[MOCs/Knowledge MOC]]`.

### The Review Loop

Every 1-2 months, open your oldest growing notes and ask:
1. Has my understanding of this idea changed?
2. Are there newer notes that should link to this?
3. Is this still atomic, or has it grown into multiple ideas?
4. Can I strengthen the title to be more precise?

---

## Knowledge Maturity Lifecycle

```mermaid
stateDiagram-v2
    [*] --> Fleeting : Idea captured\nin Inbox

    Fleeting --> Discard : Not worth\ndeveloping
    Fleeting --> Literature : From a\nspecific source
    Fleeting --> Seedling : Original\ninsight

    Literature --> Seedling : Extract\nkey idea

    Seedling --> Growing : Reviewed,\nlinks added,\ntitle refined
    Seedling --> Discard : Idea not\ngeneralizable

    Growing --> Evergreen : Battle-tested,\ndensely linked,\nfully in own words
    Growing --> Seedling : Needs more\nwork on revisit

    Evergreen --> Evergreen : Refined\non revisit
    Evergreen --> Split : Idea was\nnot atomic

    Split --> Seedling : Each part\nbecomes new note

    Discard --> [*]
    Evergreen --> [*] : Deprecated\n(rare)

    note right of Evergreen : Status: evergreen\n5+ links\nMultiple revisions\nOwn voice throughout
    note right of Growing : Status: growing\n3-5 links\nAt least 1 revision\nMostly own words
    note right of Seedling : Status: seedling\n0-2 links\nFirst draft\nMay need rewrite
```

---

## Common Mistakes and How to Avoid Them

> [!bug] Mistake 1: Writing Topic Summaries Instead of Idea Notes
> **Problem:** "Everything I know about motivation" crammed into one note.
> **Fix:** Identify the single most important insight. Write that. Create separate notes for other insights.

> [!bug] Mistake 2: Linking Without Context
> **Problem:** `See also: [[Related Note]]` at the end of a note, without explanation.
> **Fix:** Every link should be embedded in a sentence that explains the relationship: "This mechanism is what makes [[Spaced repetition produces durable memory]] effective in practice."

> [!bug] Mistake 3: Never Promoting Seedlings
> **Problem:** Dozens of seedling notes that have never been reviewed or connected.
> **Fix:** During weekly review, pick 3 seedlings and either promote them to growing or discard them. The inbox of your knowledge system should be small.

> [!bug] Mistake 4: Mistaking Detail for Depth
> **Problem:** Long evergreen notes with many paragraphs and subclaims.
> **Fix:** If your note needs multiple H2 headings, it contains multiple ideas. Split it. A great evergreen note is often just 3-5 well-crafted sentences.

> [!bug] Mistake 5: Orphaned Notes
> **Problem:** Evergreen notes with no inbound links — nothing in the vault references them.
> **Fix:** Run the orphan notes search periodically. An unreferenced evergreen note is either misfiled, poorly titled, or needs to be linked from relevant contexts.

---

## Evergreen Note Checklist

Before promoting a note from seedling to growing:

- [ ] Title is a complete declarative statement expressing exactly one idea
- [ ] Content is entirely in your own words
- [ ] Note contains exactly one idea (if not, split it)
- [ ] At least 3 outgoing wikilinks with relationship context
- [ ] Has been reviewed at least once after initial writing
- [ ] Tagged with `#status/growing` and relevant topic tags
- [ ] Added to relevant MOC or linked from a cluster hub

Before promoting from growing to evergreen:

- [ ] Has been revised at least twice
- [ ] Has at least 5 outgoing wikilinks
- [ ] Is referenced (has inbound links) from at least 3 other notes
- [ ] Has survived a "stress test" — you've considered counterarguments
- [ ] Tag updated to `#status/evergreen`

---

## Claude Assistance for Evergreen Notes

| Task | Prompt / Command |
|------|-----------------|
| Convert literature note | `/create-evergreen` skill |
| Refine a title | "Make this title more precise and declarative: [title]" |
| Find connections | `/find-connections` skill |
| Stress test an idea | `/challenge` skill |
| Split a compound note | "This note contains multiple ideas — help me identify them and split into separate atomic notes" |
| Rewrite in own words | "Rewrite this in a more personal voice, as if I'm explaining it to a knowledgeable friend" |

See `[[07 - Prompt Library/Note Processing/Note Processing Prompts]]` for full templates.

---

## Related Guides

- `[[03 - Resources/Knowledge Workflows/Literature Notes Guide]]` — The precursor to evergreen notes
- `[[03 - Resources/Knowledge Workflows/Capture Process Connect]]` — The full workflow context
- `[[Templates/Evergreen Note]]` — The template to use
- `[[MOCs/Knowledge MOC]]` — Where evergreen notes live in the graph
