# Mindscape Music Board

Reproduction of the early PC sound card of the same name.

**Status: Untested**

![Render of PCB](https://raw.githubusercontent.com/Board-Folk/Mindscape_Music_Board/master/images/mmb_pcb.jpg)

**Caution:** ensure the ISA clock of your PC is no greater than 5 MHz. The
ISA clock is halved before feeding this to the AY chips, which are rated for
a maximum of 2.5 MHz. Anything faster than this may damage them. The original
IBM PC and XT run at 4.77 MHz, which is fine. You might get away with a 6 MHz
AT but the pitch of the audio will be way off what was intended. A later 8 MHz
AT would be pushing it.

## Settings

The base address is set using the DIP switch `SW1` whose positions correspond
to address lines `A2` thru `A9`. Note however that somewhat counterintuitively
the switch marked `1` on the original board (joining pins 1 and 16) corresponds
to `A9` and the switch marked `8` (joining pins 1 and 16) corresponds to `A2`.

To set the default base address of `300h` one must therefore close all switches
except those for `A8` and `A9`. This can also be done with wire jumpers instead
of an actual DIP switch.


## BOM/Parts

Refer to the KiCad project for the most up-to-date BOM.

Some capacitor values have been guesstimated but most don't appear to be
critical. As the original board omits many of the decoupling capacitors, these
are marked "Do Not Populate" but you may prefer to fit them anyway.

The volume potentiometer `R4` doesn't appear to be easily available. Setting
the volume with a dial on the back of the PC isn't particularly convenient
anyway, so you may prefer to set the volume at a predetermined level using
fixed resistors and leave volume control up to your amplifier/speakers.


## Legal

As the product of this project is a replica of a proprietary product, the
the author makes no claim of copyright to the schematics nor PCB layouts and
releases these into the public domain, solely for the purposes of study and
historical preservation.

You are free to produce PCBs based on this project's designs at your own risk
and without limitation, for your own use or for sale and/or repair at a
reasonable price. Attribution is appreciated. The authors are not obliged to
provide support of any kind.

Under no circumstances will the authors be held responsible or liable in any
way for losses, damages or costs resulting from the use of the information
and/or resources of this project.

The resources are provided "as-is" without warranty of any kind, either
expressed or implied, including, but not limited to, the implied warranties
of merchantability and fitness for a particular purpose.
