# genrock-aiblock

Reusable UI design skill with a consistent **Genrock Industrial** identity: IBM Plex Sans, solid surfaces, precise borders, restrained forest-green accents, and direct copy.

## What is included

- [SKILL.md](SKILL.md): workflow, modes, identity contract, and module routing.
- [Visual foundation](reference/foundation.md): typography, colors, density, spacing, shapes, theme, and native guidance.
- [Design Integrity](reference/design-integrity.md): honesty, functionality, purposeful visual techniques, and consistency.
- [UI patterns](reference/ui-patterns.md): forms, tables, navigation, interaction states, and accessibility.
- [Delivery gate](reference/delivery-gate.md): evidence-based PASS / FAIL / NOT TESTED / N/A checks.
- [DESIGN.md template](templates/DESIGN.md): product-specific design direction.
- [CSS tokens](assets/genrock-tokens.css): web starter, not a complete component library.
- [Single-file skill](genrock-aiblock.md): all modules and tokens in one document.
- [Industrial preview](previews/industrial.html): downloadable static visual reference with embedded IBM Plex Sans.

## Use in Replit

Download genrock-aiblock.md and add it through workspace settings → Knowledge → Skills. A file in this repository is not automatically active in your Replit conversations.

## Use with folder-based agents

Copy SKILL.md, reference/, templates/, and assets/ into your agent’s supported skills location under genrock-aiblock/. For agents that support .agents/skills/, the resulting path is .agents/skills/genrock-aiblock/SKILL.md. Verify discovery requirements in your tooling.

Example request:

> Pakai genrock-aiblock. Buat UI booking dengan Genrock Industrial, IBM Plex Sans, comfortable density. Jangan membuat testimoni atau angka palsu.

Audit without editing:

> Audit UI ini dengan genrock-aiblock. Laporkan masalah dan rekomendasi tanpa mengubah kode.

## Principles

Keep a shared visual identity without imposing one layout on every product. Choose structure and density from user tasks. Do not fabricate claims or present demo behavior as a working backend. Report what was actually tested.

## Preview and font license

Open previews/industrial.html locally in a browser; GitHub displays its source rather than hosting a live app. It contains labeled example data and visual-only controls. IBM Plex Sans font data is included for this preview under the [SIL Open Font License](licenses/IBM-Plex-OFL.txt). Production apps must load their own licensed font assets.

## Scope and version

Version 1.0. This is a design skill, not a runnable app or a guarantee of WCAG compliance. Representative palette checks do not replace UI testing. No private profile, credentials, temporary files, or unrelated app code are included.

## Inspiration

The discussion of purpose-based filtering and direction/verification separation was inspired by [initial reference](https://github.com/miqdadbadjuber/anti-slop). Genrock rules are independently written for the Industrial direction; this repository is not affiliated with that project or Replit’s design system.
