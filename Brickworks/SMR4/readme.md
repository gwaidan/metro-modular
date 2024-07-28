# Brickworks SMR4 Voicecard
This is a fork from Pichenettes' Ambika SMR Voicecard at https://github.com/pichenettes/ambika/tree/master/controller/hardware_design. This was the consensus pick for the best of the original three voicecards released for the Ambika. 


<b>v0.51j (initial):</b> Main changes are: 

-conversion to Kicad v8 from the deprecated EAGLE format;

-addition of an additional trimmer and associated circuitry to adjust central tune point as well as v/oct span. This permits much better matching between voicecards to avoid "voice cycling" artifacts, as well as moving parts around and reversing the TL084P to better accommodate it;

-adding an (optional) inexpensive dual matched SOT363 transistor footprint to replace the dual 2N3906 filter OTA drivers, for advanced solderhounds;

-replacing the LM13700N footprints with surfacemount LM13700M equivalents. A hard call, but the thru-hole version is now out of production by TI (it was discontinued by JRC years ago) and Mouser now charge a premium for them, which they can afford to do as they hold the last remaining stocks anywhere. Given the availability situation, the additional expense of 18 parts across a full voicecard set, plus the fact that the Ambika was always intended for advanced builders, it made sense to go surfacemount for this part. Plus SO-16 is pretty easy, especially in this layout (hint: solder them before anything else);

-output audio jack footprints have added pins to allow the option of the Neutrik NRJ6HF stereo jack-not only is this jack often cheaper and more readily available than the mono NRJ4HF, it also allows for passive line balancing by adding 470R resistors to ground on the individual output ring terminals, and a ground connection on the mix output ring terminal. The footprint is fully back-compatible with the NRJ4HF.

-some tweaking of layout to reduce trace lengths and eliminate signal vias where possible;

-removing branding/trademarks and renaming in accordance with Pichenettes' wishes.
