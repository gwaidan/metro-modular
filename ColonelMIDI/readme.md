# ColonelMIDI 5x5 Port USB-MIDI Interface

This is an updated take on the [nILS GM5x5x5](http://www.midibox.org/dokuwiki/gm5x5x5>) multiport implementation of the [Ploytec GM5](https://www.usb-audio.com/gm5/) reference board, based around an Atmel AT90USB processor with preloaded custom firmware. Although it uses the published mechanical dimensions of the GM5x5x5, it is effectively a new circuit design that improves in many respects on both the Ploytec reference design and the GM5x5x5, with care taken to return to datasheets to ensure that part values are compatible with specifications.


<b>v0.1 (initial):</b> Main improvements over antecedents are: 

-usage of Kicad v9 rather than the deprecated EAGLE format;

-reverse voltage proection Schottky diode;

-zener diodes to protect USB data lines against over/reverse voltage; 

-modern SOT236 high-current CMOS schmitt trigger buffers for LED driving and signal buffering; 

-LEDs located directly in front of the ports they indicate; 

-6-pin AVRISP port added for those who might want to program their own firmware from scratch on a blank chip;

-GM5x5x5 option for external power and guidance for reducing the number of ports are not included, as this is intended as a standalone "full-function" device rather than an embedded submodule;

-adding a location marker to keep JLCPCB production batch numbers hidden out of sight;

-tidied-up board layout with ground planes both sides;

-cc-by-sa licensing with no restrictions on use

<b>v0.11:</b> 

-fix incorrect port labelling on LED side of board

<b>v0.12 (first source publication):</b> 

-use "spare" gates in input-side LED drivers for "belt and braces" buffering of 6N137 optocoupler outputs;

-add 10u SMT cap on Vcc line near MCU
