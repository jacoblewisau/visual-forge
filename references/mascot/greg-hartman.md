<!-- TOC
  - who_he_is
  - when_to_channel_hartman
  - core_design_principles
  - shape_language_reference
  - cast_building_framework
  - what_this_means_for_mascot_design
  - key_references
-->

<reference name="greg_hartman" domain="mascot">

<section name="who_he_is">

Head of Art at Duolingo. Designed every evolution of Duo the owl from flat logo to the most meme-able mascot in tech. Built the entire character universe (Lily, Bea, Zari, Oscar, Eddy, Junior, Lin, Lucy, Vikram) that populates the app. Published "Shape Language: Duolingo's Art Style" on the Duolingo blog. Previously at Gunner animation studio before joining Duolingo.

</section>

<section name="when_to_channel_hartman">

- Enterprise or growth SaaS products that need characters at scale
- Products with gamification, streaks, or engagement loops
- Apps that need a CAST of characters, not just one mascot
- Products where the mascot must function as a UI component (not just brand art)
- Apps designed for animation from day one

</section>

<section name="core_design_principles">

<subsection name="shape_language_is_structure_not_style">

"Duo is constructed very simply — basically a chicken nugget with a face."

Every character is built from a strict vocabulary of geometric primitives:
- **Circles** for friendliness and approachability
- **Rounded rectangles** for stability and reliability
- **Ovals** for expressiveness and dynamism

The fewer shapes that compose a character, the better it animates, the clearer it reads at small sizes, and the more expressive it can be. Complexity is the enemy of personality.

</subsection>

<subsection name="eyes_do_everything">

At any size, eyes are the primary vehicle for emotion. Hartman's characters have disproportionately large eyes relative to body size. When a character is reduced to 16px, only the eyes need to change to communicate a different state.

**Eye rules:**
- Eyes are always the largest feature relative to the face
- Pupil position conveys attention (looking at the user, looking at content, looking away)
- Eyelids convey mood (half-closed = sassy/tired, wide = excited/surprised)
- Blink rate conveys energy (fast = nervous, slow = calm, none = focused)

</subsection>

<subsection name="one_mascot_is_never_enough">

Raroque designs one creature per app. Hartman designs one *world* per app.

The Duolingo approach: start with a single mascot, then gradually introduce supporting characters with contrasting personalities. Each character fills an emotional role:
- **Duo** (owl): The enthusiastic guide. Optimistic, encouraging, slightly guilt-trippy.
- **Lily** (goth girl): The reluctant participant. Sarcastic, cool, relatable to users who find learning tedious.
- **Zari** (confident): The overachiever. Represents the user's aspiration.
- **Eddy** (slacker): The lovable mess. Represents the user's self-doubt.

This cast creates a social world inside the app. Users identify with different characters at different moments, creating deeper engagement than a solo mascot can.

</subsection>

<subsection name="the_mascot_is_a_ui_component">

Hartman's characters aren't decoration — they're functional UI elements:
- **Streak notifications**: Duo's expression conveys urgency better than text
- **Progress indicators**: Character reactions replace generic progress bars
- **Error states**: Sympathetic character > error icon
- **Empty states**: Characters with personality > blank screens
- **Celebrations**: Proportionate character reactions > confetti

The mascot should have defined states in the design system, just like buttons or cards.

</subsection>

<subsection name="guilt_as_engagement">

Duolingo pioneered the "guilt-trip mascot" — Duo looking sad when you miss a lesson. This was so effective it became a meme. The key insight: characters that express disappointment create obligation, not just delight.

**Rules for guilt-pattern:**
- Must be lighthearted, never aggressive
- The character should be sad FOR you, not AT you
- Must be opt-out-able (respect user boundaries)
- Works best when there's a clear action to resolve the guilt
- Proportionate: mild sadness for missed day, not devastation

</subsection>

<subsection name="animate_first_illustrate_second">

Characters are designed for motion from the start — shapes chosen for how they deform, not just how they look static. A character that looks great in a poster but can't animate is a failed product mascot.

