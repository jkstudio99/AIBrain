---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/project-management
  - topic/para
  - topic/workflow
  - status/evergreen
related:
  - "[[MOCs/Projects MOC]]"
  - "[[Templates/Project Note]]"
  - "[[03 - Resources/Knowledge Workflows/Capture Process Connect]]"
  - "[[MOCs/Daily Systems MOC]]"
aliases:
  - Project Guide
  - PARA Project Management
---

# Project Management Guide

In the PARA system, a **project** has a specific definition that most people overlook: it is something with both a **clear outcome** and a **deadline** (explicit or implicit). This distinction is what separates projects from areas of responsibility — and keeping it sharp is what makes the system work.

> [!abstract] The PARA Definition of a Project
> A project is "a series of tasks linked to a goal, with a deadline." If there's no deadline, it's an area. If there's no clear outcome, it's a resource. Misclassifying these is the most common reason PARA systems break down.

---

## What Qualifies as a Project?

**Is a project:**
- Write and publish a blog post about X (outcome: published post; implicit deadline: before topic becomes stale)
- Complete the onboarding documentation for the new tool (outcome: docs; deadline: before launch)
- Read and synthesize *Book Title* (outcome: literature note + key evergreens; deadline: by end of month)
- Build the habit tracker dashboard in Obsidian (outcome: working dashboard; deadline: this sprint)

