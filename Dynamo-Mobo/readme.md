# Dynamo Motherboard

This is a fork from Pichenettes' Shruthi Digital v08 board at https://github.com/pichenettes/shruthi-1/blob/master/shruthi/hardware_design/pcb/ The Shruthi is a fantastic digital/analog hybrid synthesiser, and this board is the instrument's digital heart. It is fully compatible with the enclosure designs and software of the original. In line with the original, it is released under a Creative Commons cc-by-sa 3.0 license. 


<b>v0.95j:</b> This version has changed the keyswitch footprints to fit the E-Switch 320.02E11, and is not compatible with the keyswitches that fit v0.9j or earlier. This switch raises the buttons by 3mm and is more expensive, however it has ten times the rated service life of the original TL1100, has gold internal contacts so should avoid intermittent operation issues caused by aging or oxidation, and most importantly has an extended plunger that will mate properly with the friction lock inside TAC keycaps, so keycaps will remain secure and not fall out if you turn the unit upside down! Hurrah!

-added R17 aka the "missing" 220R resistor on the UART side of the MIDI out jack. (this was missing in the original design, and is needed to balance the MIDI signal)

-updated the MIDI jack connections to the 2014 MIDI 1.1 standard, by grounding the shell connection on the output jack, and connecting the shell and ground at the input jack to ground via 100n capacitors that remove RFI but block audio ground loop hum.


<b>v0.9j (initial):</b> As the original was a well iterated, well-proven, and mature design, there was not a lot to do. Main changes are: 

-conversion to Kicad v8 from the deprecated EAGLE format;

-adding holes for locator pegs so that Omron/Alps keyswitches will fit as well as the standard E-Switch TL1100;

-pads for an SMD1210 capacitor to attempt to mitigate noise bleedthrough from OLED displays; 

-moving the AVRISP header slightly for better mechanical clearance from the Edit 2 pot; 

-slotted encoder body tab pads to allow the Bourns PEC11R series;

-less defensive design rules to improve ground plane connectivity (taking into account the improvements in quality of small-batch PCB fab houses such as JLC since 2012);

-slightly beefed-up ground plane stitching;

-moving a signal via away from the crystal footprint to allow the option of untented vias;

-adding a location marker to keep JLCPCB production batch numbers hidden out of sight;

-removing branding/trademarks and renaming in accordance with Pichenettes' wishes.
