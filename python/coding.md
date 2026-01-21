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
- **Dependency Injection:** Prefer passing dependencies explicitly over global state or side-channel imports.
- **Composition:** Prefer composition over deep inheritance hierarchies.
- **Error Handling:** Use custom exceptions for domain-specific errors. Catch specific exceptions, never bare `except:`.

## Testing Patterns
- **Framework:** `pytest` is the standard.
- **Mocks:** Use `unittest.mock` or `pytest-mock` to isolate units.
- **Fixtures:** Use `pytest` fixtures for setup/teardown logic.
- **Coverage:** Aim for high branch coverage.
