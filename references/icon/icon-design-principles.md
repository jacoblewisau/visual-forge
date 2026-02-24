<reference name="icon-design-principles" domain="icon">

<!-- TOC: grid_system, stroke_conventions, optical_corrections, metaphor_methodology, clarity_hierarchy, apple_hig_alignment, lucide_alternative, size_tiers, common_mistakes -->

<section name="grid_system">

Every icon lives on a grid. The grid ensures visual consistency across an icon set — alignment, proportions, and whitespace are uniform even when the content varies.

**Standard Grids:**

| Grid Size | Use Case | Content Area | Padding |
|-----------|----------|-------------|---------|
| 16px | Inline text icons, favicons | 12x12px | 2px all sides |
| 20px | Compact UI, tool palettes | 16x16px | 2px all sides |
| 24px | Standard UI icons (most common) | 20x20px | 2px all sides |
| 32px | Emphasized icons, touch targets | 26x26px | 3px all sides |

**Grid Rules:**
- Content stays within the content area — padding is sacred whitespace
- Anchor shapes to grid lines — circles centered, rectangles aligned to edges
- Diagonal lines land on grid intersections where possible
- Circular icons use the full content area height and width
- Rectangular icons fill the taller or wider axis and optically center the other
- Key lines (circle, square, landscape rect, portrait rect) define the bounding shapes

</section>

<section name="stroke_conventions">

Stroke weight is the single most important consistency factor in an icon set. Inconsistent stroke weight makes icons look like they come from different families.

**Stroke Weight by Grid:**

| Grid Size | Stroke Weight | Corner Radius | End Caps |
|-----------|--------------|---------------|----------|
| 16px | 1px or 1.5px | 0-1px | Square or round |
| 20px | 1.5px | 1px | Round |
| 24px | 2px (standard) | 1-2px | Round |
| 32px | 2px or 2.5px | 2px | Round |

**Consistency Rules:**
- ONE stroke weight per icon set — never mix 1.5px and 2px in the same set
- Interior detail strokes may be 0.5px thinner than primary strokes
- Corner radius must be consistent across the entire set
- End caps (round vs. square) must be consistent — round for friendly, square for precise
- Joins: round joins for organic, miter joins for geometric (pick one per set)
- Gaps in strokes should be consistent width (usually 2px at 24px grid)

</section>

<section name="optical_corrections">

Mathematically correct geometry often looks visually wrong. Optical corrections make icons feel right.

**Common Corrections:**

| Issue | Correction |
|-------|-----------|
| Circle looks smaller than square at same dimensions | Scale circle to ~103-105% of square |
| Horizontal lines look thicker than vertical | Thin horizontal strokes by ~0.5px or use optical balancing |
| Triangle pointing right looks off-center | Shift ~1-2px right of mathematical center |
| Play button (triangle) inside circle looks misaligned | Shift triangle ~1px right of circle center |
| Dense icons look heavier than sparse ones | Reduce stroke weight by 0.25px or increase whitespace |
| Rounded corners on small features disappear | Use sharper corners on elements smaller than 4px |

**Testing:** Always verify icons at actual display size, not zoomed. What looks perfect at 400% may be illegible at 24px.

</section>

<section name="metaphor_methodology">

Icon metaphors must be instantly recognizable. The best icons use universal visual metaphors that transcend culture and context.

**Metaphor Selection Process:**
1. Define the concept in one word (e.g., "search", "settings", "home")
2. List 3-5 visual metaphors for that concept (magnifying glass, binoculars, radar, spotlight, eye)
3. Pick the most universal — what would the widest audience recognize instantly?
4. Check for conflicts — does this metaphor mean something else in your icon set?
5. Simplify to the essential shape — remove everything that isn't the metaphor

**Metaphor Categories:**

| Type | Examples | Strength |
|------|---------|----------|
| Object literal | Magnifying glass = search, Trash can = delete | Strongest — instant recognition |
| Action representation | Arrow = direction, Plus = add | Strong — learned convention |
| Container metaphor | Folder = group, Box = package | Good — spatial reasoning |
| Abstract symbol | Circle = record, Square = stop | Requires learning but compact |
| Domain-specific | Beaker = lab, Microscope = research | Only works for target audience |

**Scientific/Lab Metaphors (domain-specific):**
- Beaker/flask = experiment, sample
- Microscope = inspection, detail
- DNA helix = genetics, structure
- Atom = molecular, composition
- Petri dish = culture, growth
- Pipette = transfer, precision
- Crystal structure = organization, formation
- Temperature = conditions, environment

</section>

<section name="clarity_hierarchy">

At small sizes, every pixel counts. Icons must communicate through a strict clarity hierarchy.

**The 3-Second Rule:** A user should identify the icon's meaning within 3 seconds at display size without any label. If they can't, the icon fails.

