# ttocyobitnA

ttocyobitnA (or Antiboycott) is a drop-in PCB for [Ttocyobitna](https://trashman.wiki/en/keyboards/ttocyobitna) with support for multiple layouts.

The original was made by [Trash Man](https://trashman.club/) while under the alias of Pycki47.
The open sourced files for it can be found [here](https://github.com/evangs/ttocyobitna).

## Status

**Currently Untested.** ***Order at your own risk.***

Note: JLCPCB may not have a preview show since they struggle to render hatched fills. It was able to render with a solid fill though so it should be fine.

Dimensions: 266.67mm x 76.17mm

Firmware can be found ([here](https://github.com/shinkaimayano/Firmwares)).

## Changes

- General Cleanup
  - Makes use of more default KiCad 6 libraries
    - Only external libraries used are [marbastlib](https://github.com/ebastler/marbastlib) and [ai03's Switch Symbol](https://github.com/ai03-2725/MX_Alps_Hybrid)
  - Organized files and folders
    - Removed old libraries and footprints
- Redone Eeschema
  - Switched to a USB-C 2.0 symbol
  - Tray mount holes are now included in the schematic
  - More clear labeling of the switch matrix
- Revamped PCBNew
  - Rerouted with curved traces and changed to a hatched GND fill
  - Capacitors and resistors have been changed to a smaller footprint (0605 &rarr; 0402)
  - Replaced the 1uF capacitor for a 10uF on the VBUS line
    - This is recommended by the 32U4 datasheet (Section 21.5)
  - Replaced the TVS diodes with a SRV05-4
  - Switched the USB-C footprint to the more common HRO-M-12
  - Added two extra 100nF decoupling capacitors
  - Added a 1k&Omega; resistor to the crystal to protect it from being over-driven
  - Added an ISP breakout
    - Also acts as an RGB strip breakout (top pads)
    - Removed reset button as a result
  - Proper shield implementation (4.7nF capacitor, 1M&Omega; resistor, and a screw hole connected to Earth)
- More layout options (see [KLE](http://www.keyboard-layout-editor.com/#/gists/c1b2365e78564452fc1ebb7e3b01f5bb))
  - Added silkscreen text to explicitly show mod size and layout options
  - Rotary encoder support in the top right as well as 1u/1.5u
  - Stepped caps-lock support
    - Supports 3.0mm THT LED indicator
  - Full right shift support (2.75u)
  - 6.25u Spacebar bottom rows
  
![KLE](Images/ttocyobltnA-layouts.png)

## Renders

![Front](Images/front.png)

![Back](Images/back.png)
