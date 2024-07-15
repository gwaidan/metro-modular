# Dynamo Motherboard

This is a fork from Pichenettes' Shruthi Digital v08 board at https://github.com/pichenettes/shruthi-1/blob/master/shruthi/hardware_design/pcb/ The Shruthi is a fantastic digital/analog hybrid synthesiser, and this board is the instrument's digital heart. In line with the original, it is released under a Creative Commons cc-by-sa 3.0 license. 


<b>v0.95j (initial):</b> This is a "fork of a fork", in that it incorporates the v0.9j mods, with the only difference that it has been modified to fit E-Switch 320.02E11 keyswitches, and so is *not* compatible with the standard TL1100 keyswitch footprint.


<b>v0.9j (initial):</b> As the original was a well iterated, well-proven, and mature design, there was not a lot to do. Main changes are: 

-conversion to Kicad v8 from the deprecated EAGLE format;

-adding holes for locator pegs so that Omron/Alps keyswitches will fit as well as the standard E-Switch TL1100;

-pads for an SMD1210 capacitor to attempt to mitigate noise bleedthrough from OLED displays; 

-moving the AVRISP header slightly for better mechanical clearance from the Edit 2 pot; 

-slotted encoder body tab pads to allow the Bourns PEC11R series;

-less defensive design rules to improve ground plane connectivity (taking into account the improvements in quality of small-batch PCB fab houses such as JLC since 2012);

-slightly beefed-up ground plane stitching;

-moving a signal via away from the crystal footprint to allow the option of untented vias;

-removing branding/trademarks and renaming in accordance with Pichenettes' wishes.
