# Portfolio image drop folder

Drop new portfolio screenshots / workflow images here. Then tell Claude
"add these to the site" with a short blurb per image and they'll be wired
into `index.html` as new portfolio cards.

## Naming
- Use the project / workflow name with normal capitalization and spaces
  (e.g., `Stripe Refund Router.png`). Matches the existing convention.
- PNG preferred. JPG/JPEG/SVG also fine.

## Per-image info Claude needs to build a card
- **Title** (short, ~5-8 words)
- **One-line description** (what it does)
- **Benefits** (3-4 bullets, pipe-separated when handed to Claude)
- **Ideal for** (one sentence: who this is for)
- **Tech tags** (3 max, e.g., `n8n`, `Gmail`, `OpenAI`)
- **Status** (Live / Demo / Case study)

If you only drop the image with no notes, Claude will draft copy from
the filename + memory profile and ask you to confirm.
