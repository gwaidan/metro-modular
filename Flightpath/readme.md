# Flightpath monosynth

This is a fork from Pichenettes' Anushri Rev C boards at https://github.com/pichenettes/anushri/tree/master/anu/hardware_design. The Anushri was a unique all-analogue signal path VCO monosynth with very responsive digital modulation sources, a hands-on interface, and a unique lo-fi digital drum machine that piloted the subsequent Grids Euro module, all in two circuit boards. In line with the original, it is released under a Creative Commons cc-by-sa 3.0 license. 


<b>vDj (initial):</b> Main changes are: 

-conversion to Kicad v8 from the deprecated EAGLE format;

-converting keyswitch footprints to fit the E-Switch 320.02E11. This switch raises the buttons by 3mm and is more expensive, however it has ten times the rated service life of the original TL1100, has gold internal contacts so should avoid intermittent operation issues caused by aging or oxidation, and most importantly has an extended plunger that will mate properly with the friction lock inside TAC keycaps, so keycaps will remain secure and not fall out if you turn the unit upside down! Hurrah!

-as the through-hole 2N5485 JFET required by the VCO is now obsolete, as are the through-hole verions of recommended substitutes like the J112, a SOT23 surfacemount footprint has been added for those who are confident with soldering and want to avoid the hive of scum and villainy that is aftermarket semiconductor sales on eBay.

-jack footprints have added pins to allow the option of the Neutrik NRJ6HF stereo jack-not only is this jack often cheaper and more readily available than the mono NRJ4HF, it also allows for passive line balancing by adding 470R resistors to ground on the individual output ring terminals, and a ground connection on the mix output ring terminal. The footprint is fully back-compatible with the NRJ4HF.

-slotted encoder body tab pads to allow the Bourns PEC11R series;

-less defensive design rules to improve ground plane connectivity (taking into account the improvements in quality of small-batch PCB fab houses such as JLC since 2012);

-slightly beefed-up ground plane stitching;

-specifying and labelling a 74HC4050 for IC3 rather than CD4050, to try and improve SD card performance;

-removing branding/trademarks and renaming in accordance with Pichenettes' wishes.
