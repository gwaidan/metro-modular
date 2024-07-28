# Flightpath monosynth

This is a fork from Pichenettes' Anushri Rev C boards at https://github.com/pichenettes/anushri/tree/master/anu/hardware_design. The Anushri was a rich, modern-sounding VCO monosynth with very responsive digital modulation sources, a hands-on interface, and a unique lo-fi digital drum machine that piloted the subsequent Grids Euro module, all in two circuit boards. It is fully compatible with the emnclosure designs and software of the original. In line with the original, it is released under a Creative Commons cc-by-sa 3.0 license. 


<b>Rev Dj (initial):</b> Main changes are: 

-conversion to Kicad v8 from the deprecated EAGLE format;

-converting keyswitch footprints to fit the E-Switch 320.02E11. This switch raises the buttons by 3mm and is more expensive, however it has ten times the rated service life of the original TL1100, has gold internal dome contacts so should avoid intermittent operation issues caused by ageing or environmental oxidation, and most importantly has an extended plunger that will mate properly with the friction lock inside TAC keycaps, so keycaps will remain secure and not fall out if you turn the unit upside down! Hurrah!

-as the through-hole 2N5485 JFET required by the VCO is now obsolete, as are the through-hole versions of recommended substitutes like the J112, a SOT23 surfacemount footprint has been added for those who are confident with soldering and want to avoid the wretched hive of scum and villainy that is aftermarket semiconductor sales on eBay;

-the drum output in Rev C had a very simple passive RC lowpass filter down 3dB about 15kHz, with significant passband droop starting well below 10k. When the drum output is isolated via the 3.5mm jack, this powpass assive filter is directly loaded by the destination's input impedance, so that low impedance loads can affect its response. To get around this a, a new IC25 dual opamp has been added, half of which implements an active 2-pole Butterworth filter with basically the same 3dB point, but a flat passband up to a "hard knee" at about 10kHz, and fast rolloff thereafter. The filter provides buffered output thru a 470R limit resistor. The "spare half" of IC25 is used to buffer the master volume pot's output, again so it will not be loaded down by low impedance mixer or audio interface inputs;

-main jack footprints have added pins to allow the option of the Neutrik NRJ6HF stereo jack-not only is this jack often cheaper and more readily available than the mono NRJ4HF, it also allows for passive output line balancing by adding a 470R resistor to ground on the main output ring terminal. The footprints are fully back-compatible with the NRJ4HF;

-the footprint for the 3.5mm jackfield connectors has been redone. Due to the tight spacing and need to keep 10mm maximum height, neither of the modern Qingpu jacks commonly used in Eurorack was suitable to replace the Lumberg 1502 03, however Rev C's 1502 03 footprint had multiple errors, and has therefore been revised. Vertical jack coordinates have been offset by 0.01" to account for the fact that the Rev C case design evidently did so to compensate one of the aforementioned footprint errors (I need paracetamol!);

-Rev C's gate and clock I/O go directly to their respective 3.5mm jacks from IC15 (CD4050N) without any addtional current limit protection, polarity protection or diode clamping. Given any of these may be connected to Euro equipment with normalled voltages between +12V and -12V, this was a concern. I may be paranoid, but the circuit now specifies a more robust 74HC4050 for IC15, and there are current limit resistors on all four outputs and inputs as further mitigation;

-less defensive design rules to improve ground plane connectivity (taking into account the improvements in quality of small-batch PCB fab houses such as JLC since 2012);

-slightly beefed-up ground plane stitching, and the component board now has ground pours on both sides;

-removing branding/trademarks and renaming in accordance with Pichenettes' wishes.
