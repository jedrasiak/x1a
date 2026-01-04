# jedrasiak:x1a

## commiting

### Format
```
type: note title [- brief context if needed]
```

### Types
- `add` - New note created
- `edit` - Content modified (use description for what changed)
- `move` - Relocated in hierarchy
- `link` - Added connections between notes
- `delete` - Note removed
- `merge` - Combined multiple notes
- `split` - Broke note into multiple parts
- `refactor` - Restructured without changing core content

### Guidelines
1. **Keep commits atomic** - One logical change per commit
2. **Title is enough** - Only add description if change isn't obvious
3. **Link changes** - When connecting notes, commit both ends
4. **Move carefully** - Update all references when relocating

### Examples
```
add: Boolean Logic Fundamentals
edit: ALU Design - added ripple carry implementation
move: Power Supply Design - Embedded Systems/Tools → Computer Architecture/Tools
link: CPU Design ↔ Assembly Programming
delete: Outdated Arduino Notes
merge: Three separate flip-flop notes into Sequential Logic
refactor: Digital Logic - reorganized subcategories
```

### When to commit
- After completing a note session (daily is fine)
- Before major restructuring
- When you want to preserve a snapshot

### What NOT to commit every time
- Typo fixes (batch these)
- Minor formatting
- Single-sentence additions

Commit when the change has **semantic meaning**, not mechanical edits.