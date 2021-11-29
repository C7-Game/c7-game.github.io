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

#### Known issues

- It relies on having a Civilization III install on the machine and knowing where it is (via Windows registry or via CIV3_HOME environment variable)
- This is more of a progress demonstrator and an early peek at the game and is not a fully functioning game
- There are many UI buttons displayed but don't do anything (but some do!)
- There is very little exception handling, so crashes to desktop may happen
- Audio may cut off very quickly in some situations or not play at all
- For Windows you may have to unblock the downloaded executable
- For all non-Windows you will need to copy the file tree of a Civilzation III install and set the environment variable CIV3_HOME to the path of this file tree.
- For Mac:
  - Mac will try hard not to let you run this; it will tell you the app is damaged and can't be opened and helpfully offer to trash it for you. From a terminal you can `xattr -cr /path/to/C7.app` to enable running it.
  - Mac will crash if you hit buttons to start a new game (New Game, Quick Start, Tutorial, or Load Scenario) because it cant find our 'new game' save file we're using as a stand-in for map generation. But you can Load Game and load the c7-static-map-save.json file or open a Civ3 SAV file to open that map
- Opening modded SAV files may crash (or may not!)
