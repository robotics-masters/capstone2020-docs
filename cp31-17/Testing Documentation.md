## Testing Documentation

**Still Image Testcases**

This was our first iteration of testing early in the development lifecycle and has essentially been replaced via other methodologies.

In order to run these tests:

1. Enter the directory mysim/rmracerlib/still_image_testcases

2. Run each of the python files (each file pertains to a different sign to be tested)


*Note: The images within this form of testing is a combination of real-world images and images captured within the unity simulator*

**Efficiency Testing**

This testing methodology is a custom script in which the user will provide classification for each frame from a set of test footage. This footage comprises a run-up to the sign, appropriate range for detection for the sign and blank data after already passing the sign to be tested.

In order to run these tests:

1. Enter the mysim/rmracerlib directory

2. Run any of the python files which match the syntax "eff_**Sign Name**.py"

3. A frame will be displayed which needs to be classified according to if a box can be seen or not as the follow guideline below dictates

4. Upon completion of all the frames; enter your name for logging purposes

5. Results can be found summarised in the appropriate text document "**Sign Name**_Efficiency.txt"

*Guideline for classifying frames*

Q = Detection is present and correct location (True Positive)

W = Detection present in wrong location (False Positive)

E = Two or more detections where one of them is in the correct location (True Positive & False Positive)

R = No detection but there SHOULD be (False Negative)

T = No detection but there SHOULD'NT be (True negative)

Y (only for turn signs) = Incorrect direction on the turn sign 

**Automated Real-World Testing**

The testing methodology takes thousand of pre-sorted images from the real-life Robotics-Masters Shenzhen track. 

In order to run these tests:
1. Enter the mysim/rmracerlib directory
2. Enter on the terminal `Python real_life.py`
3. The results will display within terminal for the stop sign, green park, left turn and right turn