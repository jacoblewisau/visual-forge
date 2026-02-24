<reference name="visual_language" domain="shared">

<!-- TOC
  - illustration_style_spectrum
  - color_relationship_rules
  - expression_library
  - anatomy_rules
  - integration_points
  - typography_pairing
  - deliverable_format
-->

<section name="illustration_style_spectrum">

Based on Chris Raroque's visual DNA and collaborations (particularly Cecilia Kim's Luna work):

<subsection name="the_sweet_spot_playful_professional">

- Clean vector illustration with personality
- Geometric foundations with organic details
- Flat or subtle gradients (no heavy 3D rendering)
- Confident line weight (consistent, not sketchy)
- Would look at home on an Apple product page or Stripe landing page

</subsection>

<subsection name="style_parameters">

**Line weight:** Medium-consistent. Not hairline (too technical), not thick (too childish).
**Corners:** Rounded but not bubbly. Think 8px radius, not 20px.
**Proportions:** Slightly exaggerated features (larger eyes, rounder body) but anatomically readable.
**Color fills:** Solid or subtle gradient. No heavy textures or patterns.
**Detail level:** Enough to recognize the species, not enough to count individual feathers/hairs.

</subsection>

</section>

<section name="color_relationship_rules">

<subsection name="per_product_palette">

Each mascot gets its own color world. The palette should:
1. Have ONE dominant accent color tied to the mascot/creature
2. Include 2-3 supporting colors for depth
3. Work in both light and dark mode
4. Not clash with the app's existing UI palette — the mascot colors should COMPLEMENT

</subsection>

<subsection name="color_to_creature_guidelines">

| Creature Archetype | Natural Palette | Suggested Accent |
|-------------------|-----------------|------------------|
| Warm animals (cat, dog, fox) | Amber, orange, warm brown | Orange or warm yellow |
| Cool animals (penguin, owl, fish) | Blue, teal, silver | Cool blue or teal |
| Nature animals (rabbit, bear, deer) | Green, earth brown, cream | Sage green or warm brown |
| Exotic (axolotl, octopus, chameleon) | Pink, purple, coral | Vibrant pink or purple |
| Insects (bee, firefly, butterfly) | Gold, amber, green | Gold or bright amber |
| Neutral (hedgehog, capybara) | Cream, soft gray, muted tones | Warm gray or muted sage |

</subsection>

<subsection name="extended_color_mapping_new_species">

