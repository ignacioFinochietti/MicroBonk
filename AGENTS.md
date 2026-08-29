# MicroBonk Development Agent Rules

These rules are enforced by the Gentleman Guardian Angel code review assistant for the MicroBonk repository.

## Coding Standards

- **Vanilla JS & HTML5 Canvas**: Keep the game dependencies to 0. Do not use external libraries, frameworks, or bundlers.
- **Performance & Allocation**: Do not allocate new objects (arrays, objects, functions) inside the main `loop` or `update` ticks. Use the existing pool functions (`createPool`, `poolGet`, `clearPool`).
- **Global State**: Keep global state in the `G` object to maintain modularity.
- **Visuals & Feedback**: All damage hits must display floating texts (`spawnDmgText`). Normal hits must be small and white; critical hits must say `CRÍTICO` in bold red.
- **Boss Portal**: Bosses must spawn through portals and generate direction/distance indicators when off-screen.

## Commit Hygiene

- **Conventional Commits**: Commit messages must follow the Conventional Commits specification (e.g., `feat: add sound effects`, `fix: correct orbiter cooldown`).
- **No AI Attribution**: Never include "Co-Authored-By" or AI attribution footers in commit messages.
