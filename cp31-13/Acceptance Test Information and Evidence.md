# Implementation of Client Specified tracks
For our acceptance tests, we would run the simulation with our newly created tracks and verify that nothing within the simulator was breaking. Unfortunately, we do not have any evidence which shows this. Our other main acceptance test would be showing the client the new tracks and getting verification that they met his specifications. Evidence of this is on our Discord channel, with screenshots being shown below:
![Track 1.PNG](https://bitbucket.org/repo/oo8byMk/images/665743985-Track%201.PNG)
![track 2.PNG](https://bitbucket.org/repo/oo8byMk/images/590062446-track%202.PNG)

# Integration of OpenCv code into the simulator and making the car react to signs
For our acceptance tests, we would run the simulator and see if the car was detecting signs through output files, and by observing the car's camera. Evidence can be found [here](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/src/0ba8e7f8cf0625a55023998559909f0653d3c4d2/donkey%20gym/mycar/rmracerlib/cv/signs.py#lines-119) and [here](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/src/0ba8e7f8cf0625a55023998559909f0653d3c4d2/donkey%20gym/mycar/rmracerlib/cv/signs.py#lines-173). These lines write the images of the detected signs to the [examples folder](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/src/Simulator-testing/donkey%20gym/mycar/examples/).
 Similarly for testing that the car was reacting to the signs, we would run the simulator and ensure that the car was reacting appropriately (ie stopping before stop signs and turning at turning signs). We would also send demos to the client to ensure that the Donkey Car was expecting as he expected. Evidence: https://youtu.be/KUbAHsUcolg

# Additional testing of detection code performance 
To allow for easier testing, the stop sign OpenCV detection code was modified so that it would be OOP, and test cases were added to help with fast confirmation of successful detections and false positives. 
(https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/465766e630f7109ffe582c6df3ed4fd71a2bc358)

Later improvements were made to streamline this, and added some test cases.
(https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/e0ee41cabe4610a0822b66ddcdb92d770e7abe37)