<reference name="apple-hig-sf-symbols" domain="icon">

<!-- TOC: design_grid, nine_weights, three_scales, rendering_modes, optical_weight, encapsulation, text_alignment, variable_color, custom_symbol_design -->

<section name="design_grid">

SF Symbols use a typographic grid anchored to SF Pro's cap height. All symbols align to text metrics, not arbitrary pixel grids.

**Template Canvas:** 3300 x 2200 points containing 27 variations (9 weights x 3 scales).

**Key Vertical Guides (Regular-Medium anchor):**
- Capline-M: y = 1055.54pt
- Baseline-M: y = 1126pt
- Cap height span: ~70.46pt between capline and baseline

**Horizontal Margins:**
- Left/right margins are symbol-specific and adjustable (define optical width)
- Top/bottom guides are fixed — never move them
- Negative side margins are supported for badges/enclosures that extend beyond the cap-height column

**Key Lines (bounding templates):**

| Shape | Purpose | When to Use |
|-------|---------|-------------|
| Circle | Round symbols, status indicators | Symbols with equal width/height, badges |
| Square | Grid-aligned, app-icon-like | Dashboard tiles, grid layouts |
| Horizontal rectangle | Wide symbols | Landscape-biased actions (e.g., slider, progress) |
| Vertical rectangle | Tall symbols | Portrait-biased content (e.g., document, phone) |

Symbols fill the appropriate key line shape. Circular symbols touch all four edges of the circle key line. Rectangular symbols fill the taller or wider axis and optically center the other — matching the principle in the standard grid system.

</section>

<section name="nine_weights">

Nine weights map 1:1 to SF Pro text weights. When a symbol sits next to text of a given weight, the matching symbol weight produces visually consistent stroke density.

| Weight | Stroke Character | SF Pro Equivalent |
|--------|-----------------|-------------------|
| Ultralight | Hairline, minimal presence | SF Pro Ultralight |
| Thin | Delicate, refined | SF Pro Thin |
| Light | Gentle, approachable | SF Pro Light |
| Regular | Default balance | SF Pro Regular |
| Medium | Slightly assertive | SF Pro Medium |
| Semibold | Confident, clear | SF Pro Semibold |
| Bold | Strong emphasis | SF Pro Bold |
| Heavy | High impact | SF Pro Heavy |
| Black | Maximum weight | SF Pro Black |

**Weight Axis Behavior:**
- Ultralight → Medium: near-linear stroke growth
- Medium → Black: sub-linear growth on certain strokes to prevent counter spaces (enclosed negative areas) from collapsing at heavier weights
- This non-linearity is a deliberate optical correction, not a limitation

**For custom icons:** Match the stroke thickness of an analogous system symbol at the target weight. At Regular-Medium, the reference stroke width is approximately **7 points** in the template coordinate space.

</section>

<section name="three_scales">

Three scales control the symbol's glyph size within a fixed point size. The point size stays the same — the glyph grows or shrinks.

| Scale | Relative Size | Stroke Adjustment | Usage |
|-------|--------------|-------------------|-------|
| Small | ~20% smaller than Medium | Slightly thinner strokes | Dense UIs, supplementary info, inline annotations |
| Medium | Default (baseline) | Standard strokes | Toolbars, navigation bars, lists, labels |
| Large | ~30% larger than Medium | Slightly thicker strokes | Primary actions, prominent labels, hero placements |

**Scale Multipliers (from Regular baseline):**
- Large: multiply by **1.29x**
- Small: multiply by **0.79x**

**Optical centering:** All three scales are vertically centered to SF Pro's cap height, not the mathematical midpoint of the em square.

</section>

<section name="rendering_modes">

Four rendering modes control how color is applied across symbol layers. Each symbol path belongs to a layer (primary, secondary, tertiary).

**Monochrome:**
- All layers render in a single color at 100% opacity
- No layer differentiation — entire symbol is one shape
- Use when: high contrast required, abstract controls, colored backgrounds where layered opacity degrades legibility

**Hierarchical:**
- Single base color across all layers with opacity differentiation:
  - Primary: 100% opacity
  - Secondary: ~50% opacity
  - Tertiary: ~30% opacity
- Creates depth and foreground/background distinction
- Use when: conveying layered objects, camera filters, translucent interfaces

**Palette:**
- Up to 3 independent colors assigned to primary, secondary, tertiary layers
- Surplus layers inherit the last specified color
- Use when: full color control needed (map pins, category icons, status indicators with distinct semantic colors)

**Multicolor:**
- Colors baked into the symbol design — cannot be overridden
- Fixed colors that do not adapt to light/dark mode automatically
- Use when: representing real-world objects with recognized color (fire = orange/red, sun = yellow, leaf = green)

**Layer Draw Modes:**

| Mode | Behavior |
|------|----------|
| Draw | Renders path normally (additive) |
| Erase | Cuts through layers below, creating transparent holes |
| Behind | Renders below the layer stack (backgrounds in multicolor) |

**Automatic Mode (iOS 16+):** Each symbol declares a preferred rendering mode. The `.automatic` setting renders in the symbol's preferred mode. Always verify the result in context.

</section>

<section name="optical_weight">

Visual consistency across a symbol set requires optical corrections, not mathematical uniformity.

