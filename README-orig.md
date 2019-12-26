
(Info below comes from the original project website: http://www.icculus.org/armoda/ )
---------------------------------

## Armoda Music System
Armoda is a music and sound effects system for games and other multimedia applications.
It is one of John Hall's side projects, and is still under development. However,
Armoda is already quite usable as a command line module player.

## Features

*    Support for 4-, 6-, and 8-channel Protracker compatible .mod modules.
*    Support for ScreamTracker 3 .s3m modules.
*    Support for DSIK .dsm modules.
*    Callback-based effects system, allowing additional formats to be added with comparatively little effort.
*    Pluggable mixer backends. Currently there is a software mixer with SDL audio output, but the interface was designed with hardware mixing and higher-quality software mixing algorithms in mind.
*    Ability to allocate additional mixer channels for game sound effects and other non-music uses.
*    mod2c utility for embedding modules as C data structures.

## To Do List

*    Support for FastTracker 2 .xm modules. This will be a challenge due to XM's rich feature set, but I consider this a priority.
*    Support for Impulse Tracker .it modules. This is less of a priority than XM.
*    High-quality software mixer with cubic interpolation.
*    Hardware mixer implementation. (EMU10k perhaps?)

## Known Issues

*    SDL buffering is rather clunky and should be cleaned up.
*    Effect chaining (used, for instance, to implement S3M effects on top of certain MOD effects) isn't as clean as I would like. And it breaks every time I look at it funny.
*    Glissando is not implemented. However, I have yet to find a track that uses this effect, and it's something of a pain to code.
*    Funkrepeat is not implemented. Same reason as glissando, but even more so.
*    Some S3M effects are buggy. An afternoon of listening and tweaking should take care of most of these problems.
*    Volume levels for mixing need some reconsideration.
*    DSM support is still buggy, thanks to a complete lack of documentation for this format.

## Compatibility
I test Armoda against the weirdest modules I can find. It plays the infamous blkqueen.mod and ode2ptk.mod modules perfectly (as far as I can tell), and handles some other files that MikMod has trouble with. Protracker .mod support is very good. .s3m is mostly supported, but needs some work. .dsm modules are mostly recognizable, but almost always have glitches.

## Download
No binaries yet, but feel free to grab the code from Subversion. Thanks to icculus.org for SVN and web hosting.

`svn co svn://svn.icculus.org/armoda/trunk/ armoda`

## License
Ugh, I hate software licensing. So I've chosen a rather unrestrictive one. Armoda is licensed under Overcode's Source License. In return for my efforts, I request bug reports and, where appropriate, credit for my code. However, these are not required.
