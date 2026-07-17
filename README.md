# Icalia Labs — Collateral Library

A collection of Icalia Labs sales collateral (playbooks, decks, one-pagers),
published via GitHub Pages.

**Live:** https://icalialabs.github.io/icalia-labs-services-deck/

## Structure

```
index.html            → the hub / landing page (lists all collateral)
collateral/
  services-deck.html  → Services Overview deck
  talent-engine.html  → Talent Operations Playbook
```

The hub reads a small manifest (the `COLLATERAL` array inside `index.html`) and
renders a card for each item.

## Publishing a new collateral

No build step. To add one:

1. Drop a self-contained `.html` file into `collateral/`.
2. Add one entry to the `COLLATERAL` array near the bottom of `index.html`:
   ```js
   {
     title: "My One-Pager",
     description: "Short summary shown on the card.",
     category: "One-pager",
     url: "collateral/my-one-pager.html"
   }
   ```
   For collateral hosted elsewhere, add `external: true` and use its full URL.
3. Commit and push to `main` — GitHub Pages auto-deploys.

The whole library is `noindex` (not surfaced in search) — share by link.

## Deck navigation

- **Arrow Keys** / **Space** — next slide · **Left Arrow** — previous · **Swipe** on mobile
