---
title: Dispensing Robot
tags: Dispensing Robot Epoxy 2S Sensors
---

# Dispensing Robot

* Used for gluing Kapton Isolators to 2S sensors. 
    * Every 2S module needs 6 isolators
        * A complete 2S module consists of 2 strip sensors. Each strip sensor gets 3 kapton isolators: 2 for the aluminum carbon fiber (ACF) bridges, 1 for the stump bridge 
* Also used to attach high voltage tails to 2S sensors (after gluing the high voltage tails are wire bonded and then coated with epoxy for protection)
    * Every 2S module has 3 high voltage tails
        * The bottom strip sensor has 2 high voltage tails, and the top strip sensor has one high voltage tail.
* PS modules sit on a carbon fiber base plate and only gets one kapton isolator
    * You need to make sure the epoxy (glue) is only on the side of the carbon fiber base plate, not the sensor side facing upward. 
    * PS modules consist of one pixel sensor and one strip sensor. The pixel sensor is higher resolution and therefore we want it to receive more radiation - used in high luminosity. 
* Another test the dispensing robot is used for is testing how long epoxy is good for (i.e. after its expiration date, or if its lid is let off overnight)
* The dispensing robot uses a program to dispense the glue, creating a line (vectors) for the glue to follow
    * There are existing programs with set line patterns created for most of the tests ran in this lab
* This is a 3 axis robot, meaning the needle used for dispensing moves in the x and z direction, and the tray in which sensors are placed moves in the y direction. 
* There are two major types of Epoxy:
    * For 2S module: 601LV epoxy 
        * **PART A** : PART B 100:35 in weight 
        * 2 hour working life time
        * Use the 25 gauge (red) needle tip to dispense = lower viscosity 
    * For PS module: TC437 epoxy
        * **PART A** : PART B 10:1 in weight
        * 20-40min working time 
        * Uses the 22 gauge (blue) needle tip to dispense: higher viscosity
* **SOPs**: in shared Brown HEP google drive, go to assembly, choose either PS or 2S assembly folder, choose either PS or 2S assembly procedure (PS is outdated, chose the new spacer + jigs file)

## Mixing Epoxy Steps
* wear safety goggles and gloves
* In the lab hood, zero out the mass balance
* Grab a plastic cup from the cabinet directly below the mass balance
    * Zero out the cup 
* NOTE: In order to use the epoxy, you need more than 5 grams
* FOR THE 601LV = In the chemical storage cabinet in the lab hood grab:
    * Polytec EP 601-LV Part A (large plastic bottle)
    * 601-lv Part B (small amber bottle)
* Pour Part A into the cup, stopping when the scale reads roughly 4.2 grams
* Use the calculator on your phone to figure out the total volume needed
    * Ex. part A grams x 1.35 = total volume
* Fill up to that total volume using the part B bottle (using pipet cap)
* Use a wood stick to mix the epoxy until it becomes transparent (~1min) and until bubbles go away (for TC437, mix until homogenous)
    * The Smartmix X2 can be used to remove air from the epoxy, but hand stirring is sufficient

Grab a syringe from the dispensing station and block the tip with your finger. Pour the epoxy into the syringe. 
    * Put the stopper into the bottom of the syringe, invert the syringe using a kimwipe to  block the tip, and slowly push it forward until it meets the epoxy. Dispense a tiny amount of epoxy from the tip and wipe it away with a kimwipe. Wipe the inside of the syringe (towards the bottom) clean with a kimwipe. 
    * Place a needle tip onto the syringe (25 gauge)
* Connect the bottom end of the syringe to the Ultimus with the yellow connector (attached to a vacuum tube = vacuum seals the syringe). Turn the yellow connector to lock it. 
* Place the syringe into the black holder on the dispensing machine. Lock the syringe in by tightening the screw near the needle
* Turn on the and the vacuum (sitting under the table, connect the vacuum tube to the square jig)
    * We want the Ultimus to read 10.0 psi and 3.0 inH2O = this controls the pressure differences in the syringe that go in opposite directions
* Clean the jig (metal tray) as well as the glass sheet with a kim wipe soaked in isopropyl alcohol
* Place the glass onto the jig, covering the extra vacuum holes with yellow strips
* In the program, hit the home button to send the needle to the home position

## Program
* The x & z buttons move the needle and the y buttons move the jig. The negative direction is the needle going up, positive going down

## Calibration
* Adjust the Z Height
    * We don’t want to scratch the glass (or a sensor) so place a blue strip acting as a shim under the needle on top of the glass. Lower the needle slowly (speed controls in program) until it touches the shim (can no longer pull the shim out)
        * The shim is roughly 100 microns thick, and we want the needle to be 150 microns above the surface. Press the relative button (saves this 100 micron height; i.e. relative to wear the needle was) and then increase the z height slowly until it reads roughly -0.050 (50 microns). Remove the shim.
* Note the total z height (usually around 42) and change the z values in the line code to that number. This can be done by clicking the change z height button to the left of the code.
* Adjust the X & Y coordinates of each point in the pattern manually 

* The graph shows the design pattern that the needle will dispense. The code describes the vectors in this pattern. You can double click points on the lines to get the needle into that position on the glass. Make sure the glass in in the correct spot so that the machine does not dispense onto the jig
    * The line speed (speed at which the needle dispenses) can be set in the program
