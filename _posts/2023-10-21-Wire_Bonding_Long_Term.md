---
title: Wire Bonding Long Term 2S and PSs Sensors
tags: Test Irradiation Wire Bonding Long Term 2S PSS Sensors 
---

# Wire Bonding: Long Term 2S and PSs Sensors

* For long term testing of the 2-S and PSs sensors, we wire bond the 2S and PSs sensors to a green base plate. Two bonds are made on each sensor, one connecting the bias ring to the PCP board (copper surrounding sensor), and the other connecting the bonding surface between fiducial 5 & 6 to the PCP board. 
    * This holds the sensor in place. They are then placed into a box so as not to expose the sensor to outside air when transported between labs. The zero volt ionizer fan can be used to help remove any charge from the sensors before adding the bonds
* For long term testing, we use the second bonding machine. This machine is older and has to always be kept on.
* First, turn on the monitor connected to the bonding machine. 
    * Turn on the light switch (top left, right of microscope )
    * Turn on the camera: yellow button on the camera control unit (machine left of microscope)
    * turn on microscope =press the emergency stop button
    * Turn on stages vacuum:  power switch in front of the monitor stand
* The dials in front of the base of the bonding machine move the stage around 
* The height of the stage can be adjusted by turning it. Tightening the screw on the stage base locks it into place, loosening it allows you to adjust the stage height. Turn CW (right) to loosen, turn CCW (left) to tighten. 
* The log book for the wire bonder has a list of settings needed in order to bond
    * This list provides settings for both the first and second bond
    * For the power, there are 2 buttons under the camera control unit (leftmost button)
    * You can change the settings to only the 1st wire, only the 2nd, or both wires. 

| Settings               	| Value 	|
|----------------------------	|-----	|
| Power (1st)                	| 2.5 	|
| Power (2nd)                	| 2.7 	|
| LH (1st) (loop height)     	| 250 	|
| RVH (1st) (reverse height) 	| 275 	|
| RVL (1st)                  	| 50  	|
| Bond Time (1st)            	| 65  	|
| Bond Time (2nd)            	| 75  	|
| TIP (both)                 	| 75  	|
| CVL (both)                 	| 20  	|
| RHT (1st)                  	| 55  	|
| Z UP (2nd)                 	| 25  	|
| Feed (2nd)                 	| 34  	|
| Tear (2nd)                 	| 30  	|


* `NOTE: Sometimes you may need to change the height of the bond because the height between the sensor and the board varies from sensor to sensor. You can change the reverse height (RVH) to 350 if you need more height in order to form the bond`{:.info}
    * Hit RVH button, hit the change button, type in new number (i.e. 350), hit accept button, chose the one wire button
        * it will only make this change in height for that bond only, not any of the following bonds. If you want this change to be carried across every bond, hit the all devices button = a permanent change
    * The dial under/next to the light switches can change the intensity of the light
* Make sure the system is in manual mode & that wired is threaded to the wedge
    * The other bonder is more automated: it follows a program script to bond
* NEXT, lower the stage as far down as possible 
* Place the sensor (w/ the green base) on the stage & turn on the vacuum
    * For the 2S sensor: Rest the nut sticking out of the bottom of the top right corner of the sensor against the stage
    * For the PSs sensor: when the pusher and the nut are touching = correct spot on the stage
* Raise the stage up until the camera comes into focus on the monitor screen. 
    * You can also use the # buttons on the right side of the microscope to manually adjust the focus, usually set to 5, increased up to 7 if needed
* For the first bond (bias ring): 
    * The calibration of the bonder is slightly off, so aim slightly to the left of where you want it to bond, do not bond to a previous location (marks present). 
    * Each bond is made up of 2 bonding points. The first bonding point is on the bias ring of the sensor (top right corner), the second is on the PCP board (i.e. the copper surrounding the sensor on the green base)
        * For the second point, you may need to increase the focus to 7, since the PCP board is lower down and therefore farther away from the camera. 
* Once you get to a position you are happy with, hit enter, get second point, hit enter again
* If you accidentally choose the wrong spot for your bond point, you can hit the “IPA” button to redo the spot. 
* Make the bond in Debug mode = only performs one step at a time, waits for your approval to move onto the next step
    * To move onto the next step, hit the error button
* For the second Bond (fiducial): 
    * The first point is between fiducials 5 & 6 on the right side of the sensor (fiducials are square alignment markings on the edge of the sensor). The rectangle sitting between these two fiducials is the bonding surface. 
    * The second point is on the PCP board to the right of the sensor. 
* NOTE: If your bond breaks/doesn/t stick, you can bond off to the other side of the copper strip.
* Once you have completed bonding:
    * Loosen the stage’s screw, lower the stage as far down as you can (clockwise), turn off the vacuum, wait a few seconds, remove the sensor board. 
    * Give the now-bonded sensor board to Andre to put back into the box for safety. 
* Repeat this process until all sensors are bonded
* DO NOT TURN OFF THE WIRE BONDER AFTERWARDS
    * Only turn off the lights, the monitor, the vacuum, and the camera, put into emergency stop position

## Halfmoon to Alibava Board Bonding

* Use the newer bonder to complete the 4 bias ring to pcp board bonds 
    * Select the file “andrew_halfmoons” 
        * Loop, loop -> change the second loop height from 1000 to 3000 for these longer bonds
            * This gives them the length/height they need to bond without the bond breaking
* Use the older bonder to do the HM to alibava board bonds
    * Set the loop height (bond 1) to 350
    * Set the RVH (bond 1) to 375
    * Set the power for bond 2 to 2.8
    * Focus the camera on the HM at 9
        * the focus on the alibava board bond pads will be 4 as a result 
* Start bonding at the right end of each chip and go straight across to the other end 
    * The existing bonds on the alibava board created noise in the center of both alibava board bond pads that we were not able to get rid of. Therefore, we bond from the edge of the HM to the edge of the alibava board (pads 1-60 on each bond pad) 

## Bonding HV tail to Sensor 

* Set loop height = 150 
* Set RVH = 150 
* Set bond strength B1 = 2.6 
* Set bond strength B2 = 2.8 
* Encapsulant PartA:PartB 10:1
* Make at least 10 bonds 