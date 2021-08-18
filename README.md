# ZGloom

A port of [ZGloom](https://github.com/Swizpig/ZGloom) for the PlayStation Vita.

# Instructions

## Linux

1. Install the [VitaSDK](https://vitasdk.org/)
2. Install the LibXMP vita library port
3. Generate makefile with cmake .
4. Compile with `make`.

# How to play

Gloom was made freely available by its developers [here](https://github.com/earok/GloomAmiga/archive/master.zip).
To play on vita download and move the assests into the following location on vita:
ux0:/data/zgloom/ 


# In-game music

ZGloom can now add in-game music using any module that XMP can play. Put the mods in the sfxs folder and add "song_blitz.mod" or whatever the module name is to the script. Multiple song_ commands are allowed, allowing per-level music.

# TODO
change renderer

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
