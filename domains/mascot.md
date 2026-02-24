<domain name="mascot">

<description>
Design app mascots and brand characters through five parallel designer lenses. From narrative development through SVG illustration, the mascot domain handles creature selection, personality mapping, visual direction, UI integration, family cohesion audits, and adversarial SVG generation.
</description>

<workflows>

Choose a workflow based on the request:

<route trigger="full, from scratch, complete, design a mascot" workflow="workflows/mascot/full-forge.md">
Full Forge — narrative + visual + integration. The complete mascot creation pipeline.
</route>

<route trigger="narrative, story, name, personality" workflow="workflows/mascot/narrative.md">
Narrative Only — story, personality, species selection, and naming.
</route>

<route trigger="visual, look, art direction, illustration style" workflow="workflows/mascot/visual-direction.md">
Visual Direction — given a narrative, define visual identity.
</route>

<route trigger="integration, UI, touchpoints, where does it appear" workflow="workflows/shared/integration.md">
Integration Plan — mascot-to-UI touchpoints. Uses shared workflow with domain=mascot.
</route>

<route trigger="family, audit, cohesion, multiple mascots" workflow="workflows/mascot/family-audit.md">
Family Audit — cohesion review of a multi-mascot ecosystem.
</route>

<route trigger="quick, rapid, concepts, 3 ideas" workflow="workflows/shared/quick-concept.md">
Quick Concept — 3 competing mascot ideas fast. Uses shared workflow with domain=mascot.
</route>

<route trigger="quiz, personality, discover, help me figure out" workflow="workflows/shared/personality-quiz.md">
Personality Quiz — 7 questions to discover the mascot personality. Uses shared workflow with domain=mascot.
</route>

<route trigger="svg, illustrate, generate svg" workflow="workflows/shared/svg-forge.md">
SVG Forge — adversarial SVG generation with critique rounds. Uses shared workflow with domain=mascot.
</route>

After reading the workflow, follow it exactly.

</workflows>

<inputs>
Required inputs for mascot workflows:
- App name (or "help me name it")
- What the app does (1-2 sentences)
- Target audience
- Emotional vibe (warm/precise/playful/etc.)

Optional:
- Existing brand elements (colors, typography, dark mode)
- GSD context (reads PROJECT.md/ROADMAP.md)
- Lens preference (Auto recommended, or specify 2 contrasting lenses for Agents B/C. Agent A always uses Raroque, all concepts get Eggleston quality gate)
</inputs>

<mascot_references>
Mascot-specific references in `references/mascot/`:
- chris-raroque.md — Warmth lens (pet naming, beauty as feature)
- greg-hartman.md — Systems lens (shape language, character casts)
- healing-character.md — Healing lens (exhaustion as empathy)
- burnt-toast.md — Cynicism lens (playful wit, sticker-ready)
- narrative-framework.md — Species mapping, naming conventions

Shared references in `references/shared/`:
- brookes-eggleston.md — Quality gate for all concepts
- visual-language.md — Color palettes, expressions, size cascade
- svg-generation.md — SVG constraints, critique checklist
- integration-patterns.md — UI touchpoints
- lens-assignment-rules.md — Vibe-to-lens routing
</mascot_references>

</domain>
