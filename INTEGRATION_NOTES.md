# Integration Notes

This repo is a pattern source for timeline/scheduler UI.

Adoption expectations:

- Timeline primitives should live in `src/components/**` (grid, block, lane list, inspector).
- Keep drag/resize math in `src/lib/**` so we can transplant it.
- Use the shared `--ux-*` token contract.
