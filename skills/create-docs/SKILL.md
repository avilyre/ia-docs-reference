---
name: create-docs
description: When the user wants to create the project documentation to keep AI flow optimized
---

# Create docs based on the core project files

Perform a complete analysis of the project, and create the architecture files separated by domain.
The domains must be created in `.opencode/reference/` using the following files:

Note: Each file must contain a maximum of 200 lines. If it exceeds this limit, it must be compacted to comply with the rule.
Existing structure must be preserved whenever possible, creating only what is necessary.

- `.opencode/reference/code-patterns.md`, `.opencode/reference/clean-code.md` -
  Coding conventions, folder ownership, patterns, API/content conventions, and styling implementation rules.
- `.opencode/reference/important-notes.md` - Operational constraints, environment requirements, runtime caveats, cache behavior, and high-impact safety notes.
- `.opencode/reference/architecture.md` - Route map, domain boundaries, integration points, and end-to-end runtime data flows.
- `.opencode/reference/design.md` - Design tokens, typography and layout rules, motion/effects, and markdown content styling behavior.

Ensure that:
- Ensure agents can clearly understand when and how to use each reference in `AGENTS.md`
- If `AGENTS.md` does not exist, create it in the root of the project with the following content for the domains created:

```
# Agent Reference Index

Use this index before making changes. Load only the domains that match the task.

## Rules Domain

- Path: `.opencode/reference/code-patterns.md`
- Purpose: Coding conventions, folder ownership, patterns, API/content conventions, and styling implementation rules.
- When to use: Any code edit, refactor, new feature, or file placement decision.

- Path: `.opencode/reference/important-notes.md`
- Purpose: Operational constraints, environment requirements, runtime caveats, cache behavior, and high-impact safety notes.
- When to use: API/env changes, deployment/runtime behavior work, or risky edits touching data flow.

## Architecture Domain

- Path: `.opencode/reference/architecture.md`
- Purpose: Route map, domain boundaries, integration points, and end-to-end runtime data flows.
- When to use: Planning features, tracing bugs across layers, or modifying page/API responsibilities.

- Path: `.opencode/reference/design.md`
- Purpose: Design tokens, typography and layout rules, motion/effects, and markdown content styling behavior.
- When to use: UI updates, CSS changes, animation edits, or visual consistency checks.
```

# Create good practices file
## Rules Clean code file
Create the following files:
- `.opencode/reference/clean-code.md`
with the following content:
```
### Global project rules

- Clear all whitespace from the code.
- Clear all comments from the code (if it's not necessary).
- Clear all unused variables, functions, or classes.
- All code must to be in English.
- Void to use any special characters or symbols.
- Void to use for variables, functions, or classes one character in it's name.
- Wrap every fetch request in a try catch block following the fetch request.
- Handle the error in the catch block.
- Return the response in the try block.
```
