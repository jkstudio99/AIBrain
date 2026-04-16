---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/daily-systems
  - area/note-taking
  - status/evergreen
related:
  - "[[MOCs/Daily Systems MOC]]"
  - "[[Templates/Daily Note]]"
  - "[[05 - Daily Systems/Daily Systems]]"
  - "[[05 - Daily Systems/Weekly & Monthly Reviews]]"
  - "[[05 - Daily Systems/Journaling/Journaling with Claude]]"
---

# Daily Notes — Guide

> [!abstract] Purpose
> Daily notes are the **operational core** of this vault. They serve as your daily capture pad, task manager, reflection space, and the connective tissue between all other systems.

A daily note is not a diary. It is a **working document** — something you open first thing in the morning and close last thing at night. Think of it as your command center for the day.

---

## The Three Purposes of Daily Notes

### 1. Capture
Every thought, idea, task, or reference that crosses your mind during the day lands here first. The goal is **zero friction** — write it down, then decide what to do with it later.

- Quick thoughts → captured in `## Inbox` section
- Tasks → captured with `- [ ]` syntax for the Tasks plugin
- Meeting notes → captured inline, later moved to `[[01 - Projects/]]`
- Links and references → captured with the URL, processed during evening review

### 2. Reflect
The daily note provides structured prompts for end-of-day reflection. Regular reflection is what transforms raw experience into learning.

- What went well?
- What was blocked?
- What surprised you?
- What would you do differently?

### 3. Track
By maintaining consistent properties and checkboxes, daily notes become a queryable dataset about how you actually spend your time.

- Habit checkboxes give a streak view over time
- Priority items show what you committed to vs. what you did
- Energy and mood ratings reveal patterns over weeks

---

## Template Walkthrough

The template at `[[Templates/Daily Note]]` is structured as follows. Each section has a specific purpose.

### Frontmatter

```yaml
---
type: daily
created: "{{date}}"
tags:
  - type/daily
week: "{{week}}"
mood: 
energy: 
---
```

- `week` — links to the weekly review note for this week
- `mood` — optional 1–5 integer, used in Dataview queries
- `energy` — optional 1–5 integer, useful for identifying high/low energy patterns

### `## Today's Focus`

Your three most important tasks (MITs) for the day. Write these during your morning routine.

```markdown
## Today's Focus
1. [[Project Alpha]] — finish the draft proposal
2. Review and respond to stakeholder email
3. 30 min: research for [[03 - Resources/Topic X]]
```

> [!tip] The Rule of Three
> Limiting yourself to three priorities forces you to make real decisions about what matters. If everything is a priority, nothing is.

### `## Tasks`

All tasks for the day, including carry-overs from yesterday.

```markdown
## Tasks
- [ ] #task Draft proposal sections 2–4 📅 2026-04-16
- [ ] #task Reply to Alex re: meeting 📅 2026-04-16
- [x] #task Weekly review ✅ 2026-04-15
```

> [!info] Tasks Plugin Syntax
> Use `📅 YYYY-MM-DD` for due dates and `✅ YYYY-MM-DD` for completion dates. These are recognized by the Obsidian Tasks plugin for filtering and queries.

### `## Notes & Captures`

A free-form section for anything captured during the day — meeting notes, ideas, links, quotes, passing thoughts.

### `## Reflection`

Completed during the evening review. Structured prompts keep reflection consistent without being rigid.

### `## Habits`

Checkboxes for daily habits. Kept in the daily note so they are easy to tick off throughout the day.

---

## Tips for Consistency

> [!tip] Make It Automatic
> Consistency comes from removing decisions. Set up a keyboard shortcut or Templater hotkey that creates today's daily note instantly — no folder navigation required.

**1. Use a Templater hotkey**
Configure Templater to create a new daily note from your template with a single keystroke. This removes all friction from starting the day.

**2. Open to the daily note on vault launch**
Set your vault to open `[[🏠 Home]]` or today's daily note automatically. Out of sight means out of mind.

**3. Keep the template short enough to fill**
A template that takes 5 minutes to complete beats a comprehensive template you skip. Start minimal and add sections only when you feel the gap.

**4. Don't backfill**
If you miss a day, don't try to reconstruct it. Skip the note and start fresh. Guilt about gaps is more destructive to consistency than the gaps themselves.

**5. Review yesterday before starting today**
Spend 2 minutes reading yesterday's note. It surfaces carry-over tasks and provides context for continuing work.

---

## How Claude Helps with Daily Notes

The `/daily-review` command triggers Claude to assist with your daily note in several ways:

**Morning mode** (run at start of day):
- Summarizes yesterday's open tasks
- Suggests today's top priorities based on project deadlines
- Pulls in any relevant notes from the inbox

**Evening mode** (run at end of day):
- Prompts you through the reflection section
- Identifies tasks to reschedule
- Suggests captures that should be processed into proper notes
- Generates a one-paragraph summary of the day for the weekly review

> [!example] Example Claude Prompt for Daily Notes
> "Review my daily note for today, identify any open tasks that need to be rescheduled, and summarize the key reflection points in 2–3 sentences."

---

## Dataview Queries for Daily Note Insights

### Recent Daily Notes

```dataview
TABLE mood, energy, file.ctime as "Created"
FROM "05 - Daily Systems/Daily Notes"
WHERE type = "daily"
SORT file.ctime DESC
LIMIT 14
```

### Average Mood & Energy (Last 30 Days)

```dataview
TABLE WITHOUT ID
  round(average(mood), 1) as "Avg Mood",
  round(average(energy), 1) as "Avg Energy",
  length(rows) as "Days Tracked"
FROM "05 - Daily Systems/Daily Notes"
WHERE type = "daily" AND date(file.ctime) >= date(today) - dur(30 days)
FLATTEN mood
FLATTEN energy
```

### Days With Notes This Month

```dataview
LIST
FROM "05 - Daily Systems/Daily Notes"
WHERE type = "daily"
  AND date(file.ctime).month = date(today).month
SORT file.ctime ASC
```

---

## Common Pitfalls

> [!warning] Avoid These Traps

**Over-engineering the template** — A 10-section template creates daily overwhelm. Start with Focus, Tasks, Notes, and Reflection. Add sections only when you notice consistent gaps.

**Using the daily note as a project log** — Daily notes are ephemeral; project notes in `[[01 - Projects/]]` are persistent. Move substantive project notes as soon as they're captured.

**Treating every capture as a task** — Not every capture needs action. Some are ideas, some are references, some are just thoughts. The evening review is the right time to classify them.

---

## Related Notes

- `[[MOCs/Daily Systems MOC]]` — All daily systems at a glance
- `[[Templates/Daily Note]]` — The template itself
- `[[05 - Daily Systems/Daily Systems]]` — Master overview of all daily systems
- `[[05 - Daily Systems/Task Management/Task & Priority Management]]` — Task system in depth
- `[[05 - Daily Systems/Habit Tracking/Habit Tracking]]` — Habit tracking in daily notes
- `[[05 - Daily Systems/Journaling/Journaling with Claude]]` — Reflection and journaling guide
