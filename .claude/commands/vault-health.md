Run a comprehensive vault health check:

1. **Orphan Notes**: Find notes with no incoming or outgoing links
2. **Empty Notes**: Find notes with no content (just frontmatter)
3. **Broken Links**: Find [[wikilinks]] that point to non-existent notes
4. **Missing Frontmatter**: Find notes without proper YAML frontmatter
5. **Inbox Status**: Count items in `00 - Inbox/` awaiting processing
6. **Tag Consistency**: Check for similar/duplicate tags
7. **Template Usage**: Verify notes follow their type's template structure
8. **Stale Notes**: Find notes not modified in 30+ days that are still "active"

Present results as a health scorecard with actionable recommendations.
