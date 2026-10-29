# Feeless Memory

A free, single-file browser memory game with crypto coin pairs. Nano (XNO) is always in the deck. No build step, no backend, no fees.

## Play

- **Free play:** Easy (6 pairs), Normal (8), Hard (10) or Expert (12).
- **Daily board:** the same 8-pair board for everyone, new every day at 00:00 UTC. Clear it to keep your daily streak.
- **Peek:** once per board, show every unmatched card for a moment (costs 50 points).
- **Scoring:** 100 per pair, +25 for each extra match in a combo, -10 per miss, plus a time bonus when you clear the board.
- A short fact about each coin appears when you match it. Coins are drawn as simple tickers in their usual colours, not official logos.

Best score and best time are stored per board size in the player's browser.

## Deploy on GitHub Pages

1. Create a new repository, for example `feeless-memory`.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Open **Settings > Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save.
4. After a minute the game is live at `https://<your-username>.github.io/feeless-memory/`.

## Donations

The tip card works the same way as in Feeless Defence and Crypto Clash:

- A `nano:` payment link with the chosen amount, shown as a QR code and an **Open in wallet** button.
- A **Copy address** button.
- An **I've sent it, check** button that asks public Nano nodes whether a matching payment arrived, and unlocks the supporter card backs (Gold, Neon, Mint) on that browser.

To use a different wallet, change `NANO_ADDRESS` near the top of the script in `index.html`. If the public RPC endpoints in `RPCS` ever block browser requests, point them at your own proxy.

The supporter unlock is stored in `localStorage`, so it is a thank-you perk, not secure access control.

Add `?selftest` to the URL to expose a small `window.__fm` object for automated tests.
