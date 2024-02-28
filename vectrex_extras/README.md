# Vectrex Extras

![Vectrex](https://github.com/dyreschlock/pocket-platform-images/blob/main/pics/home/vectrex.png?raw=true)

The Vectrex is a unique system that is stand alone from a TV. All graphics are vector-based, and you can add a transparent overlay on the screen to show some color, graphics, and instruction.

The Vectrex core was created by <a href="https://github.com/obsidian-dot-dev">Oblivion</a>, and has support for these overlays. For the 0.9.0 version, upon opening the core, you're asking to choose a Game ROM and choose an Overlay. However, switching between games is cumbersome as you must change the game and then change the overlay in a two-step process. For multi-file rom-based setups, devs have been using JSON files to describe what it needed so you only need to choose the JSON file and be ready to go.

Vectrex Extras is a collection of JSON files based on a particular rom-pack. Vectrex Extras changes v0.9.0 of the Vectrex core to accept JSON files. Additionally, Vectrex Extras is set up as a new core implementation of Vectrex, so if the Vectrex core is changed to accept JSON files in the future, it doesn't conflict.

## Usage Note

To install, copy all of the vectrex-extras.zip contents to your SD card. Again, this is a separate core compliation of the Vectrex core. You'll need to change cores to Vectrex-Extras in the openFPGA menu.

## Set-up Note #1

The distribution does not contain the actual RBF core flie. Please source it yourself from Obsidian's distribution.

Place the RBF file in the core folder, here:
- /Cores/obsidian.Vectrex/


## Set-up Note #2

All of the JSON files are set up using a particular rom-pack. Originally, this was meant to be the HTGDB pack, but it's slightly out of date. There are more games to play, and a few other things, too. The HTGDB pack will still work, but I added two more folders:

- (3) Vectrex Academy Student Works
- (4) More Homebrew and Hacks

You can find the updated rom-pack on Archive.org.  Just search for <b><a href="https://archive.org/search?query=openfpga+vectrex+extras">openfpga vectrex extras</a></b>.

## Pocket-Sync Fetch - Archive.org

If you use Pocket Sync for updating your cores, you can create a <b>Fetch</b> command to grab all of the files on Archive.org.

<img src="pocket-sync-fetch.png" />

- Choose 'Internet Archive'
- Put in the archive key found at the end of the URL.
- Choose /Assets/vectrex/common/ as your destination
- Leave File Extensions blank, or type in bin, BIN, vec, ovr