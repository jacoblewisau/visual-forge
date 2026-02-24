<domain name="button">

<description>
Design illustrated buttons and action elements through five parallel designer lenses. Illustrated buttons combine functional UI components with character-driven artwork — they must be instantly readable as interactive elements while carrying visual personality. The button domain handles context analysis, concept generation, state design, and button set cohesion.
</description>

<workflows>

Choose a workflow based on the request:

<route trigger="forge, design, create, full, from scratch, button for" workflow="workflows/button/button-forge.md">
Button Forge — context analysis, concept generation, state design, SVG specification. The complete button pipeline.
</route>

<route trigger="quick, rapid, concepts, 3 ideas" workflow="workflows/shared/quick-concept.md">
Quick Concept — 3 competing button directions fast. Uses shared workflow with domain=button.
</route>

<route trigger="svg, generate svg, illustrate" workflow="workflows/shared/svg-forge.md">
SVG Forge — adversarial SVG generation with critique rounds. Uses shared workflow with domain=button.
</route>

After reading the workflow, follow it exactly.

</workflows>

<inputs>
Required inputs for button workflows:
- What action the button triggers (save, delete, submit, navigate)
- Context (where it appears, what screen, what surrounds it)
- Emotional vibe or design system alignment

Optional:
- Existing button styles to match
- Illustration level (subtle accent vs. fully illustrated)
- Target sizes (32px, 40px, 48px)
- State requirements (hover, pressed, disabled, loading)
- GSD context
</inputs>

<button_references>
Button-specific references in `references/button/`:
- button-design-principles.md — Illustrated button anatomy, state design, personality calibration
- button-lens-system.md — How each designer lens applies to button illustration

Shared references in `references/shared/`:
- brookes-eggleston.md — Shape language fundamentals
- svg-generation.md — SVG constraints including button-specific tiers (32/40/48px)
- lens-assignment-rules.md — Vibe-to-lens routing for buttons
</button_references>

</domain>