* Before dispensing, check the pressure to make sure it reads 10 psi and 3 inH2O (manually adjust with knobs on nordon if needed)
* Bring the needle to the home position by clicking the home button, Then hit the dispenser purge button on the front bottom of the machine & wipe the excess glue of the needle with a kimwipe
* On the computer, hit the Run button & let the epoxy dispense. 
* The glue can be cleaned off the glass with isopropyl alcohol.
* For the PS Module: Carbon Fiber Sheet & Kapton isolator:
    * A Kapton isolator (yellow sheet) is glued onto a carbon fiber sheet 
    * Using a second square jig for the kapton isolator, attach the vacuum tube to the jig. Place the 3 screws into the jig and use them to center the yellow strip into proper formation. Place the isolator on the jig, get into formation and turn on the vacuum. 
    * Program for design pattern: incolla_Kapton_BPO_red_SRC
    * Align the Z height as described previously (sitting 150 microns above the carbon fiber sheet)
    * We want the 2 dots on the centerline of the pattern to be symmetric with the screws on the jig for the carbon fiber sheet (the dots lining up with the inner edge of the screws). Make sure the center of the pattern lines up with the center of the sheet. When adjusting the dot locations manually, the whole difference in the location (x,y) needs to be noted in the code for every point, since changes could shift the whole pattern back and forth.
        * The camera can be used to complete this process with higher accuracy but lining up points on the graph outside the pattern to points on the carbon fiber sheet 
    * Send the needle back to home position, hit the glue dispenser purge button, clean the needle, and then hit the run button (it will dispense the pattern twice to increase the amount of glue in each line
    * Once the glue is done dispensing, turn off the nordson vacuum and pick up the carbon fiber sheet. Flip the sheet over so that the glue side faces the ground. Carefully bring over to the kapton isolator jig and slowly lower the sheet onto the kapton isolator, using the metal nails on the jig as a guide in the holes of the sheet
    * Place the top weight on top of the jig, making sure it lines up properly. Add an extra 600 grams on top of the weight (3 200 gram gold weights)
    * After 20 minutes, Lift off the weight plate and use a squeegee to apply pressure on the back of the CFBP to help spread the glue = this helps result in close to 100 percent coverage. When finished, place the weights back on top of the CFBP. 
    * Turn off the vacuum for the jig (if left on, it will create a pattern on the isolator where the holes were)
        * Let the carbon fiber sheet/kapton isolator combo cure overnight (since this is practice, clean them both off with isopropyl alcohol)

## PS Module: Spacers
* For each PS module, 4 spacers are glued to the MAPsa, which is then connected to PS sensors (the second gluing step for the PS module is gluing the carbon fiber base plate to the kapton isolator)
    * For practice runs, use the thickest spacers (4.0mm)
    * The pattern for this run consists of 4 lines, one for each spacer, each line consisting of 3 vectors following the shape of the spacer. Then, each spacer has 2 dispenser dots, one on each tooth in the middle stretch of the spacer (8 dispenser dot locations in total). 
* The PS spacer gluing procedure can be found in the shared drive: assembly, PS assembly, PS spacer gluing SOP_new spacer + jigs
* The program for gluing the spacers to the maps can be found on the computer: new volume, save - ps module, sort by date, PS_spacers_new.SRC
    * File, open, ps, ps spacer new 
* First, clean the jig, base plate, and the spacers themselves with isopropyl. 
* Using the proper jig and base plate for the PS spacers, place 4 of the spacers onto the jig using the plastic tip tweezers to move them into position, covering the vacuum holes. Turn on the vacuum for the jig. 
* Before making the epoxy, first calibrate the z height and the x/y coordinantes.
    * Z height: use the blue shim paper as described previously, increase the z height by 50 microns above the blue shim ( add -0.050)
    * Calibrate each point on the lines, as well as the dots (for the teeth in the middle of the spacers) in the x and y direction, adding or subtracting from the values in the program to get to the correct coordinates
* Set Ultimus Machine to an outward pressure of about 14-15 PSI, 3.0-3.5 inH20 such that no glue is dripping from the syringe tip.
* Onces all points are calibrated, you can start making the epoxy
    * In the hood, turn on the light, retrieve a small plastic cup, a stick for stirring, and kimwipes. First turn on the scale and zero out the mass of the cup
    * Next, get a syringe, a blue 22 gauge syringe tip, and a white stopper from the dispensing table. 
    * Wear Goggles and Gloves when working with the epoxy
    * Take out the TC437 part A and part B epoxies. 
    * Open the Part A epoxy, wipe the sides of the container with a kimwipe to remove excess epoxy, and pour ~5 grams of part A into the cup, using the stick as a spoon. Weigh on the scale
    * The ratio for TC437 is 10:1 PartA:PartB. Using the dripper, drop ~10% of part A’s mass of Part B into the cup. 
    * Mix the epoxy until homogenous, it will have a green/yellow tint. Tap out the bubbles to the best of your ability
    * Pour the epoxy into the syringe, and push out any air bubbles. 
* Connect the syringe to the Ultimus vacuum and secure it to the dispensing machine. 
* Before dispensing, check the z height again, and make sure you discharge some epoxy from the tip of the needle. 

* When done gluing, clean off the jig with isopropyl
* Dispose of epoxy syringe in the large red needle disposal bin on the floor between the hood & the glue station
* Put away epoxy A and B bottles in the chemical storage cabinet 
* Let the cup and stick used for stirring the epoxy harden overnight in the red bin inside the hood. Once hard, place into the black bucket inside that same bin.