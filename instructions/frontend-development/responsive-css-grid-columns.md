# Responsive CSS Grid Columns

## Purpose

Create a responsive CSS Grid layout using flexible column sizing rather than unnecessary breakpoint-specific column definitions.

## Instruction

```text
Create or refactor the requested layout using semantic HTML and CSS Grid.

Inputs:
- Content or component description: [CONTENT]
- Minimum practical item width: [MINIMUM WIDTH, such as 16rem]
- Maximum item width, if required: [MAXIMUM WIDTH OR "NONE"]
- Desired gap: [GAP]
- Existing HTML, CSS, or framework constraints: [CONTEXT]

Requirements:
1. Use `grid-template-columns` to define the column structure.
2. Prefer flexible `fr` units over fixed pixel columns unless a fixed dimension is required by the design.
3. Use `repeat()` when multiple columns share the same sizing rule.
4. Use `minmax()` to define useful lower and upper size bounds.
5. For a fluid card-style grid, prefer a pattern such as:

   `grid-template-columns: repeat(auto-fit, minmax(min(100%, [MINIMUM WIDTH]), 1fr));`

6. Explain whether `auto-fit` or `auto-fill` is appropriate. Use `auto-fit` when empty tracks should collapse and existing items should expand; use `auto-fill` when empty tracks should remain reserved.
7. Prevent horizontal overflow at narrow viewport widths.
8. Preserve logical reading and keyboard-navigation order; do not visually reorder content in a way that conflicts with the DOM.
9. Use responsive spacing and avoid unnecessary media queries.
10. Respect existing design tokens and browser-support requirements.

Return:
- Complete, copy-ready HTML and CSS, or a focused patch when existing code is supplied.
- A concise explanation of the selected grid formula.
- The expected behavior at narrow, intermediate, and wide widths.
- Any compatibility or content-size assumptions.

Keep the solution minimal and accessible. Do not use JavaScript for layout behavior that CSS Grid handles directly. Do not use fixed column counts when the content should adapt naturally to available space.
```

## Key concepts

- `fr` distributes available space proportionally.
- `repeat()` expresses repeated track definitions without duplication.
- `minmax()` constrains how small or large a track may become.
- `auto-fit` collapses unused tracks and lets populated tracks expand.
- `auto-fill` retains available tracks even when some are empty.
