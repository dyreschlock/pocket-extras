# Extra Files for the Analogue Pocket

This repository contains several extra files to get more out of some FPGA cores. The majority of these files are extra JSON and MRA for more games that currently run on released cores, but were not included in their releases for whatever reason. If any of this stuff gets added to those releases in the future, it'll be removed from here.

Additionally, I've added a combination core that collects all of the games from the Toaplan Version 2 Hardware arcade board.

Current extras and edits are collected into the following 3 categories:
- <b>Jotego Extras</b>
- <b>Donkey Kong Extras</b>
- <b>Vectrex Extras</b>
- <b>Toaplan V2 Combination Core</b>

## Jotego Extras

<b>Jotego</b> has done some amazing work in the FPGA scene for the Mister and Pocket. To date, he has released the most amount of arcade cores on the Pocket, including CPS1, CPS2, Sega System 16, The Simpsons, TMNT, and so many more. Please support Jotego on <b><a href="https://www.patreon.com/jotego">Patreon</a></b>.

### Capcom CPS2 CPS1.5 CPS1

![CPS2](https://github.com/dyreschlock/pocket-platform-images/blob/v4.0.0/pics/arcade/jtcps2.png?raw=true)

Included in `pocket-extras` are several games that work on the release including: 
- CPS1 and CPS1.5 Conversions to CPS2, including The Punisher, Street Fighter II Championship Edition, and Final Fight 30th Anniversary Edition
- CPS1 Conversions to CPS1.5, including Mega Man Power Battle and Street Fighter Zero
- <a href="https://github.com/atrac17/Arcade_Offset">Arcade_Offset</a> hacks for CPS2 and CPS1

CPS Conversions were done by <b><a href="https://github.com/terminator2k2">terminator2k2</a></b>.

In particular, for Arcade_Offset, the color blind hacks for Super Puzzle Fighter are included. However, I changed the MRA files slightly. Originally, those MRA files created roms with identical names to the main rom. I changed the MRA files so they create a separate rom.

For example: For `Super Puzzle Fighter II X' Prime (Euro 2100823)`, the rom is named `spf2xe.rom`. Previously, for `Super Puzzle Fighter II X' Prime (Euro 2100823) [CB V.1]` it would use the same name. I changed it so it now makes this rom: `spf2xec1.rom`. The JSON files in the repo will look for this rom.

For almost every JSON file I have in the repo, I've also included the MRA file. And, each JSON has the corresponding Presets.

### Other Jotego Extras

There are some extra MRA files, other games and hacks floating around out there that create ROMs that work on released Jotego cores. Those have been included and are as follows.

- Dokaben 2 for JTpang
- Bubble Bobble Ultra for JTbubl (instructions <a href="/jotego_extras/Assets/jtbubl/mra/README.md">here</a>)

## Donkey Kong and Radar Scope

![DonkeyKong](https://github.com/dyreschlock/pocket-platform-images/blob/v4.0.0/pics/arcade/donkeykong.png?raw=true)

The <b><a href="https://github.com/ericlewis/openFPGA-DonkeyKong">Donkey Kong</a></b> and <b><a href="https://github.com/ericlewis/openFPGA-RadarScope">Radar Scope</a></b> cores were created by Eric Lewis, and he developed them to load a single rom at a time.  When you select the core, it'll immediately boot into Donkey Kong. Modern arcade cores allow you to choose a JSON file for the game you want to play, which allows the core to play multiple games, rather than just one.  Donkey Kong has many many romhacks, so I made some edits to the `data.json` which allows JSON to be selected.

Included in `pocket-extras` are:
- edits to allow game selection
- JSON and MRA files for all Donkey Kong games from Mister
- JSON and MRA files for romhacks from donkeykonghacks.net

Additionally, all of these will run on the RadarScope core, so I made the same edits and additions there.

Thanks to <b><a href="https://github.com/GoldZabu">GoldZabu</a></b> for all the dkhacks.net Hacks! :)

For instructions building the dkhacks.net Hacks, <a href="/dk_extras/Assets/donkeykong/mra/donkeykonghacks.net/README.md">look here</a>.

## Vectrex Extras

![Vectrex](https://github.com/dyreschlock/pocket-platform-images/blob/main/pics/home/vectrex.png?raw=true)

The Vectrex core was created by <a href="https://github.com/obsidian-dot-dev">Oblivion</a>, and has support for overlays. For the 0.9.0 version, upon opening the core, you're asking to choose a Game ROM and choose an Overlay. However, switching between games is cumbersome as you must change the game and then change the overlay in a two-step process. For multi-file rom-based setups, devs have been using JSON files to describe what it needed so you only need to choose the JSON file and be ready to go.

Vectrex Extras is a collection of JSON files based on a particular rom-pack. Vectrex Extras changes v0.9.0 of the Vectrex core to accept JSON files. Additionally, Vectrex Extras is set up as a new core implementation of Vectrex, so if the Vectrex core is changed to accept JSON files in the future, it doesn't conflict.

<b>**Note</b>: The distribution does not contain the actual RBF core flie. Please source it yourself from Obsidian's distribution.

<b>**Note 2</b>: The particular rom-pack for Vectrex Extras can be found on Archive.org.  Just search for <b><a href="https://archive.org/search?query=openfpga+vectrex+extras">openfpga vectrex extras</a></b>.

Please read full instructions: <b><a href="/vectrex_extras/README.md">here</a></b>


## Toaplan Version 2 Hardware combo-core

![Toaplan](https://github.com/dyreschlock/pocket-platform-images/blob/main/pics/arcade/toaplan2_c.png?raw=true)

The Coin-Op Collection group has now released all of their games based on the Toaplan Version 2 Hardware arcade board on the Analogue Pocket. In 2022, <a href="https://github.com/psomashekar">pram0d</a> released <b>Battle Garegga</b>, <b>Battle Bakraid</b>, <b>Sorcer Strike</b>, <b>Kingdom Grand Prix</b>, <b>Armed Police Batrider</b>, and <b>Snow Bros 2</b> for the Pocket. And recently, in 2023, <a href="https://github.com/atrac17">atrac17</a> released <b>Truxton 2</b> and <b>Pipi & Bibs</b>. There are more games based on this arcade hardware, but these 8 games are all of the ones currently implemented in FPGA.

All of them have been released as Single Game cores. You can find those implementations here: <a href="https://github.com/Coin-OpCollection/Distribution-OpenFPGA">Coin-OpCollection/Distribution-OpenFPGA</a>

I've taken all of these cores and combined them into a single Arcade Multi core. This should help clean up your Arcade folder on the openFPGA menu.

<b>**Note</b>: This distribution does not contain the actual RBF core files. Please download the cores from Coin-Op, and copy the RBF files into the correct locations.

<b>**Note 2</b>: All JSON files are expecting the full set name rather than a truncated 8 character one. (Similar to Jotego's approach)

Please read full instructions: <b><a href="/toaplan2_complete/README.md">here</a></b>

## Final Note

Many of these MRA files require some extra work in order to generate the roms correctly. The pocket updaters should pull down the correct files for each of these JSON, so you can skip making them yourself, if you'd like.

Thank you to <b><a href="https://github.com/mattpannella">Matt Pannella</a></b> and <b><a href="https://github.com/retrodriven">Retro Driven</a></b> for that!
