<reference name="lens_assignment_rules" domain="shared">

<section name="agent_structure">

- **Agent A** always channels **Chris Raroque** (warmth, personal naming — the baseline)
- **Agents B and C** channel contrasting lenses for concept diversity
- **All agents** read brookes-eggleston.md for quality self-checking

</section>

<section name="auto_selection_by_vibe">

If the user specifies a lens preference, use it. Otherwise auto-select B and C:

| Vibe Keywords | LENS_B_FILE | LENS_C_FILE |
|---|---|---|
| Enterprise, professional, scale, growth, gamification | greg-hartman.md | healing-character.md |
| Scientific, calm, research, exhaustion, wellness, lab | healing-character.md | burnt-toast.md |
| Creative, social, community, edgy, witty, irreverent | burnt-toast.md | greg-hartman.md |
| Default (any other vibe) | greg-hartman.md | burnt-toast.md |

</section>

<section name="worked_examples">

**"Offline lab data capture for CryoEM researchers" — vibe: "precise, scientific, calm"**
Keywords match: scientific, calm, lab → Row 2.
- Agent A: Raroque (warmth) → intuitive creature, personal naming
- Agent B: Healing Character → exhausted-but-present lab companion, passive empathy
- Agent C: Burnt Toast → precision with dry wit, opinions about lab chaos

**"Social recipe sharing app" — vibe: "warm, community, fun"**
No exact keyword match → Default row.
- Agent A: Raroque → warm creature, food-adjacent personality
- Agent B: Hartman → scalable character system, cast of ingredient creatures
- Agent C: Burnt Toast → foodie with opinions, judges your recipe choices (gently)

**"Enterprise project management SaaS" — vibe: "professional, scalable, gamification"**
Keywords match: enterprise, professional, gamification → Row 1.
- Agent A: Raroque → personal mascot that softens enterprise feel
- Agent B: Hartman → Duolingo-style character system, streak creatures, cast building
- Agent C: Healing Character → calm presence for stressed project managers

</section>

<section name="icon_vibe_to_lens">

For icon domain, the same lens system applies but the lenses influence visual treatment rather than creature personality.

| Vibe Keywords | LENS_B | LENS_C |
|---|---|---|
| Professional, enterprise, systematic, dashboard | Hartman (systems) | Healing (gentle) |
| Scientific, research, precision, lab, data | Healing (minimal) | Burnt Toast (personality) |
| Creative, playful, social, expressive | Burnt Toast (quirky) | Hartman (structured) |
| Default (any other vibe) | Hartman (systems) | Burnt Toast (personality) |

</section>

<section name="button_vibe_to_lens">

For button domain, lenses influence the illustration style and state design personality.

| Vibe Keywords | LENS_B | LENS_C |
|---|---|---|
| Professional, enterprise, formal | Hartman (component) | Healing (subtle) |
| Scientific, calm, precision | Healing (gentle) | Burnt Toast (wit) |
| Creative, playful, social, fun | Burnt Toast (attitude) | Hartman (systematic) |
| Default (any other vibe) | Hartman (systematic) | Burnt Toast (personality) |

</section>

<section name="rationale">

Each row maximizes contrast: Hartman's systems thinking vs. Healing's passive empathy, Healing's stillness vs. Burnt Toast's opinions, Burnt Toast's edge vs. Hartman's structure. Agent A (Raroque warmth) is always the anchor — the other two push in opposing directions. This principle holds across all three domains — mascots, icons, and buttons.

</section>

</reference>
