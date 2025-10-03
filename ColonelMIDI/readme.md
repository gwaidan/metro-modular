# ColonelMIDI 5x5 Port USB-MIDI Interface

This is an updated take on the nILS GM5x5x5 multiport implementation of the Polytec GM5 reference board, based around an Atmel AT90USB processor with preloaded custom firmware. Although it uses the published mechanical dimensions of the GM5x5x5, it is effectively a new circuit design that improves in many respscts on both the reference board and the GM5x5x5, with care taken to return to datasheets to ensure that part values are compatible with specifications.


<b>v0.1 (initial):</b> Main improvements over antecedents are: 

-usage of Kicad v9 rather than the deprecated EAGLE format;

-reverse voltage proection Schottky diode;

-zener diodes to protect USB data lines against over/reverse voltage; 

-modern SOT236 high-current CMOS schmitt trigger buffers for LED driving and buffering; 

-LEDs located directly in front of the ports they indicate; 

-6-pin AVRISP port added for those who might want to program their own firmware from scratch on a blank chip;

-GM5x5x5 options for external power and for configuring the number of ports downwards are not ncluded, as this is intended as a standalone device rather than a legacy "MIDIbox module"

-adding a location marker to keep JLCPCB production batch numbers hidden out of sight;

-tidied-up board layout with ground planes both sides

<b>v0.11:</b> 

-fix incorrect port labelling on LED side of board;

<b>v0.12 (first publication):</b> 

-use "spare" gates in input LED drivers to buffer 6N137 optocoupler outputs;
