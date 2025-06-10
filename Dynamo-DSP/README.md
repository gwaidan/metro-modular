# Dynamo DSP daughterboard

This is a fork from Pichenettes' Shruthi DSP board. This is an ultra lowfi board that uses an Arduino-class processor to give funky digital filtering and effects processing. It is fully compatible with the enclosure designs and software of the original. In line with the original, it is released under a Creative Commons cc-by-sa 3.0 license. 


<b>v0.41j (initial):</b> Main changes are: 

-conversion to Kicad v9 from the deprecated EAGLE format;

-change jack footprints for jacks to stereo versions (fully backwards compatible with mono jacks) to allow wider choice of jacks;

-optional circuitry connected to the output jack ring connection to allow for passive balancing; 

-isolate the digital ground from the analogue ground back to a defined star point at the power inlet; 

-label the input aliasing and output clock noise filters; 

-optimise filter layouts so there is plenty of room for precision polypropylene caps should you desire;

-less defensive design rules to improve ground plane connectivity (taking into account the improvements in quality of small-batch PCB fab houses such as JLC since 2012);

-adding a location marker to keep JLCPCB production batch numbers hidden out of sight;

-removing branding/trademarks and renaming in accordance with Pichenettes' wishes.
