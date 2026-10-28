---
name: DAISY Lab
description: "A research lab site in the spirit of IBM's Carbon system: IBM Plex Sans with light-weight display type, square corners, flat surfaces told apart by a step in tone, and one accent, the daisy's yellow. The subject supplies the pictures: the daisy whose petals are the lab's research directions, a live diffusion network, a working Text-to-SQL console, and real photographs of the campus."

colors:
  paper: "#fcfcfb"          # the ground
  surface: "#f1f2ef"        # one tone step: page heads, toned sections, panels
  surface-2: "#e4e6e1"
  ink: "#161719"            # running text is always full ink or ink-2
  ink-2: "#3f454c"
  muted: "#5d646d"          # secondary notes only
  daisy: "#f2c434"          # the one accent: current page, link underlines, join band, data
  daisy-soft: "#fbf0c4"
  link: "#1d4f80"
  rule: "#d9dcd6"           # tables and form fields only
  dark: { paper: "#111315", surface: "#1b1e21", surface-2: "#272b2f", ink: "#eceee9", ink-2: "#c0c6cb" }

typography:
  family: IBM Plex Sans (interface, headings), Source Serif 4 (Markdown bodies, paper titles), IBM Plex Mono (code only)
  display: { size: "clamp(3.5rem, 7.4vw, 7rem)", weight: 300, tracking: "-0.045em" }   # the lab's name, home hero
  h1: { size: "--fs-3xl", weight: 300, tracking: "-0.03em" }
  h2: { size: "--fs-xl", weight: 400, tracking: "-0.02em" }
  h3: { size: "--fs-lg", weight: 600 }
  body: { size: 16px, line-height: 1.6 }

rounded: 0px everywhere; circles only for small author avatars
spacing: { section: "clamp(64px, 9vw, 128px)", gutter: "clamp(16px, 4vw, 40px)", wrap: 1240px }
---

# Rules

These keep the site looking designed rather than generated. Check new pages against them.

- **No thin lines** as dividers, outlined boxes or card borders. Separate things with space, or with a step in tone (`--surface`, `--tint`). Tables and form fields keep their lines.
- **No shadows** on things at rest. Only what floats (the More menu) casts one.
- **No gradients, no glows, no glass, no blur.** Flat colour or a real photograph.
- **No small label above a heading.** Put the type, date or category under the heading, in the meta line.
- **Monospace only for real code** (the SQL console, BibTeX).
- **One accent.** Yellow marks the current page, link underlines, data and the join band; nothing else is coloured.
- **Headings stay on two lines or fewer.** Long paper titles use the smaller title size.
- **Pictures are real.** Lab photos, the director's portrait, the campus from Wikimedia Commons (credited in `src/data/photo-credits.json`, shown on /about/#photo-credits). Never stock photos, never AI images.
- **Motion has a job.** The diffusion network and the daisy are the signature; sections enter part by part once; the campus photo drifts with the scroll. Everything respects `prefers-reduced-motion`.
- **Browser surfaces are themed:** selection, caret, scrollbar, focus ring, tabular figures.

# Adding a photograph from Wikimedia Commons

1. Put the file in `public/images/campus/` (about 2000px wide, quality 80).
2. Add an entry to `src/data/photo-credits.json` with caption, author, licence and source page.