**Clarity Stack (most to least important):**
1. **Silhouette** — The outer shape tells the story. If the silhouette reads, the icon works.
2. **Primary feature** — ONE internal detail that disambiguates (the lens in a magnifying glass, the roof peak on a house)
3. **Secondary features** — Supporting details that refine but aren't essential
4. **Decorative details** — Remove these first when simplifying

**Size-Adaptive Clarity:**
- At 32px: all 4 levels visible
- At 24px: levels 1-3 visible, level 4 removed
- At 20px: levels 1-2 visible, level 3 simplified
- At 16px: level 1 only — pure silhouette with maybe one internal feature

</section>

<section name="apple_hig_alignment">

Apple's Human Interface Guidelines and SF Symbols represent the gold standard for icon design in native app contexts. When designing icons, SF Symbols conventions are the primary baseline.

**Core SF Symbols Principles:**
- Typographic grid anchored to SF Pro cap height — icons align to text metrics, not arbitrary pixel grids
- Round cap and round join on all strokes (system-wide convention)
- 9 weights (ultralight → black) mapping 1:1 to SF Pro text weights
- 3 scales (small/medium/large) controlling glyph size within fixed point size
- 4 rendering modes: monochrome, hierarchical, palette, multicolor (layer-based)
- Stroke-to-outline conversion — symbols are defined by filled paths, not stroked paths
- Optical weight over mathematical uniformity — horizontal strokes thinner than vertical

**Key Lines (bounding templates):**
- Circle, square, horizontal rectangle, vertical rectangle
- Symbols fill the appropriate key line shape
- Circular symbols touch all four edges; rectangular symbols fill the dominant axis and optically center the other

**Fill vs. Outline Context Rules:**
- Tab bars: fill variant (system-enforced)
- Toolbars, navigation bars, sidebars: outline variant
- Selected states: fill; unselected: outline
- Swipe actions: fill

**Rendering Mode Selection:**
- Monochrome: high contrast, abstract controls, colored backgrounds
- Hierarchical: depth/layering (primary 100%, secondary ~50%, tertiary ~30%)
- Palette: distinct semantic colors per layer (up to 3)
- Multicolor: real-world objects with recognized color associations

**For detailed SF Symbols grid, weights, scales, and custom design rules, see `apple-hig-sf-symbols.md`.**

</section>

<section name="lucide_alternative">

Lucide is an alternative baseline for open-source and cross-platform projects where SF Symbols conventions don't apply (web apps, Electron, Android).

**Lucide Conventions:**
- 24px grid with 2px stroke weight
- Round end caps and round joins
- 1px corner radius on internal corners, 2px on outer shapes
- Consistent 2px gap for broken strokes
- Minimal fills — stroke-based design language
- No shadows, no gradients, no dimension

**When to Use Lucide Instead of Apple HIG:**
- Cross-platform web applications
- Open-source projects needing freely available icon sets
- Projects already using Lucide/Feather icons throughout
- Android or Linux-targeted applications

</section>

<section name="size_tiers">

Icons exist at specific size tiers, each with constraints on complexity.

| Tier | Grid | Shapes | Colors | Use Case |
|------|------|--------|--------|----------|
| Micro | 16px | 2-4 | 1-2 | Inline, status indicators |
| Compact | 20px | 3-6 | 1-2 | Toolbars, dense UI |
| Standard | 24px | 4-8 | 1-3 | Primary UI icons |
| Emphasis | 32px | 6-12 | 2-4 | Feature icons, empty states |

**Critique Checklist (adapted from mascot SVG critique):**

| Criterion | What a 10 Looks Like |
|-----------|---------------------|
| Metaphor clarity | Concept identifiable without label in 3 seconds |
| Grid alignment | All anchors on grid, consistent padding |
| Stroke consistency | Weight uniform, caps consistent, joins consistent |
| Optical balance | Visually centered, no heavy/light spots |
| Set cohesion | Matches siblings in weight, style, complexity |
| Size appropriateness | Detail level matches the tier constraints |

</section>

<section name="common_mistakes">

1. **Inconsistent stroke weight** — Mixing 1.5px and 2px in the same set destroys visual cohesion.
2. **Too much detail at small sizes** — 24px icons don't need interior texture or shading.
3. **Centered mathematically, not optically** — Play buttons, arrows, and asymmetric shapes need manual adjustment.
4. **Metaphor collision** — Two icons in the same set using similar silhouettes for different concepts.
5. **Ignoring the grid** — Freehand placement leads to icons that look misaligned even when technically correct.
6. **Fill vs. stroke inconsistency** — Mixing filled and outlined icons in the same set without clear purpose.
7. **Color as the only differentiator** — Icons must work in monochrome. Color is enhancement, not identity.
8. **Ignoring dark mode** — Light-stroke icons on dark backgrounds need weight or brightness adjustments.

</section>

</reference>
