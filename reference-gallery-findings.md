# Reference Gallery Findings

Source reviewed: `view-source:https://shotoniphone.lorenzobocchi.com/`
Live page reviewed: `https://shotoniphone.lorenzobocchi.com/`

The reference is a Next.js site titled “Shot on iPhone in Black & White.” Its source exposes a large image-driven gallery with many optimized Next image URLs, a small centered cluster of portrait-oriented image tiles in the initial viewport, and a dark near-black presentation. The source references Geist and Geist Mono webfonts and multiple Next static CSS/JS chunks. The live viewport shows a minimal black canvas with a compact centered run of portrait photo cards, plus small navigation/debug-like controls near the upper-right and lower-right edges.

The useful replication target for the birthday site is the reference’s restrained portrait-card presentation, tight consistent card spacing, small-card visual rhythm, and smooth image-strip movement. The reference-specific black theme, controls, branding, and unrelated page content are not to be copied into the birthday page.

## Flow View Observation

The live Flow view places tall portrait frames in a single horizontal row across a black canvas. At the 896×895 browser viewport, five portrait images are visible across the middle with tight, nearly uniform gaps; cards are tall and narrow, with no visible matte or caption treatment. The interface uses a very restrained chrome: small top-left brand text, small top-right Flow/Grid/Map controls, and tiny bottom-left controls. For the birthday page, only the portrait-card row, tight spacing, and smooth horizontal flow should be replicated; the black canvas and controls should not replace the existing birthday styling.

## Motion Model Observation

Live DOM inspection shows the reference intentionally locks page overflow (`html` and `body` are hidden) and uses a full-viewport wrapper. The gallery is a `.photo-strip` transformed as a single large strip; it is scaled by `matrix(1.25, 0, 0, 1.25, 0, 0)` in the inspected state. Individual `.photo-strip-item` elements are 304×405 CSS pixels at the inspected viewport, with a 20px horizontal gap (x positions differ by 324px), and the strip is centered vertically. The first visible row is a continuous horizontal sequence of portrait cards, not a native horizontal scrollbar. This supports implementing a fixed/section-level viewport with a translated horizontal track driven by vertical progress and eased interpolation, while keeping the birthday site’s existing visual styling unchanged.
