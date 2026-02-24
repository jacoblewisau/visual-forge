<reference name="svg_generation" domain="shared">

<!-- TOC
  - size_specific_rules
  - path_optimization_rules
  - critique_checklist
  - species_simplification_cascade
  - common_mistakes_to_avoid
-->

<section name="size_specific_rules">

SVG mascots exist at three size tiers. Each has strict constraints on complexity, color count, and shape budget.

<subsection name="favicon_32px_display">

```
viewBox="0 0 32 32"
```

- **Shape budget:** 5-8 shapes maximum
- **Color budget:** 2-3 colors (primary + accent, optional outline)
- **Goal:** Instantly recognizable silhouette at 16px rendered size
- **Content:** Head only, maximum simplification — the ESSENCE of the creature
- **Lines:** No fine detail lines. Shapes only. Everything must read as a filled region.
- **Eyes:** Single shape per eye (circle or ellipse). No pupil detail at this size.
- **Test:** Blur it at 50%. Is it still recognizable? If no, simplify further.

</subsection>

<subsection name="head_portrait_128px_display">

```
viewBox="0 0 128 128"
```

- **Shape budget:** 8-15 shapes
- **Color budget:** 3-5 colors (full palette minus body colors)
- **Goal:** Personality and expression visible. The mascot's "profile picture."
- **Content:** Head + neck/upper body. Room for expression details.
- **Eyes:** Pupil detail allowed. Eye shape conveys the current expression.
- **Features:** Species-distinctive features visible (whiskers, horns, antennae, etc.)
- **Line weight:** 2-3px for outlines if using stroked paths. Prefer filled shapes.

</subsection>

<subsection name="full_body_256px_display">

```
viewBox="0 0 256 256"
```

- **Shape budget:** 20-40 shapes
- **Color budget:** 4-7 colors (full palette)
- **Goal:** Complete character with pose, personality, and distinctive traits.
- **Content:** Full body in a characteristic pose. The mascot's "hero shot."
- **Details:** Paws, tail, markings, accessories all visible.
- **Pose:** Should convey the default personality (curious lean, calm sit, alert stance).
- **Negative space:** Leave breathing room. Don't fill the entire viewBox — 10-15% margin.

</subsection>

</section>

<section name="path_optimization_rules">

<subsection name="general">

- Use `<circle>`, `<ellipse>`, `<rect>` for geometric shapes — don't path-trace a circle
- Use `<path>` only for organic/curved shapes that need custom Bezier control
- Minimize path points: each curve should use the fewest control points possible
- Use relative commands (`m`, `l`, `c`, `s`) for shorter path data
- Close paths with `Z` — don't repeat the starting coordinate
- Round coordinates to 1 decimal place maximum (no `14.283746`)

</subsection>

<subsection name="viewbox_convention">

- Always set explicit `viewBox` — never rely on width/height alone
- No `xmlns` needed when SVG is inline in HTML (add it for standalone files)
- Set `role="img"` and `aria-label="[Mascot name] mascot"` for accessibility

</subsection>

<subsection name="color_application">

**Palette source:** Species-specific color palettes (hex values, dark mode adjustments, bioluminescence/iridescence effects) are defined in `visual-language.md`. SVG generation agents should read both this file AND visual-language.md to ensure color accuracy.

- Use CSS custom properties for colors when possible: `fill="var(--mascot-primary)"`
- Fallback: inline `fill` attributes with hex values
- Dark mode: provide a sibling SVG or CSS overrides, not runtime color switching
- No gradients at favicon size. Subtle gradients OK at 128px+. Full gradients at 256px.

</subsection>

</section>

<section name="critique_checklist">

The critic agent scores each SVG on these criteria, 1-10 per criterion:

