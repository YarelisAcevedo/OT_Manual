---
title: Wire Bonding (half moon sensors for alibava test)
tags: HM Test Irradiation Analysis Alibava Wire Bonding
---

# Wire Bonding (half moon sensors for alibava test)

* Start by turning on the computer as well as the mechanical bonder 
    * Computer = red button on the right side 
    * Make sure you chose the autobonding option 
    * The computer should show the microscopic view, the tablet acts as a sort of control pad, giving you options to change how the needle bonds the wire to the sensor
        * The tablet lets you set the specific force and the amount of time you want the needle to bond for,  as well as how much wire to use
            * On the touchpad: file, loop, 2 axes x and y (the needle also moves in the z direction)
            * The bonding force is set to 50, and the bonding time is set to 150. 
* Before starting, make sure that the needle is actually bonding the wire
    * There is an extremely thin wire going through the head of the needle
    * Before starting work on a real sensor, there is a test sheet of aluminum with small gold squares on it (gold acts as a good bonding surface, it does not oxidize)
        * Place the practice piece onto the vacuum platform surface
            * The vacuum pump sucks air in through the tiny holes on the surface of the platform and holds the practice piece down
            * Make sure you turn on the vacuum
    * There is a joystick  and 2 buttons on the setup itself (blue bottom section)
        * The rightmost joystick controls movement, moving the needle head in the x and y direction 
        * The leftmost button lets you switch between your starting bonding location and your second bonding location, both of which you set using the joystick
        * The rightmost button tells the bonder to bond
    * We control where the bonder will make the bond, which is why we need the microscopic view on the computer as well as the microscope itself to be able to put the needle in the correct location
    * After hitting the bond button, watch the bonding process through the microscope
        * The bonder automatically goes from the first location to the second
        * The microscope view allows you to diagnose any problems that may occur during the bonding process
            * I.e. the bond failing, the wire breaking, the bond being too angled (can be fixed with tweezers)
        * Everytime you bond, once the bond is complete the needle automatically shifts over to your next bonding location (you can set this on the touchpad)
* `IMPORTANT: When placing the sensor on the platform, make sure the area that we are going to be bonding (the 2 chips (halfmoons taped on) and the fanout board (light yellow)) are not touching the vacuum holes in the platform`{:.warning}
    * Rest the green portion of the sensor on the platform, with the yellow portion going out towards you. 
* The sensor is composed of 2 chips (chip 0 (left) and chip 1 (right)) 
    * These chips are being bonded to the yellow fanout board directly above them
        * Each chip has 60 strips 
        * The fanout board has 2 sets of 128 strips ( center at strip 64)
        * The spacing between each strip on the fanout board is narrower than that between the strips on the chips
            * Also. the spacing between strips does not equal the strip width
            * Over time as you bond, the wire will become slightly angled to the left or right 
            * The 2s sensor has a spacing of 90 microns, the Pss sensor has a spacing of 100 microns 
    * When bonding we start in the center of the chip (strip 30) and bond directly to the center of the fanout board (~64)
        * From this, we first bond all the strips to the right and then all the strips to the left
            * Make sure to keep your bonding locations in as straight a line as you can
            * There will be empty strips leftover on the fanout board, but that is to be expected
            * NOTE: As you bond, you will need to shift the base of the platform in order to compensate for the angle produced by the unequal interstrip distances between the chip and the fanout board. Once the default second location is greater than 3 strips off from where it should be, slowly rotate the platform until the x axis values are closer for location 1 and 2 
                * Bad = off by more than 500 microns. We want to be off by under ~50 microns 
    * `IMPORTANT: For chip 0, center the needle in the middle of each strip. For chip 1, skew the needle off center to the right of each strip. By doing this, the needle will hit the center of the strip. Chip 1 is more rounded/arched than chip one (flat), and skewing the bonding location helps compensate for this.`{:.warning}
        * Because of this, it is easier to start with chip 1 because you will more likely run into bonding errors. 
        * Make sure you bond to the strip surface, not to the black space between strips

