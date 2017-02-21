Servo tester PCB firmware
=========================

This is the firmware for my servo tester PCB [&rarr;more info][1].

The firmware for the ATtiny2313 is written in C. Just execute ```make``` and have it flashed on your &micro;C.

For unknown reasons, I am not using the Makefile in the firmware/ folder to set the AVR's fuse bits. Here they are, in the format as arguments for avrdude:
```
-U lfuse:w:0xe4:m -U hfuse:w:0xdf:m -U efuse:w:0xff:m
```

User interface
--------------
The current way how this works is: With the potentiometer you can select the duty cycle between 0 and 100%.
The red button has no function.

A future UI concept is sketched in [future_ui_concept.jpg](future_ui_concept.jpg).

[1]: http://www.tb-kaiser.de/pcbs/servo_tester_2016_10_10/