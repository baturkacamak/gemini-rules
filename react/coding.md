# React & TypeScript Coding Standards

## Code Style
- **Components:** Functional Components with Hooks ONLY. No Class components.
- **Language:** TypeScript (`.tsx`, `.ts`) is mandatory.
- **Types:**
    - Use `interface` for public API definitions (props, state).
    - Use `type` for unions, intersections, and primitives.

## State & Data
- **Local State:** `useState` for simple UI state.
- **Global State:** `useContext` + `useReducer` for moderate complexity. External libraries (Zustand/Redux) only if strictly needed.
- **Side Effects:** encapsulate `useEffect` logic in custom hooks (e.g., `useWindowSize`).

## Performance
- **Memoization:** Use `useMemo` and `useCallback` strategically, not by default.
- **Keys:** Never use array index as keys for lists if the list can change.

## Styling
- **Approach:** CSS Modules, Tailwind CSS, or Styled Components (Project specific, but stick to one).
