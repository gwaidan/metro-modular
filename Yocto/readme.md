# Yocto

This is forked from the Yocto v0.2007 hardware design files originally published at https://midisizer.com/midialf/](https://github.com/e-licktronic/Yocto-V2.0/tree/main/Eagle 

The original is a really cool, faithful DIY TR808 clone enhanced with an added onboard PC-2 percussion synth clone, a 909-ish sequencer and a modern (by Roland standards at least :) ) 16x2 alphanumeric interface.


<b>v0.25j (forthcoming initial release):</b> Changes from the original will include:


-ported to KiCad 9 from the deprecated EAGLE format;

-updated the MIDI jack connections in line with the 2014 CA-033 revision of the MIDI 1.0 standard, by connecting the shell and ground at the input jack to ground via 100n capacitors that remove RFI but block audio ground loop hum;

-conversion of power supply to all-switching to allow a universal voltage external DC power brick.

-removal of the 10n capacitors to ground on all audio outs, which appear to be a copy/paste from the TR909's output circuitry. They are not needed here due to much less digital circuitry in the tone generators, and they also affect high frequency response, particularly on the main outs!;

!-encoder footprint with slotted retention tab pads to accommodate the Bourns PEC11R series;

!-ground plane pour on both sides of the board.
