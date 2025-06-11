# Polivoks DSP daughterboard

This is a fork from Pichenettes' Polivoks filter board at https://github.com/pichenettes/shruthi-1/tree/master/shruthi/hardware_design/pcb. This is an adaptation of Marc Bareille's take on the classic Soviet programmable-power multimpde opamp filter, that Pichenettes turned out during her insane burst of creativity from 2010 to 2014, and never iterated past the first v0.1. It is fully compatible with the enclosure designs and connectivity of the original. In line with the original, it is released under a Creative Commons cc-by-sa 3.0 license. 


<b>v0.2j (initial):</b> Main changes are: 

-conversion to Kicad v8 from the deprecated EAGLE format;

-change jack footprints for jacks to NMJ6HFD2 stereo versions (fully backwards compatible with NMJ4HFD2 mono jacks) to allow wider choice of jacks;

-optional circuitry connected to the output jack ring connection to allow for passive balanced output with NMJ6HFD2 stereo jack; 

-based on my experience designing the Steel Falcon VCF, programmable power opamps are very sensitive to noise at low drive current (ie low frequency), and the original of this design was no exception-therefore the CV summer/driver and expos converter transistor driver have been moved to IC4 to minimise trace lengths to the LM4250s; 

-general layout tweaks;

-double-sided ground plane;

-less defensive design rules to improve ground plane connectivity (taking into account the improvements in quality of small-batch PCB fab houses such as JLC since 2012);

-adding a location marker to keep JLCPCB production batch numbers hidden out of sight;

-removing branding/trademarks and renaming in accordance with Pichenettes' wishes.

