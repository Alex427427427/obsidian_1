**Conductor**: Alexander Li, student ID 30630711, contactable via alii0024@student.monash.edu
**Date**: 2024 August 22
# Risk Assessment
![[RA.png]]
# Aim
To observe and quantitatively measure the two-slit interference pattern of a monochromatic source in two situations: one using a laser that emits a barrage of photons, allowing multiple photons to be present in the apparatus simultaneously, and another with a source that emits only one photon at a time, thus observing the wave-particle duality of light. 
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
- 2 days later, I returned to the lab and turned everything on. I moved the micrometer to see if I get maxima and minima in the counts. I do, which means the bulb light is still aligned correctly. This makes sense, considering there was no one else that used this equipment in the time I was away. 
- I try to obtain a high count to start the optimisation process for light-dark discrimitation. So I align the micrometer until the count is at a maximum. 
- To make searching for the maximum more tractable in the time I have, I reduce the gate time of the counter down. Once I did this, I noticed the count fluctuates a lot. At around 500 counts/s, the fluctuation is roughly 100. I make a note to check the fluctuation at each measurement in the future, to obtain the uncertainties. 
- I found a micrometer position where, given 700V applied to the PMT, the count was around 500. Now that a maximum was found, I turned the gate time back to 10 seconds. 
- I adjusted the PMT voltage, and for each voltage, noted down the counts when the shutter was open (representing the light from the bulb shining on the PMT), and when the shutter was closed (representing the ambient noise in dark conditions). 
- I made sure I stayed at one position for a full 10 second update of the counter, so that my measurements aren't contaminated by the previous measurement. Therefore, I take the second update on the counter as my measurement. 
- I plotted the results in Excel.
![[light dark.png]]
![[excel_optim.png]]
- I notice a sharp drop between 525 and 500V, so I took more measurements around there. 
![[more meas optim.png]]
![[more meas optim ratio.png]]
- At 525V, the signal to noise ratio is the highest, so I chose this PMT voltage. 
- Additionally, I recorded the uncertainty in the counts with respect to the light level, and produced a table, to be used in future uncertainty analysis. 
### 3.8 Collecting Data for the Single Photon Interference
- I set the PMT voltage to 525V. 
- I had 3.5 hours left, so I did a quick calculation on how finely I should take the measurements. Provided that the slit separation is the same as previously, and the slit width is the same, and the wavelength of the bulb's green light ($545 nm$) is slightly shorter than the red laser light ($670nm$), the fringes will be ever so slightly closer together compared to the laser. For the laser pattern, there were roughly 5 fringes within 4 mm, meaning there was 0.8mm per fringe. So, using the proportionality of the fringe spacing to the wavelength, the green light from the bulb should produce $0.8 \times\frac{545}{670}=0.65mm$. 
- Suppose I took 5 points per fringe; that means I needed to move in increments of roughly $0.125mm$, meaning there would be 8 measurements per mm, so 64 measurements over the range of 1mm to 9mm. If I had to wait 20 seconds per measurement, that is $64\times20=1280s\approx21min$, which meant I had more than enough time. 
- I moved the micrometer to 9mm, making sure to only move down to avoid hysteresis. Then I took measurements by waiting for the second 10s update at every location, to avoid the previous measurement interfering with the current one. I took measurements with increments of $0.125mm$. 
- I noticed the count still fluctuates over subsequent 10s updates, so I decided to record the 2nd, 3rd, and 4th update. This would still leave me enough time to complete the experiment. 
- I obtained the plot of the double slit pattern.
![[bulb double excel pattern.png]]
### 3.9 Quick Test Fitting of the Pattern in Python
- I put the data into a python file, supplied the model and the initial guess for the parameters, calculated from the parameters supplied in the lab manual, and plotted. 
![[bulb double slit fit.png]]
- Seeing that I obtained a successful fit, I packed up and left.