| # | Criterion | What a 10 Looks Like | Common Failures |
|---|-----------|---------------------|----------------|
| 1 | **Silhouette Test** | Species identifiable from silhouette alone | Blobby, generic shape; no distinctive features in outline |
| 2 | **Expression Clarity** | Emotion readable at intended display size | Eyes too small, expression lost at size, ambiguous mood |
| 3 | **Color Harmony** | Palette matches spec, works on light and dark bg | Colors from spec ignored, poor contrast, muddy palette |
| 4 | **Shape Economy** | Within shape budget, no unnecessary complexity | Over-detailed for size tier, redundant shapes |
| 5 | **Species Accuracy** | Key anatomical features present and correct | Wrong proportions, missing species-defining traits |
| 6 | **Personality Match** | Visual conveys the mascot's personality traits | Generic cute animal, no personality-specific features |
| 7 | **Technical Quality** | Clean paths, proper viewBox, accessible markup | Unoptimized paths, missing viewBox, no aria-label |
| 8 | **Size Appropriateness** | Detail level matches the size tier constraints | Favicon too complex, full body too sparse |

**Passing score:** Average ≥ 8/10 across all 8 criteria.

**Critique format:**
```
SCORE: [criterion]: [N]/10 — [specific observation]
ISSUES: [numbered list of specific things to fix]
STRENGTHS: [what works well — preserve these in refinement]
```

</section>

<section name="species_simplification_cascade">

How to reduce each species to its essential shapes at small sizes. This guides favicon and head-portrait design.

<subsection name="original_12_species">

| Species | Favicon Essence (5 shapes) | Key Distinguishing Shape |
|---------|---------------------------|------------------------|
| Cat | Pointed ears + round head + eye slits | Triangular ear silhouette |
| Dog | Floppy/pointed ears + round snout + tongue | Snout protrusion from head circle |
| Owl | Round head + large round eyes + ear tufts | Concentric circles (head + eyes) |
| Fox | Pointed ears + narrow snout + bushy tail hint | Narrow snout angle + large ears |
| Bear | Round ears + round head + small nose | Circular ear bumps on top of head |
| Rabbit | Long ears + round body + small nose | Tall vertical ear shapes |
| Penguin | Oval body + white chest + small beak | Tuxedo two-tone pattern |
| Octopus | Round head + 2-3 tentacle curves | Tentacle curves below dome head |
| Bee | Round body + stripes + wings | Stripe pattern + wing shapes |
| Hedgehog | Spiky back dome + small face | Zigzag or spike silhouette on top |
| Axolotl | Round head + gill frills + smile | External gill branch shapes |
| Capybara | Rectangular head + small ears + calm expression | Flat-topped head shape |

</subsection>

<subsection name="new_scientific_lab_species">

| Species | Favicon Essence | Key Distinguishing Shape |
|---------|----------------|------------------------|
| Tardigrade | Barrel body + 2 stub legs visible + round head | Barrel/pill body shape |
| Mantis Shrimp | Eye stalks + curved body + claw hint | Bulbous eye stalks |
| Cuttlefish | W-shaped pupil + mantle dome + 2 tentacles | W-pupil eye shape |
| Salamander | Long body + visible spots + flat head | Spotted pattern + flat silhouette |
| Lab Mouse | Large round ears + pointed nose + whiskers | Oversized circular ears |
| Narwhal | Rounded body + dorsal ridge + tusk line | Forward-pointing tusk line |

</subsection>

<subsection name="new_precision_technical_species">

| Species | Favicon Essence | Key Distinguishing Shape |
|---------|----------------|------------------------|
| Hawk | Sharp beak + fierce eye + crest/brow | Hooked beak + angular brow |
| Spider | Round body + 4 visible legs (suggest 8) + eye cluster | Multiple small eye dots |
| Crane | Long neck curve + pointed beak + red crown dot | S-curve neck + red spot |
| Ant | Segmented body (3 parts) + antennae | Three-circle body chain |
| Gecko | Flat head + splayed toes + spotted body | Splayed toe pads |
| Praying Mantis | Triangular head + folded forelegs + long body | Triangular head + folded arm shapes |

</subsection>

<subsection name="new_creative_unconventional_species">

