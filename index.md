---
layout: page
title:  C7 Game Home Page
date:   2022-03-23 18:25:00 -0800
---
# C7 Game

- [Discussion Forum](https://forums.civfanatics.com/forums/civ3-future-development.604/)
- [Open source GitHub project](https://github.com/C7-Game/Prototype)

## Downloads


##### v0.1 Babylon Has Been Released!

The C7 team has reached the second development milestone, Babylon. 

New features in Babylon:

- Significant map improvements.  Hills, forests, marshes, rivers, and resources all appear on the map.
- Cities now auto-produce units, allowing you to expand throughout your landmass.
- There is now a very basic AI, which will also have auto-produced units, and will attempt to settle its entire starting landmass.
- Barbarians now exist to make your life more difficult, and they will periodically send out Warriors.
- There is now combat, including unit animations of the combat.
- We have our first custom art, on the main menu, and the main menu plays background music.
- Many BIQ and SAV files can be loaded (although only the map part is processed, and many don't load yet either).

Thus, there is a game to be had with the Babylon release - can you outclass the AI in effectively settling your home continent?

Media files from Civilization III are still required in this milestone.

##### Download Babylon

* [Windows](https://github.com/C7-Game/Prototype/releases/download/v0.1-babylon/C7_0.1-Babylon-Windows.zip)
* [Mac](https://github.com/C7-Game/Prototype/releases/download/v0.1-babylon/C7_0.1-Babylon-Mac.zip)
* [Linux x86-64](https://github.com/C7-Game/Prototype/releases/download/v0.1-babylon/C7_0.1-Babylon-Linux-x86_64.zip)

All official releases of C7 can be found on the [GitHub releases page.](https://github.com/C7-Game/Prototype/releases/)

##### Windows Installation

This is a Windows 64-bit executable and requires 64-bit windows and a Civilization III installation to be present on the computer for access to media files. C7 will find this install in the Windows registry automatically.

- Download and extract the zip file
- Double-click C7.exe
- If it is blocked, you may need to unblock it by
  - Right click
  - Click on Properties
  - Check the "Unblock" checkbox near the bottom buttons in the "Security" section
  - Click OK

##### Linux Installation

This is an x86-64 Linux executable, and it requires media files from a Civilization III installation. We devs just copy the top-level "Sid Meier's Civilization III Complete" ("Complete may not be there if your install was from pre-Complete CDs, but that's OK) folder and its contents to our Linux machine.

- Download and extract the tgz file
- Set the CIV3_HOME environment variable to point to the Civ3 files, e.g. `export CIV3_HOME="/path/to/civ3"`
- Run C7.x86_64

##### Mac Installation

This is a universal 64-bit executable, so it should run on both Intel and M1 Macs, and it requires media files from a Civilization III installation. We devs just copy the top-level "Sid Meier's Civilization III Complete" ("Complete may not be there if your install was from pre-Complete CDs, but that's OK) folder and its contents to our Mac.

- Download the zip; it may complain bitterly, and you may have to tell it to keep the download instead of trashing it
- Double click the zip file, and a folder with C7.app and a json file will appear
- If you try to open C7.app it will tell you it's damaged and try to trash it; it is not damaged
- To unblock the downloaded app, from a terminal run `xattr -cr /path/to/C7.app`; you can avoid typing the path out by typing `xattr -cr ` and then dragging the C7.app icon onto the terminal window
- Set the CIV3_HOME environment variable to point to the Civ3 files, e.g. `export CIV3_HOME="/path/to/civ3"`
- From that same terminal where you set CIV3_HOME, run C7.app with `open /path/to/C7.app`, or again just type `open ` and drag the C7 icon onto the terminal window and press enter

#### Known issues

- It relies on having a Civilization III install on the machine and knowing where it is (via Windows registry or via CIV3_HOME environment variable)
- With some BIQ or SAV files, crashes to desktop may happen
- For Mac:
  - Mac will try hard not to let you run this; it will tell you the app is damaged and can't be opened and helpfully offer to trash it for you. From a terminal you can `xattr -cr /path/to/C7.app` to enable running it.
  - Mac will crash if you hit buttons to start a new game (New Game, Quick Start, Tutorial, or Load Scenario) because it cant find our 'new game' save file we're using as a stand-in for map generation. But you can Load Game and load the c7-static-map-save.json file or open a Civ3 SAV file to open that map
