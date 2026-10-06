# PalPal

**A desktop planner for Palworld that reads your world save and tells you what to do next.**

[![Latest release](https://img.shields.io/github/v/release/DylanMLoszak/PalPal?label=release)](https://github.com/DylanMLoszak/PalPal/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/DylanMLoszak/PalPal/total)](https://github.com/DylanMLoszak/PalPal/releases)
![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-blue)
![Palworld](https://img.shields.io/badge/Palworld-1.0.4-orange)

PalPal replaces the spreadsheet. Point it at a world and it works out which Pals should staff each base,
which pairs to breed and how many eggs to expect, what to catch, and which Pals are safe to let go.
It only ever reads your save.

---

## Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Getting started](#getting-started)
- [Dedicated servers](#dedicated-servers)
- [Updating](#updating)
- [Privacy and safety](#privacy-and-safety)
- [Troubleshooting](#troubleshooting)
- [Game data and compatibility](#game-data-and-compatibility)
- [Disclaimer](#disclaimer)
- [Licence](#licence)

## Features

| Page | What it gives you |
| --- | --- |
| **Do next** | A short, ordered list of the most useful things you can act on right now. |
| **Pals** | Every Pal in scope with its passives, talents, location and what it is being kept for. |
| **Bases** | Per-base job coverage: who works where, which jobs are uncovered and the best fix for each. |
| **Catch list** | Species and passives worth catching, grouped by where to find them. |
| **Breed** | Breeding routes to better workers and party Pals, with the parents to use and the expected eggs. |
| **Workers** | The best Pal you own for each job, and the upgrade that would beat it. |
| **Party** | Party builds by purpose, compared against the party you actually carry. |
| **Upgrade next** | Where Pal Souls and condensing pay off first. |
| **Spares** | A box-by-box map of what to keep, what is fodder and what you can release, with the reason for each. |
| **Trait Bank** | Every passive you own, who carries it and which carrier to protect. |
| **Breed tree** | The full family tree for any species you want to reach. |
| **Breeding unlocks** | Which single missing parent would open up the most new species. |

Also included:

- **Surgery Table and Pal Reverser support**, each behind its own switch, so plans only use what you can afford.
- **Global palbox and Dimensional Pal Storage** as optional sources, chosen page by page or player by player.
- **Automatic re-import** when the game writes a new save, so the advice follows your session.
- **Export** of the current world state to a zip. The server login and local folder paths are left out; the
  zip does contain your player name, your Pals with their nicknames, your bases, your PalPal settings and the
  save's internal ids for those Pals, bases and players.

## Requirements

- Windows 10 or 11, 64-bit
- [Python 3](https://www.python.org/downloads/) on your `PATH`, with two packages PalPal uses to read the save:

  ```powershell
  pip install palworld-save-tools pyooz
  ```

No .NET install is needed; the runtime is bundled in the exe. The game does not have to be installed on the
same PC unless you use **Refresh from game**.

## Installation

1. Download `PalPal.exe` from the [latest release](https://github.com/DylanMLoszak/PalPal/releases/latest).
2. Put it in a folder you can write to (for example `Documents\PalPal`). Avoid `Program Files`, where PalPal
   cannot update itself.
3. Run it. Windows SmartScreen may warn that the app is unrecognised because it is not code-signed:
   choose **More info**, then **Run anyway**.

PalPal is a single file. To uninstall, delete the exe and the `%LOCALAPPDATA%\PalPal` folder.

## Getting started

1. Click **Browse** and pick your world folder, the one that contains `Level.sav`. Local worlds live under
   `%LOCALAPPDATA%\Pal\Saved\SaveGames\<steam id>\<world id>`.
2. Click **Import**.
3. Choose who you are under **Me**, then open **Do next**.

Everything else (which jobs to plan for, other players' Pals, storage sources, Surgery Table options) is under
**Settings**.

## Dedicated servers

If your world runs on a hosted dedicated server, PalPal can read the save straight from the host over FTP.
Switch on **Dedicated server** under **Settings**, enter the host, port, user name and password, test the
connection, then import as usual. PalPal finds the world folder on the server by itself and only downloads; it never uploads.

> **FTP is not encrypted.** The user name, password and save travel as plain text between your PC and the
> host. Use a server login you do not use anywhere else.

A server writes its save on its own schedule, so PalPal shows the time the save was written. Advice can lag the
game by up to the server's autosave interval.

## Updating

PalPal checks this page each time it starts. When a newer version is available, an **Update to X** button
appears in the status bar. Nothing is downloaded or replaced until you click it. PalPal then downloads the new
version, verifies it against the SHA-256 checksum GitHub publishes for the release, swaps itself and restarts.
If the download fails or does not match, it is discarded and the version you have keeps working. After an
update the previous exe is kept beside the new one as `PalPal.exe.old` and removed on a later start.

The version you are running is shown in the window title. Your settings and flags are stored separately in
`%LOCALAPPDATA%\PalPal` and survive every update.

## Privacy and safety

- **Read-only.** PalPal never writes to a save file, locally or on a server.
- **Your Pals only, by default.** Other players' Pals in a shared world stay hidden until you switch them on.
- **No telemetry.** PalPal makes two kinds of network request: the update check against this GitHub page, and
  the FTP connection to a server you configure yourself.
- **Local data.** Settings and logs are kept on your PC under `%LOCALAPPDATA%\PalPal`. The server password is
  stored there encrypted for your Windows account, and is sent only to the server you entered (unencrypted,
  see [Dedicated servers](#dedicated-servers)).
- **Logs are personal.** They record your PC and Windows user names, folder paths, the server host and player
  names. Read a log before you send it to anyone.

## Troubleshooting

| Problem | What to do |
| --- | --- |
| Import says Python was not found, or is missing a package | Check that `python --version` works in a terminal and that both packages above are installed. If Python is not on your `PATH`, set the environment variable `PALPAL_PYTHON` to the full path of `python.exe`. |
| The advice looks out of date | PalPal reads the last save the game wrote. Sleep or wait for an autosave in game, then import again. |
| No **Update to X** button | You are on the latest version, or GitHub could not be reached; PalPal tries again on the next start. |
| Something else | Logs are in `%LOCALAPPDATA%\PalPal\logs`; the latest one says what PalPal was doing when it went wrong. |

## Game data and compatibility

PalPal ships with reference tables for **Palworld 1.0.4** (species, passives, breeding combinations, work
suitabilities). After a game patch, **Refresh from game** re-reads what it can from your installed copy;
refreshing is always a manual action, and a failed refresh keeps the previous tables.

## Disclaimer

PalPal is an unofficial fan-made tool. It is not affiliated with, endorsed by or sponsored by Pocketpair, Inc.
Palworld is a trademark of Pocketpair, Inc.

## Licence

PalPal is free to download and use, and is provided as is, without warranty. This repository hosts releases
only; the source code is not published. See [LICENSE.md](LICENSE.md), and
[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) for the game data and open-source components it contains.
