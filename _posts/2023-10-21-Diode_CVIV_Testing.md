---
title: Probe Station (550 Lab) Diode CV/IV Testing 
tags: HM Test CVIV Irradiation Analysis Probe Station
---

# Probe Station (550 Lab): Diode CV/IV Testing 

<div class="card">
  <div class="card__content">
    <div class="card__header">
      <h4>Probe station 550 setup:</h4>
    </div>
    <ul>
        <li>Temp control</li>
        <li>Measuring currents pin diode</li>
        <li>Measuring and sending the voltage to the chuck/diode</li>
        <li>IV: Setting the voltage and measuring currents</li>
        <li>CV: Measuring capacitance </li>
    </ul>
  </div>
</div>

There are 3 types of diodes:

P-type : HGcal diodes, Half Moon diodes; a negative voltage is applied
{:.info}

N-type : DO diodes (on baggies says CO); a positive voltage is applied
{:.info}

Pin : Pin diodes
{:.info}

* `Fluence : amount/degree of radiation that structures have experienced: the damage done `{:.info}
    * This damage can be measured = IV/CV measurements of the test structures
* A voltage is set using a ground box, and is then transferred to the probe
    * This probe sets a voltage and then measures the current that results from that voltage 
        * The voltage is set on the big aluminum puck that the diodes are placed on. Anything that gets placed on this puck gets set to that same voltage 
        * Two needles are placed onto the diode:
            * One touching the active area of the diode
                * The active area is the working part of the sensor. We can see how much current is flowing through it and measure what the capacitance of the system is when the voltage is increased
            * One touching the guard ring of the diode
                * The guard ring keeps all the voltage going through the active area of the diode only, stops any from traveling through other inactive parts of the diode
    * `Capacitance : a measure of how much charge can accumulate in certain geometric structure`{:.info} 
        * Increasing the capacitance increased the amount of energy stored
        * A capacitor acts as a way to store energy instead of a circuit = like a battery 
    * **IV** = current voltage measurement (in Amps)
    * **CV** = capacitance voltage (in F (farads))

### First

Turn on the wall air & the power strip for the set-up
* Make sure wall air is at `~60`{:.warning}


### Second 

Turn on all of the temp control & current measuring machines, making sure the Julabo is set to the appropriate temperature needed for the test. 
* Unirradiated diodes get ran at room temperature 20°C
    * Set the temp on the Lulabo to `19.25`{:.warning} & the temp in labview to 20°C
* Irradiated diodes are run at 0°C (HGcal, D0) or -20°C (HM).
    * For 0°C, set Julabo to -0.5°C

### Third 

Open labview. Hit the **run** arrow button, select the load configuration, select the sensor type (P, N, or pin), set the temperature, & hit the **start temp control** button
* `IMPORTANT: you need to flip the switch on the set up to either heat or cool in order for labview to start controlling the temperature.`{:.warning} 
* `IMPORTANT: The load configuration & sensor type are different for each diode`{:.warning}:
    * **Dzeros**: either `D0_preirr_IV.cfg` or `D0_preirr_CV.cfg` & `N type`
        * For irradiated diodes: `D0_postirr_IV.cfg` or `D0_postirr_CV.cfg`
    * **Halfmoons**: `IT_Diodes_Preirr_IV.cfg` & `IT_Diodes_Preirr_CV.cfg`  
    * **P type**
        * OR: `IT_Postirr_Diodes_Half.cfg`  &  `P type`
            * We only need to run the CV of unirradiated diodes up to 600V, this older config file runs them up to 1000 volts. Irradiated diodes need their CVs tested up to 1000V.
        * Irradiated: `IT_Postirr_Diodes.cfg`
    * **HGcal**: `IT_Postirr_Diodes_Half.cfg` & `P type`
        * Irradiated: `IT_Postirr_Diodes.cfg`
    * **Pin**: `PinDiode_Irrad_HighFluence.cfg` & `Pin` type for unirrad and irrad

### Fourth
Fill out the test information for the specific diode you are testing.
    
