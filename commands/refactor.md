---
description: "Audit and optimize an existing Gemini skill for performance (context thinning)."
---

# Command: /gskills-forge:refactor
**Goal**: Audit and optimize an existing Gemini skill for performance (context thinning).

## Procedure
1. **Audit**: Call `list_directory` and `read_file` on `SKILL.md`.
2. **Context Thinning**: 
   - Move procedural logic > 2KB to `references/`.
   - Ensure imports use correct syntax `@./references/file.md`.
3. **Optimizing Tools**:
   - Check if `grep_search` is used efficiently.
   - Consolidate multiple turns into parallel tool calls.
4. **Validation**: Test and confirm no instruction regression.
