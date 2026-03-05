# Design System Brief (Must Follow)

These rules exist so this repo’s output is **production-reusable** across the ByteLyst workspace dashboards and product web apps.

## Non-negotiable rules

- No `console.log`.
- No hardcoded API URLs.
- No network calls in this repo (use mock data / local JSON / localStorage).
- **No hardcoded colors** (no hex/rgb/hsl or Tailwind arbitrary hex).

## Token usage

- Use the shared token contract in `UX_TOKEN_CONTRACT.md`.
- Prefer `bg-[var(--ux-*)]` / `text-[var(--ux-*)]`.

## Component architecture (reusability)

- Reusable components live in `src/components/`.
- Pages under `src/app/**` compose components.
- Components must NOT import from `src/app/**`.

## Accessibility + UX

- Keyboard accessible.
- `Esc` closes overlays.
- Focus management for dialogs/drawers.