**Animation-first checklist:**
- Can this character's body squash and stretch?
- Does the silhouette read at 12fps?
- Are the limbs riggable (clear joints, consistent proportions)?
- Do the expressions work as 2-frame transitions?
- Is the color palette simple enough for motion (< 5 colors per character)?

</subsection>

</section>

<section name="shape_language_reference">

<subsection name="primary_shape_meanings">

| Shape | Personality | Examples |
|-------|-----------|---------|
| Circle/Sphere | Friendly, approachable, soft, safe | Duo's body, friendly NPCs |
| Rounded rectangle | Stable, reliable, modern, grounded | Supporting characters, UI elements |
| Triangle/Angular | Sharp, dangerous, villainous, energetic | Antagonists, alert states |
| Organic/Blob | Relaxed, natural, unpredictable | Background characters, nature |

</subsection>

<subsection name="proportion_rules">

| Character Role | Head:Body Ratio | Eye Size | Limb Style |
|---------------|-----------------|----------|------------|
| Main mascot | 1:1.2 (large head) | 30-40% of face | Short, stubby |
| Supporting friend | 1:1.5 | 25-35% of face | Medium, proportionate |
| Background/NPC | 1:2 | 20-25% of face | Longer, varied |

</subsection>

<subsection name="color_budget_per_character">

Each character gets a maximum of 4-5 colors:
1. **Body primary** (dominant, 60% of character)
2. **Body secondary** (belly, face, 25%)
3. **Accent** (eyes, accessories, 10%)
4. **Outline/shadow** (definition, 5%)
5. **Optional highlight** (shine, expression accent)

More colors = harder to animate, harder to recognize at small sizes, harder to maintain.

</subsection>

</section>

<section name="cast_building_framework">

<subsection name="the_personality_spectrum">

When building multiple characters for one product, map them on two axes:

**Energy axis:** Low energy <-- --> High energy
**Warmth axis:** Cool/sarcastic <-- --> Warm/enthusiastic

The main mascot should be warm + medium-high energy. Supporting characters should fill different quadrants to give the cast range:
- Warm + high energy: The cheerleader
- Warm + low energy: The comforter
- Cool + high energy: The rival
- Cool + low energy: The skeptic

</subsection>

<subsection name="introduction_cadence">

Don't launch all characters at once:
1. **Launch**: Main mascot only. Establish personality.
2. **Month 2-3**: Introduce 1 supporting character with contrasting personality.
3. **Month 4-6**: Introduce 1-2 more. Now you have a cast.
4. **Ongoing**: Seasonal variants, special appearances, community favorites.

</subsection>

<subsection name="relationship_mapping">

Every pair of characters should have a defined dynamic:
- Duo + Lily = eager teacher + reluctant student
- Duo + Eddy = disciplined + chaotic
- Lily + Zari = opposites who secretly respect each other

These relationships create narrative potential for empty states, onboarding, and seasonal content.

</subsection>

</section>

<section name="what_this_means_for_mascot_design">

1. **Start with geometry** — Build the character from 2-3 primitive shapes before adding any detail.
2. **Design the cast, not just the hero** — Even if shipping one character, plan the personality spectrum for future characters.
3. **Eyes are the expression engine** — Invest the most design energy in eye expressiveness.
4. **Animate first** — If a character can't squash and stretch, redesign the shape language.
5. **Budget colors ruthlessly** — 4-5 max per character. Fewer = more recognizable.
6. **The mascot IS a UI component** — Define states (idle, active, success, error, loading) like any design system element.
7. **Guilt is powerful but dangerous** — Character emotion drives engagement, but must remain lighthearted and opt-out-able.

</section>

<section name="key_references">

- Duolingo Blog: "Shape Language: Duolingo's Art Style" by Greg Hartman
- Portfolio: dribbble.com/gregoryhartman
- Duolingo Blog author page: blog.duolingo.com/author/greg/

</section>

</reference>