| Creature | Natural Palette | Suggested Accent | Dark Mode Adjustment |
|----------|----------------|------------------|---------------------|
| Tardigrade | Translucent amber, soft pink, microscope blue | Warm amber #F59E0B | Brighten to golden glow, add subtle translucency |
| Mantis Shrimp | Iridescent teal, coral, electric blue | Electric teal #06B6D4 | Saturate accent, keep coral warm |
| Cuttlefish | Deep ocean purple, shifting turquoise, ink brown | Shifting purple #8B5CF6 | Rich purple glow on dark, turquoise highlights |
| Salamander | Mossy green, wet-stone gray, fire-belly orange | Earthy orange #EA580C | Warm orange belly becomes focal point |
| Lab Mouse | Clean white, pink ears/nose, warm gray | Soft pink #F472B6 | Invert to light gray on charcoal, pink stays |
| Hawk | Tawny brown, golden eye, cream breast | Gold #D97706 | Golden eye brightens as anchor point |
| Spider | Charcoal, silver thread, ruby markings | Silver #94A3B8 | Silver threads glow against dark backgrounds |
| Crane | White/light gray, black wingtips, red crown | Crimson spot #DC2626 | White body becomes light silhouette, red crown pops |
| Ant | Dark brown, amber body segments, earth tones | Rich amber #B45309 | Amber segments glow, dark body integrates with bg |
| Luna Moth | Pale mint green, lavender edges, cream body | Soft mint #A7F3D0 | Mint and lavender become luminous on dark |
| Chameleon | Gradient green-to-teal, golden eye, earth feet | Adaptive (mirrors app accent) | Matches app dark mode palette automatically |
| Jellyfish | Translucent blue-pink, bioluminescent core | Bioluminescent pink #F0ABFC | Full glow effect — translucent body, bright core |
| Seahorse | Coral, sandy gold, pale blue spots | Warm coral #FB923C | Coral brightens, gold spots become highlights |
| Pangolin | Warm bronze scales, soft cream belly, dark eyes | Bronze #A16207 | Metallic scale reflection effect on dark bg |
| Elephant | Warm gray, gentle brown eyes, ivory tusk accent | Warm gray #78716C | Subtle warm shift, eyes and tusks become focal |
| Crow/Raven | Iridescent black-purple, sharp silver eye | Iridescent purple #7C3AED | Purple iridescence shimmers on dark backgrounds |
| Otter | Rich brown, cream belly, bright dark eyes | Warm brown #92400E | Eyes brighten, belly provides contrast anchor |
| Dolphin | Blue-gray, silver belly, bright eye | Ocean blue #0284C7 | Silver belly reflects, blue-gray body glows subtly |
| Firefly | Warm black body, golden-green abdomen glow | Bioluminescent gold #FACC15 | Abdomen becomes primary light source, body fades to dark |
| Sloth | Mossy brown-green, cream face, dark eye patches | Mossy green #65A30D | Green moss highlights glow subtly, cream face anchors |
| Gecko | Lime green, spotted pattern, golden eyes | Vivid lime #84CC16 | Spots become luminous dots, eyes anchor on dark bg |
| Narwhal | Arctic blue-gray, cream belly, ivory tusk | Arctic blue #7DD3FC | Tusk becomes silver-white highlight, body shifts cooler |
| Hamster | Golden-orange, cream belly, pink ears/nose | Warm gold #F59E0B | Gold fur brightens, pink ears provide warm contrast |
| Kiwi (bird) | Warm brown, fuzzy texture, dark beak, small eye | Earth brown #78350F | Fuzzy body silhouette, eye becomes bright anchor point |
| Praying Mantis | Leaf green, triangular head, large compound eyes | Sharp green #16A34A | Eyes become focal points, body integrates with dark |
| Snail | Warm amber shell, soft gray body, dark eye stalks | Shell amber #D97706 | Spiral shell glows warm, body provides soft contrast |

</subsection>

<subsection name="bioluminescence_and_iridescence_effects">

Some scientific creatures have special color properties that deserve extra design attention:

**Bioluminescent species** (Jellyfish, Tardigrade, Luna Moth, Firefly):
- In dark mode, these creatures should appear to emit their own light
- Use radial gradients from a bright core to translucent edges
- Subtle CSS `box-shadow` or `filter: drop-shadow()` can simulate glow
- Keep the glow soft — medical instrument display, not neon sign

**Iridescent species** (Mantis Shrimp, Cuttlefish, Crow/Raven):
- Color should appear to shift depending on viewing context
- In practice: use 2-3 gradient stops that suggest color-shifting
- Dark mode amplifies the effect (iridescence is more visible on dark)
- The shifting quality mirrors adaptability — good for theming/customization mascots

**Translucent species** (Tardigrade, Jellyfish):
- Use reduced opacity in body fills (0.7-0.85) with solid outlines
- Internal structures (organs, food) can show through subtly
- In dark mode, this creates a "backlit specimen" effect that feels scientific

</subsection>

<subsection name="dark_mode_mascot_rules">

- Mascot colors should BRIGHTEN slightly in dark mode (not just invert)
- The mascot should feel like a warm presence against dark backgrounds
- Eyes should always be visible and expressive, even at small sizes
- Outline/silhouette must read clearly on both light and dark

</subsection>

</section>

<section name="expression_library">

Every mascot needs a minimum expression set. These are the states the mascot can appear in:

<subsection name="core_expressions_minimum_viable_mascot">

1. **Neutral/Resting** — Default state. Calm, present, approachable. Used on home screens, settings.
2. **Happy/Success** — Celebratory but proportionate. Eyes slightly wider, subtle smile. Used after completions.
3. **Curious/Active** — Engaged, interested. Head tilted, eyes focused. Used during active tasks.
4. **Sympathetic/Error** — Gentle concern, not panic. Used for errors, empty states.

</subsection>

<subsection name="extended_expressions_full_personality">