| Species | Favicon Essence | Key Distinguishing Shape |
|---------|----------------|------------------------|
| Luna Moth | Wings spread + eye spots + feathered antennae | Wing eye-spot circles |
| Chameleon | Curled tail + domed head + spiral eye | Curled tail spiral |
| Jellyfish | Dome bell + 2-3 trailing tendrils | Dome + dangling lines |
| Seahorse | Curved S-body + snout + curled tail | S-curve body profile |
| Pangolin | Overlapping scale pattern + curved body + small head | Diamond scale pattern |
| Firefly | Oval body + wing covers + glowing abdomen circle | Glowing abdomen dot |
| Sloth | Round body + long arms + dot eyes + smile | Curved long-arm silhouette |
| Kiwi (bird) | Round fuzzy body + long beak + tiny legs | Long beak on round body |
| Snail | Spiral shell + soft body + eye stalks | Spiral shell shape |

</subsection>

<subsection name="new_utility_work_species">

| Species | Favicon Essence | Key Distinguishing Shape |
|---------|----------------|------------------------|
| Elephant | Large ear + trunk curve + tusk hint | Fan-shaped ear + trunk |
| Crow/Raven | Sharp beak + sleek head + glossy eye | Angular beak profile |
| Otter | Round head + whiskers + visible paws | Whisker dots + round face |
| Dolphin | Curved body + dorsal fin + beak snout | Dorsal fin + arced body |
| Hamster | Round body + small round ears + cheek pouches | Puffy cheek bulges |

</subsection>

</section>

<section name="icon_size_tiers">

Icon SVGs have different constraints from mascot SVGs. Icons prioritize clarity and grid alignment over personality.

| Tier | viewBox | Shapes | Colors | Stroke | Use |
|------|---------|--------|--------|--------|-----|
| Micro | 0 0 16 16 | 2-4 | 1-2 | 1-1.5px | Inline, status |
| Compact | 0 0 20 20 | 3-6 | 1-2 | 1.5px | Toolbars, dense UI |
| Standard | 0 0 24 24 | 4-8 | 1-3 | 2px | Primary UI icons |
| Emphasis | 0 0 32 32 | 6-12 | 2-4 | 2-2.5px | Feature icons, empty states |

**Icon-Specific Rules:**
- Grid padding: 2px all sides (3px at 32px)
- Stroke weight must be uniform across the icon set
- Round end caps and round joins for friendly sets; square caps and miter joins for precise sets
- No gradients at 16-24px. Subtle gradients OK at 32px
- `role="img"` and `aria-label` on every icon SVG

</section>

<section name="button_illustration_tiers">

Button illustration SVGs are embedded within button components. They must work alongside labels and within button containers.

| Tier | viewBox | Shapes | Colors | Use |
|------|---------|--------|--------|-----|
| Accent | 0 0 16 16 | 3-5 | 1-2 | Small decorative element beside label |
| Companion | 0 0 24 24 | 5-10 | 2-3 | Character element alongside label |
| Hero | 0 0 32 48 | 10-20 | 3-5 | Featured illustration, label integrated |

**Button-Specific Rules:**
- Illustration is decorative: `aria-hidden="true"` on the SVG
- Must work on the button's background color (not just white/dark)
- State variants (hover, pressed, disabled) may need separate SVGs or CSS transforms
- Animation-ready: shapes should support CSS transform transitions
- Total illustration asset budget per button: under 5KB

</section>

<section name="common_mistakes_to_avoid">

1. **Too many path points.** If a curve has more than 4 control points, simplify. Mascots are stylized, not photorealistic.

2. **Centered bullseye composition.** Don't dead-center everything. Slight asymmetry (tilted head, off-center pose) adds life.

3. **Outline-only at small sizes.** Favicons need filled shapes, not outlines. Strokes collapse at 16px.

4. **Ignoring the viewBox padding.** Don't push shapes to the viewBox edge. Leave 5-10% margin on all sides.

5. **Generic "cute animal" syndrome.** If you could swap the species and nobody would notice, the design lacks species-specific personality. Every SVG must have at least ONE shape that only this species has.

6. **Gradient abuse at small sizes.** Gradients at 32px become muddy bands. Use flat fills at favicon tier.

7. **Forgetting dark mode.** Test every SVG on both `#FFFFFF` and `#1A1A1A` backgrounds. Add outline/shadow if needed for dark bg visibility.

8. **Too many colors for the tier.** Stick to the budget. Fewer colors = more iconic. The favicon should work in 2 colors.

</section>

</reference>
