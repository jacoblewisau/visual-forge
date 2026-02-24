<!-- TOC
  - the_story_first_method
  - the_five_questions
  - naming_conventions
  - family_cohesion_rules
  - anti_patterns
-->

<reference name="narrative_framework" domain="mascot">

<section name="the_story_first_method">

A mascot without a story is just clip art. The narrative must exist BEFORE any visual work begins. The story constrains and guides every design decision.

</section>

<section name="the_five_questions">

Every mascot narrative must answer these five questions:

<subsection name="what_creature_is_this_and_why">

The species choice is the single most important decision. It determines personality archetypes, visual silhouette, and naming direction.

**Species-to-Value Mapping:**

**Top 8 (start here for most projects):** Cat (personal/tracking), Owl (research/analytics), Fox (dev tools/optimization), Bear (security/storage), Penguin (science/collaboration), Axolotl (creative/recovery), Tardigrade (science/resilience), Capybara (wellness/community).

| Creature | Archetype Values | Best For |
|----------|-----------------|----------|
| Cat | Independence, curiosity, precision, comfort | Personal tools, journaling, tracking |
| Dog | Loyalty, enthusiasm, reliability, companionship | Social apps, team tools, reminders |
| Owl | Wisdom, patience, observation, night work | Research tools, analytics, education |
| Fox | Cleverness, adaptability, quick thinking | Developer tools, search, optimization |
| Bear | Strength, protection, calm, hibernation | Security, backup, storage |
| Rabbit | Speed, alertness, agility, multiplication | Messaging, notifications, productivity |
| Penguin | Community, endurance, cold precision | Science tools, collaboration, Linux-adjacent |
| Octopus | Multitasking, flexibility, problem-solving | Integration tools, multi-workspace |
| Bee | Industry, community, sweetness, structure | Project management, organization |
| Hedgehog | Defense, gentleness, small but mighty | Privacy tools, minimalist apps |
| Axolotl | Regeneration, uniqueness, playfulness | Creative tools, version control, recovery |
| Capybara | Calm, social, universally loved, chill | Wellness, meditation, community |

**Scientific / Lab Creatures:**
| Creature | Archetype Values | Best For |
|----------|-----------------|----------|
| Tardigrade | Indestructible, resilient, microscopic wonder | Science tools, backup, survival/recovery |
| Mantis Shrimp | Hyper-perception, powerful precision, hidden depth | Data visualization, color tools, analytics |
| Cuttlefish | Camouflage, intelligence, fluid adaptation | Theming engines, adaptive UI, personalization |
| Salamander | Regeneration, quiet resilience, damp-lab energy | Version control, recovery, lab tools |
| Lab Mouse | Experimental, brave, foundational to science | Research tools, testing, prototyping |
| Narwhal | Uniqueness, deep diving, exploration, wonder | Research tools, search, data exploration |

**Precision / Technical Creatures:**
| Creature | Archetype Values | Best For |
|----------|-----------------|----------|
| Hawk | Sharp vision, decisive, high perspective | Monitoring, dashboards, oversight tools |
| Spider | Architecture, patience, intricate networks | Network tools, dependency graphs, web apps |
| Crane (bird) | Grace, patience, precision, longevity | Deployment tools, careful migration, CI/CD |
| Ant | Collective strength, tireless, organized | Task runners, automation, queue systems |
| Gecko | Adhesion, adaptability, night vision, stealth | Plugin/extension tools, dark mode apps |
| Praying Mantis | Focus, patience-then-strike, precision | Code review, debugging, quality tools |

**Creative / Unconventional Creatures:**
| Creature | Archetype Values | Best For |
|----------|-----------------|----------|
| Luna Moth | Ethereal beauty, nocturnal, ephemeral | Design tools, night-mode apps, creative capture |
| Chameleon | Adaptation, color mastery, watchful calm | Theming, accessibility, multi-platform |
| Jellyfish | Flow, transparency, bioluminescent glow | Data flow tools, streaming, ambient apps |
| Seahorse | Patience, uniqueness, gentle strength | Niche tools, personal databases, collection apps |
| Pangolin | Armored gentleness, rare, protected | Privacy tools, encryption, sensitive data |
| Firefly | Illumination, warmth, brief brilliance, attention | Voice/note capture, alerts, idea apps |
| Sloth | Patience, mindfulness, deliberate pace, calm | Slow/mindful apps, anti-productivity, wellness |
| Kiwi (bird) | Grounded, unique, nocturnal, resilient | Local-first apps, night apps, offline tools |
| Snail | Persistence, home-carrying, patience, steady progress | Portable apps, PWAs, progress trackers |

