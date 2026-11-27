# Kaisha

A Star Citizen companion app for planning and tracking, with a bring-your-own-key voice AI for
hands-off control. It runs on your second monitor next to the game.

This repository holds the Windows installers and the update feed. The source code is not public.

> Kaisha is an unofficial fan project. It is not affiliated with or endorsed by Cloud Imperium
> Games or Roberts Space Industries. Star Citizen® is a trademark of Cloud Imperium Rights LLC.

## What it does

- **Fleet:** your ships with stats from the game files, and per-ship overrides.
- **Trade and hauling:** commodity prices, trade-loop planning, and hauling contracts ordered into
  the fewest stops.
- **Industry:** refinery jobs with countdowns and notifications, mining lookups, crafting targets
  and crew splits.
- **Shopping lists:** where to buy each item, planned by fewest stops, cheapest or nearest.
- **Vehicle loadouts:** fit components, compare builds, and see where to buy or loot the parts.
- **Navigation:** saved locations that turn with their planet, the way back to them, and a
  hologram map of each system.
- **Voice ship AI (optional):** push-to-talk control of the app by voice, using your own xAI API
  key. Voice stays off until you add a key.

Your data (ships, jobs, loadouts, history) is stored in a local database on your PC. It isn't
uploaded anywhere. The app fetches public reference data, such as prices, from community APIs.

## Install

Requires Windows 11 (x64).

1. Open the [latest release](../../releases/latest).
2. Download the file ending in `_x64-setup.exe` and run it.
3. The installers aren't code-signed yet, so Windows SmartScreen may say "Windows protected your
   PC". Choose **More info → Run anyway**.

The `.sig` file next to each installer is the update signature. You don't need to download it.

## Updates

New versions are published here. To upgrade, run a newer installer over the top of the old one.
Your data is kept, and the app backs up its database before any upgrade that changes it.
Automatic updates are coming: the app will check this repository's latest release and offer the
update, and it only installs updates signed with the project's key.

## How it works with the game

Kaisha reads the game's installed files (read-only) and, only if you turn them on in Settings:

- reads your screen (refinery and contract screens) with Windows' built-in text recognition,
- presses the game's own key binds for a small set of allowed ship actions,
- connects to the game's local telemetry feed.

It never reads game memory, injects into the game process, or modifies the game. Screenshots stay
on your PC. Sending key presses to the game is a grey area under the game's terms, so use the ship
controls at your own risk.

## Uninstall

Use **Settings → Apps → Installed apps**. Leave the option to delete application data unticked
unless you want to lose your saved data.

## Feedback

Found a bug or have an idea? [Open an issue](../../issues) in this repository.