## Possible Mistakes & how to fix them
* If a bond fails, when fixing it make sure you start that bond below the failed bond location
    * Though necessary, this is not ideal because as a result the wire bond will be longer and could start to sag down. When/if this happens, you can use the tiny hand-held needle to lift the wire back up
    * The tiny needle can also be used to separate wire bonds, which may be necessary when the bonds become too angled, resulting from either not bonding in the center of the strip, or from the offset between the chip and the fanout board.
* It is important to try to get your bonding locations as centered as possible because if they are off centered, the wire will either skew to the left or right, meaning it could touch a previous wire or be in the way of the next bond you need to make. This can be adjusted by lightly pushing the wire back into the center with the hand needle.
* If the wire breaks after attaching the second bond, there will be a tail attached to the second bond as well as excess wire on the needle itself. 
    * First, make sure you check the wire is still threaded into the needle: on the touch screen hit the feed wire button, then zoom out on the microscope itself and see if you can see the wire coming out of the needle tip
    * This extra needle wire can be removed by creating a bond on the practice piece.You can remove the tail on the sensor bond with the hand needle.
* When replacing needle wire (i.e. a break):
    * Hit the joystick button on the touch screen (crosses it out, making it so the joystick wont move the needle if touched)
    * There is a clamp that holds the wire in place before it is fed into the needle. Hit the clamp button inorder to open the clamp – NOTE: the clamp only stays open for 30 seconds. Pull the wire out from the clamp using tweezers 
    * Feed the wire back into the head of the needle with the tweezers (need light to see it)
    * Cut off the damaged portion of the wire with scissors and place the excess into a cup (=trash) 
    * Next, reopen the clamp with the clamp button and place the wire back inside
    * Remove the excess wire sticking out of the needle with the practice piece and practice a few times to ensure that the needle is bonding properly. 
* To stop what you are doing, hit the abort button. 
* Once you have finished bonding the chips to the fanout board there are only 4 more bonds that need to be completed before irradiation in the lab
    * When making these bonds you are going to have to rotate the sensor so that it is lying horizontally. There are 2 bonds on each side, one to the circuit board, one to the bias ring. 
    * The z and y data needs to be changed in the tablet for these bonds in order to create a bigger loop
    * There are two bonds with the circuit board (one on either side of the sensor) where the circuit board is bonded to a strip of copper on the outside of the sensor
        * Make at least 3 bonds for each one as a failsafe 
        * NOTE: on the circuit board, the red wire is the bias (active) wire and the black wire is the ground. 
        * Make sure you scratch off any oxidation on the copper with the hand needle before bonding
    * The last 2 bond spots are connecting the bias ring towards the corners to a different set of copper strips on the outside of the sensor.
* Placing in Alibava setup: (TBA)
    * Using the soldering iron (light blue) connect the ground wire (black) and the bias wire (red) (one of each on each chip)
    * Line up the black line on the aluminum base of the sensor to the brown base of the machine
    * Attach the ground for the machine to the sensor (yellow tipped thick grey wire)
    * Attach the green C0 wire (chip zero)
    * Attach the green C1 wire (chip 1)
    * Control for humidity etc. gets attached at the end of the green part of the sensor
    * The very thick grey wire that supplies power to the sensor gets plugged in at the end of the green section, to the left of the humidity control
    * ADD THE RADIATION SOURCE

### Replacing the Needle, AKA “Wedge”, of the wire bonding machine
* We want the flat side of the needle to face us, the user, and we want the top of the needle to be flush with the arm holding it in place
* The only thing holding the needle/wedge onto the arm is a bronze screw, needs a specific screwdriver (35 newton cms)
* For the Alibava wire bonding machine, we use SPT needles, the long term bonding machine uses Gyser
* First, pull the wire out of the wedge through the hole at the top of the wedge
* Remove the old/damaged wedge with an M2 allen wrench
* Open a new wedge, making sure to not touch it with your hands (wear gloves)
* Place the new wedge, making sure the flat side is facing you
    * Use a torque wrench to screw into place and readjust as needed
    * We want the correct height and the correct facing angle
* Rethread the wire.
    * Release the clamp, thread the wire through the head/top of the needle, and then thread it through the tip of the needle. Then place the needle back into the clamp.
* Test the new needle to make sure it is bonding properly and that it does not need anymore adjustments