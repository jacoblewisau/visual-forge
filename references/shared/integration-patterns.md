<reference name="integration_patterns" domain="shared">

<!-- TOC
  - how_mascots_live_in_apps
  - pattern_library
  - implementation_priorities
  - technical_considerations
  - gsd_integration_points
-->

<section name="how_mascots_live_in_apps">

A mascot that only exists on the landing page is a logo, not a mascot. True integration means the creature has a presence throughout the app experience — subtle, purposeful, and never intrusive.

</section>

<section name="pattern_library">

<subsection name="1_the_app_icon_mascot">

**Where:** Home screen icon, browser tab favicon
**Implementation:**
- The mascot face/silhouette IS the app icon
- At 1024px: full detail, distinctive silhouette, recognizable species
- At 180px (iOS): simplified, fewer colors, bolder shapes
- At 32px (favicon): essential shape only, 2-3 colors max
**Chris's pattern:** His apps use clean, illustrative icons where the mascot or its energy defines the icon shape.

</subsection>

<subsection name="2_empty_state_companion">

**Where:** Any screen with no content yet
**Implementation:**
- Mascot appears centered, above a call-to-action
- Expression: curious or gently inviting
- Size: 120-180px
- Copy tone: first-person from mascot or warm third-person
  - "Nothing here yet. Let's add your first [item]."
  - NOT: "Error: No data found."
**Rule:** Empty states are the mascot's best opportunity. This is where personality earns its keep.

</subsection>

<subsection name="3_onboarding_guide">

**Where:** First-launch sequence, setup wizard
**Implementation:**
- Mascot introduces itself on slide 1
- Guides through setup with different expressions per step
- Welcoming expression → curious expression → happy expression
- The mascot narrates in second person: "I'll help you track..."
**Chris's pattern (Amy):** "Hi, I'm Chris" alongside the pet. Personal, warm, casual.

</subsection>

<subsection name="4_success_celebration">

**Where:** Task completion, milestone achievement, streak continuation
**Implementation:**
- Mascot shows excited/happy expression
- Brief animation (200-400ms): subtle bounce or scale
- Proportional: small wins = subtle smile, big wins = full celebration
- Optional: confetti, sparkle, or sound effect accompanies mascot
**Rule:** NEVER celebrate mundane actions (saving settings, closing a modal). Only meaningful achievements.

</subsection>

<subsection name="5_error_sympathy">

**Where:** Failed operations, network errors, validation failures
**Implementation:**
- Mascot shows sympathetic expression
- Size: smaller than empty state (64-96px)
- Positioned near the error message, not replacing it
- Copy: "Something went wrong. Let's try again."
- NOT: "Oops! [Mascot] is confused!" (anthropomorphized blame)
**Rule:** The mascot shows empathy, never confusion. The mascot always knows what happened — it's sympathetic, not helpless.

</subsection>

<subsection name="6_loading_processing_companion">

**Where:** Page loads, data processing, search
**Implementation:**
- Mascot shows thinking expression or species-appropriate idle animation
- Cat: ear twitch or tail sway
- Owl: slow blink
- Penguin: gentle waddle
- Duration-aware: short loads (< 1s) skip mascot. Long loads (> 2s) show it.
**Rule:** Loading mascots must be lightweight. Don't add a 500KB Lottie animation to replace a 2KB spinner.

</subsection>

<subsection name="7_tab_bar_presence">

**Where:** Bottom navigation, sidebar
**Implementation:**
- Simplified mascot face as one tab icon (usually "home" or "profile")
- Monochrome when inactive, colored when active
- Must be recognizable at 24-28px
- Alternative: mascot silhouette as the app's "home" concept
**Rule:** Optional. Only if the mascot silhouette reads clearly at icon size.

</subsection>

<subsection name="8_settings_and_about">

**Where:** Settings page, "about this app" section
**Implementation:**
- Full mascot illustration with credits
- Developer introduction alongside mascot (Chris's "Hi, I'm Chris" pattern)
- Version number near mascot
- Optional: photo gallery of the real pet (if pet-naming approach used)
- Easter egg: tap mascot for a special animation or sound

</subsection>

<subsection name="9_seasonal_contextual_variants">

**Where:** Holiday periods, special events, time-of-day
**Implementation:**
- Subtle accessories: Santa hat, sunglasses, party hat
- Palette shifts: warmer at night, cooler in morning
- Should be opt-out-able (respect user preference)
**Rule:** Variants are delighters, not requirements. Ship v1 without them.

</subsection>

<subsection name="10_cross_module_personality">

**Where:** Different sections of the same app have different moods
**Implementation:**
- The mascot's expression subtly shifts per module
- Archive module: meticulous expression
- Dashboard: relaxed expression
- Settings: neutral expression
- The shift is subtle — same mascot, different micro-mood

</subsection>

</section>

<section name="implementation_priorities">

<subsection name="mvp_ship_first">

1. App icon
2. Empty states (all modules)
3. Onboarding welcome

</subsection>

<subsection name="v2_after_launch">

4. Success celebrations
5. Error sympathy
6. Settings/about page

</subsection>

<subsection name="v3_polish">

7. Loading companion
8. Tab bar presence
9. Seasonal variants
10. Cross-module personality shifts

</subsection>

</section>

<section name="technical_considerations">

<subsection name="format_recommendations">

| Context | Format | Why |
|---------|--------|-----|
| App icon | SVG master → PNG export | Crisp at all sizes |
| In-app illustrations | SVG or optimized PNG | Resolution independence |
| Animations | CSS/JS or Lottie (< 50KB) | Keep bundle small |
| Favicon | .ico or SVG | Browser compatibility |

</subsection>

<subsection name="performance_budget">

- Total mascot assets: < 200KB for MVP
- Individual illustrations: < 30KB each
- Animations: < 50KB Lottie or pure CSS/JS
- No full-page mascot illustrations that block render

</subsection>

<subsection name="accessibility">

- All mascot images need alt text describing the emotion/state
- Mascot animations must respect `prefers-reduced-motion`
- Mascot should not be the ONLY indicator of state (always pair with text)
- Color-blind safe: mascot should read in grayscale
- Screen readers should describe the mascot naturally: "Amy the cat looks happy" not "mascot-success-state.svg"

</subsection>

</section>

<section name="gsd_integration_points">

When working within a GSD-managed project:

<subsection name="during_phase_planning">

```yaml
# In PLAN.md tasks
<task type="auto">
  <name>Task N: Implement mascot empty states</name>
  <files>components/{module}/empty-state.tsx</files>
  <action>
  Reference MASCOT-SPEC.md for:
  - Expression to use (sympathetic for errors, curious for empty)
  - Color palette for mascot elements
  - Size variant appropriate for this context
  - Alt text pattern from accessibility section
  </action>
</task>
```

</subsection>

<subsection name="cross_phase_mascot_work">

If the mascot spans multiple phases:
- Phase N: Create MASCOT-SPEC.md (narrative + visual direction)
- Phase N+1: Implement app icon + onboarding
- Phase N+2: Implement empty states + error states
- Phase N+3: Polish (celebrations, loading, variants)

Each phase references the same MASCOT-SPEC.md for consistency.

</subsection>

</section>

</reference>
