#Dynamo Motherboard

This is a fork from pichenettes' Shruthi Digital v08 board at https://github.com/pichenettes/shruthi-1/blob/master/shruthi/hardware_design/pcb/

v0.9j (initial): As the original was well iterated and a mature design, there was not a lot to do. Main changes are: 
-conversion to Kicad v8 from the deprecated EAGLE format; 
-adding holes for locator pegs so that Omron keyswitches will fit; 
-pads for an SMD1210 capacitor on the power supply to the display module to attempt mitigate noise bleedthrough from passive matrix OLED units, 
-moving the AVRISP header slightly for better mechanical clearance from the Edit 2 pot; 
-slotted encoder body tab pads for compatibility with the Bourns PEC11R;
-less defensive design rules to improve ground plane connectivity (taking into account the improvements in quality of small-batch PCB fab houses such as JLC since 2012);
-slightly beefed-up ground plane stitching.