* **File Name**:
    * **HGcal**: `IV or CV_N####_UR` or `LL_DIODE_GR_Irradiated_ Annealed_60C_#min`
        * HGcall diodes get irradiated from 0 - 100 minutes, in ten minute increments
        * We test the DIODE and DIODE QUARTER for HgCals with 2 diodes, and DIODE, DIODEHALF, and DIODE QUARTER for Hgcals with 3 diodes. The Hgcal diodes can either be UL, LL, UR, or LR. 
        * Unlike the half moons, we need to have a needle down on the guard ring for hgcal diode measurements
    * **D0** 
        * preirrad: `IV or CV_D0_CO###_LargeDiode_GR`
            * We only test the large diode of the Dzero diode, the small diode does not have a ground ring
            * Gets ran before irradiation, directly after irradiation (0 min annealing) and after 80 min of annealing
    * **Halfmoon** 
        * preirrad: `IV` or `CV_#####_###_PSS` or `2-S_HM_XX_DIODE`
        * DIODE, DIODEHALF, DIODEHALFPSTOP, DIODEHALFPSTOP_GR, DIODEQUARTER
        * For HMs, we only use the bias needle when running the test, the ground needle is only used when testing diodehalfpstop
    * **Pin** 
        * Preirrad: `Pin###`
* For the annealing status, either write “Not irradiated.” If the diode has been irradiated, write: 
    * **Irradiated and annealed at ___°C for ___Minutes**

<div class="card">
    <div class="card__content">
        <div class="card__header">
            <h4>DIODE Annealing steps:</h4>
        </div>
        <ul>
            <li>Set oven to warm up to 60°C</li>
            <li>Uses oven underneath benchtop along wall with dehumidifier</li>
            <li>Using heat gloves, take out the aluminum plate from the oven</li>
            <li>Place the diodes on the aluminum plate such that the tip of the diode sticks off (for easy removal from plate)</li>
            <li>Place diode in oven to anneal for ___ minutes (set timer)</li>
            <li>When you go to remeasure the diode, change the annealing status and the file name to account for the additional annealing time</li>
            <li>Take out the diode from the oven and place in the freezer until you are ready to measure it </li>
            <li>Run CV/IV for the diode</li>
        </ul>
    </div>
</div>

### Fifth

Make sure you flip she switch to CV or IV depending on which test you are running. 

### Sixth
Placing the diodes:
* **Unirradiated diodes** are stored in the dry boxes at room temperature, so you are free to open their baggies right away & can place them in the testing box
* **Irradiated diodes** are stored in the freezer, and need to be allowed to sit on the testing bench until they reach room temperature before their bags can be opened
    * We do not want the change in humidity to result in water droplets forming on the diodes
* Do not touch the diodes with your bare hands, and do not put your fingers inside their baggies. Use plastic tipped tweezers to remove the diode from the bag, and then use the vacuum pen to place the diodes inside of the plastic test box.
* Make sure you place the diode onto the vacuum holes on the platform (if testing more than one diode, do not let the diodes touch on the platform)
    * **Dzero**: place horizontally with large diode on the right
    * **Halfmoon**: place vertically with diode-side pointing towards the wall
    * **Pin Diodes** are not placed into the test box:
        * Move the yellow High_In wire (plugged in next to the CV/IV switch) & plug it into the hexagon shaped box sitting on top of the Current measuring units (@ spot labeled Hi In)
        * Connect the black hook wire to the larger terminal on the pin diode and the red hook wire to the little terminal on the diode
            * Make sure the red side of the diode is facing up
        * In Labview: Skip #5. There is no ground ring, no IV, and no CV
        * @ 6. Repeat for each sensor
            * Pre irrad Set number measured = 6, & delays = 20  or 10, 15
            * Postirrad: num meas =15, delays= 20
            * Test is ran multiple times in order to produce an average
        * Hit the Run Pin Diode Test (Multi) button to run test
        * The value we get for unirradiated diodes not not matter, so it is ok if you do not test them (they always end up being the same number = ~0.56)
        * Current range = 0.1mAmp - 2mAmp (0.0001 - 0.002), time of application ~1ms
            * Graph goes up to 0.002 
        * Make sure once you are finished running the pin diodes that you put the High_In wire back. 
