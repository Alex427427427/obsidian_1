**Conductor**: Alexander Li, student ID 30630711, contactable via alii0024@student.monash.edu
**Date**: 2024 August 22
# Risk Assessment
![[RA.png]]
# Aim

# 1 Background Theory

# 2 Preparatory Questions

# 3 Log of the Experiment
### 3.1 Initial Set up
{Explain what the set up consists of}
- I arrive at the lab, turn off the room light and examine the apparatus. 
- I make sure that everything was turned off, and push the shutter rod all the way in, before removing the lid. 
- I study what is inside.
- I examine the available double slits, and practice mounting them onto the magnetic holder at S2. 
### 3.2 Aligning the Laser
- I place the laser in its fixture and turn it on. I see the laser on but no light after the first slit, so I adjust the orientation of the laser holder until I see a diffracted light pattern pass through. I notice how sensitive the system is to small adjustments in the orientation of the laser.
- I aligned the laser by adjusting the vertical orientation of the holder with an allen key, and the horizontal orientation by rotating the holder horizontally after loosening the thumb screw beneath the apparatus. 
- Lab time was over, I had to turn everything off and leave the lab. 
### 3.3 Measuring the Double Slit Pattern with Laser
- I returned to the set up on a new day and found the laser to be misaligned. I took out the slits, adjusted the orientation of the laser until the light was centered at the end, and inserted the slits back: a single slit at the start for collimation, a double slit labeled "16" at S2, and a slit blocker. 
- I closed the lid to make sure no ambient light is being detected by the photodiode. 
- I connected the output of the photodiode to the digital multimeter. 
- I varied the S3 micrometer to notice the change in the measured voltage. The voltage jumps between the order of millivolts to the order of hundreds of millivolts. 
- I noticed that it took just a bit less than 1mm for the voltage to vary from minimum to maximum to minimum again. If i want 5 data points per fringe, I should vary the micrometer by 0.2mm per data point. 
- I noticed that the voltage reading fluctuates in the 4th significant figure, and is slightly decreasing over time. Could S3 be every so slowly varying on its own by the force of the spring on the other side of S3? I should take measurements quickly. 
- I put all the measurements into a table, and did a quick plot. 
![[double laser.png]]
- I notice the maxima and minima, and that there isn't much voltage measurement in the lowest and highest ranges. I keep this in mind for future measurements. 
- I also notice that the baseline measurement is around 7.6 mV. 
- Further analysis on this result will be performed after the experiment, when I have time. 
### 3.4 Measuring the Single Slit Pattern with Laser
- Since I want to capture multiple large lobes for the single slit Fraunhofer pattern, I changed the slit to the one labelled "18", realigned but allowing the whole pattern to be shifted sideways a bit, so I can capture higher order large lobes. 
![[single laser.png]]
- It was at this point I immediately realised that having a different spacing would not at all affect the single slit Fraunhofer pattern. Nevertheless, the further slit separation helped to make controlling the slit blocker easier. 
### 3.5 Quick Test Fit of the Double Slit Pattern
- I left the lab for lunch, and wrote a python script to fit the double slit data. It was not fitting correctly. 
- After many attempts, I realised that in the initialisation of the parameters, I calculated them wrong. Firstly, I was implicitly assuming my independent variable $x$ was $\theta$. But in fact I needed to write $x/z$, where $z$ is the distance of the double slit to the detector. 
- I measured this, found it to be around 492.5 mm, with an uncertainty of 0.5 mm due to the ambiguous thickness of the slit frame, obscuring measurement. 
- The resulting fit was successful.
![[laser double test fit.png]]
### 3.6 Setting up the Lightbulb for Single Photon Interference
- {impossible alignment with paper}
- Measured 820mm between collimating slit to the detection slit, 1m between bulb and detection slit. 
### 3.7 Optimising the Light Dark Trigger Discrimination
