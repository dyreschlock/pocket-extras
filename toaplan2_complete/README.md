# Toaplan Version 2 Hardware Combination Core

The Coin-Op Collection group has now released all of their games based on the Toaplan Version 2 Hardware arcade board on the Analogue Pocket. In 2022, <a href="https://github.com/psomashekar">pram0d</a> released <b>Battle Garegga</b>, <b>Battle Bakraid</b>, <b>Sorcer Strike</b>, <b>Kingdom Grand Prix</b>, <b>Armed Police Batrider</b>, and <b>Snow Bros 2</b> for the Pocket. And recently, in 2023, <a href="https://github.com/atrac17">atrac17</a> released <b>Truxton 2</b> and <b>Pipi & Bibs</b>. There are more games based on this arcade hardware, but these 8 games are all of the ones currently implemented in FPGA.

All of them have been released as Single Game cores. You can find those implementations here: <a href="https://github.com/Coin-OpCollection/Distribution-OpenFPGA">Coin-OpCollection/Distribution-OpenFPGA</a>

I've taken all of these cores and combined them into a single Arcade Multi core. This should help clean up your Arcade folder on the openFPGA menu.

## Usage Note

Some Toaplan2 games use the Standard 4x3 horizontal resolution, known as Yoko mode. Others use the Rotated vertical resolution, known as Tate. These resolutions can't be configured through files only, so the combination core is split into two parts: Rotated and Standard. Because they share the same `platform_id`, they will display in the openFPGA as a single entry. To switch between the two, choose `Core` from the openFPGA menu.

Games are not shared between Rotated and Standard, so only Tate games will show up when Rotated is selected. Likewise, only Yoko games will show up when Standard is selected.

## Set-up Note #1

This distribution does not contain the actual RBF core files. Please download the cores from Coin-Op, and copy the RBF files into the correct locations.

Check inside the following locations to place RBF files:
- /Cores/coinop.Toaplan_V2_Rotated/
- /Cores/coinop.Toaplan_V2_Standard/

## Set-up Note #2

I modified the MRA files slightly by changing the RBF to toaplan2_c. 

Also, all of the JSON files for the core are expected the full set name, rather than a truncated 8 character name. So, you won't be able to do a straight ROM copy from your current cores.

The pocket updaters should pull down the correct files for each of these JSON, so you can skip making them yourself, if you'd like.

Thank you to <b><a href="https://github.com/mattpannella">Matt Pannella</a></b> and <b><a href="https://github.com/retrodriven">Retro Driven</a></b> for that!
