---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/daily-systems
  - area/habits
  - status/evergreen
related:
  - "[[MOCs/Daily Systems MOC]]"
  - "[[Templates/Daily Note]]"
  - "[[05 - Daily Systems/Daily Systems]]"
  - "[[05 - Daily Systems/Weekly & Monthly Reviews]]"
  - "[[05 - Daily Systems/Daily Notes/Daily Notes]]"
---

# Habit Tracking

> [!abstract] Why Track Habits in Obsidian
> A habit tracker in your daily note puts measurement where your attention already is. Unlike a separate app, it integrates directly with your reflection, task management, and weekly review — turning habit data into actionable insight.

Habit tracking in this vault is designed to be **frictionless, queryable, and reflection-oriented**. The goal is not to gamify your life but to create an honest record that helps you understand your own behavior patterns.

---

## The Core Principle

> [!quote] James Clear, Atomic Habits
> "You do not rise to the level of your goals. You fall to the level of your systems."

Habit tracking is a system for making the invisible visible. When you track, you create a feedback loop between intention and behavior. The data becomes a mirror — not a judge.

Three rules for effective habit tracking:

1. **Track fewer habits** — 3–5 is sustainable; 15 is a burden
2. **Track simply** — checkbox (done / not done) beats complex scoring for consistency
3. **Review regularly** — data without review is just noise

---

## Setting Up Habit Tracking in Daily Notes

Habit tracking lives in the `## Habits` section of the daily note. The setup uses two approaches: **checkbox habits** for binary tracking and **scored habits** for nuanced measurement.

### Checkbox Habits (Binary)

Best for: sleep, exercise, specific actions

```markdown
## Habits
- [x] 💧 8 glasses of water
- [x] 🏃 Exercise (any kind)
- [ ] 📵 No phone before 8am
- [x] 📚 Read 20+ min
- [ ] 🧘 Meditation
- [x] 🌙 In bed before 11pm
```

### Scored Habits (1–5)

Best for: sleep quality, energy level, mood, focus quality

```markdown
## Habits
- [x] 💧 Water: `8` glasses
- [x] 😴 Sleep quality: `4`/5
- [x] ⚡ Energy: `3`/5
- [ ] 🎯 Deep focus blocks: `1`/3
```

### Frontmatter Properties for Dataview

For Dataview queries to work across daily notes, key habit scores should also be in frontmatter:

```yaml
---
type: daily
created: "2026-04-16"
mood: 4
energy: 3
sleep_quality: 4
exercise: true
meditation: false
---
```

> [!tip] Choose Your Tracking Style
> Checkbox-only is more sustainable for beginners. Add frontmatter scoring only for habits you want to query in Dataview. Don't track what you won't review.

---

## Example Habit System

Here is a well-designed starting set of habits, organized by category:

### Foundation Habits (track daily)

| Habit | Tracking | Why |
|-------|----------|-----|
| Sleep (7+ hours) | Checkbox + frontmatter `sleep: true` | Foundation of everything else |
| Exercise | Checkbox | Mood, focus, energy |
| Water (6–8 glasses) | Checkbox or count | Often overlooked |
| No screens first 30 min | Checkbox | Sets tone for the day |

### Cognitive Habits (track daily)

| Habit | Tracking | Why |
|-------|----------|-----|
| Read 20+ min | Checkbox | Compound knowledge building |
| Daily note opened | Checkbox | The system's keystone habit |
| Inbox processed | Checkbox | Prevents capture rot |

### Optional / Seasonal (track only when actively building)

| Habit | Tracking | Why |
|-------|----------|-----|
| Meditation | Checkbox | Track for 30-day builds |
| Journaling | Checkbox | Encourage consistency |
| Language practice | Checkbox / minutes | Spaced repetition benefit |
| Cold shower | Checkbox | Discipline building |

> [!warning] Don't Track Too Many Habits at Once
> Tracking 12 habits daily creates anxiety and decision fatigue. Run a maximum of 3–5 habits at any one time. Once a habit is automatic and needs no tracking, remove it and replace it with the next one you're building.

---

## Dataview Queries for Habit Dashboard

### Habit Completion Rate (Last 14 Days)

```dataview
TABLE WITHOUT ID
  file.link as "Date",
  exercise as "🏃",
  meditation as "🧘",
  sleep as "😴",
  mood as "Mood",
  energy as "Energy"
FROM "05 - Daily Systems/Daily Notes"
WHERE type = "daily"
SORT file.ctime DESC
LIMIT 14
```

