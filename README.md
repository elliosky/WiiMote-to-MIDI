This script, originally found via the Wayback Machine on a 2015 tutorial blog, was modified to fire two WiiMote controls (A and B buttons) over multiple MIDI CCs.

REQUIREMENTS:
WiiMote (preferably with WiiMotion Plus); a Bluetooth connection; GlovePIE or equivalent software; LoopBe or equivalent software.

BEFORE CONNECTING:
Make sure you've correctly paired the WiiMote to your PC at least once using the legacy hardware procedure in Device Manager;
make sure LoopBe is running (I highly recommend setting it as a startup app).

HOW TO CONNECT:
Open GlovePIE and load the script; select the GUI window within the program; enable Bluetooth scanning;
hold down buttons 1 and 2 on the WiiMote at the same time and make sure the LEDs are flashing;
the GUI page helps the operating system find the WiiMote via Bluetooth; once connected, run the script.

HOW IT WORKS:
1. If you press B on the Wii Remote and tilt it up or down (even pitch), it will take control of MIDI Ctrl-14, Ctrl-3, Ctrl-22, Ctrl-Pitchwheel on MIDI channel 5.
2. If you press A on the Wii Remote and rotate it left or right (rolling), it will take control of MIDI Ctrl-15 on MIDI channel 5.
You can potentially control many other individual parameters using all the Wiimote1 parameters, the WiiMotionPlus parameters, or the Nunchuk parameters; just explore GlovePIE.

WARNING:
1. Make sure the device's MIDI output is not occupied by other devices.
2. For each CC you write, GlovePIE creates a "noise dump" of the CC, so make sure it dumps it to a disabled CC: the dump is automatic, cannot be controlled, and usually occurs on unmapped CCs above 30.
3. If you don't have a WiiMotion Plus, the "wiimote1." parameters are slightly different than what I wrote and you must rewrite them accordingly.
4. The pitchbend range is limited, if you want a full scale just change the variables to +-90° and "0.3, 0.7" to "0, 1"
