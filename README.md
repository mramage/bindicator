# Bindicator

The Bindicator is a small light-up wheelie bin to remind me which bin needs to be taken out each week. The idea has been around for a while, with a number of implementations.  This is my version.  It is built on ESPhome, with the scheduling/control of the light done through Home Assistant.

# Dimensions
85mm tall, 44mm wide, 51mm deep


# Parts used

- 3d printed parts:
  - Bin body
  - Bin lid
  - Base
  - 2x wheels
  - a small length of filament to use as the axle (also locks the parts together) and for the lid hinge
- Seeed Studio XIAO ESP32C6 (or equivalent)
- USB-C cable that has a thin cable (needs to fit through the small hole in the rear)
- WS8212 5V addressable LED strip. I used a 4-led segment measuring 66mm long
- a few short lengths of small wire
- soldering iron
- solder
- adhesive of some kind. Hot glue, super glue, thick double sided tape, bubblegum you found last week on your shoe, whatever...

# Assembly

1. Print out the parts listed above.
2. Cut the LED strip to length, and solder a short piece of wire (roughly 8cm) to the 5V, 0V, and signal input pins of the LED strip.
3. Attach the USB cable to the esp32 board, and test fit the placement of the board on the rear of the vertical LED post of the printed base. Check the cable fits out the rear cable entry between the base and bin body. Mark this location on the post.
4. Test the placement of the LED strip on the vertical face of the base piece, with the wires attached at the bottom end of the strip.
5. Route the wires around to behind the printed based, and find what length they need to be to attach to the appropriate pins on the ESP32 board you are using.  For the Seeed Studio XIAO ESP32C6, I used the following pins:
    - signal wire to GPIO20
    - 0V to any 0V pin
    - 5V to any 5V pin
6. Strip and solder the wires
7. Program the ESP32C6 with the bindicator firmware, and check it works before full assembly!
8. Stick the LED strip and the esp32 board to the post, and make the wiring neat and tidy.
9. Carefully slide the assembled base up inside the bin body.
10. Secure the body and base by inserting a short length of filament through the hole in the side of the bin, making sure to pass through the hole in the base.
11. glue a wheel onto each end of the filament.  Or just one side if the other wheel fits on tight enough to not fall off.
12. Use another length of filament to secure the bin lid onto the body. Heat up the end of the fillament enough to squish it a bit so it can't slide out. (FYI - don't glue it at both ends, otherwise the lid won't open)
13. Plug it in, and pair it up with your wifi and connect in to home assistant. If you are making this, I'm assuming you know what esphome is and homeassistant.


# License

## 3D model
It is heavily based on the 3d model here: https://www.printables.com/model/189899-wheelie-bin-for-the-bindicatorbindaycator

As a result, the 3d model is licensed as CC-NC-4.0 https://creativecommons.org/licenses/by-nc/4.0/

I have remodelled significant parts of the bin, but it was originally derived from that model, so I am keeping that license for all parts of the 3d model.

## Software
I am releasing the parts of the software that I have created under the MIT license: https://opensource.org/license/mit

Any software components that I have not created retain their original license as indicated in their respective source files/project repositories/websites.
