---
name: frontend-dev
description: React frontend development. Use when the user works on or asks about React components, hooks, JSX, client-side logic, CSS/styling, React state (useState, context, Redux), React Router, data fetching (React Query, SWR, fetch), build tools (Vite, Create React App), responsive design, or frontend testing in React.
---

# Frontend Dev (React)

Apply when implementing or reviewing **React** frontend code: components, hooks, styling, client state, routing, or data fetching.

## When to Use This Skill

- React components, hooks, JSX
- Client-side state (useState, context, Redux)
- Styling (CSS, CSS-in-JS, Tailwind)
- React Router or client-side routing
- Data fetching (React Query, SWR, fetch)
- Frontend performance (bundle size, lazy load)
- Frontend testing in React

## Principles

- **Component composition**: Single responsibility; small, reusable components; lift state only as needed.
- **Hooks rules**: Only call hooks at top level; only call from React functions or custom hooks.
- **Accessibility**: Semantic HTML (button, a, label, headings in order); visible focus; don’t rely on color alone; contrast and alt text.
- **Performance**: Use `React.memo` for expensive renders when needed; `lazy()` and code-splitting for routes or heavy components; avoid unnecessary re-renders.

## Patterns

- **Components**: Prefer functional components with hooks over class components.
- **Data fetching**: Prefer React Query or SWR over raw `useEffect` + `fetch` (caching, loading/error state, refetch).
- **Forms**: Controlled components or React Hook Form; clear validation and error messages.
- **Routing**: React Router; protect routes when auth is required; use layout routes where it fits.

## Conventions

- Reuse existing project components and design tokens before adding new ones.
- Follow the project’s React structure (e.g. feature folders, shared components).
- Check for existing patterns (e.g. how data is fetched, how forms are handled) and match them.

For UI/UX and mobile CRUD design, combine with ui-ux-expert or ui-design-crud when relevant.
