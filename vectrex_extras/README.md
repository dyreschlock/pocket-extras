# Vectrex Extras

![Vectrex](https://github.com/dyreschlock/pocket-platform-images/blob/main/pics/home/vectrex.png?raw=true)

The Vectrex is a unique system that is stand alone from a TV. All graphics are vector-based, and you can add a transparent overlay on the screen to show some color, graphics, and instruction.

The Vectrex core was created by <a href="https://github.com/obsidian-dot-dev"><b>Obsidian</b></a>. The base implementation only includes JSON files for the official release set of 29ish games.

Vectrex Extras is a collection of JSON files based on a particular rom-pack that includes Homebrew games, Hacks, and much more. It's set up as a new core implementation of Vectrex so the new JSON files do not conflict with the JSON files in v0.9.1 of the Vectrex core.

## Usage Note

To install, copy all of the vectrex-extras.zip contents to your SD card. Again, this is a separate core compliation of the Vectrex core. You'll need to change cores to Vectrex-Extras in the openFPGA menu.

## Set-up Note #1

The distribution does not contain the actual RBF core flie. Please source it yourself from Obsidian's distribution.

Place the RBF file in the core folder, here:
- /Cores/obsidian.Vectrex-Extras/

## Set-up Note #2

All of the JSON files are set up using a particular rom-pack. Originally, this was meant to be the HTGDB pack, but it's slightly out of date. There are more games to play, and a few other things, too. The HTGDB pack will still work, but I added two more folders:

- (3) Vectrex Academy Student Works
- (4) Homebrew by Author

The **Vectrex Academy** games are from a software development course in Germany focusing on game programming using C++. The **Homebrew by Author** category is more than an organization of the Homebrew folder. It contains all games from each author up through 2023, which is more complete than the Homebrew folder.

You can find the updated rom-pack on Archive.org.  Just search for <b><a href="https://archive.org/search?query=openfpga+vectrex+extras">openfpga vectrex extras</a></b>.

## Usage Note #2

All Games have been tested on the Vectrex, but several of the Homebrew games and official games do not run in the Vectrex core. In particular, the Vectrex core does not support 3D games, Analogue input, and Light Pen input. So, I've put all of those games in the ```_broken``` folder. Other games in this folder don't boot or don't respond to input when they should. I included all of the "broken" games in case they'll be supported in the future.

**ALSO**, There are several games that don't run using Firmware 2.1 but do run using Firmware 2.2. Be sure you have the latest Analogue OS firmware installed on your Pocket. <b><a href="https://www.analogue.co/support/pocket/firmware">Download Here</a></b>.

## Pocket-Sync Fetch - Archive.org

If you use <a href="https://github.com/neil-morrison44/pocket-sync">Pocket Sync</a> for updating your cores, you can create a <b>Fetch</b> command to grab all of the files on Archive.org.

<img src="pocket-sync-fetch.png" />

- Choose 'Internet Archive'
- Put in the archive key found at the end of the URL.
- Choose /Assets/vectrex/common/ as your destination
- Leave File Extensions blank, or type in bin, BIN, vec, ovr

## Pupdate Fetch

You can also use <a href="https://github.com/mattpannella/pupdate">Pupdate</a> to get updates for Vectrex Extras. It should already be available in the menu option for Pocket Extras.

Additionally, to retrieve all of the roms automatically, you'll need to manually update ```pupdate_settings.json``` Under the section labeled ```archives```, you'll need to add the following bit of code. Replace ```URL_KEY_TO_ARCHIVE``` with the ending key of the archive's URL.

```
{
  "config": {

   ...

    "archives": [

      ...

      {
        "enabled": true,
        "name": "obsidian.Vectrex-Extras",
        "type": "core_specific_archive",
        "archive_name": URL_KEY_TO_ARCHIVE,
        "file_extensions": [
          ".vec",
          ".ovr",
          ".bin"
        ],
        "has_instance_jsons": true
      },

      ...

    ]
  },
  "core_settings": {

  ...

  }
}  
```