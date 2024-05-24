# Capcom Z80 Combination Core

![Capcom Z80](https://github.com/dyreschlock/pocket-platform-images/blob/main/pics/arcade/jtcz80_c.png?raw=true)

In the mid-80s, Capcom used the Z80 cpu to power its Arcade games. This began with the arcade classic <b>1942</b>, and includes many others. <b><a href="https://www.patreon.com/jotego">Jotego</a></b> has implemented cores for all of these games, but they've all been released as separate cores with slightly different implementations. Many of them have the same resolution, so I have combined them into a single core.

This combines the following cores: <b>1942</b>, <b>1943</b>, <b>Black Tiger</b>, <b>Commando</b>, <b>Exed Exes</b>, and <b>Gun.Smoke</b>

## Set-up Note #1

As usual, this distribution does not contain the actual RBF core files. Please download the cores from Jotego's repository, and copy the RBF files into the correct locations.

Check inside the core folder for which files are required:
- /Cores/jotego.jtcz80_c/

## Set-up Note #2

I didn't include any MRA files. These cores are using the same roms as they would be normally, so just copy them from your other core folders, or use the updaters to get new copies.