**Is NOT a project (it's an area):**
- "Maintain the blog" — no end state; this is ongoing
- "Keep up with reading" — perpetual habit, not a deliverable
- "Improve my note-taking" — too vague, no clear done state

**If you're unsure**, ask: *"How will I know when this is finished?"* If you can't answer clearly, it's an area or a goal, not a project.

> [!tip] The Weekly Review Test
> During weekly review, every item in `01 - Projects/` should answer "yes" to: *Is this actively being worked on this week or next week?* If the answer is "no, but eventually," it should be paused or archived.

---

## Project Lifecycle

A project in this vault moves through five stages. Understanding these stages helps you know what action to take at any moment.

### Stage 1: Create

A new project is born when you identify a clear outcome and decide to pursue it. At creation:

1. Create a new folder: `01 - Projects/[Project Name]/`
2. Create the main project note using `[[Templates/Project Note]]`
3. Set the frontmatter: `status:: in-progress`, `priority:: high|medium|low`, `due:: YYYY-MM-DD`
4. Write the project brief: what is the outcome? Why does it matter? What does done look like?
5. Add to `[[MOCs/Projects MOC]]`

```yaml
---
type: project
created: "2026-04-16"
status: planning
priority: high
due: "2026-05-01"
tags:
  - type/project
  - status/active
  - area/[relevant-area]
related: []
---
```

### Stage 2: Plan

Before executing, spend 15-30 minutes planning. A plan doesn't need to be comprehensive — it just needs enough runway to start moving without stopping to think at every turn.

**Planning outputs:**
- A task list with clear, actionable next actions (not vague goals)
- An identified "next physical action" — the very next concrete step
- Any known dependencies or blockers
- Resources needed (links to relevant notes, external resources)

> [!example] Good vs. Bad Tasks
> **Bad task:** "Work on the report"
> **Good task:** "Write the introduction section (500 words, covering background and problem statement)"
>
> **Bad task:** "Research the topic"
> **Good task:** "Read and take literature notes on chapters 3-5 of [[Source Name]]"

Use Dataview-compatible task syntax for all project tasks:

```markdown
- [ ] Task description [due:: 2026-04-20] [priority:: high]
- [ ] Another task [status:: in-progress]
```

### Stage 3: Execute

Execution is where most of your project time is spent. The key discipline: **update the project note** as you work, not after.

**Execution habits:**
- Check the project note at the start of every work session
- Mark tasks complete as you finish them (`- [x]`)
- Add blockers or new tasks as they emerge
- Link to any notes or resources created during execution
- Log key decisions in a "Decision Log" section

**During a work session:**
1. Open the project note
2. Identify the next action
3. Do it
4. Update the note (check off, add new tasks, log decisions)
5. Note where you stopped for the next session

### Stage 4: Review

A project review happens in two contexts: **ongoing** (weekly) and **closing** (at completion).

**Weekly project review questions:**
- Is this project still active? (If not, pause or archive it)
- What is the next action?
- Are there any blockers I need to resolve?
- Is the deadline still realistic?

**Closing review questions:**
- Was the original outcome achieved? What changed?
- What worked well in how this was managed?
- What would I do differently next time?
- What knowledge should be extracted into evergreen notes or resources?
- Are there follow-on projects or areas this work feeds?

> [!info] The Closing Review Is Investment
> The closing review feels like overhead, but it's where compound returns come from. The 15 minutes you spend extracting learnings from a completed project become evergreen notes that improve every future project.

### Stage 5: Archive

When a project is complete (or permanently paused), move it to `04 - Archive/Projects/[Year]/[Project Name]/`. Do not delete.

Before archiving:
- [ ] Closing review complete
- [ ] Key learnings extracted to evergreen notes or resources
- [ ] Relevant assets linked from appropriate folders
- [ ] Status updated to `status: completed` or `status: paused`
- [ ] Removed from `[[MOCs/Projects MOC]]` (or marked as archived there)

---

## Project Lifecycle Diagram

```mermaid
stateDiagram-v2
    [*] --> Planning : Project identified\n(outcome + deadline clear)

    Planning --> Active : Plan drafted,\nnext action identified

    Active --> OnHold : Blocker encountered\nor deprioritized

    OnHold --> Active : Blocker resolved\nor priority restored

    Active --> InReview : Work complete,\nawaiting closing review

    InReview --> Completed : Closing review done,\nlearnings extracted

    InReview --> Active : Gaps identified,\nmore work needed

    Completed --> Archived : Moved to\n04 - Archive/

    Active --> Cancelled : Project no longer\nrelevant or possible

    Cancelled --> Archived : Archived with\ncancellation note

    Planning --> Cancelled : Decided not\nto pursue

    Archived --> [*]

    note right of Planning : status: planning\nFocus: Define outcome\nWrite project brief
    note right of Active : status: in-progress\nFocus: Execute\nUpdate tasks daily
    note right of OnHold : status: on-hold\nDocument blocker\nSet resume trigger
    note right of Completed : status: completed\nExtract learnings\nLink artifacts
```

---

## Using the Project Template

The `[[Templates/Project Note]]` provides structure for all project notes. Key sections:

### Project Brief

A 2-3 sentence description of:
1. What you are creating/achieving
2. Why it matters
3. What "done" looks like

This section should be so clear that someone unfamiliar with the project can understand it in 30 seconds.

### Task Management with Dataview

Use Dataview properties inline with tasks for powerful querying:

```markdown
## Tasks

### Next Actions
- [ ] Draft the introduction [due:: 2026-04-18] [priority:: high]
- [ ] Review competitor analysis [priority:: medium]

### In Progress
- [ ] Set up project folder structure [status:: in-progress]

### Completed
- [x] Define project scope [completed:: 2026-04-16]
```

**Useful Dataview queries for project dashboards:**

```dataview
TASK
WHERE !completed AND file.path = this.file.path
SORT priority DESC
```

```dataview
TABLE status, due, priority
FROM "01 - Projects"
WHERE status != "completed" AND status != "archived"
SORT due ASC
```

### Decision Log

Keep a running log of significant decisions:

```markdown
## Decision Log

### 2026-04-16 — Chose approach X over Y
Context: [brief situation]
Decision: [what was decided]
Reasoning: [why]
Trade-offs accepted: [what you gave up]
```

This becomes invaluable during the closing review and when revisiting similar decisions in future projects.

---

## Task Management Principles

### The Next Action Rule

Every project must always have exactly one "next action" — a concrete, physical task that can be done without any additional decisions. Stuck projects are almost always stuck because the next action is unclear.

Bad next action: "Think about the design"
Good next action: "Sketch 3 rough wireframe options for the dashboard layout"

### Task Granularity

Tasks should be completable in a single work session (1-3 hours). Larger items should be broken down. A task like "write the report" is not a task — it's a project.

### Priority Levels

| Priority | Meaning | Default attention |
|----------|---------|-------------------|
| `priority:: high` | Blocking other work or has near deadline | Daily attention |
| `priority:: medium` | Important but flexible timing | Weekly attention |
| `priority:: low` | Nice to have, can slip | As time allows |

---

## Project Review Cadence

| Review Type | Frequency | Questions |
|-------------|-----------|-----------|
| **Daily check-in** | Daily (during daily note) | What's the next action? Any blockers? |
| **Weekly review** | Every Sunday | All projects still active? What needs attention? |
| **Monthly review** | First of month | Any projects to archive? Any new projects to start? |
| **Closing review** | At project completion | What worked? What to extract? What's next? |

> [!info] Weekly Review Integration
> The weekly project review should be part of your regular `[[05 - Daily Systems/Weekly Review]]` workflow. See `[[MOCs/Daily Systems MOC]]` for the full weekly review template.

---

## When to Archive vs. Pause a Project

### Archive (Completed)
- The original outcome has been achieved
- Closing review is complete
- All artifacts are organized and linked

### Archive (Cancelled)
- You've decided the project is no longer worth pursuing
- Document *why* it was cancelled — this is valuable future context
- Note any learnings even from cancelled projects

### Pause (On Hold)
- The project is temporarily blocked by an external dependency
- You're intentionally deprioritizing it but plan to return
- Set a "review trigger" — a date or event when you'll reassess

> [!warning] The Zombie Project Problem
> The most dangerous project state is "technically active but actually dead." Projects that haven't had a next action completed in 3+ weeks are zombies. During weekly review, be ruthless: either revive it with a concrete next action or archive it. A small active list beats a long neglected one.

---

## Related Resources

- `[[MOCs/Projects MOC]]` — Overview of all active projects
- `[[Templates/Project Note]]` — Project note template
- `[[03 - Resources/Knowledge Workflows/Capture Process Connect]]` — How project notes fit the workflow
- `[[MOCs/Daily Systems MOC]]` — Weekly review where projects are assessed
- `[[03 - Resources/Knowledge Workflows/Research & Synthesis Guide]]` — For research-heavy projects
