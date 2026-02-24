<!-- TOC
  - who_he_is
  - when_to_channel_raroque
  - the_pet_naming_convention
  - core_design_principles
  - visual_language
  - expression_framework
  - copy_tone
  - what_this_means_for_mascot_design
  - key_references
-->

<reference name="chris_raroque" domain="mascot">

<section name="who_he_is">

Solo indie app developer in Dallas, Texas. Co-Founder of Aloa (software outsourcing + AI research). Builds a suite of productivity apps, each named after a real pet. 65K+ YouTube subscribers documenting the build-in-public journey. Collaborates with illustrator Cecilia Kim for formal illustration systems.

</section>

<section name="when_to_channel_raroque">

- Consumer products where the mascot IS the brand identity (not a supplement)
- Apps where personal warmth and craft should be the primary emotional signal
- Products that benefit from a pet-naming convention (creature name = app name)
- The default baseline lens — when no other lens has a stronger claim
- Solo developer / indie studio products where authenticity matters
- Apps that need beauty as a core feature, not decoration

</section>

<section name="the_pet_naming_convention">

| App | Role | Creature | Key Insight |
|-----|------|----------|-------------|
| Ellie | Daily planner | Elephant | Elephant iconography, memory/organization mapping |
| Luna | Budgeting | Moon/cat | Lunar thematic, watchful presence |
| Amy | Food journal | Cat (real pet) | Real cat photos on landing page, developer introduces himself alongside the pet |
| Lily | Meetings copilot | Pet name | Gentle, structured personality |
| Mogul | Networking | None | **The exception** — professional domain, no character mascot, proves Raroque modulates by audience |

**The pattern:** The creature's name becomes the product name. Personality traits map to the app's emotional identity. The mascot is not marketing — it's the entire brand.

</section>

<section name="core_design_principles">

<subsection name="beauty_is_a_feature">

Luna's explicit principle: "really good UI and design so you don't mind it being so manual." Beautiful design compensates for intentional friction. The mascot must be beautiful enough to earn emotional investment. If the mascot feels like an afterthought, it damages the entire product perception.

</subsection>

<subsection name="problem_driven_personal_origin">

Every app starts from a personal pain point. The mascot inherits this authenticity — it's not a focus-grouped corporate icon, it's part of the creator's life. Users buy into the developer's journey; the mascot carries that personal story.

</subsection>

<subsection name="design_as_emotional_experience">

Chris talks explicitly about how apps "feel" and wanting to "inject some life" into products. Micro-interactions, animations, and haptics make products feel alive. The mascot is the ultimate expression of this — it gives the app a living presence.

</subsection>

<subsection name="modulate_by_domain">

Not every app needs a playful character. Mogul proves Raroque adjusts the mascot approach by audience:

| Domain | Mascot Approach | Visual Register |
|--------|----------------|-----------------|
| Consumer / personal | Full character, pet name, playful | Warm, illustration-forward |
| Productivity / creative | Moderate character, restrained animation | Clean, beautiful, subtle |
| Professional / enterprise | No character mascot, functional iconography | Minimalist, high-contrast |

</subsection>

<subsection name="think_in_families">

Even a single mascot should feel like it could have siblings. Each app's design system teaches something that feeds back to the others. When one mascot gets better, the family should level up.

</subsection>

</section>

<section name="visual_language">

<subsection name="color_palette">

Raroque's palette shifts per-product but follows a "playful-professional" register — sophisticated enough for an Apple product page, warm enough to feel personal:

| Tone | Hex Range | Feeling | Use For |
|------|-----------|---------|---------|
| Warm accent | #F59E0B — #FB923C | Friendly energy, primary identity | Hero color, mascot highlight |
| Soft cream | #FFF8F0 — #FEFCE8 | Clean warmth, approachable | Backgrounds, light mode surfaces |
| Cool complement | #60A5FA — #818CF8 | Balance, depth, trustworthy | Secondary accents, dark mode highlights |
| Warm neutral | #78716C — #A8A29E | Grounded, understated | Text, subtle elements |
| Blush/rose | #FDA4AF — #FCA5A5 | Gentle personality, soft warmth | Emotional moments, onboarding |

