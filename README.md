# iPhone widget for World Chess Championship 2026

The tracker also comes as an iPhone home screen widget. It shows the same match as the extension: the board, both clocks, the last move, the score and Sesse's evaluation. 

It runs in [Scriptable](https://apps.apple.com/app/scriptable/id1405459188), a free app that runs small JavaScript widgets.

## Sizes

- **Small:** score, game, last move, evaluation and both clocks.
- **Medium:** the board in the middle. The match is on the left. The clocks are on the right, with the evaluation bar between them.
- **Large:** a bigger board, with each player's clock above and below it.
- **Lock screen:** a rectangular version (score, game, last move, evaluation) and a one-line version.

## Set it up

1. Install **Scriptable** from the App Store.
2. Get `WCC 2026.js` into Scriptable. Pick one of these:
   - **From a computer:** drop the file into `iCloud Drive/Scriptable`.
   - **On the iPhone:** open the file, tap Share, choose **Save to Files**, and save it to `iCloud Drive → Scriptable`.
   - **By hand:** open Scriptable, tap **+**, and paste in the whole file.
3. Open Scriptable and tap the script once. A preview of the medium widget should appear.
4. Go to your home screen and long-press an empty area. Tap **Edit → Add Widget**, find **Scriptable**, choose a size and tap **Add Widget**.
5. Long-press the new widget, tap **Edit Widget**, and set **Script** to `WCC 2026`.

**Lock screen:** long-press the lock screen and tap **Customize → Lock Screen**. Tap the widget area, add Scriptable's rectangular or inline widget, and pick `WCC 2026`.

**If tapping opens Scriptable instead of Lichess:** go to **Edit Widget**, set **When Interacting** to **Open URL**, and paste this link:

```
https://lichess.org/broadcast/fide-world-chess-championship-2026/qfkdt8mn
```

## What to expect

- **It refreshes when iOS lets it.** iOS decides when widgets update, usually every 5 to 15 minutes. The widget asks for every 5 minutes during a live game and every 30 minutes otherwise. It is a glance at the game, so new moves won't appear the second they are played.
- **The running clock ticks.** The side to move's clock counts down live, using iOS's built-in timer. The other clock shows the time left after that player's last move.
- **Between games** it shows the final position of the last game and when the next one starts.
- **Offline,** it shows the last state it saved, marked "Offline".
- **Light and dark mode** both work. The widget follows your phone's setting.

## Where the numbers come from

Moves, clocks and results come from the [Lichess broadcast](https://lichess.org/broadcast/fide-world-chess-championship-2026/qfkdt8mn). The evaluation comes from [Sesse](https://analysis.sesse.net/), and nowhere else. The widget shows Sesse's number only when Sesse has analysed exactly the position on the board. If it hasn't, the widget says so. It never guesses.

Each refresh makes three small requests to Lichess and one or two to Sesse.

## Updating

Replace `WCC 2026.js` in your Scriptable folder with the new version. Widgets already on your home screen pick it up on their next refresh.

## Credits

Chess pieces by Colin M.L. Burnett (GPLv2+), via Lichess, embedded in the script as small images.
