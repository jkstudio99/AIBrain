---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/vault
  - topic/templates
related:
  - "[[03 - Resources/Vault Foundation/Vault Foundation]]"
---

# Templates System

## Goal
Templates keep note creation consistent so Dataview, Claude, and manual review all work smoothly.

## Current Templates
- [[Templates/Fleeting Note]]
- [[Templates/Literature Note]]
- [[Templates/Evergreen Note]]
- [[Templates/Project Note]]
- [[Templates/Area Note]]
- [[Templates/Daily Note]]
- [[Templates/Weekly Review]]
- [[Templates/Monthly Review]]
- [[Templates/MOC Template]]

## Required Properties
- `type`
- `created`
- `tags`

## Template Policy
- Start from the closest template instead of a blank note.
- Keep sections stable so Claude can extend notes safely.
- Add `related` when a note should join a cluster.

## Related
- [[03 - Resources/Core Plugins/Templater & QuickAdd]]
- [[03 - Resources/Vault Foundation/Metadata & Dataview Guide]]
