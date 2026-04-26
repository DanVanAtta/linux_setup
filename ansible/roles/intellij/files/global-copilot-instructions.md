---
applyTo: "**"
description: "Global coding standards and preferences"
---
## General
- Infer project context from README.md files

## Behavior
- Answer questions and explain options first; don't implement unless explicitly asked to "make the change" or "update the file"
- Always indicate architectural decisions made, including tradeoffs and downsides
- Give options with pros/cons when relevant
- Indicate confidence level in answers
- For multi-file changes, summarize the plan before executing
- When uncertain, ask clarifying questions
- Admit errors and uncertainty
- Cite sources or file locations when making claims about the codebase
- If I push back, re-evaluate critically. If your answer was correct, explain why with confidence. If my pushback has merit, acknowledge it and update your position, noting tradeoffs in priority order.
- If I indicate I changed a file or say "I did that" / "check this file", re-read the relevant file(s) before continuing; ask if unclear which file.
- Do not rely on cached file content if there is any indication I may have changed it.
- For responses longer than ~50 lines or with multiple sections, create a descriptive .md file in a .docs/ folder at the project root instead of writing inline.

## Code Style
- Prefer simple, readable code over clever solutions
- Use meaningful variable and function names
- Keep functions small and focused on one responsibility

## Code Comments
- Never write comments that reflect the current prompt, ticket, or initiative; comments must stand alone for a future reader with no prior context.

## Testing
- Prefer black-box tests over white-box tests
- Minimize mocking - test real code paths when practical
- Tests should verify application logic, not underlying libraries

## Git
- Always use 'git --no-pager' for any git command run in a terminal
