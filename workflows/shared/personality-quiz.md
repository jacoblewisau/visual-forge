<domain_context>
This is a shared workflow parameterized by {DOMAIN} (mascot/icon/button).
When invoked, the orchestrator replaces {DOMAIN} with the active domain.
This quiz is domain-neutral in its questions — the same personality discovery
applies regardless of whether the output feeds into mascot, icon, or button
design. The transition at the end routes to the correct domain's forge workflow.
</domain_context>

<context_preservation>
This workflow is a guided personality discovery — pure orchestrator Q&A with no agent spawning.
The 7 questions map to specific design parameters that feed into forge/quick workflows.
This is the ONLY workflow that reads NO reference files and spawns NO agents.

**Orchestrator Discipline (HARD RULES):**
You are the quizmaster. NEVER: spawn agents, read reference files, rush questions, judge answers. ONLY: ask one question at a time, track answers, synthesize profile, offer transition to forge/quick.
</context_preservation>

<process>

<step number="1" name="Introduction">

Present to the user:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
VISUAL FORGE PERSONALITY QUIZ
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

7 quick scenarios to discover your app's visual personality.
No right answers — just gut reactions. I'll translate your
responses into a design profile that feeds directly into
the visual forge.

Ready? Let's start.
```

</step>

<step number="2" name="Ask All 7 Questions">

Present each question, wait for the answer, then proceed to the next. Track all answers.

<question number="1" name="The Error Personality">

> Your app just hit an unexpected error. What does the ideal response FEEL like?
>
> **A.** A calm guide who already knows the way back — "Here's what happened, here's what to do."
> **B.** A sympathetic friend who sits with you — "That's frustrating. Let's figure this out together."
> **C.** A skilled craftsperson who's already fixing it — "On it. Give me a sec."
> **D.** A wise mentor who turns it into a lesson — "Interesting. This tells us something useful."

**Maps to → Relationship Archetype:**
- A = Guide
- B = Companion
- C = Craftsperson
- D = Mentor

</question>

<question number="2" name="The Room">

> If your app were a room, which would it be?
>
> **A.** A sunlit workshop with tools organized on pegboards and warm wood surfaces.
> **B.** A cozy library with deep armchairs, ambient lighting, and a crackling fireplace.
> **C.** A sleek control room with dark panels, precise readouts, and cool blue light.
> **D.** A clean whiteboard room — bright, minimal, nothing unnecessary.

**Maps to → Color Temperature + Vibe:**
- A = Warm palette, maker/craft energy
- B = Warm palette, cozy/intimate energy
- C = Cool palette, precision/scientific energy
- D = Neutral palette, minimal/clean energy

</question>

<question number="3" name="The Feeling">

> When someone uses your app and it works perfectly, what emotion do you want them to feel?
>
> **A.** Calm confidence — "I've got this handled."
> **B.** Quiet delight — "This is genuinely nice to use."
> **C.** Proud accomplishment — "Look what I just did."
> **D.** Effortless flow — "That was so easy I barely noticed."

**Maps to → Emotional Personality Trait:**
- A = Steadfast, reliable
- B = Warm, delightful
- C = Encouraging, celebratory
- D = Invisible, seamless

</question>

<question number="4" name="The Complexity">

> Your app has to handle something complicated. How should it approach complexity?
>
> **A.** Hide it completely — the user should never feel the complexity exists.
> **B.** Reveal it progressively — start simple, let users dig deeper when ready.
> **C.** Organize it visually — make the complexity beautiful and navigable.
> **D.** Narrate through it — walk the user through step by step.

**Maps to → Functional Personality Trait:**
- A = Discreet, elegant
- B = Patient, layered
- C = Meticulous, visual
- D = Articulate, guiding

</question>

<question number="5" name="The Sound">

> If your visual asset made a sound, what would it be?
>
> **A.** A soft purr or hum — present but unobtrusive.
> **B.** A cheerful chirp — bright and acknowledging.
> **C.** A low rumble — deep, grounding, reassuring.
> **D.** A precise click — crisp, satisfying, mechanical.

**Maps to → Interaction Style + Distinctive Trait:**
- A = Ambient presence, subtle personality
- B = Responsive feedback, expressive personality
- C = Grounding weight, steady personality
- D = Tactile precision, detail-oriented personality

</question>

<question number="6" name="The Data Relationship">

> Your app stores something the user cares about. What's the visual asset's relationship to that data?
>
> **A.** Keeper — guards it carefully, treats it as sacred.
> **B.** Collector — gathers it enthusiastically, organizes with pride.
> **C.** Messenger — carries it where it needs to go, reliably.
> **D.** Companion — walks alongside the data journey, observes and supports.

**Maps to → Narrative Relationship Type:**
- A = Guardian
- B = Collector
- C = Messenger
- D = Companion

</question>

<question number="7" name="The Trust Signal">

> What makes a user trust your app?
>
> **A.** The developer's personal touch — knowing a real person made this with care.
> **B.** Professional polish — everything looks and feels premium.
> **C.** Transparency — the user can see exactly what's happening.
> **D.** Reliability — it just works, every time, no drama.

**Maps to → Brand Approach:**
- A = Personal warmth (Raroque style — dev personality, craft feel)
- B = Craft quality (beauty-as-feature, illustration investment)
- C = Honest design (show-your-work, build-in-public energy)
- D = Functional trust (minimal visual presence, let the work speak)

</question>

</step>

<answer_tracking>

Track answers in this format as each question is answered. Build this block incrementally — after each answer, append the new line:

```
ANSWERS:
Q1 (Archetype): [A/B/C/D] → [Guide/Companion/Craftsperson/Mentor]
Q2 (Room): [A/B/C/D] → [warm-craft/warm-cozy/cool-precision/neutral-minimal]
Q3 (Feeling): [A/B/C/D] → [steadfast/delightful/encouraging/seamless]
Q4 (Complexity): [A/B/C/D] → [discreet/patient/meticulous/articulate]
Q5 (Sound): [A/B/C/D] → [ambient/responsive/grounding/precise]
Q6 (Data): [A/B/C/D] → [guardian/collector/messenger/companion]
Q7 (Trust): [A/B/C/D] → [personal/polished/transparent/reliable]
```

This block is your working state. Do NOT show it to the user until the synthesis step.

</answer_tracking>

<step number="3" name="Synthesize Profile">

After all 7 answers, build the personality profile using this mapping:

**Answer-to-Species Matching**

Score each species based on answer alignment. Each answer maps to species traits:

**Q1 (Archetype) weights heavily:**
- Guide → Owl, Hawk, Crane, Elephant, Narwhal
- Companion → Cat, Dog, Capybara, Otter, Dolphin, Sloth, Kiwi
- Craftsperson → Fox, Spider, Ant, Crow/Raven, Gecko, Praying Mantis
- Mentor → Bear, Pangolin, Salamander, Seahorse, Snail

**Q2 (Vibe) filters:**
- Warm/maker → Fox, Otter, Bee, Crow/Raven, Ant, Hamster, Firefly
- Warm/cozy → Cat, Dog, Capybara, Bear, Hedgehog, Sloth, Kiwi
- Cool/precision → Owl, Penguin, Hawk, Mantis Shrimp, Tardigrade, Praying Mantis, Narwhal
- Neutral/minimal → Crane, Lab Mouse, Chameleon, Jellyfish, Gecko, Snail

**Q3 (Emotion) refines:**
- Steadfast → Bear, Elephant, Penguin, Tardigrade, Pangolin, Snail, Narwhal
- Delightful → Axolotl, Otter, Luna Moth, Seahorse, Dolphin, Firefly, Kiwi
- Encouraging → Dog, Bee, Rabbit, Ant, Crow/Raven, Hamster
- Seamless → Cat, Fox, Chameleon, Cuttlefish, Spider, Gecko, Sloth

**Q5 (Sound) as tiebreaker:**
- Purr/hum → Cat, Capybara, Jellyfish, Luna Moth, Sloth, Snail
- Chirp → Rabbit, Bee, Otter, Dolphin, Axolotl, Firefly, Kiwi, Hamster
- Rumble → Bear, Elephant, Pangolin, Tardigrade, Narwhal
- Click → Fox, Mantis Shrimp, Crow/Raven, Spider, Ant, Gecko, Praying Mantis

Select the TOP 3 species that have the most answer alignment. Break ties with Q6 (data relationship) and Q7 (brand approach).

</step>

<step number="4" name="Present Results">

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
YOUR VISUAL PERSONALITY PROFILE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ARCHETYPE: [from Q1 — Guide/Companion/Craftsperson/Mentor]
COLOR WORLD: [from Q2 — warm-craft/warm-cozy/cool-precision/neutral-minimal]
EMOTIONAL CORE: [from Q3 — steadfast/delightful/encouraging/seamless]
COMPLEXITY APPROACH: [from Q4 — discreet/patient/meticulous/articulate]
INTERACTION STYLE: [from Q5 — ambient/responsive/grounding/precise]
DATA RELATIONSHIP: [from Q6 — guardian/collector/messenger/companion]
TRUST SIGNAL: [from Q7 — personal/polished/transparent/reliable]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
TOP 3 SPECIES RECOMMENDATIONS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. [Species] — [2 sentences on why this is the strongest match]
2. [Species] — [2 sentences on why this is a strong alternative]
3. [Species] — [2 sentences on the wild-card option]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

This profile feeds directly into the visual forge.

→ "forge" — Run Full Forge with this profile pre-loaded
→ "quick" — Get 3 quick concepts using this profile
→ "retake Q[N]" — Change your answer to question N
```

</step>

<step number="5" name="Transition">

If user says "forge", transition to **workflows/{DOMAIN}/full-forge.md** with the profile embedded in the vibe/personality fields.

If user says "quick", transition to **workflows/shared/quick-concept.md** with the profile as the vibe input.

If user says "retake Q[N]", re-ask that single question, then recalculate the profile and re-present results.

</step>

</process>

<success_criteria>
- [ ] All 7 questions asked one at a time
- [ ] All answers tracked in structured format
- [ ] Personality profile synthesized with all 7 dimensions
- [ ] Top 3 species recommended with reasoning
- [ ] Transition offered to forge or quick concept
- [ ] Zero agents spawned, zero reference files read
</success_criteria>

<!-- Budget: ~350 lines main context, 0 agents. Pure orchestrator Q&A.
     Architecture note: This is intentionally the ONLY zero-agent workflow.
     Quiz is pure state collection — each question maps to a design parameter,
     and the orchestrator synthesizes answers using static lookup tables.
     Spawning agents for Q&A would add latency and token cost without value,
     since no reference files or creative work are needed. The quiz output
     feeds into forge/quick workflows where agents DO the creative work. -->
