# Beat the Box (v3.8)

A lightweight, mobile-friendly card game playable in the browser.  
**Rule fix in this version:** A correct **Same** guess consumes a deck card, keeps the original pile card as-is, and **always triggers a PUSH** (revive an inactive pile, or grant a bonus life if none are inactive).

## Live Demo (Vercel)
You can deploy this repo to Vercel in ~1 minute. See **Deploy to Vercel** below.

## Features
- 3×3 grid, deck counter, bonus lives, streaks & longest streak
- Sound effects + **Sound On/Off** toggle (persisted)
- Optional **Queen theme** audio that plays once when choosing **Lower** on a **Queen**
- Mobile-first layout so the 3×3 grid is always visible
- Custom **card back** upload (persists locally)
- Celebrations for streaks and “margin” guesses ("inch or a mile", etc.)

## How to Run Locally
Just open `index.html` in a browser. No build step needed.

- Double-click `index.html`, or
- Serve it (optional) with a tiny web server:
  ```bash
  python3 -m http.server 5173
  # then open http://localhost:5173 in your browser
  ```

## Deploy to Vercel
1. Create a new GitHub repo and push these files.
2. In Vercel, **New Project** → **Import Git Repository** → select your repo.
3. Framework preset: **Other** (static).  
4. Build Command: **None**  
5. Output Directory: **/** (root)  
6. Deploy.

> Alternatively, drag-and-drop the whole folder into **New → Project** on Vercel.

### Optional: Pre-bundle your Queen audio
Put an audio file at `public/sounds/queen-theme.m4a` and use that URL in the app (paste `/sounds/queen-theme.m4a` in the "Queen Theme (optional audio)" URL box).

## Project Structure
```
.
├─ index.html           # the whole game (HTML/CSS/JS inline)
├─ public/
│  └─ sounds/           # place optional audio here (e.g., queen-theme.m4a)
├─ vercel.json          # helpful defaults for static hosting
├─ .gitignore
├─ LICENSE              # MIT by default
└─ README.md
```

## License
MIT — see `LICENSE`.
