---
type: prompt
created: "2026-04-16"
tags:
  - type/prompt
  - prompt/reflection
  - status/evergreen
related:
  - "[[07 - Prompt Library/Reflection/Reflection & Synthesis.md]]"
  - "[[MOCs/Daily Systems MOC]]"
  - "[[MOCs/Prompt Library MOC]]"
aliases:
  - Weekly Synthesis Prompt
  - Weekly Review Prompt
---

# Weekly Synthesis

A prompt for synthesizing a week's worth of notes, experiences, and work into patterns and actionable insight. Use this to end each week with clarity rather than a vague sense of what happened.

> [!tip] Why This Matters
> A weekly synthesis is not a summary — it's a pattern-extraction process. You're looking for what the week is *revealing*, not just cataloguing what occurred. Done consistently, this is one of the highest-leverage habits in a knowledge practice.

---

## When to Use This Prompt

- Every Sunday evening or Monday morning (the primary cadence)
- After an intense sprint or project phase when you want to consolidate learning
- Before a monthly review to prepare consolidated input
- When you feel scattered or unfocused and want a reset
- After returning from a conference, course, or intensive learning period

---

## Full Prompt Template

```text
I want to synthesize my week. Here is my input:

DAILY NOTES / KEY EVENTS:
[Paste or summarize your daily notes, key events, completed tasks, 
and major moments from the week. Can be bullet points or prose.]

NOTES CREATED THIS WEEK:
[List the titles or brief summaries of notes you created or significantly 
updated this week — fleeting notes, literature notes, project updates.]

OPEN THREADS:
[Any questions, problems, or ideas you started but didn't resolve this week.]

Please structure your synthesis as follows:

1. THEMES OF THE WEEK
   - What are the 2–4 major themes or through-lines of this week?
   - Is there a sentence that captures what this week was "about"?
   - Were there unexpected connections between different areas of work/life?

2. WHAT MOVED FORWARD
   - What made meaningful progress? (Projects, understanding, relationships)
   - What habits or systems worked well?
   - What created the most value this week?

3. WHAT STALLED OR CREATED FRICTION
   - Where did energy go without producing results?
   - What recurring obstacles or interruptions appeared?
   - What did you avoid, and why?

4. INSIGHTS AND PATTERNS
   - What did you learn or understand this week that you didn't before?
   - Is there a pattern emerging across multiple weeks?
   - What surprised you?
   - What do you want to remember from this week one year from now?

5. OPEN LOOPS
   - What questions are you still sitting with?
   - What decisions are pending?
   - What tasks or ideas need to carry forward?

6. PRIORITIES FOR NEXT WEEK
   - Given everything above, what are the top 3 priorities for next week?
   - What is the ONE thing that, if done, would make next week a success?
   - Is there anything you should stop, reduce, or delegate?
   - What does "good" look like by next Sunday?
```

---

## Example Input and Output

> **Input snippet:**
> *Monday: deep work session on the emergence article, got stuck on the "intentionality" section. Tuesday: read Hofstadter chapter 5 and took 8 highlights. Wednesday: client call ran long, killed afternoon focus. Thursday: breakthrough — realized emergence and intentionality are actually in tension, not aligned. Friday: drafted the first 400 words.*
>
> **Output (section 4 sample):**
> *Key insight: The tension between emergence and intentionality isn't a problem to resolve — it's the productive friction that makes complex systems interesting. This reframes the entire article from "explaining emergence" to "navigating the tension." Client interruptions on Wednesday weren't just noise — they revealed how fragile single-session deep work is without buffer days.*

---

## Preparing Good Input

The quality of the synthesis scales directly with the quality of input. The best input includes:

| Input Type | How to Prepare |
|-----------|---------------|
| Daily notes | Paste titles or key bullets from `05 - Daily Systems/` |
| Created notes | List titles from `06 - Knowledge/` and `00 - Inbox/` |
| Completed tasks | Export or paste done items from your task system |
| Key conversations | 2–3 sentence summaries of important discussions |
| Emotional texture | One sentence on the general mood or energy of the week |

---

## Output Processing

After running this prompt:

1. Create a weekly note in `05 - Daily Systems/Weekly/` titled `Week of YYYY-MM-DD`
2. Paste the full synthesis output into that note
3. Extract any **insights** (section 4) into fleeting notes for later processing
4. Add **open loops** (section 5) to your task system with `status:: todo`
5. Set **next-week priorities** (section 6) as your Monday morning anchors

> [!tip] Compound the Value
> After 4 weekly syntheses, run `/knowledge-audit` to see patterns across the month. The weekly syntheses become the input for your monthly review.

---

## Variations

| Situation | Modification |
|-----------|-------------|
| Project retrospective | Replace "week" with "project" throughout |
| Learning sprint recap | Expand section 4 (Insights) significantly |
| Quarterly review prep | Run on 12–13 weekly syntheses at once |
| Post-conference synthesis | Add a "What to implement" section after section 6 |

---

## Related Prompts

- [[07 - Prompt Library/Reflection/Reflection & Synthesis.md]] — Overview of all reflection prompts
- [[07 - Prompt Library/Reflection/Daily Reflection.md]] — The daily input that feeds this prompt
- [[07 - Prompt Library/Reflection/Knowledge Audit.md]] — Monthly review of the knowledge system itself
- [[07 - Prompt Library/Note Processing/Note Processing Prompts.md]] — Process insights surfaced here
- [[MOCs/Daily Systems MOC]] — The full daily/weekly/monthly system
