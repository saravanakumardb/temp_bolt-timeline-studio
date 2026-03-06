# Bolt — Timeline Studio

**GitHub repo:** `saravanakumardb/temp_bolt-timeline-studio`

## Push Instructions

- Push directly to `main` — do NOT open a PR
- Only modify files in this repo

## Rules

- No `console.log`
- No network calls — mock data / localStorage only
- No hardcoded colors — no hex, no rgb/rgba/hsl, no `bg-[#123456]` Tailwind classes
- Do NOT commit `.env*`, `.next/`, `node_modules/`, `.vercel/`
- pnpm only
- `pnpm run check` must pass (`tsc --noEmit` + `eslint`)
- `pnpm run build` must pass (`next build --webpack`)

## CSS Token Contract

Define in `src/app/globals.css` under `:root` (add `.dark` override):

- `--ux-bg` — page background
- `--ux-surface` — card/panel surface
- `--ux-surface-2` — elevated surface
- `--ux-border` — borders
- `--ux-text` — primary text
- `--ux-text-muted` — secondary text
- `--ux-accent` — primary accent
- `--ux-accent-foreground` — text on accent
- `--ux-danger` — destructive/error
- `--ux-warning` — warning
- `--ux-success` — success
- `--ux-ring` — focus ring
- `--ux-shadow` — shadows

Use only via Tailwind: `bg-[var(--ux-surface)]`, `text-[var(--ux-text)]`, `border-[var(--ux-border)]`

## Component Architecture

- Reusable components → `src/components/`
- Pages in `src/app/**` compose components only
- Components must NOT import from `src/app/**`

## Stack

- Next.js 16 App Router, React 19, TypeScript strict
- TailwindCSS v4, pnpm

## Mission

Build a **Timeline Studio** micro-app demonstrating timeline/scheduler editing (drag, resize, inspector). Reusable inspiration for ChronoMind timelines and routines UX.

Additional: lucide-react icons

## Pages

- `/` overview + recent plans
- `/studio` main editor
- `/export` JSON import/export

## Layout

Left sidebar (plans list), main canvas (timeline grid), right inspector (edit selected block)

## Timeline Interactions

- Lanes (Work, Personal, Health)
- Blocks: create (button + click), select, drag to move, resize via handles
- Snap-to-grid (5 min), zoom levels (15m / 30m / 60m)
- Keyboard: `Esc` deselect, `Delete` remove, `Cmd+Z` undo (history stack)

## Inspector

Title, start/end time, lane, tags, notes — persist to localStorage (plans, blocks, zoom, last opened plan)

## UX Quality

Clear selection states + resize handles, good hit targets, subtle animations, empty state hints

## Verification

```
pnpm install && pnpm run check && pnpm run build
```
