# Soulcounter Desktop

Soulcounter Desktop is a free Windows app for Deadlock. It picks up every match you load into from the game itself, then shows the shop call in an overlay over the game: the golden item, your buy order, the best spend for your souls, mid-game pivots, and what each enemy is really building.

**Download:** https://soulcounter.app/desktop (or grab `Soulcounter-Setup.exe` from [Releases](https://github.com/IceWhistle/soulcounter-desktop/releases/latest)).

The web version is at https://soulcounter.app.

## Set it up once

1. **Install it.** Run `Soulcounter-Setup.exe`, or use `Soulcounter-Portable.exe` if you'd rather not install anything. The app is not code-signed yet, so Windows SmartScreen may say "Windows protected your PC": choose **More info**, then **Run anyway**.
2. **Turn on Deadlock's console log.** In Steam, right-click Deadlock → Properties → General → Launch options, add `-condebug` (keep anything already there), then restart Deadlock.
3. **Play in borderless windowed or windowed mode.** Overlays can't draw over exclusive fullscreen.

**F8** shows or hides the overlay. **Ctrl+F8** lets you move and resize it.

## How it works

- Deadlock writes `Lobby … for Match <id> created` to its console log when you load in. Soulcounter reads that line and loads the match into Live mode, which gets the broadcast from [api.deadlock-api.com](https://deadlock-api.com). The feed runs about a minute behind the game.
- Counter-pick, lane and item stats are the same as on soulcounter.app, refreshed twice a day, and the app downloads new numbers by itself.
- The installed app updates itself: new versions download in the background and install once Deadlock is closed. The portable exe tells you when a new version is out.
- No Overwolf, no memory reading, no injection. Soulcounter only reads the game's text log and public match data.

Soulcounter is a fan-made tool and is not affiliated with Valve.
