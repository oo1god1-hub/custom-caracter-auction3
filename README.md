# Custom Character Auction

A real-time multiplayer character auction game for up to 3 players.

## Run on Replit

1. Create a new **Node.js** Replit project.
2. Upload/extract this ZIP into the project so `package.json` and `server.js` are at the project root.
3. Open the Shell and run:

   ```bash
   npm install
   ```

4. Click Run. The app starts with `npm start` (or configure the Run command to `npm start`).
5. Open the Replit web preview. For multiplayer testing, open the published/deployed app URL on separate devices or browser sessions.

## Game rules included

- 3 players maximum per room; at least 2 to start.
- 10,000 coins per player.
- 15 fixed characters with fixed starting prices, tiers, and power.
- Sheetal (100), Riya (99), and Chanchal (98) are the three strongest.
- 20-second opening timer; each valid bid resets it to 10 seconds.
- Highest bidder wins; no bids means unsold.
- Final ranking uses total character power, not money spent.

## Character images

Before the auction starts, the room host can upload an image for each character from the roster in the waiting room. PNG, JPG, WEBP, and GIF are supported, up to 5 MB each. Images are stored in the app's `uploads` folder and served to everyone in that room.

## Important limitations of this starter

- Room state is held in server memory. Rooms and active auctions reset if the server restarts or sleeps. This starter is intended for initial testing; persistent database storage and reconnect tokens are future upgrades.
- For a fair live multiplayer game, all players should connect to the same running deployed Replit app URL. Do not use separate development previews as separate servers.
- Character abilities are placeholders until you decide their actual abilities.
- The room host can upload images before the auction starts. Uploads are stored on the server filesystem; for a production deployment, use persistent object storage.

## Troubleshooting

- If the app does not start, check the Shell for the first error and run `npm install` again.
- If port configuration is needed, the server uses `process.env.PORT` automatically.
- If the preview is blank, check the Replit Console and browser console for errors.