* Turn on the vacuum (switch behind the test box) and close the test box
* Use the microscope & light to place the needles on the diode
    * Bias needle (front)= active part of sensor
    * Ground needle (back)= ground ring
* Allow the test box to reach the desired temperature & dew point before testing. 
    * The dew point needs to be below the test temperature. 
* Lower the metal box over the test set up = high voltage protection & keeps the light out; the test is light sensitive

### Seventh

Run the test by selecting the setting for either IV or CV and hit the “Run” button
* **IV** = Meas I, Meas GR (max V is 1000v), flip switch to IV, change file name to IV
* **CV** = Meas C (max V is 1000v, 600v for Dzero diodes), Flip switch to CV, change file name

### Eighth
Once the test is finished, and the voltage has decreased back to 0 volts, lift up the metal cover, and move the needles to their next location.  

### Ninth
Transfer the files into the HEP Shared Drive:
* For HGcal diodes: HEP_Shared - Testing - CVIV - Data - HGCal - preirrad or post irrad - batch # - diode #
* HGcal diodes get run for CV/IV preirradiation, and then post-irradiation, in annealing steps from 0 - 100 minutes in 10 minute increments. This is done to find the minimum depletion voltage  
* For D0 diodes: HEP_Shared - Testing - CVIV - Data - D0 diodes - either 0min, 80 min, OR pre-irradiation
    * The D0 diodes get testing for CV/IV three times: before irradiation, directly after irradiation with no annealing (0 minutes), and then after 80 minutes of annealing 
* For Pin diodes: HEP_Shared - Testing - Pin diodes - data - irradiated or unirradiated - specific pin diode #
* For Halfmoon diodes: HEP_shared - pre production - irradiation studies - data - post irrad OR preirrad - 2S OR PSs - specific batch number folder - specific sensor number folder

Once you are finished testing  your diodes, do not open the test box until the temperature within the box reaches 20°C. Once room temperature is reached, remove the diode using the vacuum pen and place it back into its baggie. Put that baggie back into the dry box (if unirradiated) or into the freezer (irradiated)

* Turn off all the machines and the wall air/power strip
* To close labview: right click, hit close all windows, x out of labview, hit quit

### Tenth

Coding step using Spyder: (TBA)
* Place the Cumulative data script in a folder containing the CV and IV files you want to analyze 
* In Spyder navigate to that script within that folder
    * Run the program
    * This will produce a series of graphs displaying the depletion voltage as well as an excel document with depletion voltages and current amplitudes

* Comet:
    * Open the Anaconda Powershell Promt app on your desktop
        * Type in: conda activate comet
            ```bash
            cd C:\Comet
            python comet.py
            ```
        * This will open the data visualization window
            * Navigate to the CV file you want to look at
            * Set to `IVCV_Brown`
            * Navigate to the folder where you want to save any graphs
            * Hit the render button to produce the graphs
                * Look at the 10K and 1K depletion voltage graphs for the CV data and record the depletion voltages given
                * Save both these graphs
                * Look at the fit of the graph, make sure it makes sense
            * Navigate to the corresponding IV file
                * Look at the IV graph and using the depletion voltages go along the curve and find the corresponding current amplitude
                * Save this graph for future reference
* Finding the inflection point, aka the peak performance of the diode, of the depletion voltages can be done by running a series of annealing steps.
    * **HGCal diodes**:  Depletion and then reverse depletion - turns around at an inflection point 
        * When the annealing begins to degrad the sensor instead of improve its performance like it did previously. 
        * For HGCal diodes, we perform this annealing in a series of 10 minute annealing steps  at 60C from 0-100 minutes, and if needed 30 minute annealing steps up to 240min. 
    * **Dzeros** only need an 80 minute annealing step at 60C. We know this is the ideal amount of annealing needed to reach the inflection point by performing enough tests on irradiated Dzeros. 