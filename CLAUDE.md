# Wisselcoach MO9

Single-page app (one file: `index.html`, no build step) that helps coach the girls' U9 hockey team:
fill in the team, run the match clock, and get an alarm when a substitution is due.

- Match: 2 × 25 min (configurable). The clock stops itself at half time and waits for "Start 2e helft",
  so the length of the break doesn't matter.
- Schedule is generated per line (voorhoede / achterhoede): whoever has played most goes to the bench,
  ties broken by the rotation order set on the "Invullen" tab. Injuries mid-match re-plan the rest.
- State lives in `localStorage` on the device (key prefix `wisselcoach-mo9-v1`).
- The page is also published as a claude.ai Artifact; republish from this file after changes.
- UI text is Dutch.
