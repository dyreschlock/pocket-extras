# Donkey Kong and Radar Scope Extras

![DonkeyKong](https://github.com/dyreschlock/pocket-platform-images/blob/v4.0.0/pics/arcade/donkeykong.png?raw=true)

The <b><a href="https://github.com/ericlewis/openFPGA-DonkeyKong">Donkey Kong</a></b> and <b><a href="https://github.com/ericlewis/openFPGA-RadarScope">Radar Scope</a></b> cores were created by Eric Lewis, and he developed them to load a single rom at a time.  When you select the core, it'll immediately boot into Donkey Kong. Modern arcade cores allow you to choose a JSON file for the game you want to play, which allows the core to play multiple games, rather than just one.  Donkey Kong has many many romhacks, so I made some edits to the `data.json` which allows JSON to be selected.

Included in `pocket-extras` are:
- edits to allow game selection
- JSON and MRA files for all Donkey Kong games from Mister
- JSON and MRA files for romhacks from donkeykonghacks.net

Additionally, all of these will run on the RadarScope core, so I made the same edits and additions there.

Thanks to <b><a href="https://github.com/GoldZabu">GoldZabu</a></b> for all the dkhacks.net Hacks! :)

For instructions building the dkhacks.net Hacks, <a href="/dk-extras/Assets/donkeykong/mra/donkeykonghacks.net/README.md">look here</a>.

### Note

Many of these MRA files require some extra work in order to generate the roms correctly. The pocket updaters should pull down the correct files for each of these JSON, so you can skip making them yourself, if you'd like.

Thank you to <b><a href="https://github.com/mattpannella">Matt Pannella</a></b> and <b><a href="https://github.com/retrodriven">Retro Driven</a></b> for that!
