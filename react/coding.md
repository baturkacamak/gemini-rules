# React & TypeScript Coding Standards

## Code Style
- **Components:** Functional Components with Hooks ONLY. No Class components.
- **Language:** TypeScript (`.tsx`, `.ts`) is mandatory.
- **Types:**
    - Use `interface` for public API definitions (props, state).
    - Use `type` for unions, intersections, and primitives.

## Architecture & Patterns
- **Interfaces for Dependencies:**
    - API clients and Services should be defined by `interface` to allow mocking in tests.
    - Example: `useAuth(service: AuthProvider)` where `AuthProvider` is an interface.

## State & Data
- **Local State:** `useState` for simple UI state.
- **Global State:** `useContext` + `useReducer` for moderate complexity. External libraries (Zustand/Redux) only if strictly needed.
- **Side Effects:** encapsulate `useEffect` logic in custom hooks (e.g., `useWindowSize`).

## Performance
- **Memoization:** Use `useMemo` and `useCallback` strategically, not by default.
- **Keys:** Never use array index as keys for lists if the list can change.

## Styling
- **Approach:** CSS Modules, Tailwind CSS, or Styled Components (Project specific, but stick to one).

## Testing & TDD
- **TDD Protocol (Mandatory):**
    - Logic/Hooks: Write unit tests first (Vitest/Jest).
    - Components: Write interaction tests first (Testing Library).
    - E2E: Write "User Journey" tests first (Playwright/Cypress) for critical paths (ATDD).
- **Tooling:** Vitest (Unit), React Testing Library (Component), Playwright (E2E).
- **Rule:** No component is complete without a corresponding test file.
