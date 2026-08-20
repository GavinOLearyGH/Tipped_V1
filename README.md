# Tipped V1

Combined shell for the two TIP quick-hit products.

- **TIP7** = Quick Body: Stretch + Strength
- **TIP9** = GOLF-HITT / Quick Practice: Swing + Skill

## Current architecture

Tipped is now the single product URL and navigation shell. The header switches between the **live TIP7** and **live TIP9** engines in place.

This deliberately avoids duplicating two growing applications into one fragile JavaScript file. TIP7 and TIP9 remain independently testable in their source repositories, while Tipped presents them as one product family.

### TIP7

Loads the current working TIP7 Level 1 engine, including onboarding, calendar/streak behavior, PREPARE/WORK timer, exercise instructions, controls, completion and prototype reset.

### TIP9 / GOLF-HITT

Loads the current working TIP9 v0.2 engine, including location choice, recommendation-led `Give me 9`, the expanded practice library, clearer What To Do / Success language, adaptive Swing blocks, scored Skill blocks, levels and prototype reset.

## Shared design language

Tipped uses TIP7 as the visual reference: dark green, cream type, lime accent, rounded outlined panels and lime primary actions. Where browser same-origin rules permit, the shell applies this same presentation layer to TIP9 so the engines feel like siblings while retaining different workflows.

## Product behavior

Only one engine is visible at a time. TIP7 and TIP9 no longer append sections underneath each other in the combined product. Switching the header tab replaces the visible application view while preserving the independent local progress of each engine.