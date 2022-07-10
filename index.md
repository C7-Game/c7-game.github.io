---
layout: page
title:  C7 Game Home Page
date:   2022-07-09 18:25:00 -0800
---
# About C7
C7 (working title) is an in-development 4X strategy game built with Godot and C#, with a historical focus inspired by games such as _Civilization_, _Galactic Civilizations_, and _Humankind_. We aim to create a new game that looks and plays like classic Civ but incorporates features from the best of the genre and our own dreams.

- [CivFanatics subforum](https://forums.civfanatics.com/forums/civ3-future-development.604/)
- [GitHub](https://github.com/C7-Game/Prototype)
- [Discord](https://discord.gg/uwxUuWhM89)

# Get C7 Carthage

## v0.2 Carthage Preview 1 Has Been Released!

The C7 team has released the first preview of the "Carthage" milestone.  This is a general enhancement over the "Babylon" release, and recommended for all newcomers.

New features in this preview:

- A right-click menu allows you to select units from a stack, or change city production
- C7-native JSON files can be loaded to start a game
- Units can be moved with the mouse via the Go To button, or via the arrow keys/fn+arrow keys (for diagonal movement), in addition to via the Num Pad
- The AI now has a concept of tile visibility, and uses explorers to reveal tiles (the human can still see all tiles)
- Polish has been added to the unit animation and lower-right info box

You'll also now be playing as the Carthaginians, and the Romans have been added to the map to provide you with a proper rival.

Media files from _Civilization III_ are still required in this milestone.

### Download Carthage Preview 1

* [Windows](https://github.com/C7-Game/Prototype/releases/download/v0.2-carthage-preview-1/C7Carthage_Preview_1-Windows.zip)
* [Mac](https://github.com/C7-Game/Prototype/releases/download/v0.2-carthage-preview-1/C7Carthage_Preview_1-Mac.zip)
* [Linux x86-64](https://github.com/C7-Game/Prototype/releases/download/v0.2-carthage-preview-1/C7Carthage_Preview_1-Linux-x86_64.zip)

All official releases of C7 along with more detailed release notes can be found on the [GitHub releases page.](https://github.com/C7-Game/Prototype/releases/)

## Installation

### Windows Installation

This is a Windows 64-bit executable and requires 64-bit windows and a Civilization III installation to be present on the computer for access to media files. C7 will find this install in the Windows registry automatically.

- Download and extract the zip file
- Double-click C7.exe
- If it is blocked, you may need to unblock it by
  - Right click
  - Click on Properties
  - Check the "Unblock" checkbox near the bottom buttons in the "Security" section
  - Click OK

### Linux Installation

This is an x86-64 Linux executable, and it requires media files from a Civilization III installation. We devs just copy the top-level "Sid Meier's Civilization III Complete" ("Complete may not be there if your install was from pre-Complete CDs, but that's OK) folder and its contents to our Linux machine.

- Download and extract the tgz file
- Set the CIV3_HOME environment variable to point to the Civ3 files, e.g. `export CIV3_HOME="/path/to/civ3"`
- Run C7.x86_64

### Mac Installation

This is a universal 64-bit executable, so it should run on both Intel and M1 Macs, and it requires media files from a Civilization III installation. We devs just copy the top-level "Sid Meier's Civilization III Complete" ("Complete may not be there if your install was from pre-Complete CDs, but that's OK) folder and its contents to our Mac.

- Download the zip; it may complain bitterly, and you may have to tell it to keep the download instead of trashing it
- Double click the zip file, and a folder with C7.app and a json file will appear
- If you try to open C7.app it will tell you it's damaged and try to trash it; it is not damaged
- To unblock the downloaded app, from a terminal run `xattr -cr /path/to/C7.app`; you can avoid typing the path out by typing `xattr -cr ` and then dragging the C7.app icon onto the terminal window
- Set the CIV3_HOME environment variable to point to the Civ3 files, e.g. `export CIV3_HOME="/path/to/civ3"`
- From that same terminal where you set CIV3_HOME, run C7.app with `open /path/to/C7.app`, or again just type `open ` and drag the C7 icon onto the terminal window and press enter

## Known issues

- C7 relies on having a Civilization III install on the machine and knowing where it is (via Windows registry or via CIV3_HOME environment variable, as described in the respective installation instructions)
- With some BIQ or SAV files, crashes to desktop may happen
- For Mac:
  - Mac will try hard not to let you run this; it will tell you the app is damaged and can't be opened and helpfully offer to trash it for you. From a terminal you can `xattr -cr /path/to/C7.app` to enable running it.
  - Mac will crash if you hit buttons to start a new game (New Game, Quick Start, Tutorial, or Load Scenario) because it cant find our 'new game' save file we're using as a stand-in for map generation. But you can Load Game and load the c7-static-map-save.json file or open a Civ3 SAV file to open that map
