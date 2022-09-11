# VCAmp

PCB and Front Pannel designed by me based off the [Mortiz Klein VCA](https://www.youtube.com/c/MoritzKlein0). This designs blends some of the presented ideas to make the amplifier I wanted.

## Features
- **EURORACK** compatible. 100KOhm output and 1KOhm input impedances. Compatible with eurorack sizes standard (128.5mm (3U) x 12HP).
- Two oscillators with independent CV and outputs.
  - **AMP-A** Recieves a signal in the CV input, offset can be added with the *ofsset* knob to adjust its workign. 
  - **AMP-B** Recieves a signal in the CV input, gain to the CV signal can be added with the *gain* knob. The gain is calculated for a 12V 555 (8V) ADSR to get the maximum useful voltage.

![](./imgs/vca.JPG)
![](./imgs/front.png)

## Components

Full list of components needed are included in the VCA.csv file. 

### Potentiometers
- Potentiometers are Vertical Alpha 9mmm. 
- Jack sockets are PJ301M-12.

### Capacitors

Input "coupling" capactior can be replaced for a different high value like 1uF for example, or even bypassed.

## Matching offset

Since the amplifier is based on a differential pair amplifier, the transistors have to be matched. Since standard BC547 transistors are being used, we can make reduce the matching difference by applying base voltage on the non-input transistor. 

- For the **left amp channel** matching pot is **RV3** trimmer.
- For the **right amp channel** matching pot is **RV4** trimmer.

Also any other matching would be useful, for example both the load resistors and the Differential Opamp (substractor) resistors.
 
![](./imgs/Schematic.png)