**Never:** Neon colors, heavy gradients, stark black-on-white without warmth. The palette should feel handmade, not corporate.

**Per-product rule:** Each app gets its OWN dominant accent. No universal brand color. The creature's natural coloring guides the palette.

</subsection>

<subsection name="proportion_rules">

| Feature | Raroque Style | Why |
|---------|--------------|-----|
| Head-to-body | 1:1.2 — 1:1.5 (slightly large head) | Approachable, not childish |
| Eyes | 25-35% of face, expressive, open | Emotional range without exaggeration |
| Mouth | Small, expressive line (not absent) | Can smile — warmth requires visible happiness |
| Limbs | Short but present, functional | The creature can gesture, hold things |
| Posture | Upright or slight lean forward | Engaged, attentive, present |
| Outline | Clean, confident, consistent weight | "Playful-professional" — not sketchy, not stiff |

</subsection>

<subsection name="illustration_style">

- Clean vector with personality — geometric foundations, organic details
- Flat or subtle gradients (no heavy 3D rendering)
- Confident, consistent line weight (not hairline, not thick)
- Slightly exaggerated features (larger eyes, rounder body) but anatomically readable
- Would look at home on an Apple product page or Stripe landing page
- Custom bespoke illustrations, never stock (Cecilia Kim collaboration as reference)

</subsection>

</section>

<section name="expression_framework">

Raroque mascots have a WARM expression range — biased toward positive emotions with genuine personality:

| Expression | Visual Description | When Used |
|-----------|-------------------|-----------|
| **Resting/Present** | Calm, slight smile, eyes open and attentive. "I'm here with you." | Default state, home screen |
| **Happy** | Genuine smile, eyes brighten. Proportionate — not over-the-top. | Success, completion |
| **Curious** | Head tilted, eyes focused, slight lean forward. Engaged. | Active tasks, search, exploration |
| **Sympathetic** | Gentle concern, soft eyes, slight head tilt. Never panicked. | Errors, empty states |
| **Sleepy** | Eyes half-closed, relaxed posture. Charming, not checked-out. | Idle, night mode, long absence |
| **Delighted** | Full smile, eyes wide, subtle bounce. The biggest celebration. | Major milestones only |

**Explicitly excluded:** Angry, disappointed, guilt-inducing, sarcastic, judgmental. Raroque mascots are always on the user's side.

</section>

<section name="copy_tone">

If the mascot "speaks" through UI copy, the tone is warm, personal, and casual:

| Context | Raroque Voice | Anti-Pattern |
|---------|--------------|-------------|
| Empty state | "Nothing here yet. Let's add your first one." | "Error: No data found." |
| Error | "Something went wrong. Let's try again." | "Oops! [Mascot] is confused!" |
| Success | "Nice. First entry saved." | "AMAZING JOB!!!" |
| Loading | "Working on it..." | "Please wait while we process your request." |
| Long absence | "Welcome back." | "We missed you! Don't forget to..." |
| Onboarding | "Hi, I'm [Name]. I'll help you [core function]." | "Step 1 of 7: Configure your preferences." |

**Voice rules:** First person, present tense, casual. Uses the mascot's name naturally. Emoji sparingly (1-2 per screen max). Never guilt-trips, never over-celebrates.

</section>

<section name="what_this_means_for_mascot_design">

1. **Start with a real creature** (or one that could be real). Not abstract shapes, not robots.
2. **The creature's name becomes the product name** (or deeply integrates with it).
3. **Map creature traits to product values** — a patient creature for patience, a precise creature for precision.
4. **The tone is personal, not corporate** — first-person voice, casual copy, the mascot feels like the developer's companion.
5. **Visual quality must be impeccable** — beauty is a feature, not decoration.
6. **Modulate by domain** — playful for consumer, restrained for professional, warm for personal.
7. **Think in families** — even a single mascot should feel like it could have siblings.

</section>

<section name="key_references">

- Chris Raroque apps: Amy, Ellie, Luna, Lily, Mogul
- YouTube: build-in-public design process documentation
- Illustration collaborator: Cecilia Kim (Luna design system)
- Style benchmark: "Would this look at home on an Apple product page?"

</section>

</reference>
