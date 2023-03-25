# FringeLocker
## Intro
 FringeLocker, as its name indicates, is an electronic system designed to lock interference fringes of an optical interferometer or a holography recording setup.
 The purpose of locking an interferometer is usually to stabilize unstable interference fringes due to mechanical vibrations or thermal drifts.<br />
 Demo video: https://youtu.be/0IrlpE1sPkQ
 
 <p align="center"> <img src="/FringeLocker/Photos/Back.jpg" width="702" title="Overview"> </p> <br /><br />
 <p align="center"> <img src="/FringeLocker/Photos/Front.jpg" width="702" title="Overview"> </p> <br /><br />
 <p align="center"> <img src="/FringeLocker/Photos/Schematic.jpg" width="702" title="Overview"> </p> <br /><br />
 
## Working principle
Two photodiodes sample the interference fringes and detect any movement of those. 
A low noise amplifier and feedback loop drive a mirror which is placed on a piezo transducer in order to move one arm of the interferometer and compensate for the detected fringe movements

## Setup
This version of FringeLocker is powered by two MN21/A23 12V batteries. Alternatively connector J3 on the board can be used to power the board with an external supply of
your choice (remove the batteries first!). The board accepts supply voltages up to +/-18Volts and so currently I am using two 9V batteries in series for each voltage ramp in order to increase lifetime on battery.
The photodiodes need to be masked of, leaving just one slit 0.5mm wide per photodiode. See image in the photos folder.
Slider switch SW2 switched ON/OFF the board.  
There are three adjustments to be performed on the board. 

1- Servo Gain
RV1 10 turns potentiometer adjusts the servo gain. Start by adjusting it to minimum

2- Output bias
RV2 10 turns potentiometer adjusts the level of bias voltage to the piezo transducer. Since positive or negative voltages can be applied to the transducer it is necessary to apply
a bias to it. Use a voltmeter to measure the bias voltage between ground (the pcb mounting holes in each corner are grounded) and Test Point 2 (TP2 or TP Bias) and adjust it to 18 volts or so.

3- PresScaler switch
SW1 is a rotary switch which selects a preamplification of the photodiodes signal with various gains. Start by adjusting it to minimum

## Servo loop adjustment
Place the photodiodes within interference fringes of the interferometer. Adjust the interference fringes spacing so that their spacing is approximately 15mm (twice the spacing between the photodiodes). 
Power the board and start with the lowest gain on the PreScaler switch SW1 and move to larger gains incrementally until the feedback loop starts oscillating.
Revert to the previous gain setting in order to stop the oscillation. You can then fine adjust the loop gain RV1 by increasing it slowly until the loop starts oscillating, then reverting a bit to stop the oscillation.

## Bugs
An unpolarized 100nF capacitor needs to be manually added in parallel with R2 in order to create an active low pass filter and prevent the feedback loop from oscillating

## Credits
Thanks to Phil Hobbs for his help on the schematic design