# FringeLocker
##Intro
 FringeLocker, as its name indicates, is an electronic system designed to lock interference fringes of an optical interferometer or a holography recording setup.
 The purpose of locking an interferometer is usually to stabilize unstable interference fringes due to mechanical vibrations or thermal drifts.
 
## Working principle
Two photodiodes sample the interference fringes and detect any movement of those. 
A low noise amplifier and feedback loop drive a mirror which is placed on a piezo transducer in order to move one arm of the interferometer and compensate for the detected fringe movements

# Setup
This version of FringeLocker is powered by two MN21/A23 12V batteries. Alternatively connector J3 on the board can be used to power the board with an external supply of
your choice (remove the batteries first!). The board accepts supply voltages up to +/-18Volts. 
Slider switch SW2 switched ON/OFF the board. A small 1mA Led (D3) indicates that the board is powered. 
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


 
