# General Development Standards

These rules apply to all projects, regardless of language.

## Git & Version Control
- **Conventional Commits:** ALWAYS use conventional commits.
    - `feat: add user login`
    - `fix: resolve null pointer in dashboard`
    - `docs: update readme`
    - `chore: update dependencies`
- **Branching:** Use `feature/` or `fix/` prefixes (e.g., `feature/dark-mode`).
- **Secrets:** NEVER commit API keys, tokens, or passwords.

## Tone & Style
- **Brevity:** Be concise. Don't explain "what" you did unless asked. Focus on "why".
- **Safety:** Always analyze existing code before changing it. Do not break existing functionality.
- **Independence:** If a requested library is missing, check if it's installed. If not, ask before adding it.
