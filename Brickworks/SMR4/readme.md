# Brickworks SMR4n Voicecard
This is a fork from Pichenettes' Ambika SMR4 Voicecard at https://github.com/pichenettes/ambika/tree/master/controller/hardware_design. With a raw, Roland-y sound, this was generally regarded by users as the best of the original three voicecards released for the Ambika.  It is fully compatible with the enclosure designs and software of the original. In line with the original, it is released under a Creative Commons cc-by-sa 3.0 license. 

<b>v0.51j (initial):</b> Main changes are: 

-conversion to Kicad v8 from the deprecated EAGLE format;

-adding an extra trimmer and associated circuitry to adjust central tune point as well as V/oct span, as well as moving parts around and reversing the TL084P to better accommodate it. This change permits much better alignment between voicecards to avoid "voice cycling" artifacts;

-adding an extra footprint for an (optional) inexpensive dual matched SOT363 transistor instead of the dual 2N3906 filter OTA drivers, for advanced solderhounds;

-replacing the LM13700N footprints with surfacemount LM13700M equivalents. A hard call, but the thru-hole version is now out of production by TI (it was discontinued by JRC years ago) and Mouser now charge a premium for them, which they can get away with as they hold the last remaining verified legit stocks anywhere. Given the availability situation, the additional expense of 18 parts across a full voicecard set, plus the fact that the Ambika was always intended for advanced builders, it made sense to go surfacemount for this part. Plus SO-16 is pretty easy, especially in this layout (hint: solder them before anything else);

-some tweaking of layout to reduce trace lengths and eliminate signal vias where possible;

-adding a location marker to prevent JLCPCB production batch numbers from corrupting aesthetics;

-removing branding/trademarks and renaming in accordance with Pichenettes' wishes.
