# WS218xHat
Hat for controlling WS218x leds using a RPi for a cleaner setup. This, altough is not technically a har since it does not follow [raspberry hats guidelines](https://github.com/raspberrypi/hats "Rasbperry Hat guidelines"), but for all practicall purposes it is


This hat was made with the intention of make a Hyperion setup cleaner and easier by making all the wire splicing and connections directly on the board, reducing clutter behind your tv or near the LED strip connections.

##Features



- **Easy connection to the power supply:** This board includes a barrel jack that make an easy connection to an external power supply.
- **Voltage translator:** This board incorporates a voltaje translator from 3.3V to 5V on GPIO18 to aid with certain led strips that do not work well with 3.3V signaling, this can be bypass by soldering the JP2 jumper behind the board and not placing, but I strongly recommend to solder these components for better compatibility
- **Direct power from the 40-pin connector:** This board has the capability of powering the RPi board directly from the 40-pin connector by soldering JP1, but its important to note that **you only should do this if your power supply is within USB specs** because this voltaje will also reflects on your USB devices. In my case my power supply provided 5.3V and was out of spec (5.25V is the max allowed by these specifications) so I had to power the Raspberry from the USB connector on the board.
- **Power from USB connector on the board:** This usb connector on the board takes the power from the barrel jack and enables to powering the RPi from a short usb cable. Powering from the usb cable has certain advantages like a fuse and voltage regulators that drop down the 5.3V from my power supply to 5.1V, making it safe for the usb devices connected to the Raspberry pi
- **Easy connection to LEDs strips**: Most led strips came with a wire that you can plug easily to a terminal block. I just had to extend this enough to put the electronics in the cabinet instead of the back of my TV and connect the 3 wires to the terminal block on the board
