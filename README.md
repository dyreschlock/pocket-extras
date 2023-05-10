# Extra Files for the Analogue Pocket

This repository contains several extra files to get more out of some FPGA cores. The majority of these files are extra JSON and MRA for more games that currently run on released cores, but were not included in their releases for whatever reason. If any of this stuff gets added to those releases in the future, it'll be removed from here.

Current extras and edits are as follows

## Capcom CPS2

The CPS2 core is currently in beta from <b>Jotego</b>. Please support Jotego on <b><a href="https://www.patreon.com/jotego">Patreon</a></b> as he has done absolutely amazing work in the FPGA scene for the Mister and the Pocket.

Included in `pocket-extras` are several games that work on the beta release including: 
- Darkstalkers 1
- Phoenix Edition of supported games
- Punisher cps1.5 conversion
- Street Fighter II Championship Edition cps1 conversion
- Final Fight 30th Anniversary CPS2 version
- some Arcade_Offset hacks

In particular, from Arcade_Offset, the color blind hacks for Super Puzzle Fighter are included. However, I changed the MRA files slightly. Originally, those MRA files created roms with identical names to the main rom. I changed the MRA files so they create a separate rom.

For example: For `Super Puzzle Fighter II X' Prime (Euro 2100823)`, the rom is named `spf2xe.rom`. Previously, for `Super Puzzle Fighter II X' Prime (Euro 2100823) [CB V.1]` it would use the same name. I changed it so it now makes this rom: `spf2xec1.rom`. The JSON files in the repo will look for this rom.

For every JSON files I have in the repo, I've also included the MRA file. And, each JSON has the corresponding Presets.

## Donkey Kong and Radar Scope

The <b><a href="https://github.com/ericlewis/openFPGA-DonkeyKong">Donkey Kong</a></b> and <b><a href="https://github.com/ericlewis/openFPGA-RadarScope">Radar Scope</a></b> cores were created by Eric Lewis, and he developed them to load a single rom at a time.  When you select the core, it'll immediately boot into Donkey Kong. Modern arcade cores allow you to choose a JSON file for the game you want to play, which allows the core to play multiple games, rather than just one.  Donkey Kong has many many romhacks, so I made some edits to the `data.json` which allows JSON to be selected.

Included in `pocket-extras` are:
- edits to allow game selection
- JSON and MRA files for all Donkey Kong games from Mister
- JSON and MRA files for romhacks from donkeykonghacks.net

Additionally, all of these will run on the RadarScope core, so I made the same edits and additions there.

Thanks to <b><a href="https://github.com/GoldZabu">GoldZabu</a></b> for your help :)

## Pang and Block Block

The Pang core released by <b><a href="https://www.patreon.com/jotego">Jotego</a></b> can play some more games than the JSON available in the core release.  Included are all the JSON and MRA files for them.

However, Block Block is a vertical game that requires screen rotation in the dipswitches. I'm not sure what those settings are, but <b><a href="https://github.com/terminator2k2">Terminator2k2</a></b> made a duplicate of the pang core that will rotate the screen and make the game playable. This core is called `jtblock`

To make this core, duplicate `Cores/jotego.jtpang` on your SD card and call it `Cores/jotego.jtblock`. Then copy the contents of this release into the directories.

## Final Note

Many of these MRA files require some extra work in order to generate the roms correctly. The pocket updaters should pull down the correct files for each of these JSON, so you can skip making them yourself, if you'd like.

Thank you to <b><a href="https://github.com/mattpannella">Matt Pannella</a></b> and <b><a href="https://github.com/retrodriven">Retro Driven</a></b> for that!