# Command: /gskills-forge:new
**Goal**: Scaffold a professional, syntactically correct Gemini skill.

## Procedure
1. **Interview**: Ask for name, description, and primary sub-commands.
2. **Scaffold**: 
   - Create `{name}/SKILL.md` (Main Orchestrator).
   - Create `{name}/commands/` (Command Logic).
   - Create `{name}/references/shared/` (Rules & Constants).
   - Create `{name}/templates/` (Scaffolding templates).
3. **Drafting**: Use `@./templates/SKILL.md.template` to generate a robust orchestrator.
4. **Validation**: Ensure all `@./` paths match the new folder structure.
