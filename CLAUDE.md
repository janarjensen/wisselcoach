# Wisselcoach MO9

Single-page app (one file: `index.html`, no build step) that helps coach the girls' U9 hockey team:
fill in the team, run the match clock, and get an alarm when a substitution is due.

- Match: 2 × 25 min (configurable). The clock stops itself at half time and waits for "Start 2e helft",
  so the length of the break doesn't matter.
- Schedule is generated per line (voorhoede / achterhoede): whoever has played most goes to the bench,
  ties broken by the rotation order set on the "Invullen" tab. Injuries mid-match re-plan the rest.
- State lives in `localStorage` on the device (key prefix `wisselcoach-mo9-v1`).
- Hosted on GitHub Pages: repo https://github.com/janarjensen/wisselcoach, site
  https://janarjensen.github.io/wisselcoach/ (push to `main` deploys).
- Also published as a claude.ai Artifact: https://claude.ai/artifact/K6t9sU2xkx33XEmnswCD24.
  After every change, push to GitHub **and** republish the Artifact (pass that URL), so both stay in sync.
- Bump `APP_VERSION` in `index.html` (Dutch date + time, e.g. `"1 okt, 11:15"`) on every change. GitHub Pages
  caches for 10 minutes, and the coach checks the version shown at the bottom of the Wedstrijd and Invullen tabs.
- The repo is public: never commit the players' real names. Real names live only in the coach's localStorage.
- UI text is Dutch.