**Stroke Non-Linearity:**
- Horizontal strokes are typically thinner than vertical strokes at the same weight (matching SF Pro's contrast)
- Counter spaces must remain legible at the smallest intended rendering size
- Fill variants carry more visual mass than outline variants

**Visual Mass Balancing:**
- Optically heavier symbols (more filled area) may need slight size reduction
- Optically lighter symbols (sparse strokes) may need slight size increase
- A filled circle reads as heavier than a stroked circle at identical dimensions

**Cap Height Centering:**
- All symbols are optically centered to cap height, not the em square midpoint
- The visual centroid aligns with the vertical center of an uppercase letter
- Symbols with descending elements (e.g., arrow.down) center on the cap zone, not total height

**Consistent Level of Detail:**
- Do not introduce fine details that disappear at small sizes
- System symbols are flat, front-facing, with a consistent light source (slightly top-left for fills)
- Match the level of reduction/abstraction used by adjacent system symbols

</section>

<section name="encapsulation">

Symbols come in bare and enclosed variants. The choice affects visual weight, tap targets, and context suitability.

**Bare Symbols** (e.g., `house`, `star`, `bell`):
- No bounding shape — the symbol itself defines the silhouette
- Align optically with adjacent text
- Appropriate for: toolbars, navigation bars, lists, inline content

**Enclosed Symbols** (e.g., `house.circle`, `star.square`):
- Symbol sits inside a geometric container
- Container provides consistent visual anchor and tap target
- Improves legibility at very small sizes

| Container | Usage |
|-----------|-------|
| Circle (`.circle`, `.circle.fill`) | Floating action buttons, selection indicators, avatar-like contexts |
| Square (`.square`, `.square.fill`) | Grid layouts, app-icon-like contexts |
| Rectangle (`.rectangle`, `.rectangle.fill`) | Wide buttons, landscape layouts |
| Badge (`.badge.{x}`) | Notifications, counts, status overlays |

**Fill vs. Outline by Context:**

| Context | Preferred Variant |
|---------|------------------|
| iOS Tab Bar | Fill (system-enforced) |
| iPad Sidebar | Outline |
| Navigation Bar | Outline |
| Toolbar | Outline |
| Swipe Actions | Fill |
| Selected state indicators | Fill |

</section>

<section name="text_alignment">

Symbols are typographic glyphs. They sit on text baselines and size relative to point size.

**Baseline Behavior:**
- Symbols share the same baseline as adjacent text by default
- Typographic metadata in the symbol defines baseline position
- Visual content doesn't necessarily touch the baseline — it's optically balanced

**Point Size Matching:**
- A symbol at N points next to text at N points matches in visual weight
- This works because the weight axis maps to SF Pro stroke density
- A Regular-weight symbol at 17pt has the same stroke mass as SF Pro Regular at 17pt

**Centering:**
- Uses cap height for vertical centering, not bounding box
- Important for symbols with descending elements — center on cap zone, not total height

</section>

<section name="variable_color">

Variable Color allows layers to convey progressive fill for status, progress, or strength indicators.

**Mechanism:**
- Float value from 0.0 to 1.0 controls progressive layer activation
- Layers activate sequentially in z-order (back to front) as value increases
- Non-annotated layers remain fully visible at all times

**Threshold Calculation (N layers):**
Thresholds are evenly spaced, activation requires crossing one percentage point above the rounded threshold.

Example (4 layers — signal bars):
- Layer 1: activates at > 0%
- Layer 2: activates at >= 26%
- Layer 3: activates at >= 51%
- Layer 4: activates at >= 76%

**Works in all four rendering modes.** In hierarchical mode, opacity levels and variable fill apply simultaneously.

**For custom icons:** Design with variable color in mind when the icon represents a value on a spectrum (signal strength, battery level, volume, progress).

</section>

<section name="custom_symbol_design">

Key principles for designing custom symbols that match Apple's SF Symbols set.

**Template Requirements:**
- Variable template: 3 master variations (Ultralight-S, Regular-S, Black-S) — system interpolates the rest
- All master paths must have: same number of anchor points, same path direction, same starting point, matching path correspondence

**Stroke Rules:**
- Round cap and round join on all strokes (matches system symbols)
- Convert all strokes to outlines before export — symbols are defined by filled paths, not stroked paths
- Reference stroke: ~7pt wide at Regular-M, ~6pt at Light-M

**Corner Radius:**
- No universal fixed radius — match the closest analogous system symbol
- Rounded rectangles typically use radius ≈ 1/4 of the shorter dimension
- Consistent with iOS rounded-rectangle language

**Optical Consistency Checklist:**
1. Level of detail matches adjacent system symbols
2. Optical weight feels equally "heavy" at the same weight/scale
3. Alignment maintains consistent position relative to cap height
4. Perspective is flat, front-facing, consistent top-left light source for fills
5. Counter spaces remain legible at smallest intended rendering size

**Rendering Mode Support:**
- Annotate paths with layers (primary, secondary, tertiary) for hierarchical/palette support
- Use Erase draw mode for paths that punch through filled enclosures
- Layer structure applies across all rendering modes simultaneously

**Margin Adjustment:**
- Move left/right margin guides to match optical width
- Never move top/bottom guides
- Use negative side margins for badges/enclosures extending beyond cap-height column

</section>

</reference>