**Utility / Work Creatures:**
| Creature | Archetype Values | Best For |
|----------|-----------------|----------|
| Elephant | Memory, wisdom, gentle power, never forgets | Databases, knowledge bases, long-term storage |
| Crow/Raven | Intelligence, tool-use, pattern recognition | Developer tools, debugging, code analysis |
| Otter | Playful problem-solving, dexterous, social | Collaboration tools, pair programming, chat |
| Dolphin | Communication, intelligence, joyful efficiency | Messaging, translation, voice tools |
| Hamster | Energy, hoarding, industrious, comfort | Storage, collections, personal vaults |

</subsection>

<subsection name="relationship_to_users_problem">

The mascot should embody the SOLUTION, not the problem. If the app helps with budgeting, the mascot isn't anxious about money — it's calm and organized.

**Relationship patterns:**
- **The Companion** — walks alongside the user (journaling, tracking)
- **The Guide** — knows the way, teaches (education, onboarding)
- **The Guardian** — protects something valuable (security, backup)
- **The Collector** — gathers and organizes (inventory, archive)
- **The Messenger** — carries information (notifications, communication)
- **The Craftsperson** — builds and refines (dev tools, creative)

</subsection>

<subsection name="three_personality_traits">

Choose exactly 3 traits. More is unfocused, fewer is flat.

**Trait pairing rules:**
- One trait should be FUNCTIONAL (organized, fast, thorough)
- One trait should be EMOTIONAL (warm, calm, playful)
- One trait should be DISTINCTIVE (quirky, precise, nocturnal)

**Examples:**
- Amy (food journal, cat): curious, gentle, honest
- Luna (budgeting, implied cat/moon): watchful, steady, playful
- A lab inventory tool: meticulous, cool-headed, slightly nerdy

</subsection>

<subsection name="one_sentence_origin_story">

This is the narrative hook. It should be simple enough to say in conversation.

**Formula:** "[Name] is a [creature] who [relationship to problem] because [personal motivation]."

**Examples:**
- "Amy is a cat who watches what you eat because she's genuinely curious about your choices."
- "Frost is a penguin who catalogs your specimens because she believes everything deserves a proper place."
- "Ember is a firefly who captures your voice notes because brilliant ideas shouldn't die in the dark."

</subsection>

<subsection name="creature_behavior_in_app">

The mascot's behavior at different app states reveals its personality:

| App State | Behavior Pattern |
|-----------|-----------------|
| Empty state | The creature is present, inviting, slightly bored |
| Active use | The creature is engaged, helpful, responsive |
| Success/completion | The creature celebrates (proportionate to achievement) |
| Error/failure | The creature is sympathetic, never blaming |
| Loading/waiting | The creature is patient, doing something characteristic |
| Onboarding | The creature introduces itself, shows personality |
| Long absence | The creature welcomes back warmly |

</subsection>

</section>

<section name="naming_conventions">

<subsection name="chris_raroque_rules">

1. **Short** — 2-5 letters ideal. All his apps: Ellie (5), Luna (4), Amy (3), Lily (4), Mogul (5).
2. **Human-sounding** — Could be someone's name. Not "Logify" or "DataBot."
3. **Gendered or neutral** — Chris uses feminine names (his pets). Neutral names work too.
4. **Phonetically pleasant** — Say it aloud. Does it flow? Would you call it across a room?
5. **Domain available** — Check {name}app.com, {name}.app, {name}{category}.com early.

</subsection>

<subsection name="naming_methods">

- **Direct pet name** — Use an actual pet's name (Chris's method)
- **Trait-derived** — Ember (warmth), Frost (precision), Scout (exploration)
- **Species-derived** — Kit (fox), Pip (bird), Finn (fish)
- **Sound-derived** — Names that sound like the creature (Buzz for bee, Chirp for bird)

</subsection>

</section>

<section name="family_cohesion_rules">

When designing mascots for related apps:

1. **Shared typography** — Same font family, different weights per personality
2. **Complementary palettes** — Each app gets its own color world, but they should work in a grid
3. **Consistent illustration style** — Same artist hand, different subjects
4. **Shared tagline pattern** — "A better [X]" or similar structure
5. **Cross-references** — Mascots can acknowledge each other's existence (Easter eggs)
6. **Hierarchy of personality** — Some apps are louder, some quieter. Not every mascot is equally prominent.

</section>

<section name="anti_patterns">

**DON'T:**
- Make the mascot a robot, AI assistant, or generic blob
- Use the mascot as a help chatbot personality
- Add the mascot to every screen (it becomes wallpaper)
- Make the mascot talk in tooltips (annoying fast)
- Give the mascot a tragic backstory (it's an app, not a movie)
- Use the mascot to apologize for bad UX ("Oops! Mascot is confused!")
- Create a mascot for a professional/enterprise tool that doesn't need one

**DO:**
- Let the mascot be subtle — presence without intrusion
- Use the mascot to soften empty states and errors
- Let users discover mascot personality over time (progressive disclosure)
- Keep the mascot consistent — same personality everywhere
- Make the mascot optional — it enhances but never gates functionality

</section>

</reference>
