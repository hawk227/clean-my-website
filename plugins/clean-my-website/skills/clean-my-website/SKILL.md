---
name: clean-my-website
description: Twenty-point cleanup pass for web UI — removes AI-slop decoration (filler badges, random italics, needless mono, embellishments) and fixes craft details (radii, contrast, headline wrapping, tabular numbers, loading states, feedback motion). Use when asked to clean up, polish, de-slop, tighten or review a page, landing page, component or dashboard, or says "clean my website" or "clean-my-website".
---

# Clean My Website

Run a pass over the UI in question against these 20 rules. Read the actual markup and styles first; fix in code, not in commentary. Respect the project's existing design system and brand where it has one.

## Workflow

1. Identify the target (page, component, or diff). Read its code and, if a dev server/preview exists, look at it rendered (desktop and mobile).
2. Walk the checklist below in order. For each rule note: pass / fixed / not applicable.
3. Make the fixes. Keep diffs focused; do not redesign what already passes.
4. Verify visually after changes (screenshot), then report a short table of what changed.

## The 20 rules

**Remove noise**
1. **Delete filler badges.** "New", "Beta", "✨ AI-powered", pill labels above every headline — remove unless they carry real, current information.
2. **Drop redundant labels.** No "Email" label plus "Enter your email" placeholder plus an envelope icon. One clear label. No section eyebrow that repeats the heading.
3. **Unitalicize random words.** Italic/serif-italic accents on a single word in a headline are a tell. Use italics only for real emphasis or titles.
4. **Mono only where needed.** Monospace is for code, IDs, keys, numbers that must align. Not for eyebrows, buttons or decoration.
13. **Remove embellishments.** Gradient blobs, glows, grain, sparkles, decorative borders, emoji bullets, drop shadows on everything — cut what doesn't explain or guide.

**Structure and hierarchy**
5. **Use a design system.** Spacing, type, colour, radius and shadow come from tokens/scale (e.g. 4/8px spacing, a fixed type scale). No one-off magic values.
6. **Show the actual product.** Real screenshots, real UI, real data beat abstract illustrations and stock imagery.
7. **Enlarge the main feature.** One thing is primary per view; make it clearly bigger/stronger than secondary items instead of equal-weight grids.
8. **Group with spacing.** Related items closer, unrelated further apart (proximity). Prefer whitespace over dividers and boxes.
9. **Make headlines specific.** Replace "Supercharge your workflow" with what it does for whom. Concrete nouns and verbs, numbers when true.
10. **Emphasize the CTA.** One primary action per view, highest contrast, clear verb label. Secondary actions visually quieter.
11. **Add an accent colour.** A neutral base plus one accent (the brand colour) used sparingly for actions, focus and key highlights — not everywhere.

**Craft details**
12. **Keep icons consistent.** One icon set, one stroke width, one size scale, aligned to text baseline/cap height.
14. **Inner radius = outer − padding.** Nested rounded elements: `inner = outer - gap`. Never the same radius on both.
15. **Improve text contrast.** Body text ≥ 4.5:1, large text ≥ 3:1 (WCAG AA). Light-grey-on-white secondary text is the usual offender; check dark mode too.
16. **Wrap headlines properly.** `text-wrap: balance` on headings, `text-wrap: pretty` on paragraphs; avoid orphans and lines that break mid-phrase; cap measure ~60–75ch for body.
17. **Align by eye, not pixels.** Optically adjust: play icons nudged right, round shapes slightly larger, icon+text visually centred, punctuation hung where it helps.
18. **Use tabular numbers.** `font-variant-numeric: tabular-nums` for prices, tables, counters, timers, anything that changes or aligns in columns.

**Behaviour**
19. **Add loading states.** Every async action: disabled + pending label/spinner on buttons, skeletons for content that loads, no layout shift, errors shown inline.
20. **Animate useful feedback.** Motion confirms an action or explains a change (press, add-to-cart, success, state transition). 150–300ms, ease-out, honour `prefers-reduced-motion`. No decorative looping animation.

## Report format

| # | Rule | Result | Change |
|---|------|--------|--------|
| 1 | Filler badges | fixed | Removed "New" pill on hero |

End with anything left undone and why.
