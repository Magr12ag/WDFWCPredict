# WDF World Cup 2026 Prediction Dashboard

A self-contained single-file football prediction dashboard for the FIFA World Cup 2026, built for the WDFNYREC office pool.

## Features

- 🥇 Gold / Silver / Bronze podium with tie-aware logic
- 🏅 Live leaderboard with correct tied rank numbering
- 📊 Prediction statistics bar chart
- 📅 Full match roster with manual score entry
- ⏰ Automatic daily score pull at 08:00 local time from worldcup26.ir
- 🔄 Manual refresh button with live API fallback to cached results
- ➕ Add new participants via the UI

## Scoring Rules

| Result | Points |
|--------|--------|
| Predicted team wins | 3 pts |
| Draw (team still played) | 1 pt |
| Predicted team loses | 0 pts |
| Match not yet played | 0 pts |

## How to Update Scores Manually

1. Open the dashboard
2. Scroll to **Match Roster**
3. Type the home and away scores into the input fields
4. The leaderboard and podium update instantly

## How the Auto-Pull Works

- On page load the dashboard immediately fetches results from ESPN's public scoreboard API (no key required)
- It then re-polls every 15 minutes while the page is open, and again whenever the tab regains focus
- Only matches marked as completed by ESPN are merged in, so half-time scores never lock in points early
- If the fetch fails it falls back to the baked-in API_RESULTS array
- The last pull time is shown under the leaderboard
- You can also click REFRESH SCORES at any time to trigger a manual pull

Note: knockout-round fixtures use placeholder names ("Winner match 73" etc.) until the bracket is known.
Once teams qualify, update the home/away names of those fixtures in DATA.fixtures so the auto-merge can match them.

## How to Add a New Participant

1. Scroll to **+ Add Participant**
2. Enter their name and select their 3 country picks
3. Click **Save Participant**

Note: Participants added via the UI are stored in memory only for that session.
To make them permanent add them to the DATA.predictions array in index.html

## Deployment

### GitHub Pages

1. Push index.html to your repository
2. Go to Settings then Pages
3. Set source to main branch root
4. Your dashboard will be live at https://yourusername.github.io/yourrepo

### Local

Just open index.html in any browser — no server needed.

## Data Sources

- Match fixtures: built-in FIFA World Cup 2026 official schedule
- Live results: ESPN public scoreboard API (site.api.espn.com, fifa.world league)

## Tech Stack

- Pure HTML / CSS / JavaScript — zero dependencies
- localStorage for score persistence across sessions
- Canvas API for the prediction statistics chart

## File Structure

```
index.html   — entire app (single file)
README.md    — this file
.gitignore   — git ignore rules
```

## Participants (32)

Anders, Andrea, Anna K., Anna T., Bennet, Bossba, Cansu, Effie, Elsa M.,
Helen, Jackie, Jakob, Josie, Julia, Kirza, Knut, Leif, Line, Mads J.,
Mads L., Mansingh, Marianne, Martin, Mette, Mikkel, Newton, Sanne, Sharon,
Stephen, Susana, Ulrik, Yves
