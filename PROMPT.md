# Bolt App 2 — Timeline Studio (Micro-App)

Before you start: read and follow `DESIGN_SYSTEM_BRIEF.md`.

## Mission

Build a UI/UX-rich Next.js micro-app called **Timeline Studio** that demonstrates timeline/scheduler editing patterns (drag, resize, inspector). This should be reusable inspiration for ChronoMind timelines and routines UX.

## Scope / Safety

- Only change files in this repository.
- No network calls; mock data + localStorage only
- No `console.log`
- No hardcoded colors; define CSS variables once and use Tailwind

## Stack

- Next.js 16 App Router
- React 19
- Tailwind v4
- TypeScript strict
- pnpm
- lucide-react icons

## Routes

- `/` overview + recent plans
- `/studio` main editor
- `/export` JSON import/export

## Layout

- Left sidebar: list of “plans” (templates)
- Main canvas: timeline grid
- Right inspector: edit selected block

## Timeline interactions (must-have)

- Lanes (e.g. Work, Personal, Health)
- Blocks can be:
  - created (button + click on grid)
  - selected
  - dragged to move
  - resized via left/right handles
- Snap-to-grid increments (5 min)
- Zoom levels (15m / 30m / 60m)
- Keyboard:
  - `Esc` deselect
  - `Delete` remove selected
  - `Cmd+Z` undo (simple history stack)

## Inspector (must-have)

- Title
- Start/end time
- Lane
- Tags
- Notes

Persist in localStorage:

- plans list
- blocks
- zoom
- last opened plan

## UX quality bar

- Clear selection states + resize handles
- Good hit targets
- Subtle animations
- Empty state onboarding hints

## Deliverables

- Full Next.js app with scripts: `dev`, `check`, `build`
- `build` must run `next build --webpack`

## Verification

From the repo root:

- `pnpm install`
- `pnpm run check`
- `pnpm run build`

## Output expectation

PR contains only this app.
