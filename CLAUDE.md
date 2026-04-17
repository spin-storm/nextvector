# NextVector Site

## Build Approach
Build as a **static single-page HTML site** deployed via **GitHub Pages**. Do NOT use WordPress.

## Workflow
1. Generate all images with `nanobanana "prompt" -o images/filename.png -n -q` (run in parallel with `&` + `wait`)
2. Build `index.html` with all CSS/JS inline
3. Generate a standalone preview with images base64-encoded so user can open locally
4. Deploy to GitHub Pages

## Design System (proven on spin-storm.com)
- Background: `#03020F` deep dark
- Primary: `#7B3FFF` purple
- Secondary: `#FF3F8E` pink  
- Accent: `#FFD700` gold
- Cyan: `#00F0FF`
- Fonts: **Orbitron** (headings), **Inter** (body) via Google Fonts
- Style: glassmorphism cards, neon glow effects, animated particle canvas, scroll reveal animations

## GitHub Deploy
- Create repo: `gh api --method POST /user/repos --field name="reponame"`
- Auth: `GH_TOKEN=<pat> gh api ...` — use PAT, not password
- Add CNAME file for custom domain
- GitHub Pages A records: `185.199.108-111.153`
- CNAME www → `username.github.io`

## Tools
- `nanobanana` is at `/Users/robbie/bin/nanobanana`
- Syntax: `nanobanana "prompt" -o output.png -n -q`
- Reference site: `/Users/robbie/ss/site/index.html` (spin-storm.com)
- Reference theme files: `/Users/robbie/ss/spinstorm/`
