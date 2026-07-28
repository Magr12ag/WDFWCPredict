# WDF World Cup 2026 Prediction Dashboard

A self-contained single-file football prediction dashboard for the FIFA World Cup 2026, built for the WDFNYREC office pool.

## Live Site
[magr12ag.github.io/WDFWCPredict](https://magr12ag.github.io/WDFWCPredict/)

## Features
- 🥇 Gold / Silver / Bronze podium with tie-aware logic (max 3 per step, expand for more)
- 🏅 Live leaderboard with points, W/D/L, goal difference and GF:GA
- 📊 Prediction statistics bar chart
- 🗺️ Tournament bracket progression (Group Stage → R32 → R16 → QF → SF → Final)
- 📅 Match roster with live/upcoming/completed sections
- 🎭 Animated handover scene: sad Norwegian Viking → triumphant Argentine warrior
- ➕ Add new participants via the UI

## Scoring Rules
| Result | Points |
|---|---|
| Predicted team wins | 3 pts |
| Draw (team still played) | 1 pt |
| Predicted team loses | 0 pts |
| Tiebreaker | Goal difference → Goals scored |

## Participants (32)
Anders, Andrea, Anna K., Anna T., Bennet, Bossba, Cansu, Effie, Elsa M., Helen, Jackie, Jakob, Josie, Julia, Kirza, Knut, Leif, Line, Mads J., Mads L., Mansingh, Marianne, Martin, Mette, Mikkel, Newton, Sanne, Sharon, Stephen, Susana, Ulrik, Yves

## Deployment
Push `index.html` to the `main` branch root. GitHub Pages serves it automatically at your Pages URL.

## Tech Stack
Pure HTML / CSS / JavaScript — zero dependencies. Single file.