### Average Mood and Energy This Month

```dataview
TABLE WITHOUT ID
  round(average(rows.mood), 1) as "Avg Mood",
  round(average(rows.energy), 1) as "Avg Energy"
FROM "05 - Daily Systems/Daily Notes"
WHERE type = "daily"
  AND date(file.ctime).month = date(today).month
GROUP BY "This Month"
```

### Exercise Streak (Consecutive Days)

```dataview
TABLE file.ctime as "Date", exercise
FROM "05 - Daily Systems/Daily Notes"
WHERE type = "daily" AND exercise = true
SORT file.ctime DESC
LIMIT 30
```

### Habit Completion Count This Week

```dataview
TABLE WITHOUT ID
  length(filter(rows.exercise, (x) => x = true)) as "Exercise",
  length(filter(rows.meditation, (x) => x = true)) as "Meditation",
  length(filter(rows.sleep, (x) => x = true)) as "Sleep 7h+"
FROM "05 - Daily Systems/Daily Notes"
WHERE type = "daily"
  AND date(file.ctime) >= date(today) - dur(7 days)
GROUP BY "This Week"
```

### Mood vs. Exercise Correlation View

```dataview
TABLE file.ctime as "Date", mood, energy, exercise
FROM "05 - Daily Systems/Daily Notes"
WHERE type = "daily" AND mood != null AND energy != null
SORT file.ctime DESC
LIMIT 30
```

> [!info] Dataview Plugin Required
> These queries require the Dataview community plugin. Install from Settings → Community Plugins → Browse → search "Dataview". Enable JavaScript queries in Dataview settings.

---

## Weekly Habit Review

Every weekly review should include a 5-minute habit review. Use these questions:

**Streak Review:**
- Which habits did I complete 5+/7 days this week?
- Which habits did I complete fewer than 3/7 days? Why?
- Is there a pattern to the days I miss? (weekends, high-stress days?)

**Pattern Questions:**
- Did higher exercise correlate with higher energy this week?
- Did my mood track with sleep quality?
- Which habit had the most noticeable impact on my day when I did (or didn't) do it?

**Adjustment Questions:**
- Is any habit too ambitious right now? (reduce the target)
- Is any habit so automatic I don't need to track it anymore?
- What is the one habit that, if done consistently, would have the biggest impact on my goals?

> [!example] Weekly Habit Summary Format
> Add this to your weekly review note:
> ```
> ## Habit Summary
> - Exercise: 5/7 ✅
> - Daily note: 7/7 ✅
> - Meditation: 2/7 ⚠️ (skipped Mon/Wed/Thu/Fri/Sat)
> - Sleep 7h+: 4/7 — pattern: stayed up late Fri/Sat
> 
> One insight: Energy was noticeably higher on exercise days.
> Next week focus: Protect sleep on Friday nights.
> ```

---

## The Habit-to-Identity Shift

> [!tip] Tracking Is Not the Goal
> The purpose of tracking is not to maintain streaks — it's to understand and reshape your identity. "I track exercise" eventually becomes "I am someone who exercises." The data just helps you see where you already are on that journey.

When a habit becomes truly automatic:
1. You notice you did it without thinking
2. Missing it feels genuinely strange
3. You don't need external motivation to do it

That's the signal to stop tracking it and redirect your tracking attention to the next habit you're building.

---

## Habit Tracking in the Broader System

Habit data feeds upward into the review cascade:

- **Daily notes** → raw checkbox/score data
- **Weekly review** → completion rates, pattern identification, adjustments
- **Monthly review** → trend analysis, habit graduation (automatic), new habit selection
- **Quarterly review** → alignment with long-term goals and areas

This makes habit tracking not just a personal discipline tool but a core input into how you evolve your systems over time.

---

## Related Notes

- `[[MOCs/Daily Systems MOC]]` — All daily systems
- `[[Templates/Daily Note]]` — Daily note with habit section
- `[[05 - Daily Systems/Daily Systems]]` — Master daily systems overview
- `[[05 - Daily Systems/Weekly & Monthly Reviews]]` — Review cadence and habit review
- `[[05 - Daily Systems/Daily Notes/Daily Notes]]` — Daily note guide
