fc-av-mod
=========

This is yet another Famicom AV mod with following features:
- Composite Video and Audio output
- USB-C Power Supply
- Power LED

### Pre-requisites

- 1 x C1318 Transistor
- 2 x 22K resistors
- 1 x 0.47uF electrolytic capacitor
- 2 x 4.7uF capacitors(optional)
- USB-C PD decoy breakout board
- 3.5mm 4 pole connector(female)
- 1 x LED
- 1 x 330R resistor
- small PCB

### Modify Famicom main board

1. Desolder & Tear-off RF & PSU board
2. Extract 4 pin jumper connector
    - VCC
    - GND
    - Video
    - Audio
2. Desolder Power Switch
3. Solder 2 x 4.7uF capacitors to reduce jailbar effect(I don't know how it works)
4. Solder Power LED with 330R register

### Build daughter board

1. 4 pin jumper connector(male; connect with Step. 2)
    - VCC - Power Switch
    - GND - GND
    - Video - 0.47uF capacitor - Collector of C1318
    - Audio - Audio Left & Right(TODO: Streo?)
2. USB-C PD decoy board
    - Make sure 5V output!
    - VCC - Power Switch
    - GND
3. C1318 Transistor
    - Base - VCC
    - Collector - 0.47uF capacitor <- FC Video
    - Base - 22K resistor - Collector
    - Emitter - Composite Video
    - Emitter - 22K resistor - GND
4. 3.5mm 4 pole connector
    - Audio Left
    - Audio Right
    - GND
    - Composite Video

### References

- [Nintendo FAMICOM Mod (USB Power, Composite Video, Stereo Sound)](FamicomMod.pdf) (web link is dead)
- https://miko.mobi/famav.htm
- https://8bitplus.co.uk/your-consoles/famicom-av-mod/
- https://8bitplus.co.uk/projects/famicom-av-mod-nintendo/

---
May the **SOURCE** be with you...

