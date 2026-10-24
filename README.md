# GeoDash Multiplayer

A private-room GeoGuessr-style game using Mapillary street imagery, MapLibre/OpenFreeMap, and Firebase Realtime Database.

## Run locally
1. Open this `geodash` folder in VS Code.
2. Run `index.html` with Live Server.
3. Create a room, share the 5-character code, and have friends join the same hosted site.

## Important: friends cannot join your localhost URL
`127.0.0.1` only exists on your own PC. For internet multiplayer, deploy this folder to GitHub Pages, Firebase Hosting, Netlify, etc. All players must open the same public site.

## Firebase project used
This build is configured for the GeoDash Firebase project created during setup (`geodash-447d1`). Anonymous Authentication and Realtime Database must remain enabled.

## Development security
The database was initially created in Firebase Test Mode. Before sharing the game publicly, replace Test Mode with proper Realtime Database security rules. Do not leave an internet-facing database permanently in Test Mode.

## Gameplay
- 2-8 players recommended
- Host creates a room and shares a 5-character code
- Host chooses rounds and timer
- Every player receives the same exact Mapillary image ID
- Guesses are hidden until the round ends
- Round ends when all online players guess or the timer expires
- Scores are 0-5,000 per round using the existing GeoDash distance formula
- Host advances rounds; final leaderboard appears after the last round
