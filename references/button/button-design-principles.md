<reference name="button-design-principles" domain="button">

<!-- TOC: anatomy, illustration_calibration, state_design, personality_levels, size_tiers, accessibility, common_mistakes -->

<section name="anatomy">

An illustrated button combines a functional interactive element with character-driven artwork. The illustration enhances the button's meaning and personality without compromising its function as a tappable/clickable UI element.

**Button Anatomy:**

```
┌──────────────────────────────────┐
│  [illustration]  [label text]    │
│                                  │
└──────────────────────────────────┘
     ↑               ↑          ↑
  visual accent   primary    container
                  content    (hit target)
```

**Component Roles:**

| Component | Role | Rules |
|-----------|------|-------|
| Container | Hit target, visual boundary | Must meet minimum touch target (44x44px mobile, 32x32px desktop) |
| Label | Primary communication | Must be readable without the illustration |
| Illustration | Personality, delight, reinforcement | Must not obscure or compete with the label |
| Icon (optional) | Functional clarity | Standard icon rules apply (grid, stroke, metaphor) |

**The Independence Principle:** The button must work without the illustration. The illustration is an enhancement layer — if it disappeared, the button would still be functional and clear. This distinguishes illustrated buttons from icon-only buttons.

</section>

<section name="illustration_calibration">

How much illustration is appropriate depends on context, frequency of interaction, and emotional importance.

**Calibration Scale:**

| Level | Illustration | When to Use | Example |
|-------|-------------|-------------|---------|
| 0 - None | Standard button, no illustration | High-frequency actions, form submits | "Save" / "Cancel" |
| 1 - Accent | Small decorative element (4-8px) | Medium-frequency, mild personality | Sparkle on "Publish", leaf on "Plant" |
| 2 - Companion | Small character/motif alongside label (16-24px) | Key actions, emotional moments | Mascot waving on "Get Started" |
| 3 - Hero | Illustration dominates, label integrated (32-48px) | One-time or rare actions, CTAs | Full character on "Begin Your Journey" |

**Calibration Rules:**
- Most buttons should be Level 0 or 1 — illustration is a spice, not the main course
- Only 1-2 buttons per screen should be Level 2+
- Level 3 is reserved for onboarding CTAs, empty state actions, and milestone moments
- The illustration's energy should match the action's importance

</section>

<section name="state_design">

Illustrated buttons need state design that includes the illustration's response to interaction.

**State Matrix:**

| State | Container | Label | Illustration |
|-------|-----------|-------|-------------|
| Default | Resting style | Normal weight | Neutral/resting pose |
| Hover | Subtle elevation or color shift | No change | Slight animation — ear perk, eye brightening, gentle bounce |
| Pressed | Depressed, darker | No change | Compressed/squished, or quick reaction |
| Disabled | Muted, reduced opacity | Muted | Faded, sleeping, or turned away |
| Loading | Skeleton or pulse | "Loading..." or spinner | Species-appropriate idle animation |
| Success | Accent color flash | "Done!" or checkmark | Celebration proportionate to action importance |

**Animation Budgets:**
- Hover: 100-200ms, CSS transition preferred
- Pressed: 50-100ms, immediate feel
- Loading: Loop, lightweight (CSS or tiny SVG animation, no Lottie)
- Success: 300-500ms, then return to default

**Critical Rule:** Button illustrations must respect `prefers-reduced-motion`. When reduced motion is preferred, illustrations should be static in all states.

</section>

<section name="personality_levels">

The illustration's personality should match the app's emotional register, calibrated by the designer lens.

**Register Mapping:**

| App Vibe | Illustration Register | Example Treatment |
|----------|---------------------|-------------------|
| Warm, personal | Friendly, handcrafted feel | Rounded illustration, warm accent color |
| Precise, scientific | Clean, geometric, restrained | Minimal accent, structured shapes |
| Playful, social | Expressive, slightly quirky | Bold outline, pastel fills, one quirk |
| Calm, wellness | Soft, unobtrusive, gentle | Thin strokes, muted colors, simple shapes |
| Professional, enterprise | Sophisticated, minimal | Icon-level illustration only (Level 0-1) |

</section>

<section name="size_tiers">

Illustrated buttons exist at specific size tiers matching their illustration level.

| Tier | Button Height | Illustration Zone | Max Shapes | Colors |
|------|-------------|------------------|------------|--------|
| Compact | 32px | 16x16px accent | 3-5 | 1-2 |
| Standard | 40px | 24x24px companion | 5-10 | 2-3 |
| Hero | 48px+ | 32x48px featured | 10-20 | 3-5 |

**SVG Constraints per Tier:**
- Compact: viewBox matches accent zone, 3-5 shapes, 1-2 colors, no gradients
- Standard: viewBox matches companion zone, 5-10 shapes, 2-3 colors, subtle gradients OK
- Hero: viewBox matches featured zone, 10-20 shapes, 3-5 colors, full gradients OK

</section>

<section name="accessibility">

Illustrated buttons have additional accessibility requirements beyond standard buttons.

**Requirements:**
- Button label must be sufficient for screen readers — illustration is decorative (`aria-hidden="true"` on SVG)
- Color contrast: label text must meet WCAG AA (4.5:1) regardless of illustration
- Touch target: minimum 44x44px on mobile, including illustration area
- Focus indicator must be visible around the entire button container, not just the label
- Illustration must not animate on focus (distracting for keyboard navigation)
- Disabled state must be communicated by label styling, not illustration alone

</section>

<section name="common_mistakes">

1. **Illustration competes with label** — The artwork is so prominent that users read the picture, not the text. Label must always be primary.
2. **Every button is illustrated** — Illustration fatigue. Most buttons should be Level 0-1. Save illustration for moments that matter.
3. **State changes only in illustration** — Some users don't see the illustration (screen readers, zoom, reduced motion). States must be visible in the container and label too.
4. **Illustration too complex for button size** — A 32px button can't hold a detailed scene. Match illustration complexity to tier.
5. **Animation on every state** — Hover, press, focus, and loading all animated? Too much. Pick one animated state and keep others subtle.
6. **Illustration style doesn't match the icon set** — Illustrated buttons should feel like they belong in the same design system as the app's icons.
7. **Forgetting dark mode** — Illustrations need to work on both light and dark backgrounds. Test with the container's actual background colors.

</section>

</reference>
