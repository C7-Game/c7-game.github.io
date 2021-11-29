---
layout: page
title:  C7 Game Home Page
date:   2021-11-27 18:25:00 -0800
---
# CivFanatics Creation & Customization Community's Civ3 Conquests Clone

## 20 years of Civ3, and a proposal for 20 more

- [Announcement thread on CivFanatics Forums](https://forums.civfanatics.com/threads/20-years-of-civ3-and-a-proposal-for-20-more.673944/)
- [Open source GitHub project](https://github.com/C7-Game/Prototype)

## Downloads

### v0.0 Aztec has been released!

The C7-Game team have reached the first development milestone, Aztec. This is a pre-release-quality build. It requires media files from Civilization III to be present to do anything interesting. It can "start a new game" and show a zoomable, scrollable map and some units, and it responds to some of the controls, in some ways mocking turn-taking, although nothing moves.

- [Windows](https://github.com/C7-Game/Prototype/releases/download/untagged-ffba0e0b13067151eed6/C7-Aztec-Windows.zip)
- [Linux x86-64](https://github.com/C7-Game/Prototype/releases/download/untagged-ffba0e0b13067151eed6/C7-Aztec-Linux.tgz)
- [Mac](https://github.com/C7-Game/Prototype/releases/download/untagged-ffba0e0b13067151eed6/C7-Aztec-Mac.zip)

##### Windows Installation

This is a Windows 64-bit executrable and requires 64-bit windows and a Civilization III installation to be present on the computer for access to media files. C7 will find this install in the Windows registry automatically.

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

**Note:** Mac may crash on any menu option that tries to start a new game (New Game, Quick Start, Tutorial, or Load Scenario), and this is a known issue. But you can Load Game and open the json file included with the download or any Civ3 Complete (or Conquests) .SAV file, although it may crash with .SAVs based on scenarios, Conquests, or mods.

- Download the zip; it may complain bitterly, and you may have to tell it to keep the download instead of trashing it
- Double click the zip file, and a folder with C7.app and a json file will appear
- If you try to open C7.app it will tell you it's damaged and try to trash it; it is not damaged
- To unblock the downloaded app, from a terminal run `xattr -cr /path/to/C7.app`; you can avoid typing the path out by typing `xattr -cr ` and then dragging the C7.app icon onto the terminal window
- Set the CIV3_HOME environment variable to point to the Civ3 files, e.g. `export CIV3_HOME="/path/to/civ3"`
- From that same terminal where you set CIV3_HOME, run C7.app with `open /path/to/C7.app`, or again just type `open ` and drag the C7 icon onto the terminal window and press enter

#### Known issues

- It relies on having a Civilization III install on the machine and knowing where it is (via Windows registry or via CIV3_HOME environment variable)
- This is more of a progress demonstraton and an early peek at the game and is not a fully functioning game
- Not all UI buttons perform an action
- There is very little exception handling, so crashes to desktop may happen
- Audio may cut off very quickly in some situations or not play at all
- For Windows you may have to unblock the downloaded executable
- For all non-Windows you will need to copy the file tree of a Civilzation III install and set the environment variable CIV3_HOME to the path of this file tree.
- For Mac:
  - Mac will try hard not to let you run this; it will tell you the app is damaged and can't be opened and helpfully offer to trash it for you. From a terminal you can `xattr -cr /path/to/C7.app` to enable running it.
  - Mac will crash if you hit buttons to start a new game (New Game, Quick Start, Tutorial, or Load Scenario) because it cant find our 'new game' save file we're using as a stand-in for map generation. But you can Load Game and load the c7-static-map-save.json file or open a Civ3 SAV file to open that map
- Opening modded SAV files may crash (or may not!)
