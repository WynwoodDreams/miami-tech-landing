# Miami Tech Landing — Tech Portfolio / 26

A single-page landing site for the **Job Stats Miami** 2026 cohort, showcasing 24 student build projects across 8 career tracks (AI, Cloud, CS, Cyber, Data, Help Desk, Software, IT Support).

## Stack

- Plain HTML + CSS + vanilla JS — no build step, no dependencies
- Google Fonts: Inter, JetBrains Mono
- Project data sourced from [WynwoodDreams/4Projects](https://github.com/WynwoodDreams/4Projects)

## Run locally

Open `index.html` directly in a browser, or serve the directory:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Structure

- `index.html` — entire site (markup, styles, project data, render logic)
  - **Topbar / ticker** — branding, live status, news ticker
  - **Left panel** — headline, cohort metrics, console log
  - **Right dashboard** — path-filter tabs and project grid
  - **`PROJECTS` array** (in the trailing `<script>`) — single source of truth for the 24 cards
  - **`PATHS` array** — the 8 career tracks plus an "All" view

## Editing projects

Each project entry has the shape:

```js
{
  id: 'PRJ_A01',
  path: 'ai',                    // matches a PATHS id
  level: 'intermediate',         // beginner | intermediate | advanced
  title: '...',
  summary: '...',
  tech: ['Python', 'FastAPI']
}
```

Add or remove items in the `PROJECTS` array and the grid + tab counts update automatically.

## Deploying

Static site — drop the directory on any static host (Vercel, Netlify, GitHub Pages, S3 + CloudFront).
