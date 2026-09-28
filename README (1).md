# DrDoctor — Product Marketing Manager Interview Task

An interactive, three-page presentation deck built for the DrDoctor Product Marketing Manager interview task.

- **Page 1 — Cover**
- **Page 2 — Part 1: A messaging house for Agentic Voice** (core value proposition, four pillars, proof bar)
- **Page 3 — Part 2: A launch plan outline** (new capability, objective, audience, phasing, sales enablement, success metrics)

Prepared by **Yash Chaudhary**.

## Tech

A single, self-contained static page. All CSS and JavaScript are inline, and the cover image is embedded as a base64 data URI, so there are **no external assets or build step**.

- HTML + CSS + vanilla JavaScript
- Fonts loaded from Google Fonts (with system fallbacks if offline)
- Keyboard (← / →), on-screen arrows, side dots and touch-swipe navigation

## Project structure

```
.
├── index.html      # the entire deck (self-contained: HTML, CSS, JS, embedded image)
├── vercel.json     # static hosting config
├── .gitignore
└── README.md
```

## Run locally

No dependencies. Either open the file directly:

```bash
open index.html          # macOS
# or just double-click index.html
```

Or serve it (recommended, so fonts and routing behave like production):

```bash
# Python 3
python3 -m http.server 8000
# then visit http://localhost:8000

# or Node
npx serve .
```

## Deploy to Vercel

This is a zero-config static site — Vercel serves `index.html` at the root automatically.

**Option A — Git (recommended)**

1. Create a new GitHub repository and push this folder:
   ```bash
   git init
   git add .
   git commit -m "DrDoctor interview deck"
   git branch -M main
   git remote add origin https://github.com/<your-username>/drdoctor-interview-deck.git
   git push -u origin main
   ```
2. In [Vercel](https://vercel.com/new), import the repository.
3. Framework preset: **Other** (no build). Leave Build Command empty and Output Directory as the root.
4. Deploy.

**Option B — Vercel CLI**

```bash
npm i -g vercel
vercel        # preview
vercel --prod # production
```

## Notes

- The deck is responsive (laptop / tablet / phone).
- Nothing here requires a server runtime; it is a purely static page.
