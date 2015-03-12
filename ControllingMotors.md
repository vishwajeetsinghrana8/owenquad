# Introduction #

**Basics**: ESCs expect a pulse between 1ms to 2ms, with 1ms being off, and 2ms being fully on.  The pulse should be sent at greater than 50Hz.

**Calibration**: ESC do need calibrating (to learn on/off pulse widths), to do this, turn on ESC, send 2ms pulse, wait 3 seconds, send 1ms pulse, wait three seconds.  Calibration done.

**The averaging problem**: Most ESCs do averaging, measuring 5-8 pulses and taking the average.  This is undesirable in quadcopters needing instantaneous response.  To reduce the problem, it's common to send at 400Hz (making 5-8 pulses appear faster) - or to flash the ESCs with something like BLHeli Multi firmware.