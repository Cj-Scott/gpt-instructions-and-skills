# Pure CSS Rotating Glow Border

## Purpose

Create a premium animated glowing border around a card using pure CSS.

## Instruction

```text
Create a premium animated glowing border around a card using pure CSS.

Requirements:
- Do not use images, video, SVG, canvas, or JavaScript.
- Register a custom CSS angle property using `@property`.
- Animate the angle continuously from `0deg` to `360deg`.
- Use that angle inside a `conic-gradient`.
- Position the animated gradient behind the card.
- Keep the card's content and background layered above the gradient so that only a thin rotating border is visible.
- Add a subtle blurred version of the gradient to create an outer glow.
- Respect the card's border radius.
- Include a `prefers-reduced-motion` fallback.
- Return complete, accessible HTML and CSS that can be copied into a project directly.
```

## Source summary

The technique animates a registered angle custom property and feeds it into a conic gradient positioned behind a card. The card masks the gradient's center, leaving a rotating, glowing edge.
