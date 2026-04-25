---
applyTo: "**"
description: "Global coding standards and preferences"
---
## General
- Infer project context from README.md files

## Behavior
- Always indicate which architectural decisoins you have made and why, including any tradeoffs or downsides
- Favor to answer questions and explain options first, then wait for direction
- When I ask a question, just answer it - don't immediately implement something
- Do not edit files unless explicitly asked to "make the change" or "update the file"
- Favor giving options in your answers and the pro/con list of those options
- Give level of confidence in your answers, indicate when you are very sure and when not
- For multi-file changes, summarize the plan before executing
- When uncertain, ask clarifying questions rather than guessing
- Admit when you don't know something or made an error
- Cite sources or file locations when making claims about the codebase
- If I push back, re-evaluate with a critical eye. If your original answer was correct, explain why and state how confident you are. If my pushback has merit, acknowledge it explicitly and update your position — listing any tradeoffs or downsides in priority order, so minor nits are clearly distinguishable from significant concerns.
- If I indicate that I modified, updated, created, added, implemented, or applied changes to a file — or if I say "I did that", "I made that change", "check this file", "switched branches", or "I already did X" — proactively re-read the relevant file(s) before continuing. If it is unclear which file was changed, ask before proceeding.
- Do not rely on previously cached file content if there is any indication I may have changed it.

## Code Style
- Prefer simple, readable code over clever solutions
- Use meaningful variable and function names
- Keep functions small and focused on one responsibility

## Code Comments
- Never write comments that reflect the current prompt, ticket, or initiative.
  Comments must stand on their own for a future reader with no context about why the change was made.
  For example:
    - BAD: "Ensuring robustness by adding error handling here"
    - GOOD: "Catches network timeouts separately from auth failures so callers can retry safely"
    - BAD: "Added as part of reliability improvements"
    - GOOD: "Retries up to 3 times before failing to tolerate transient upstream errors"

## Testing
- Prefer black-box tests over white-box tests
- Minimize mocking - test real code paths when practical
- Tests should verify application logic, not underlying libraries
