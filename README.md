# Gemini Rules

**The Centralized Constitution for AI-Assisted Development.**

This repository serves as the "Single Source of Truth" for coding standards, infrastructure blueprints, and development workflows. It is designed to be imported into any project (Python, PHP, React) to instantly provide Gemini with expert-level context.

## 🚀 Key Features

*   **Modular Architecture:** Import only what you need (e.g., `python/coding.md` or `react/infrastructure.md`).
*   **Scale-Ready Infrastructure:**
    *   **Automated Versioning:** Zero "Version Drift" policies using Git Tags as the single source of truth.
    *   **Mandatory Testing:** AI is required to generate unit tests for all logic.
    *   **Pre-commit Enforcement:** Tests and linters run *before* code is committed.
*   **Standardized Tooling:**
    *   **Task Running:** `Justfile` for uniform commands (`just test`, `just build`).
    *   **Dev Containers:** Reproducible environments for instant onboarding.
    *   **GitHub Actions:** Cross-platform testing and automated releases.

## 📦 How to Use

1.  **Copy the Template:**
    Copy `GEMINI_TEMPLATE.md` to your project root and rename it to `GEMINI.md` (or `.gemini/rules.md`).

2.  **Select Your Modules:**
    Uncomment the lines relevant to your stack:

    ```markdown
    @gemini-rules/general.md
    @gemini-rules/infrastructure.md
    @gemini-rules/python/coding.md
    @gemini-rules/python/infrastructure.md
    ```

3.  **Start Chatting:**
    Gemini will now adhere to these strict standards for every line of code it writes.

## 💡 Pro Tip: Instant Initialization

Don't type "Read GEMINI.md" every time. Create a shortcut to start your session with context instantly.

### Linux / macOS (Bash/Zsh)
Add this alias to your `.bashrc` or `.zshrc`:
```bash
alias gstart='gemini "Read GEMINI.md and establish the project context."'
```

### Windows (PowerShell)
Add this function to your `$PROFILE`:
```powershell
function gstart { gemini "Read GEMINI.md and establish the project context." }
```

**Usage:**
Just type `gstart` when you open your project.

## 📂 Structure

*   `general.md`: Universal rules (Git, Tone, Safety).
*   `infrastructure.md`: The "Enterprise" blueprint (CI/CD, Governance, Versioning).
*   `python/`: Standards for Python (Ruff, Poetry, Pytest).
*   `php/`: Standards for PHP (Pest, Pint, Composer).
*   `react/`: Standards for React (Vite, ESLint, TypeScript).