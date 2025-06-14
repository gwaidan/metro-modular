# Brickworks Motherboard

This is a fork from Pichenettes' Ambika Motherboard v09 board at https://github.com/pichenettes/ambika/tree/master/controller/hardware_design. The Ambika was a very impressive DIY digital/analog hybrid polysynth, and this board contains the ATMEGA that directs all the voicecards, as well as UI circuitry and audio output circuits. The original never got the product maturation it deserved, as Pichenettes was discouraged by the design constraints imposed by the 8-bit AVR platform, and efforts that were put into a 32-bit ARM version ended up being cannibalised by Mutable's incredibly successful Eurorack modules. This project is fully compatible with the enclosure designs and software of the original. In line with the original, it is released under a Creative Commons cc-by-sa 3.0 license. 


<b>v1.05j (initial):</b> Main changes are: 

-conversion to Kicad v8 from the deprecated EAGLE format;

-redesigned power supply, converting the original all-linear power supply circuitry, reliant on an external 9VAC source, to a hybrid where incoming 18VDC is subregulated by switcher modules to +/-12V supplies, which are then downregulated by linear regulators to +/-8V, and the 18VDC is also regulated by a non-isolated Murata 78SR05 switcher down to +5V for digital. This removes the need to chase down an increasingly hard-to-get AC-output plugpack, replaces it with an external switcher that will work on global supplies, and removes the need for a poorer-performing LM2940 LDO linear reg to derive +8V. The isolated switcher regulators are an industry-standard 6W footprint, which is available from MeanWell and Advanced Energy/Artesyn, with the option of a high-efficiency, lower cost 78SR12 switcher for the positive supply.

-add ground plane keepout area underneath the negative regulator's heatsink, as the 7908's heat spreader tab is at -12V potential and is in contact with the (metal) heatsink;

-converting keyswitch footprints to fit the E-Switch 320.02E11. This switch raises the buttons by 3mm and is more expensive, however it has ten times the rated service life of the original TL1100, has gold internal contacts which should avoid intermittent operation issues caused by aging or enviromental oxidation, and most importantly has an extended plunger that will mate properly with the friction lock inside TAC keycaps, so keycaps will remain secure and not fall out if you turn the unit upside down! Hurrah!

-modified SD card reader footprint. As the TE SD card reader specified in the original is long obsolete, the footprint has been revised to fit five other currently available models which share the original's signal pin layout, but differ in the position of soldered retention tabs. Along the way, a few spacing errors in the original footprint have been fixed, along with adding a keepout area to stop signal pins in the reader potentially shorting out against the ground plane.

-output audio jack footprints have added pins to allow the option of the Neutrik NRJ6HF stereo jack-not only is this jack often cheaper and more readily available than the mono NRJ4HF, it also allows for passive line balancing by adding 470R resistors to ground on the individual output ring terminals, and a ground connection on the mix output ring terminal. The footprint is fully back-compatible with the NRJ4HF.

-slotted encoder body tab pads to allow the metal-shaft Bourns PEC11R series;

-updated the MIDI jack connections in line with the 2014 CA-033 revision of the MIDI 1.0 standard, by grounding the shell connection on the output jack, and connecting the shell and ground at the input jack to ground via 100n capacitors that remove RFI but block audio ground loop hum;

-less defensive design rules to improve ground plane connectivity (taking into account the improvements in quality of small-batch PCB fab houses such as JLC since 2012);

-slightly beefed-up ground plane stitching;

-specifying and labelling a 74HC4050 for IC3 rather than the slower CD4050, which is a known fix to improve SD card performance;

-adding a location marker to keep JLCPCB production batch numbers hidden out of sight;

-removing branding/trademarks and renaming in accordance with Pichenettes' wishes.
