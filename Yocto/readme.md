# Yocto

This is forked from the Yocto v0.2007 hardware design files originally published at https://midisizer.com/midialf/](https://github.com/e-licktronic/Yocto-V2.0/tree/main/Eagle 

The original is a really cool, faithful DIY TR808 clone enhanced with an added onboard PC-2 percussion synth clone, a 909-ish sequencer and a modern (by Roland standards at least :) ) 16x2 alphanumeric interface.


<b>v0.25j (initial release):</b> Changes from the original include:

-added the "missing" 220R resistor on the UART side of the MIDI out jack. (this was also missing in the Shruthi-1 motherboard design, and is needed to balance the MIDI signal for noise reduction);

-updated the MIDI jack connections in line with the 2014 CA-033 revision of the MIDI 1.0 standard, by grounding the shell connection on the output jack, and connecting the shell and ground at the input jack to ground via 100n capacitors that remove RFI but block audio ground loop hum;

-ported to KiCad 9 from the deprecated EAGLE format;

!-encoder footprint with slotted retention tab pads to accommodate the Bourns PEC11R series;

-ground plane pour on both sides of the board.
