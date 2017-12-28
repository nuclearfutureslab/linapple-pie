# linapple-pie (with IBX ]\[ emulation)

This is a fork of the port of linapple2b.

It has additional capability to emulate the extension cards used in IBX ]\[. IBX ]\[ is an information barrier setup for nuclear warhead verification with an Apple II ([Details](www.vintageverification.org)). It was presented at 34C3.

The HV Card is automatically loaded in slot 2. For slot 4, either a 8bit or a 12bit (11 real) version of an ADC card can be loaded. This is done by adding `IBX Card = 1` (8bit) or `IBX Card = 2` (12bit) to the respective linapple.conf file. The 12bit ADC card is really an 11bit card, the MSB is always zero. Values for both cards are sampled from 256 channel radiation spectra, two examples are provided. The executable always looks for a `spectrum.dat` in the working directory (If it is not there, it will end with a segmentation fault).
