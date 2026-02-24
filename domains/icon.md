<domain name="icon">

<description>
Design app icons, module icons, and icon sets through five parallel designer lenses. Icons are functional glyphs that communicate meaning at small sizes — every pixel matters. The icon domain handles context analysis, concept generation, SVG specification, and icon set cohesion audits.
</description>

<workflows>

Choose a workflow based on the request:

<route trigger="forge, design, create, full, from scratch, icon for" workflow="workflows/icon/icon-forge.md">
Icon Forge — context analysis, concept generation, SVG specification. The complete icon pipeline.
</route>

<route trigger="quick, rapid, concepts, 3 ideas" workflow="workflows/shared/quick-concept.md">
Quick Concept — 3 competing icon directions fast. Uses shared workflow with domain=icon.
</route>

<route trigger="audit, review, consistency, set, collection" workflow="workflows/icon/icon-set-audit.md">
Icon Set Audit — consistency review across an existing icon collection.
</route>

<route trigger="svg, generate svg, illustrate" workflow="workflows/shared/svg-forge.md">
SVG Forge — adversarial SVG generation with critique rounds. Uses shared workflow with domain=icon.
</route>

After reading the workflow, follow it exactly.

</workflows>

<inputs>
Required inputs for icon workflows:
- What the icon represents (module, action, concept)
- Context (where it appears, what size, what surrounds it)
- Emotional vibe or design system alignment

Optional:
- Existing icon set to match (style, stroke width, grid)
- Color constraints (monochrome, accent, multi-color)
- Target sizes (16px, 20px, 24px, 32px)
- GSD context
</inputs>

<icon_references>
Icon-specific references in `references/icon/`:
- icon-design-principles.md — Grid systems, stroke conventions, optical corrections, metaphor methodology
- icon-lens-system.md — How each designer lens applies to icon design

Shared references in `references/shared/`:
- brookes-eggleston.md — Shape language fundamentals (circle/square/triangle)
- svg-generation.md — SVG constraints including icon-specific tiers (20/24/32px)
- lens-assignment-rules.md — Vibe-to-lens routing for icons
</icon_references>

</domain>
