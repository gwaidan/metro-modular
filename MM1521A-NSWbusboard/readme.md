# MM1521A busboard project

This busboard is based on the Moraydular wide powerbus available at https://github.com/vaeinoe/moraydular/tree/master/powerbus

The main changes were aimed at optimising the board for a synth-building workshop where it would be used in a wide 104HP case. Therefore, the MTA 0.1" connectors and the quickconnect spade connectors have been stripped out. We have just left well-labelled inlet pads and added enough extra outlet connectors to handle a 104HP row, while (just) staying within the 300-pin free limit for DipTrace.

The board has been further tweaked to optimise it for novice builders using fixed temperature soldering irons, by paying attention to the thermal isolation of solder pads, while keeping end-to-end electrical resistance as low as possible in the key supply lines of +12V, GND and -12V. 

Further tweaks include external pads for the Gate/CV lines so these can be joined across a multi-row system, and holes for mounting 4mm clip-on standoffs. 
