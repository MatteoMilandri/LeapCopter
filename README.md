LeapCopter
==========

Control your quadcopter with LeapMotion controller and the a7105 chip.

You must have Processing and Arduino environment installed.

Pull the a7105 file on the arduino ( i'm using an arduino DUE for the 3.3V output on pins). 

Wiring are in the main.ino file.

After a7105 is pulled on the arduino, just open the LeapCopter.pde file, click on the "run" button, THEN power on your quad.

Controls : 0 to switch control on/off, 1 to switch between Leap mode and keyboard mode, 2 to switch stabilisation on/off, 3 to switch rudder control on/off, 4 to lock or unlock throttle.

Keyboard mode : A = throttle up, Z = throttle down. Right, left, up and down keys to control aileron and elevator.

Leap mode : incline your hand left/right/backwards/forwards to make the quad move left/right/backwards/forward. Turn your hand left/right to make the quad yaw left/right. Close your hand for self landing. Flips not included yet.

Gestures : KeyTapGesture (just lower your finger as if you were tapping on the keyboard and put it back to starting position) allows you to switch rudder control on/off (just like "3").
Circle gesture is included in the code but doesn't do anything as of yet.

Credits goes to PhracturedBlue, Shinyshez and andy_m for the arduino part.

=========================== How to make it work for any 5v Arduino board! ============================
I managed to get it working of 5v arduino boards, with the contribution of Matias Szarfer, using a simple resistor divider system.
Here are the wirings :

10K-11K resistor between SCK of board and sck of A7105. 
A7105's SCK to 20K-22k resistor, other end of this resistor to GND.
Same between MOSI and sdio of A7015, and between MISO and  gio1 of A7105, and between pin 10 of board and scs of A7105. 
Don't forget to put the 20K-22K resistor between sdio and GND, gio1 and GND, pin 10 and GND. 
If it's not clear for you, don't risk to burn your board and e-mail me.

You can contact me at isigo@weloveminitel.eu for any type of question, I will be glad to answer.


Enjoy !!!
=========

