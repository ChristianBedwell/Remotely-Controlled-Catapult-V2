Remotely-Controlled Catapult V2
===========================================================================================
The objective of this project is to apply the fundamentals of embedded systems design to develop a remotely-controlled catapult, launching and reloading small-scale projectiles via web interface. The catapult project will fulfill a need to effectively reduce user intervention, with no need to reload, manually retract, or lock the catapult arm into place, but will only be required to fill the catapult with ammunition when it is empty. This is made possible by applying the latest technologies in software development, while emphasizing on an Internet-connected device. 

Materials Checklist
------------------------------------------------------------------------
* [x] Arduino UNO REV3 (x1)
* [x] Arduino Ethernet Shield 2 (x1)
* [x] FS90MG Micro Metal Gear Servos (x3)
* [x] Half-Sized Breadboard (x1)
* [x] 9V Battery Pack (x1)
* [x] External 5V Battery Pack (x1)
* [x] Orange Male/Male Jumper Wires (x3)
* [x] Red Male/Male Jumper Wires (x3)
* [x] Brown Male/Male Jumper Wires (x3)
* [x] Black Male/Male Jumper Wires (x1)
* [x] Red Male/Female Jumper Wires (x1)
* [x] Black Male/Female Jumper Wires (x1)

Device Construction
------------------------------------------------------------------------
The Arduino Ethernet Shield 2 is compatible with any Arduino board, so the Ethernet Shield male header pins should fit perfectly with the female header pins of the Arduino UNO REV3, just make sure that the male header pins aren’t bent when exerting force down on the Ethernet Shield to attach it to the Arduino board. 

Once the Arduino UNO REV3 and Ethernet Shield 2 have been merged, insert one of the orange male-to-male jumper wires into the digital output header pin 6 (DIO-6) on the Arduino Ethernet Shield, another one in DIO-3, and the last one in DIO-2. Now, take the free end of the orange male-to-male jumper wire assigned to DIO-6 and attach it to the orange Signal (S) pin on the reload servo. Repeat the same step for the other two orange male-to-male jumper wires, aligning DIO-3 with the S pin on the tension servo, and DIO-2 with the S pin on the lock servo. To complete the connections to the Arduino Ethernet Shield, take the black male-to-male jumper wire and connect it to one of the two GND female header pins on the Arduino Ethernet Shield. Your jumper wire configuration on the Ethernet Shield should resemble that shown below.

![Ethernet Shield Wiring](images/wiring-schematics.jpg?raw=true "Ethernet Shield Wiring Configuration")

The next step is to make use of the breadboard, in preparation of adding an external power supply. Take the free end of the black male-to-male jumper wire and connect it to the rail on the breadboard labeled with a ‘-’ icon. This is good practice to connect the ground of the Arduino to the breadboard, even if it does not rely off of the same power supply as the micro-servos. Now, take one of the red male-to-male jumper wires and insert it into one of the holes that align with the rail on the breadboard labeled with a ‘+’ icon. Repeat the same with the other two red male-to-male jumper wires, making sure that there is adequate spacing in between them for wire management purposes. 

Attach the free end of each red male-to-male wire to a red Voltage (V) pin on each servo. Similarly, take one of the brown male-to-male jumper wires and insert it into one of the holes that align with the rail on the breadboard, this time labeled with a ‘-’ icon. Repeat the same with the other two brown male-to-male jumper wires, making sure that there is adequate spacing in between them for wire management purposes. Attach the free end of each brown male-to-male wire to a brown Ground (G) pin on each servo. Note that it is important to make sure that the orange wire on each servo corresponds to the Signal (S) pin, the red wire to the Voltage (V) pin, and the brown wire to the Ground (G) pin; otherwise, the current will likely burn out the servos. 

Since all of the servos are now integrated with the breadboard, it is now time to add the 5V external power supply. When attaching the 5V external power supply to the breadboard, the power supply will feature two wires: a red wire for power and a black wire for ground. Unfortunately, both wires lack header pins to mount directly to the breadboard, so this is where two of the remaining red and black male-to-female jumper wires (one of each) will come into play. Cut each of the male-to-female jumper wires in half, making sure to use the halves with the male header pins; the other halves of the wires may be disposed of. Strip the insulation off the end of the wire halves. Using a twist-on wire connector, bind the exposed end of the red wire halve to the exposed end of the red wire on the power supply. Repeat this step with another twist-on-wire connector, this time for the set of black wires. 

Now, simply attach the male end of the red wire to the beginning of the breadboard rail labeled with the ‘+’ icon. Lastly, to finish off with the connections to the breadboard, attach the male end of the black wire to the beginning of the breadboard rail labeled with the ‘-’ icon. The configuration of the breadboard should look identical to the image provided below.

![Breadboard Wiring](images/breadboard.jpg?raw=true "Breadboard Wiring Configuration")
