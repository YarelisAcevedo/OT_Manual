---
title: Smartscope Visualization inspection
tags: Smartscope Visualization inspection 2S PSS 
---

# Smartscope: Visualization inspection

* When we receive sensors, we need to take pictures of them for quality control = visual inspection for scratches/ any damage done to the sensor before being used in the lab
* When handing the sensors, wear gloves, ESD bracelet and blue ESD grounding booties. 

## Procedure

Turn on the controller for the smartscope microscope (press on switch)
* Run the Initialize software on the desktop
* Hit the start/stop button on the controller, engage - yes, stylus - none
* Run the Measuremind 3D multisensor software (click app above the initialize app)
    * Press start/stop, press no for probe stylus being installed 
* NOTE: The joystick on the controller moves the microscope head & turning it rotates it 
    * The controller can also change the z height of the microscope
    * The big red button on the Smartscope and on the controller is for an emergency stop
* NOTE : Sensors are shipped in batches & each sensor comes in a envelope with the following serial number:
    * Ex. `39595_002_2-S_MAINO` = batch #_sensor #_module type(2-S or Pss)_MAINO (for 2S) or MAINL (Pss left) MAINR (Pss right)
    * We never receive the full 50 sensors that are supposed to come in each batch, we only receive the sensors that are up to the lab’s standards. We usually receive a few batches of sensors each month. 
    * Sensor are stored by batch in the dry boxes in the lab
        * Sensors are sensitive to humidity and temperature 
    * Each sensor has a 4 number scratch # engraved on its outer edge written in binary (long rectangles = scratch pads; hold the binary code on the sensor)
* `IMPORTANT : When handling the sensors wear gloves, wear the ESD bracelet, and stand on the black mat in front of the Smartscope`{:.info}
    * `ESD = electrostatic discharge = a shock, static, etc.`{:.info}
    * Sensors are susceptible to ESD, the wrist strap grounds you so you can’t build up charge and shock the sensor. 
    * The ESD bracelet needs to make skin contact to work
* Before using the **vacuum pen**, clean the suction tip with isopropyl alcohol n a kimwipe = prevents the vacuum from leaving marks on the sensors. Make sure you also clean the smartscope tray/jig as well
* When removing each sensor from its envelope, visually inspect the front and back side for macroscopic damage
    * If you notice deep scratches or weird markings (circle shapes) then in shared drive navigate to pre-production, visual inspection, 2s, & create folder for that sensor. In that folder create a text doc describing the unusual marking (general size, shape, etc). Take a pic with your phone phone
* Use the vacuum pen to place each sensor in numerical order onto the smartscope tray/jig. Make sure that the dark rectangles on the outer edges of one side of the sensor are on the left side when placing them in. You can adjust the sensors placement on the tray with the plastic tipped tweezers.
    * Usually we run 8 sensors at a time for the visual inspection
* GO TO: 
    `File - Open - CDrive Part rtn - 2S_VI_Tray_1sensor_currentRTN (program)`
    * For PSS: 
    `File - Open- CDrive Part rtn - PSS Edge Define 2 03132019.RTN`
* In the Toolbox - hit run routine button (top right) - hit ok - starts the visual inspection process
    * The smartscope first looks for the little Ls in the corners of the sensor to locate itself. Then it takes 20 minutes to photograph each sensor.
    * Photos are stored in the CDrive Part rtn folder (saves each photo as: ex. 2S_pos1_PNG, etc)
    * NOTE: The tiny squares with 4 dots on each sensor are called fiducials = alignment marks
* Once the smart scope finishes taking pictures, you can place the sensors back into their appropriate envelopes using the vacuum pen. Slide the sensors gently off the tray until the air pressure is released from under the sensor. 
* Copy the photos from the CDrive into the lab’s shared drive 
    * photos will all get stored on computer in Win 10×64 drive initially
    * `HEPshared Drive - pre-production - visual inspection - 2S or Pss - choose batch # - create new folder for new batch - create new folder` for each sensor in this batch (label the folder with that sensor’s serial number)
        * Within each sensor folder, create another folder named after the date in which they were visually inspected (sometimes, if damaged later on, the sensor will be photographed again)