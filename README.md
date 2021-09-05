# ZGloom-Vita

A port of [ZGloom](https://github.com/Swizpig/ZGloom) for the PlayStation Vita.<br>
A fork of [ZGloom-vita](https://github.com/JetStreamSham/ZGloom-vita) from [JetStreamSham](https://github.com/JetStreamSham)

## What's new?
1. added a launcher to the game to have all Gloom-Engine games available
2. added a cheat menu into the game menu to set invinite health photon weapon at start

## What is Gloom?

[Gloom](https://en.wikipedia.org/wiki/Gloom_(video_game)) was a 1995 Doom-clone from Black Magic Software for Commodore Amiga. It had [very messy and meaty graphics](https://www.lemonamiga.com/games/details.php?id=1781) and needed a very powerful Amiga computer back then (A1200 @ 030 was far too low). It had several official successors like Gloom Deluxe/Ultimate Gloom (a graphical enhanced Gloom), Gloom 3, Zombie Massacre and even some full-game conversion of 90's Amiga games.

# Instructions

## How to play

Gloom was made freely available by its developers [here](https://github.com/earok/GloomAmiga/archive/master.zip).<br>
For the other official games using the Black Magic "Gloom"-engine like [Gloom 3](http://aminet.net/package/game/shoot/UltimateGloomISO) or [Zombie Massacre](http://aminet.net/package/game/shoot/ZombieMassacreISO) you can load them for free on Aminet. Otherwise you can take the original game files from your game installation.

To play on PS VITA install the .vpk, download the .zip of the game(s) you want to play, extract them somewhere to your harddrive and copy only the folders (depending on the game) to the following locations on vita:

> ux0:/data/zgloom/gloom <br>
> ux0:/data/zgloom/deluxe <br>
> ux0:/data/zgloom/gloom3 <br>
> ux0:/data/zgloom/massacre

![Preview of Livearea](https://github.com/andiweli/ZGloom-vita/blob/master/images/gloom-livearea.png)

### Some screenshots from the game Gloom Deluxe itself
![Preview of the game](https://github.com/andiweli/ZGloom-vita/blob/master/images/gloom-mockup.png)

## In-game music

ZGloom can now add in-game music using any module that XMP can play. Put the mods in the sfxs folder and add "song_blitz.mod" or whatever the module name is to the script. Multiple song_ commands are allowed, allowing per-level music.

## Building on Linux

1. Install the [VitaSDK](https://vitasdk.org/).
2. Install the LibXMP vita library [port](https://github.com/JetStreamSham/libxmp). See the [porting libraries](https://vitasdk.org/) section for installtion instructions.
3. Generate makefile with `cmake CMakeLists.txt`.
4. Compile with `make`.

# TODO
Change renderer

# License

Dunno. [The Gloom source release](https://github.com/earok/GloomAmiga) says only the .s and .bb2 files are open source, but the Gloom executable bakes in some maths lookup tables (but then, they are generated by the .bb2 files), bullet and sparks graphics, and 
the title screen for Classic Gloom. I probably won't add the latter and just display the Black Magic image, or something.

Uses LibXMP for MED playback
http://xmp.sourceforge.net/

Uses SDL2 and SDL2 mixer
https://www.libsdl.org/

DeCrunchmania C code by Robert Leffman, licence unknown
http://aminet.net/package/util/pack/decrunchmania_os4

Uses Vita SDK
https://vitasdk.org/
