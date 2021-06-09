# md-driver-signatures

[Radare2](https://github.com/radareorg/radare2) signature files for well known sound drivers used in Sega Genesis/Mega Drive games. To aid in the development of MSU-MD and MD+ patches.

Currently signatures for the following drivers are available:
- [GEMS](https://segaretro.org/GEMS) (source code available)
- [Krisalis](https://segaretro.org/Krisalis_Software)

Check this [list](http://gdri.smspower.org/wiki/index.php/Mega_Drive/Genesis_Sound_Engine_List) for more info on the drivers used by games.

## How to use

Start radare cli with the ROM file.

`r2 -a m68k <ROM.bin>`

Load signature database

`[0x00000200]> zo .\signatures\<DRV>.sdb`

Run analysis

`[0x00000200]> aaa`

show found signatures

`[0x00000200]> zi`
