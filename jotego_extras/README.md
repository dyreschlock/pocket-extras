# Jotego Extras

<b>Jotego</b> has done some amazing work in the FPGA scene for the Mister and Pocket. To date, he has released the most amount of arcade cores on the Pocket, including CPS1, CPS2, Sega System 16, The Simpsons, TMNT, and so many more. Please support Jotego on <b><a href="https://www.patreon.com/jotego">Patreon</a></b>.

## Capcom CPS2 CPS1.5 CPS1

![CPS2](https://github.com/dyreschlock/pocket-platform-images/blob/v4.0.0/pics/arcade/jtcps2.png?raw=true)

Included in `pocket-extras` are several games that work on the release including: 
- CPS1 and CPS1.5 Conversions to CPS2, including The Punisher, Street Fighter II Championship Edition, and Final Fight 30th Anniversary Edition
- CPS1 Conversions to CPS1.5, including Mega Man Power Battle and Street Fighter Zero
- <a href="https://github.com/atrac17/Arcade_Offset">Arcade_Offset</a> hacks for CPS2 and CPS1

CPS Conversions were done by <b><a href="https://github.com/terminator2k2">terminator2k2</a></b>.

In particular, for Arcade_Offset, the color blind hacks for Super Puzzle Fighter are included. However, I changed the MRA files slightly. Originally, those MRA files created roms with identical names to the main rom. I changed the MRA files so they create a separate rom.

For example: For `Super Puzzle Fighter II X' Prime (Euro 2100823)`, the rom is named `spf2xe.rom`. Previously, for `Super Puzzle Fighter II X' Prime (Euro 2100823) [CB V.1]` it would use the same name. I changed it so it now makes this rom: `spf2xec1.rom`. The JSON files in the repo will look for this rom.

For almost every JSON file I have in the repo, I've also included the MRA file. And, each JSON has the corresponding Presets.

## Other Jotego Extras

There are some extra MRA files, other games and hacks floating around out there that create ROMs that work on released Jotego cores. Those have been included and are as follows.

- Dokaben 2 for JTpang
- Bubble Bobble Ultra for JTbubl (instructions <a href="/jotego_extras/Assets/jtbubl/mra/README.md">here</a>)

## Note

Many of these MRA files require some extra work in order to generate the roms correctly. The pocket updaters should pull down the correct files for each of these JSON, so you can skip making them yourself, if you'd like.

Thank you to <b><a href="https://github.com/mattpannella">Matt Pannella</a></b> and <b><a href="https://github.com/retrodriven">Retro Driven</a></b> for that!
