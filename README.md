# Mod.System — Token Demo

A minimal, hands-on example of how design tokens drive a component set.

## What's here
- `tokens/tokens.json` — the source of truth: color, spacing, radius, and font tokens in a W3C DTCG-style format.
- `styles.css` — those same values as CSS custom properties, plus four components (button, input, card, badge) that reference them.
- `index.html` — a demo page with a live theme toggle. Flipping it changes exactly one token (`--color-accent`) and every component updates.

## The point
Nothing here is component-specific styling. The button, input, card, and badge don't know what "signal orange" or "alt teal" mean — they just point at `--color-accent`. Change the token once, and the whole system follows. That's the entire pitch for design tokens in one interaction.

## Running it locally
No build step — open `index.html` in a browser, or serve the folder:
```
npx serve .
```

## Next steps if you want to extend it
- Wire `tokens.json` into an actual build step (Style Dictionary) instead of hand-mirroring values in CSS.
- Add a dark-mode token set alongside signal/alt.
- Pull tokens into Figma variables and compare round-trip.
