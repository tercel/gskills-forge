# Command: /gskills-forge:refactor
**Goal**: Audit and optimize an existing Gemini skill for performance (context thinning).

## Procedure
1. **Syntax Audit**: Fix broken `@./` paths and non-compliant frontmatter.
2. **Context Thinning**:
   - Identify monolithic logic blocks in `SKILL.md` that exceed 2KB.
   - Extract them into dedicated markdown files in `commands/` (for logic) or `references/` (for rules).
   - Inject "@./commands/[file].md" or "@./references/[file].md" instructions into the main orchestrator.
3. **Sub-agent Injection**: Identify heavy tasks (e.g., directory crawling) and update instructions to delegate them to `generalist`.
4. **Verification**: After refactoring, ensure all command references are intact.
