# Python Coding Standards

## Code Style
- **Type Hints:** ALWAYS use type hints for function arguments and return values.
    - `def calculate_total(price: float, tax: float) -> float:`
- **Docstrings:** Use Google-style docstrings.
- **Formatting:** Adhere to PEP 8 (enforced by Ruff).
- **Naming:**
    - Variables/Functions: `snake_case`
    - Classes: `PascalCase`
    - Constants: `UPPER_CASE`

## Architecture
- **Configuration First:**
    - **No Magic Values:** Do not hardcode numbers, timeouts, or paths deep in logic.
    - **Extraction:** Move them to `config.py`, `settings.py`, or class-level `CONSTANTS`.
- **Interfaces First:**
    - **Boundaries:** All external dependencies (DB, APIs, storage) MUST be typed as `Protocol` or `ABC` (Abstract Base Class).
    - **Usage:** Logic should depend on `RepositoryInterface`, never `SqlAlchemyRepository`.
- **No Global State:**
    - **Forbidden:** Singletons and mutable global variables.
    - **Avoid:** Static methods (`@staticmethod`) for logic that requires dependencies. Use instance methods or pure functions.
- **Dependency Injection:** Prefer passing dependencies explicitly over global state or side-channel imports.
- **Composition:** Prefer composition over deep inheritance hierarchies.
- **Error Handling:** Use custom exceptions for domain-specific errors. Catch specific exceptions, never bare `except:`.

## Testing Patterns
- **TDD Protocol (Mandatory):**
    1.  **Red:** Write the failing unit/integration test FIRST.
    2.  **Green:** Write the minimal code to pass the test.
    3.  **Refactor:** Improve code structure while keeping tests green.
- **Coverage:** No code is accepted without a passing test.
- **Framework:** `pytest` is the standard.
- **Mocks:** Use `unittest.mock` or `pytest-mock` to isolate units.
- **Fixtures:** Use `pytest` fixtures for setup/teardown logic.
