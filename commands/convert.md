# Command: /gskills-forge:convert
**Goal**: Migrate and "flatten" Claude Code skills into Gemini's orchestrator pattern.

## Procedure
1. **Source Audit (Sub-agent)**: Use `generalist` to scan `.claude-plugin/plugin.json` and `skills/` sub-dirs. Map all logic files.
2. **Transformation**:
   - Merge distributed `skills/` logic into single commands in `SKILL.md` or a `commands/` directory.
   - **Regex Mapping**: Convert `@../shared/` and `@shared/` to `@./references/shared/`.
   - **Tool Mapping**: Map `Task` -> `generalist`, `Edit` -> `replace` (with precise context), `ReadFile` -> `read_file`.
3. **Verification**: After writing, attempt to read the new `SKILL.md` to ensure all `@./` paths are correct.
4. **Final Check**: Ensure the new skill has the required frontmatter and `## Commands` section.
