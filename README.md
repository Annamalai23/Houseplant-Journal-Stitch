# Houseplant Journal – Verdant

A mobile-first web app for tracking your houseplant collection with photos, watering streaks, and a gentle “plant graveyard” to remember the ones you’ve lost. The UI is designed as a **digital greenhouse**: more like a botanical journal than a traditional utility app. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)

## Features

- Curated “My Collection” view with hero emphasis on priority-care plants (e.g., Fiddle Leaf Fig, Monstera, Snake Plant, Aloe). [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- Hydration status per plant: needs water, days left, and simple growth milestones like “grown 2 inches this month.” [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- Soft, editorial layout built with Tailwind, serif + sans-serif pairing (Noto Serif + Plus Jakarta Sans) for a magazine-like feel. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- Tonal, borderless UI: sections are separated using surface background shifts instead of 1px lines. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- Support for a “plant graveyard” concept in the product vision, to reflect plants you’ve lost while keeping the experience kind and reflective. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)

## Design System: “The Digital Greenhouse”

The design is driven by a custom system documented in `DESIGN.md` and inspired by a botanical editorial aesthetic. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)

- Color tokens for surfaces and states (`surface`, `surface-container-low`, `primary`, `tertiary`, etc.), mapped in `code.html` via Tailwind’s `extend.colors`. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- No hard borders: separation via background tones like `surface-container-low` (#f5f3ef) on `surface` (#fbf9f5). [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- Soft elevation via tonal layering and ultra-diffused shadows, instead of harsh drop-shadows. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- Roundedness scale using large radii (`lg`, `xl`, `full`) to avoid sharp edges and maintain an approachable look. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- Typography roles:
  - **Headline**: Noto Serif for plant names, section headers, story moments.
  - **Body/Label**: Plus Jakarta Sans for navigation, metadata, and care instructions. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)

See `DESIGN.md` for detailed rules like glassmorphism usage, “ghost borders,” and do/don’t guidelines. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)

## Tech Stack

- Static HTML prototype in `code.html` using Tailwind CSS via the CDN configuration block. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- Tailwind theme extension for:
  - Color tokens (botanical palette: deep greens, terracotta, warm neutrals). [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
  - Font families (`headline`, `body`, `label`) mapped to Noto Serif and Plus Jakarta Sans. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
  - Custom radii (`DEFAULT`, `lg`, `xl`, `full`) for cards, buttons, and pills. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- Material Symbols icon font for inline UI icons (e.g., `add_circle`, `water_drop`, `local_florist`). [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)

## Current Screens

The primary screen in `code.html` is a “My Collection” view titled **Verdant – Personal Oasis** with:

- A search bar and “Sort / Add New Plant” controls. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- A “Priority Care” section featuring key plants and a “Water Now” action. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- A Growth Milestone card and a quote block (“To plant a garden is to believe in tomorrow.” – Audrey Hepburn). [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)
- Bottom navigation with home, add, and plants icons. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)

See `screen.png` for a snapshot of the current layout. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)

## Running the Prototype

Because the current version is a static prototype:

1. Clone the repository:
   ```bash
   git clone https://github.com/Annamalai23/Houseplant-Journal-Stitch.git
   cd Houseplant-Journal-Stitch
   ```
2. Open `code.html` in your browser:
   - Double-click the file, or
   - Serve it with any static server (e.g., VS Code Live Server, `python -m http.server`). [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)

No build step is required at this stage; Tailwind is configured inline via the CDN snippet in the HTML. [github](https://github.com/Annamalai23/Houseplant-Journal-Stitch)

## Roadmap Ideas

- Turn the static prototype into a real mobile web app with a JS framework (React/Next, SvelteKit, or similar).
- Persist plant data (e.g., localStorage first, then Supabase/Firebase backend).
- Implement watering reminders, streaks, and notifications.
- Add a “Plant Graveyard” view with reflective notes and photos.
- Multi-device sync and photo uploads for each plant.

## License

Add a license of your choice here (for example, MIT) once you’re ready to open-source usage terms.
