---
name: visual-forge
aliases:
  - mascot
  - icon-forge
  - button-forge
  - character-design
  - app-mascot
  - character
description: Create SVG visual assets — mascots, icons, and illustrated buttons — through five parallel designer lenses. Use when designing brand characters, app icons, icon sets, illustrated buttons, or auditing visual asset families.
---

<objective>
Design deeply integrated visual assets for apps through five complementary designer lenses. Three domains — mascots, icons, and illustrated buttons — share a common creative architecture: parallel subagents channeling different philosophies produce diverse concepts while keeping the main context lean. Chris Raroque provides warmth. Greg Hartman brings scalable systems. Japanese healing characters offer empathy. Burnt Toast delivers playful cynicism. Brookes Eggleston provides structural quality checks applied to every concept.
</objective>

<quick_start>
State what the asset is for and the emotional vibe. The orchestrator routes to the right domain automatically.

Examples:
- "Design a mascot for my lab app — precise and scientific" → mascot domain
- "I need an icon for a DNA module — clean and minimal" → icon domain
- "Create an illustrated save button — warm and friendly" → button domain

For the fastest path, say "quick concept" with a domain — 3 competing directions in under a minute.
</quick_start>

<essential_principles>

<story_first>
For mascots, narrative before visual. Story constrains design. For icons and buttons, context before form — the asset's purpose and emotional register must be clear before any shapes are drawn.
</story_first>

<shape_language>
Brookes Eggleston's fundamentals apply to every domain. Circle = friendly. Square = stable. Triangle = danger. Silhouette test everything. Budget colors ruthlessly. These rules scale from full-body mascots down to 16px icons.
</shape_language>

</essential_principles>

<domain_routing>

Determine the domain from the request, then read the corresponding domain router. If ambiguous, ask.

<route trigger="mascot, character, creature, pet, brand character, forge mascot, full forge, narrative, family audit" domain="domains/mascot.md">
Design a mascot for my app. I need a character.
</route>

<route trigger="icon, icon set, module icon, glyph, symbol, pictogram" domain="domains/icon.md">
I need an icon for a module. Design an icon set.
</route>

<route trigger="button, illustrated button, action button, CTA, save button" domain="domains/button.md">
Create an illustrated button. Design a save action button.
</route>

After reading the domain file, follow its routing to the appropriate workflow.

</domain_routing>

<agent_architecture>

Parallel subagent spawning keeps main context minimal. Creative work happens in isolated agent contexts. Main receives structured summaries only.

SKILL_DIR resolution: Before spawning, resolve `{SKILL_DIR}` to absolute path. All agent prompts use `{SKILL_DIR}/references/...` — substitute resolved path.

Agent prompt structure: Role line, read references, context block, numbered instructions, output format template. Vary direction lines across parallel agents for creative diversity.

Orchestrator discipline (HARD RULE): Main context NEVER reads references, generates content, or pastes full agent output. ONLY: gather inputs, spawn agents, synthesize returns, coordinate waves.

</agent_architecture>

<gsd_integration>

This skill integrates with GSD at these points:

1. Phase planning: Read PROJECT.md, ROADMAP.md, phase CONTEXT.md. Output spec as `.planning/phases/{phase}/ASSET-SPEC.md`.
2. Execution: Reference ASSET-SPEC.md for visual constants, integration plan provides component locations.
3. As artifact: `@.planning/phases/{phase}/ASSET-SPEC.md` in PLAN.md context references.
4. Cross-phase: Family DNA / icon set cohesion ensures consistency across modules.

</gsd_integration>

<reference_index>

All in `references/`. Agents read these — orchestrator never reads directly.

<ref file="shared/brookes-eggleston.md" lines="~183">Quality gate (all domains)</ref>
<ref file="shared/visual-language.md" lines="~217">Color palettes, expressions</ref>
<ref file="shared/svg-generation.md" lines="~220">SVG size rules, critique (mascot + icon + button tiers)</ref>
<ref file="shared/integration-patterns.md" lines="~177">UI touchpoints</ref>
<ref file="shared/lens-assignment-rules.md" lines="~60">Vibe-to-lens routing (3 domains)</ref>
<ref file="mascot/chris-raroque.md" lines="~146">Warmth lens</ref>
<ref file="mascot/greg-hartman.md" lines="~166">Systems lens</ref>
<ref file="mascot/healing-character.md" lines="~204">Healing lens</ref>
<ref file="mascot/burnt-toast.md" lines="~165">Cynicism lens</ref>
<ref file="mascot/narrative-framework.md" lines="~171">Species mapping, naming</ref>
<ref file="icon/icon-design-principles.md" lines="~200">Grid, stroke, clarity, Apple HIG alignment</ref>
<ref file="icon/icon-lens-system.md" lines="~90">How 5 lenses apply to icons (HIG quality gate)</ref>
<ref file="icon/apple-hig-sf-symbols.md" lines="~200">SF Symbols grid, weights, scales, rendering modes, custom design</ref>
<ref file="button/button-design-principles.md" lines="~100">Illustrated button methodology</ref>
<ref file="button/button-lens-system.md" lines="~70">How 5 lenses apply to buttons</ref>

</reference_index>

<error_handling>

Agent spawn failures: If an agent returns empty or errors, retry once. If it fails again, continue with the remaining agents and note the gap. Never block on a single agent failure.

Incomplete inputs: If required fields are missing after asking once, provide sensible defaults based on available context and confirm before proceeding.

Reference file not found: If `{SKILL_DIR}` resolution fails or a reference file is missing, tell the user which file is expected and where. Do not attempt creative work without reference material — the references ARE the design methodology.

Agent returns off-format: If an agent's output doesn't match the requested structure, extract what's usable and present it. Do not re-spawn just for formatting — synthesize the content into the expected format.

Reference file corrupted or truncated: If a reference file exists but appears corrupted, truncated, or returns garbled content: note which file has issues, attempt to proceed with partial content if usable, otherwise fail gracefully with specific guidance on which file needs attention. Do not silently skip corrupted references.

</error_handling>

<success_criteria>
A complete forge produces domain-appropriate deliverables:

Mascot: name, narrative, visual direction, integration plan, family DNA, GSD artifact, SVG illustrations.
Icon: context analysis, 3 concept directions, final SVG spec with size tiers, icon set cohesion audit.
Button: context analysis, 3 concept directions, final SVG spec with state design, button set cohesion.

All creative work happens in subagent contexts. Main never reads references.
</success_criteria>