5. **Sleepy/Idle** — Charming inactivity. Used for long absence, night mode.
6. **Excited/Achievement** — Bigger celebration. Used for milestones, streaks.
7. **Thinking/Loading** — Contemplative. Used during processing, search.
8. **Welcoming** — Open gesture, warm. Used in onboarding, first launch.

</subsection>

<subsection name="expression_rules">

- **Proportional celebration**: Small wins get a subtle smile, big wins get excitement. Never over-celebrate.
- **No negative expressions**: The mascot never looks angry, frustrated, or disappointed. Sympathy yes, blame never.
- **Eyes are everything**: At small sizes (16-32px), only the eyes change. Expressions must read through eyes alone.
- **Consistency across sizes**: The same expression at 16px, 32px, 64px, and 128px should feel like the same emotion.

</subsection>

</section>

<section name="anatomy_rules">

<subsection name="size_categories">

| Context | Size | Detail Level |
|---------|------|-------------|
| App icon | 1024px master, shown at 60-180px | Full detail, recognizable silhouette |
| Onboarding | 200-300px | Full body, full expression |
| Empty state | 120-180px | Full body, contextual expression |
| Card accent | 32-48px | Head/face only |
| Inline icon | 16-24px | Silhouette or simplified head |
| Favicon | 32px (shown 16px) | Maximum simplification, just the essence |

</subsection>

<subsection name="simplification_cascade">

As size decreases, remove details in this order:
1. Body details (paws, tail decorations) → remove first
2. Body itself → crop to head/face
3. Facial details (whiskers, markings) → simplify
4. Color complexity → reduce to 2-3 colors
5. Shape → essential silhouette only

</subsection>

<subsection name="the_silhouette_test">

At every size, the mascot's silhouette alone should be recognizable. If you can't tell the species from the silhouette, the design needs more distinctive shape language.

</subsection>

</section>

<section name="integration_points">

<subsection name="tier_1_always_present">

- **App icon** — The mascot IS the icon (or the dominant element of it)
- **Splash/loading screen** — First impression, full expression
- **Empty states** — Mascot fills the void, invites action

</subsection>

<subsection name="tier_2_personality_moments">

- **Onboarding** — Mascot introduces itself, guides setup
- **Success celebrations** — Achievement unlocks, streaks, milestones
- **Error states** — Sympathetic presence, never blaming

</subsection>

<subsection name="tier_3_subtle_presence">

- **Tab bar icon** — Simplified mascot as nav element (optional)
- **Pull-to-refresh** — Mascot animation during refresh
- **Settings "about" page** — Full mascot with credits

</subsection>

<subsection name="tier_4_easter_eggs">

- **Hidden interactions** — Tap the mascot X times for a special animation
- **Seasonal variants** — Holiday versions, special occasions
- **Cross-app references** — Nods to sibling mascots

</subsection>

</section>

<section name="typography_pairing">

The mascot's personality should be reflected in the typography used alongside it:

| Mascot Personality | Primary Font Style | Weight Preference |
|-------------------|-------------------|-------------------|
| Warm & friendly | Rounded sans-serif (DM Sans, Nunito) | Regular to Medium |
| Precise & focused | Geometric sans-serif (Inter, SF Pro) | Medium to Semibold |
| Playful & quirky | Soft sans-serif (Be Vietnam Pro, Plus Jakarta Sans) | Regular |
| Serious & minimal | Clean sans-serif (Inter, Helvetica Neue) | Light to Regular |

</section>

<section name="deliverable_format">

A complete visual direction document includes:

```
## Visual Direction: [Mascot Name]

### Species & Rationale
[Why this creature for this app]

### Color Palette
- Primary: [hex] — [where used]
- Secondary: [hex] — [where used]
- Accent: [hex] — [where used]
- Dark mode adjustments: [notes]

### Expression Set
[Which of the 8 expressions apply, with context]

### Size Variants
[Which size categories needed, with detail notes]

### Integration Touchpoints
[Specific screens/states where mascot appears]

### Style Notes
[Line weight, corner radius, proportion, detail level]

### Art Direction
[Mood references, specific visual inspirations]

### Don'ts
[Specific things to avoid for this mascot]
```

</section>

</reference>
