# Visual Forge

A Claude Code skill for designing SVG visual assets — mascots, icons, and illustrated buttons — through five complementary designer lenses. Parallel creative agents channel different philosophies to produce diverse concepts, while an orchestrator synthesizes and presents the strongest options.

## What It Does

Visual Forge takes a description of what you need and spawns parallel creative agents — each channeling a different design philosophy — to produce competing visual concepts. Three domains share a common architecture:

| Domain | What You Get |
|--------|-------------|
| **Mascot** | Brand characters with narrative, visual direction, voice, integration plan, SVG illustrations |
| **Icon** | Functional glyphs with metaphor analysis, grid-aligned SVGs, icon set cohesion |
| **Button** | Illustrated action elements with state design, personality calibration, SVG output |

## The Five Lenses

| Lens | Designer | Philosophy |
|------|----------|------------|
| **Warmth** | Chris Raroque | Pet-naming, beauty-as-feature, personal storytelling |
| **Systems** | Greg Hartman | Shape language, cast building, animation-first (Duolingo) |
| **Empathy** | Japanese Healing Characters | Exhaustion-as-cuteness, passive presence (San-X: Tarepanda, Rilakkuma) |
| **Cynicism** | Scott Martin / Burnt Toast | Soft surfaces + sharp personality, sticker-ready geometric |
| **Fundamentals** | Brookes Eggleston | Quality gate: shape theory, silhouette test, color budget (applied to ALL) |

## Installation

### As a Claude Code Skill

Symlink or copy the directory to your Claude Code skills location:

```bash
ln -s /path/to/visual-forge ~/.claude/skills/visual-forge
```

Then invoke in Claude Code with:
- `/visual-forge` or `/mascot` or `/icon-forge` or `/button-forge`
- Or naturally: "design a mascot for my app" / "I need an icon for this module" / "create an illustrated save button"

## File Structure

```
visual-forge/
├── SKILL.md                              # Domain dispatcher
├── README.md                             # This file
│
├── domains/                              # Domain routers
│   ├── mascot.md                         # Mascot workflows + inputs
│   ├── icon.md                           # Icon workflows + inputs
│   └── button.md                         # Button workflows + inputs
│
├── workflows/
│   ├── shared/                           # Parameterized by {DOMAIN}
│   │   ├── quick-concept.md              # 3 parallel creative agents
│   │   ├── svg-forge.md                  # Generate → critique → refine loop
│   │   ├── integration.md                # Asset → UI placement
│   │   └── personality-quiz.md           # Zero-agent Q&A discovery
│   ├── mascot/                           # Mascot-specific
│   │   ├── full-forge.md                 # 3-wave pipeline
│   │   ├── narrative.md                  # Story + species + naming
│   │   ├── visual-direction.md           # Species anatomy + expressions
│   │   └── family-audit.md              # Multi-mascot cohesion
│   ├── icon/                             # Icon-specific
│   │   ├── icon-forge.md                 # Context → concepts → spec → SVG
│   │   └── icon-set-audit.md            # Consistency review
│   └── button/                           # Button-specific
│       └── button-forge.md               # Context → concepts → spec → SVG
│
└── references/
    ├── shared/                           # Universal design principles
    │   ├── brookes-eggleston.md          # Shape language + quality gate
    │   ├── visual-language.md            # Color palettes + style
    │   ├── svg-generation.md             # SVG rules (3 domain tiers)
    │   ├── integration-patterns.md       # UI touchpoints
    │   └── lens-assignment-rules.md      # Vibe → lens (3 domains)
    ├── mascot/                           # Character-specific
    │   ├── chris-raroque.md              # Warmth lens
    │   ├── greg-hartman.md               # Systems lens
    │   ├── healing-character.md          # Healing lens
    │   ├── burnt-toast.md                # Cynicism lens
    │   └── narrative-framework.md        # Species mapping + naming
    ├── icon/                             # Icon-specific
    │   ├── icon-design-principles.md     # Grid, stroke, clarity
    │   └── icon-lens-system.md           # Lenses applied to icons
    └── button/                           # Button-specific
        ├── button-design-principles.md   # Illustrated button methodology
        └── button-lens-system.md         # Lenses applied to buttons
```

## Credits

The designer lenses are based on publicly available work, published courses, blog posts, and portfolio analysis of:

- **Chris Raroque** — [chrisraroque.com](https://chrisraroque.com), indie app developer (Amy, Luna, Ellie, Lily)
- **Greg Hartman** — Head of Art at Duolingo, ["Shape Language: Duolingo's Art Style"](https://blog.duolingo.com/author/greg/)
- **Hikaru Suemasa** — Creator of Tarepanda (San-X), Professor at Tama Art University
- **Aki Kondo** — Creator of Rilakkuma (San-X), freelance illustrator
- **Yuri Yokomizo** — Creator of Sumikko Gurashi (San-X)
- **Scott Martin / Burnt Toast Creative** — [burnttoast.myportfolio.com](https://burnttoast.myportfolio.com), co-founder of Doodles
- **Brookes Eggleston** — Founder of Character Design Forge, author of *Character Design Made Easy*

## License

MIT
