# COMP3988_T17B_Group1 First Project Report
## COMP3988_T17B_Group1 ##

**Tutor**: Frank Fu

**Date Submitted**: Sunday 4 October 2020

[University Group Form](https://bitbucket.org/repo/G6xBMXK/images/950575578-assignment_sheet_group_1.png)

---
# Executive summary

This report provides a general idea of our system as well as shows each stages of our development process and analysis for the “Implement Sign Detection With Tensorflow” project.
 
The system we are working on is basically a sign detection model that can automatically detect different signs and make corresponding response to them. Our system will be built on the donkeycar platform using Tensorflow for model training and Unity for environment development. More detailed, we use CNN algorithm to train the model and use rmracerlib to make the model run in the simulator.
 
The project is being completed by:
 
* @ydon4228
* @zhua4138
* @sjia0385
* @yjin5856
* @hlan3540
* @moxu7046
 
We acknowledge that a significant part of the project comes from the [github repository](https://github.com/wroscoe/donkey/) owned by user @wroscoe and the [github repository](https://github.com/tawnkramer/sdsandbox.git) owned by user @Tawn Kramer.

---

# Table of Contents #
1. Introduction
1. System Specifications
    1. User Story
    1. Technical and other constraints
    1. System Architecture
    1. Plan for implementation of remaining user stories using storyboard
1. Quality of Work
    1. Overview
    1. Details of tests
    1. Test Conclusion
1. Quality of Group Processes
    1. Setup of tooling for development 
    1. Team Collaboration
    1. Client Interaction
    1. Critique
1. Technical Documentation
1. Appendices

---

# Introduction

This report serves as a phased summary for progress and status of the project in the first half of the semester. It also provides some insight of what will be done and achieved on the project after coming back from the vacation. 
We take a look at the client’s requirements and expectation of the project; the goals and scope of the projects; system specification; group work, communication, and interaction in the following sections.


- **The overall project vision** **and goals** 

    Autonomous vehicles and related technology have evolved rapidly in recent years. Among all of them the most popular and crucial player is the auto-piloting, which is essentially what differentiates manual and autonomous vehicles.
    
    Many components jointly makes the vehicle intelligent so that it can automatic drives itself; Obeying traffic rules is one of the priorities. Traffic signs detection, an important part of traffic rules, is what we are implementing in this project. 


    We employ existing technology (TensorFlow Neural Networks) to create new software solutions to detect some pre-defined traffic signs (e.g. stop, turn-left, turn-right signs). We build classifiers of signs by feeding cleaned data collected in racing car simulator into a model; train the model; and collect a classifier. The goal is to build more accurate and reliable classifiers using better simulator and better data, as well as applying better data cleaning techniques and more efficient classification algorithms.


    The team has been closely working with the clients and other teams to fully understand the evolving requirements of the client and harvests the progress of other teams working on relevant projects.


    At the end of the project, the team will compete in a challenge to test their solutions in a real-world scenario for efficiency and effectiveness.
    
- **What the project will achieve**

    The team is expected to have a functioning high-performance and accurate traffic signs detecting algorithms as well as a set-up virtual training ground used to collect data and train the model by the end of the project. 


    Documentation is expected so that any teams or individuals can quickly start off what the team has done in this project and build on top of existing fundamentals. 
    
- **The key stakeholders, what do they do, and how they interact**
    - **The key stakeholders:**
        - **Robotics master(the client):**
            The robotics company builds autonomous obstacle avoiding and auto-piloting robots. This sign detection algorithms can assists in auto-piloting of the robots (vehicles) in real traffics.
            
            The client gives requirements to the team on a weekly basis. The team implements the client’s requirement with consultations to the clients and online documentation for professional advice. Ultimately the team is building the project for this stakeholder.

        - **Human drives**
            Human drives are highly relevant to this technology as it can release humans from this dangerous and sometimes tedious jobs of daily driving. Autonomous vehicles provide safer, more efficient solutions to existing error-prone, dangerous, congested traffic caused by inherent disadvantages in human’s characteristics and minds.
            
            Autonomous driving is expected to partially and eventually fully replace human drives for a safer and less congested commuting traffic environments for all road users. Sign detection is a crucial components of any practical auto-piloting.

        - **Car manufacturer**
            Since autonomous vehicles will become the trend of the future, current car manufacturer must evolve their technologies and manufacturing process so they won’t be left behind.


            Car manufacturer needs to either develop their own technology like Tesla, or purchasing or investing into other companies to acquire such a technology.

        - **Other road users**
            Other road users include: cyclist, pedestrian, etc. Currently they share roads with cars which are manually controlled. Human drives can be distracted or have bad judgements which can post danger to them. Once autonomous vehicles are widely used they can use the roads much more safely.


            Autonomous vehicles must be able to detect the existence of other road users and place their safety as the first priorities (since they are usually more vulnerable than people sitting in vehicles)

        - **Governments and regulators**
            Autonomous vehicles require different regulation and coordination as they are controlled by computers. The effectiveness, safety, and security of computers must be carefully monitored and tested before they are legally allowed on-road. How to thoroughly test the effectiveness and safety is to be considered by the governments and transportation regulators.
    
- **Identification of resources and risks involved in the project**
     - **Resources:**
        - **Donkey Car Simulator:**
            The algorithms will be tested in a simulator provided by Donkey Car simulator, which is an open source project available for download and contributions on GitHub.


            It allows teams who don’t have a physical donkey car or robots to develop and test their algorithms in a cost-efficient and easy way. It also saves time from building a physical robots. We use donkey car simulator to collect training data which we feed into the model; to test our auto-piloting and sign detection model in the simulator for its effectiveness, etc.


        - **TensorFlow**
            TensorFlow is an open-source platform for machine learning. It provides comprehensive tools, libraries for developing machine learning models and testing machine learning algorithms.


            We use TensorFlow to write the logic for our classifier using encapsulated algorithms provided by TensorFlow. We also use tutorials provided by TensorFlow to start our project from the scratch.


        - **Unity**
            We use Unity to build new testing tracks in the simulator as well as new car models. What’s most important is that we use Unity to build models of traffic signs in existing and new tracks. 3D modeling allows easy collections of training data (e.g. pictures) in a track from different angles, scenario, and speed.
            
    - **Risk**
        Since team members collaborate remotely on the project, there won’t be any risks relating to the current pandemic. Simulations are used instead of physical models so there is no physical risks associated with the project.

---

# System Specifications
## User Story

Our project is mainly divided into two parts. Part 1 is improving the donkey car simulator environment. Part 2 is writing auto sign detection code for the car using tensorflow. According to the functional diversity of our project, we are going to write user stories separately for these two parts. 

**Part 1. Improving the donkey car simulator environment:** 

- Tester (People who drive the car using the designed track on simulator): 
    - Tester 1: As a tester, I want the track to include **as many signs as possible**. So that I can write codes to detect many signs by using one track. 
    - Tester 2: As a tester, I want  the **setup of the environment** for the track as easy as possible. So that I can easily set up the environment and focus on writing codes for detecting signs.
    - Tester 3: As a tester, I want **the raw images taken when I drive the car as clear as possible**. So that I can improve my sign detection codes. 
- Maintainer (People who is going to maintain the track for later use):
    - Maintainer 1: As a maintainer, I want to add more signs and build new tracks to the track easily in the later day. So that the maintenance job can be more efficient. 
- Leaderboard (anyone who race donkey car on leaderboard):
    - Racer 1: As a racer, I want to know if the racing environment is easy to set up on my computer. So that I can focus on the race rather than spend time on set up.
    - Racer 2: As a racer, I want to know whether or not  the racing environment will be affected by computer configuration . So that I can know the fair of the racing environment. 
    - Racer 3: As a racer, I want to see a scoreboard of the current race with lap times and personal best, so that I can know my current place in the game and other competitors’.
    - Audience: As an audience of the racer league, I want to watch the live show of the race from my own computer so that I do not have to go out.

**Part 2. Writing auto sign detection code for the car using tensorflow:**

- Automotive industry:
    - Business 1: As a business, I want to know if the certain sign detections algorithm is reliable, so that I can decide whether or not to adopt the technology.
    - Business 2: As a business, I want the sign detection model to detect as many kinds of signs as possible so that the car will not break the traffic rules.
    - Engineer 1: As an engineer, I want the system to have a high adaptability so that we can use the system inside our own system without worrying about compatibility.
- Researcher for Driver Assistance System:
    - Researcher 1: As a researcher, I want to have documentation about the limitations and benefits for certain signs detection code, so that I can clearly understand the code and make improvements in  the future.  
    - Researcher 2: As a researcher, I want to have data on the certain algorithms for the sign detections, such as the percentages to clarify the signs correctly. So that I can decide how to make improvements in  the future.  
    - Researcher 3: As a researcher, I want to have a tutorial on how to build sign detection models so that we can do further training based on the results.
## Technical and other constraints

**Version constraints**

There are some version constraints we encountered when we use tensorflow for sign detections. For example, tensorflow v2’s module has not attribute ‘app’, thus we cannot use that attribute if we downloaded tensorflow v2. The solution is to use tensorflow v1. 

Also, if we want to use GPU to train the model, we should install two packages, cudatookit and cuNN. The version of these two packages should also be restricted to the version of tensorflow. For example, tensorflow 2.1 requires cuda 10.1 while tensorflow 2.3 asks for cuda 11.0. 

**Algorithm constraints**

Our sign detections were used convolutional neural network only. While we may encounter some constraints from using CNN, such that, CNN does not have build-in understanding of 3D space. It means CNN requires tens of thousands of examples to achieve good performance. This increases difficulty in our data collection process. Also, CNN do not encode the position and orientation of object, which means to CNN, both images are similar if they contain similar elements. This may bring up a reliability issue for those similar signs in sign detection process. 

## System Architecture

Basically, our system can be split into two parts: the track and the model. The tracks with different signs are used for data collection and testing which the model is the core of our system. It should be able to detect which sign the car is meeting with and does the corresponding behaviour. That is, the model should  make the car acts like be driven by a real man.

**The Initial System (Platform)**

Initially, we have a donkeycar platform, which include the simulator and the donkeycar+gym-donkey. This allows us to set up a donkeycar in our local machine or in a virtual environment and drive the car in the simulator. There are four maps in the simulator with different environment, as shown in figure 2.a, and tracks so that we can choose one based on our requirement. Also, users can easily build a car by entering one simple command as well as change some settings based on the comments in the myconfig.py file. Furthermore, if users want to train a model and build a self-driving car, they can use the code provided by the platform to train the model. However, to further develop the system, such as adding tracks and building our own models, requires more famiarlity with Unity and in-depth researches on neural network.

![Figure 2.a](https://paper-attachments.dropbox.com/s_C4C36EBA2D1A168032A0C413C20C0FB0AAECF8650B20D7C77E3D7EF3B74D1036_1601654327682_.png)


**The Track**

Back to the requirement, we need to build a model to detect different signs such as stop sign, parking sign, etc. However, there are no such signs in the initial tracks. Therefore, we have to create a new track by our own.

The new track should include four basic signs, the stop sign, the left-turn sign, the right-turn sign and the  parking sign. The 3D objects of these signs will be built using Blender and the simulator will be set up using Unity. Also, collision systems should be added in the track to prevent the car from driving outside the map or through the sign.

**The Model**

The current code provided by the initial platform can only train a self-driving model. So, we are planning to write our own code to train model that can classify different signs. These codes will be written in Python and we will use the CNN algorithm from the tensorflow open source platform to train the model. Also, the rmracerlib library will be required to send corresponding JSON packages to the simulator so that the predicted result of the model can be displayed on the simulator.

## Plan for implementation of remaining user stories using storyboard: 

 There are 2 user stories remaining to be implement in the next sprint. 

| User story                                                                                                                                                           | Plan for implementation                                                                                                                                              |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| As a racer, I want to see a scoreboard of the current race with lap times and personal best, so that I can know my current place in the game and other competitors’. | ![](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601710476780_leaderboard.jpg)                          |
| As a business, I want the sign detection model to detect as many kinds of signs as possible so that the car will not break the traffic rules.                        | ![](https://paper-attachments.dropbox.com/s_3B5CA9CFB9EA6B3F170D08C5EDFAA518790C5F216C2BEC1BF439957E6694D9A9_1601701831916_Screen+Shot+2020-10-03+at+3.10.11+pm.png) |


# **Quality of Work**
## Overview
| Requirement                                                                                                                                                                                                          | Acceptance Test                                                                                                                                                                                                                                                                                                                                                                              | Results                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. As a tester, I want the track to include **as many signs as possible**. So that I can write codes to detect many signs by using one track.                                                                        | The track is implemented in Unity as in the given specification, including stop, turn left/right, and parking signs.                                                                                                                                                                                                                                                                         | Passed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 2. As a tester, I want the **setup of the environment** for the track as easy as possible. So that I can easily set up the environment and focus on writing codes for detecting signs.                               | There should be clear documentation on how to set up the environment for the track we built in the simulator                                                                                                                                                                                                                                                                                 | [Link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Donkey%20car%20environment%20for%20new%20created%20track%20SetUp%20Guide)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 3. As a tester, I want **the raw images taken when I drive the car as clear as possible**. So that I can improve my sign detection codes.                                                                            | The camera resolution of the image taken by the donkey car in simulator should be of 240 * 240 pixel values.                                                                                                                                                                                                                                                                                 | Passed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 4. As a maintainer, I want to **add more signs and build new tracks** to the track easily in the later day. So that the maintenance job can be more efficient.                                                       | The process of adding signs and building new tracks in Unity should be well-documented, quick and easy to follow.                                                                                                                                                                                                                                                                            | [Link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/Docs/Map_and_Sign_Implementation.pdf)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 5. As a racer, I want to know if the racing environment is **easy to set up** on my computer. So that I can focus on the race rather than spend time on set up.                                                      | There should be clear documentation on how to set up the donkey car environment and simulator.                                                                                                                                                                                                                                                                                               | [Link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Tensorflow%20and%20Donkey%20Simulator%20Environment%20Setup%20Guide)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 6. As a racer, I want to know whether the racing environment will be affected by computer configuration. So that I can know the fair of the racing environment.                                                      | During the race, the race conditions for each racer should ideally be identical, including internet connection, computational speed.                                                                                                                                                                                                                                                         | Not applicable test                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 7. As a business, I want to know if the **certain sign detections algorithm is reliable**, so that I can decide whether or not to adopt the technology.                                                              | 1. The correct prediction rate of each class is high and stable in multiple runs 2. If the model cannot detect the sign or unsure about the sign, then classified to “other” (i.e. no action)                                                                                                                                                                                             | Passed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 8. As a researcher, I want to have documentation about the **limitations and benefits** for certain signs detection code, so that I can clearly understand the code and make improvements in the future.             | There should be a description about the employed sign detection model (Neural network), and also other possible alternatives.                                                                                                                                                                                                                                                                | [Sign detection code](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_2Oct.ipynb)  [Limitation of CNN model](https://yuanda-dong.atlassian.net/browse/CP-11?atlOrigin=eyJpIjoiNmJiOWYzNjhlOGUxNGRlZmFjOWI4YWJhNDU4NjlhM2QiLCJwIjoiaiJ9) [Benefits of CNN model](https://yuanda-dong.atlassian.net/browse/CP-12?atlOrigin=eyJpIjoiYTVhNDQyYzI2MTNmNGRmZmI2MTA2MTM0MmE0ZjdhNWMiLCJwIjoiaiJ9)|
| 9. As a researcher, I want to have data on the **certain algorithms for the sign detections**, such as the percentages to clarify the signs correctly. So that I can decide how to make improvements in  the future. | 1. Model accuracies tests should be performed on the employed model. This include the percentage of correctly classified signs as a single number, and the confusion matrix. 2. Model should have low misclassification cost: If the model cannot detect the sign, then classified to “other”(i.e. no action) 3. No overfitting: ensure the model can perform well on the new images. | [Explanation of evaluation algorithm and accuracy tests for CNN model](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/CNN_model_Evaluation)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 10. Audience: As an audience of the racer league, I want to watch the live show of the race from my own computer so that I do not have to go out.                                                                    | The actual race shall be streamed live, so that audience can view it from anywhere.                                                                                                                                                                                                                                                                                                          | Not applicable test                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 11. As a business, I want the sign detection model to detect as many kinds of signs as possible so that the car will not break the traffic rules.                                                                    | 1. Sign detection model should be accurate in predicting the traffic signs including (Stop, left, right, park, other) with at least 90% accuracy. 2. Donkey car should be able to respond accordingly to the sign detected.                                                                                                                                                              | Passed except for parking sign                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 12. As a researcher, I want to have a tutorial on how to build sign detection models so that we can do further training based on the results.                                                                        | There should be documentation written on how to build a working sign detection model, including 1. Data collection and cleaning using simulator 2. Building the model using tensorflow 3. Train the model using tensorflow with the option for parameter tuning                                                                                                                 | [Simulator Documentation](https://docs.donkeycar.com/guide/simulator/) [Build and train model using tensorflow](https://www.tensorflow.org/tutorials/images/classification)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 13. As a racer, I want to see a scoreboard of the current race with lap times and personal best, so that I can know my current place in the game and other competitors’.                                             | A web-based leader-board that displays the lap time and personal best. 1. It should be able to collect Json packets from the server machine. 2. It should be able to interpret this information and display with a user friendly interface                                                                                                                                            | Awaiting implemnetation                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 14. As an engineer, I want the system to have a high adaptability so that we can use the system inside our own system without worrying about compatibility.                                                          | The system should have a fixed list of dependcies <br>and should work across platforms, with clear documentation on how to install the environment required. Preferably in the future, the system will be depolyed with a docker container.                                                                                                                                                  | [Dependency List](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Dependency%20List)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |

## Details of tests

**Unit** **Testing plan (applicable)** 

- **Test 1: Autonomous driving in the simulator** 

    To start experimenting with sign detection models, we need first build a simple autonomous vehicle in the simulator. We will test the performance of such vehicle by measuring the duration for which the donkey car can self-drive without hitting any obstacles. 


- **Test 2: Stable and high accurate image classification**

    We choose CNN model, as it is the most successful model for image classification in recent year.

    Our model can classify the input images (collected by the donkey car) into 5 classes: Right-turning, Left-turning, Park, Stop and other (Other means no sign detected). 

    By choosing the proper number of convolutional layers and epochs, we train the model using more than 6600 images, and test the model performance using extra 1200 images (test data), which are not used in the model training. 

    Firstly, we test the model has no overfitting, which means that the test accuracy using new images (test data) is close to the evaluation accuracy achieved during model training. Secondly, we test our model structure can achieve the highest test accuracy based on the hyper-parameter turning result. Thirdly, we test our model has low misclassification cost. That is, If the model cannot detect the sign, then classified to “other”(i.e. no action). 

    [Jupyter notebook link for the CNN model testing](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_2Oct.ipynb)


- **Test 3: Custom built track has the correct physics** 

    We will test whether the track we built responds to user input(via keyboard for driving)/object collision reasonably using the physics in Unity. To do this, we will divide the test into normal/abnormal test cases, where the normal test case looks at how accurate the donkey car responds to user inputs and manages to drive around the map. This will involve driving in a straight line turning and braking. In the abnormal case, we will intentionally drive the donkey car to hit the poles of traffic lights/signs, and walls to check the object collision. 


- **Test** **4****: Real-time** **sign** **detection** **in simulator**

    Given the accuracy of the CNN model is tested, the next step in our plan is to test whether the model when fed into a data stream of camera images, is able to predict the label class in real-time. The input space can be partitioned into images containing [stop, left, right, park, no sign] signs. We will test whether these camera images are correctly classified, by printing the class label to the console in real-time. 


- **Test 5: Donkey car can respond accordingly to the sign**

    Donkey car should stop by reducing the throttle value, after a stop sign is detected. Similarly, the donkey car should turn left/right when a left/right sign is detected. This can be tested by running the image detection model and self-driving model at the same time in the custom map containing traffic signs. Then, we will print out the actual throttle and angle values received by the donkey car, and observe the behaviour of the donkey car. Since the code for interfacing the image classification model and the donkey car is provided by the client, we can just use it for now. In the future, we will look at how it actually works, and perform some unit tests on that. 

**Not applicable test** 

1. Requirement 6: We can’t really test fairness issues of the race due to internet/computer connections. 
2. Requirement 10: Since the race day is not yet decided, the test for live-stream is not applicable ATM. 

**Remaining user stories for testing** 

1. Web server for leaderboard: This requirement is kept in the backlog, and we will implement and test it in the future sprints. 
2. Donkey car reaction to parking signs: This functionality has not been implemented in the code interfacing the classification model and the donkey car. 

## Relevant testing techniques

**Usability testing**

Usability tests will be an important aspect of our testing process, once the acceptance conditions for each functional requirement have been met. We aim to build a usable system with clear documentations, so that a user with little prior knowledge in autonomous vehicle can use the tools that we provide in our repository to train a self-driving car capable of sign detection, and compete in races. We intend to perform the following usability tests in the future:

1. User can produce the image dataset required for training their model by manually driving in the simulator map
2. User can create their own custom map if needed by following the documentations that we provide
3. User can build a neural network model for autonomous driving in the simulator easily 
4. User can build an traffic sign/light classification model and has the option for fine tuning of their model  
5. User shall be able to learn more about the model that we use by reading our documentation
6. User shall be able to compete in a virtual race. 

All of the above mentioned tests will be conducted with a user with little knowledge in the subject area, to ensure the usability of our system. 

**Autonomous driving and sign detection in real time inside simulator** 

At this stage, we have built a prototype implementation of the models. Since the requirements related to autonomous driving and sign detection in simulator focuses more on the behaviour aspect of the donkey car, i.e. whether it can drive without hitting obstacles, classifies signs and responds accordingly. We have devised our testing techniques to test the behaviour of the donkey car:

1. We will test the performance of self-driving model by measuring the duration for which the donkey car can self-drive without hitting any obstacles. 
2. We will test the correctness of the image classifier by printing the class label of the camera image in real-time inside the simulator. 
3. We will test the responses of the donkey car to the traffic sign, by measuring the throttle and angle values after a traffic sign is detected, and by observing the movement of the donkey car in the simulator. 

**Performance and reliability consideration**

The computational demand of training a performing neural network model can be high if the given dataset is large. However, this is not so relevant in the testing section, and we provide a free method for training the model using [Colab, which provides cloud computations](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Training%20neural%20network%20using%20google%20colab) with server-grade GPU. Therefore, the emphasis should be placed on computational costs of running both self-driving and image classification models in real-time while rendering the graphics of the donkey car simulator environment. Now, this depends critically on the CPU and the graphic cards of the computer. We expect to see some discrepancies on the model’s performance among computers of different spec, especially in race condition. In the future, we will test such differences. 

The model should be reliable in the sense that it should minimise FP (false positives). False positive occurs when the model predicts a signed class label, while the image contains no signs. In such case, the donkey car would behave abnormally. We will test this behaviours alongside with the previous part ‘sign detection in real time inside simulator’. Here, we provide one possible solution in pseudocode to increase the reliability. 

    if 100 * score (aka. confidence level) > 90:
        return class_name
    return None

Alternatively, we can keep improving the image classification model so that no false positives will be reported. 

**Quality of Dataset used for CNN model training**

The train and test data were collected by donkey car simulator given by different drivers, and we use this dataset to train and test the CNN image classification model. 

- Data folder [signed_map_test_2Oct](https://drive.google.com/file/d/1ABoMF8V9I9DZlMJxaWx_9FfOXZ4jIgLj/view?usp=sharing)
- Train data (6653 in total): 731 stop images; 1013 park images; 1233 right turn images; 1328 left turn images; 2348 other images
- Test data (1202 in total): 132 stop images; 192 park turn images; 183 right turn images; 144 left turn images; 551 other images
- We collect more images of “other” class in the dataset, as the donkey car will see more “other” image (i.e, No sign detected )
- Within the train data, we separate 20% data as the evaluation data to validate the hyper-parameter turning and avoid overfitting. 

**Convolutional neural network (CNN) algorithms introduction**

A **convolutional neural network** (**CNN**, or **ConvNet**) is a class of deep neural networks, which is commonly used for image classification. 

- `Convolution layers`: the core building block of a CNN. Our model has 3 hidden layers. 
- `Number of filters`:  the dimensionality of the output space (i.e. the number of output filters in the convolution). Our model choice 16, 32, 64, and 128 as filters in each layer.
- `Epochs`:  the number of passes of the entire training dataset the machine learning algorithm has completed. The low epoch value can result in under-fitting, high epoch value can result in overfitting. The proper number of epoch choice is necessary. Our model using epoch = 7.
- `Activation function`: determine the neuron should be activated (“fired”) or not. Our model use `relu` as activation function, as it is computationally efficient. 
- [CNN model evaluation algorithm](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/CNN_model_Evaluation)

**A summary of the details of the acceptance tests** **is in Appendix** 


## Test Conclusions 

**Summary of what test demonstrates** 

Our prototype implmentation has shown great promises in the potential of neural network techniques in real-time image-classifcation and responses. 

**Limitations of the CNN model** 

1. No data cleaning and feature engineering in the image pre-processing
- Will try to add them to improve mode performance further. 
1. Dataset limitation
- The current dataset is collected based on one map. We will add more kinds of maps' data in the next few weeks.
1. Better hyper-parameter turning tech.  
- The CNN hyper-parameter turning currently just focus on the number of layers, the number of epochs, will try more advanced techniques in the next few weeks.

**Limitation of real time image recognition and responses** 

1. Mainly concerns with computational demand of real-time image classification
2. Models are developed, trained and tested **only** **in the simulator environment** 
3. Abnormal driving behaviour is expected in case when false positives are reported 

**Further improvement** 

1. We will add more custom tracks, and continue to improve our sign detection models. 
2. We will implement a web-based leaderboard feature, and hold a virtual race soon. 
3. More usablity testings shall be conducted with unexperienced users. 

---

# Quality of Group Processes

## Setup of tooling for development 

**Bitbucket and Git**

Our team uses Atlassian Bitbucket for the collaboration and documentation of our project. This is the repository of our code base: [https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/)

![](https://lh4.googleusercontent.com/rrsVZYxhuMMZHf81sLklXyAbgrHwvLjZQPEdQsBfwp-IX85BCzvcLA23FNZFuqpe-lJxZ4A3QjDYjMQIq0yznawxNJaTByS0VtbKtj3Iz4kBDLtc5PwLCpp6LxGgK6qjITnDVk9J)

With Bitbucket, we can update our code and inform other team members as soon as we push our code onto the repository and they can see it by pulling it down to their local branch. We have two branches in the repository: master and simulator. The master branch mainly stores our updated code of sign detection and improved donkeycar model, and the simulator branch keeps the newest code for the donkeycar simulator with updated tracks built from Unity.

We use git to achieve a version control of our code. Git separates every different change made to the repository with a distinct commit object that represents a new change, such that we can distinguish which team member wrote which piece of code, and the effect of the change. Below is a part of our commit history:

![](https://lh6.googleusercontent.com/rNVEmua6xKdjKSPBUoD-6OvDjYx2-pz06Ikym-Q8moQmV4COzF_9LZfwOK14vPAOcHus7C2taTHQYdLKAhC9qzivH1AkEjvY80NCv7-0APO0rlFDFm_ZNs9EgWR5wotWAX6CD-4t)



**Bitbucket Wiki**

The wiki page of Bitbucket allows us to record and track any documentations we have regarding the project. Our group uses the wiki page to record our meeting minutes with the client and within our group, scope statement, useful links, status reports and our personal weekly update videos, **appendix J** is a snapshot of our homepage.



**Discord**

Discord is our main communication tool for the project, we use Discord to discuss anything related to the project (questions, thoughts, etc) within our group and with the client to ask for any clarifications regarding the deliverables of each week and sometimes for help on the implementation. Discord allows users to create their servers for communication and multiple channels can be used in one server, we are in the server: **Sydney2020** and our team channel for the project is: **cp32-17b1**, **appendix K** is a snapshot our daily communication. 


**Slack** (not used anymore)

We initially use Slack for communication amongst our team members, client and tutor, but our client prefers using Discord to communicate due to its convenience of communicating with multiple groups.


## Team Collaboration ##

- **Evidence of collaboration and teamwork - group roles and sharing of work, group contract, meeting minutes (team, client, tutor), project status reports**

    We adopt the extreme programming framework from agile development, that is, we define our scope statement  for the project first, which can be found on our wiki page: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Scope_Statement_overall
        **Appendix E** is a snapshot of what it looks like. 

    After that we elicit user stories for a more specific description of what the client expects our product to achieve, our user stories can be found in the system specifications part. 


- **Group roles and Documentations in XP**

- **Allocation of group roles, potential risks, constraints**

    Furthermore, we assign distinct XP roles to our team members such that each member does different jobs to make our development more fluent and maintainable. We signed a group contract to define these roles, it can be found on **appendix D**.
        
    Since our project is ML-oriented and does not fit to the traditional software development roles, we have the following XP roles in our team:
    - *manager: organises meetings and write the minutes, an example of our meeting minutes can be found in **appendix A**.
    - *tracker: track team progress and write status report, an example of the status report can be found in **appendix B**.
    - programmer: does the coding on sign detection, everyone in the group is programmer
    - tester: test the implementation code and provide feedback
    - doomsayer: provide warnings and advices on future issues/risks to group members
    - customer: represents the team to communicate with the client, due to the speciality of our project, everyone can directly asks the client their questions on Discord, however the customer role can still be adopted when communicating with the client on major events (e.g. meeting times) through email, an example can be found in **appendix C**.
        
    **role*: The critical roles that we rotate from week 2 to week 4 that we defined in our contract, we redefined our critical roles from week 5 onward, the manager and tracker are now fixed since some members are more familiar with some particular role:
    
    manager: Robert
    
    tracker: Hao
    
    Wiki maintainer: Yiran
    
    Since our wiki page determines our overall documentation style and therefore is critical when our supervisor (tutor) reviews it, we decided to add the wiki maintainer role to manage our wiki page to make it look more professional and organised.

- **collaboration and sharing of work**
    
    During Tuesday’s group meeting, our team separates the tasks to do for each week on different team members so that we can share the workload, **appendix F** shows the work separation of week 5’s tasks given by the client on Monday’s client meeting.
    
    Our team communicates and collaborates on Discord and occasional voice calls. During collaboration, we ask any questions and clarify them, and sometimes does pair programming, where one member shares their screen and do the programming, the other member watches and gives directions and clarifications. **Appendix G** describes some of our collaborations on Discord regarding discussions *(figure g.1)*, progress update *(figure g.2)*, issue identifying *(figure g.3)*.

## Client Interaction

We interact with client frequently on Discord to ask any related questions and clarifications, **appendix H** (*figure h.1 - figure h.3*) documents a few client interactions.
    
Other than direct communication on Discord, we also used emails to communicate with the client about the project initially, this can be found on appendix H *figure h.4*. We modified the scope statement he provided so that it fits the template, this can be found on **appendix E**.
    
We works closely with the clients by responding to client’s new requirements promptly. The client replies to our request for consultation and discuss our questions actively.

Overall, we believe we maintain a good interaction with the client.

## Critique 

- what has worked well and what needs to improve in terms of teamwork, group processes and XP terms
    - **Communication**
        
        Our team performed well in communication, both to fellow members using mainly Wechat and the client. Apart from discord (which is mainly used for client consultation and discussion), we communicate daily in our WeChat group chat to discuss any issues. 
        
        We hold video conference on Zoom meeting or voice call regularly to discuss issues that require collaboration or teamwork.
        
        Communication between group members always get fast responses and good solutions to issues.
        
        Overall, our communication has no major issues.


    - **Group process**

        Group members work closely together. Work loads are divided among members and each members do what they are most good at to achieve the best efficiency.
        
        When a member has other commitments in a week, his/her workload is reduced and shared among other members. We ensure everyone is having a workload that they are comfortable with.
    
    - **Progress update**

        As required by the client, we update our weekly progress with an individual weekly report page on wiki containing a summary video attached to it, each member updates their status frequently, this can be found on **appendix I**.
    
        The progress is also documented briefly in each week’s status report and submit to Canvas. We believe that our progress update is thorough and effective both to our supervisor (Canvas) and to the client (Bit Bucket)
    
    - **Agile practice**

        We can improve our work on adopting the XP framework. For example, we did not keep updating our user stories on Jira since we found it difficult to use. We haven’t kept the backlog items recorded in a weekly manner, instead we only focused on updating our wiki page since the meeting minutes contain what we should achieve for each week. Therefore we can improve our work on updating the user stories more frequently so that we don’t have to leave everything to the last minutes.


        We did well in terms of daily agile practice. We have meetings with the client on the first working day of the week to reflects on our progress from last week to the client. We also demonstrate deliverables (if any from last week) to the client. 
        
        On the last working day of a week, we have another meetings with the clients to discuss any difficulties we have during the week and report the plan for the weekend and the week to come.


        Our agile practice deserves both some compliments and some improvements in following weeks.

---

# Technical Documentation

[Link to our Wiki pages](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home) [document sections](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home) 

---

# Appendices 
## appendix A - meeting minutes
![meeting minutes for week 5 (can be found on our wiki)](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601678653515_Screen+Shot+2020-10-03+at+8.43.52+am.png)

## appendix B - status report
![status report for week 4 (can be found on canvas submission)](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601678763295_Screen+Shot+2020-10-03+at+8.45.46+am.png)

## appendix C - communication between customer and client
![our customer replying to our client on behalf of the team](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601679093943_Screen+Shot+2020-10-03+at+8.51.24+am.png)

## appendix D - group contract of roles
![our group contract of role rotations](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601682722363_Screenshot+from+2020-10-03+09-48-472x.png)

## appendix E - scope statement
![a snapshot of our scope statement](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601683240080_Screen+Shot+2020-10-03+at+9.55.49+am.png)

## appendix F - allocation of tasks
![our allocation of the tasks in week 5, given by the client on Monday’s client meeting](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601683672341_Screen+Shot+2020-10-03+at+10.07.45+am.png)

## appendix G - group discussions and collaborations
![figure g.1 - we discuss about the importance of accuracy in training results](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601684769703_Screen+Shot+2020-10-03+at+10.24.07+am.png)

![figure g.2 - we update our progress of our assigned tasks and inform others (donkeycar simulator with test signs added)](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601684980346_Screen+Shot+2020-10-03+at+10.29.26+am.png)

![figure g.3 - we identified some issues of the new track we built (different signs and colouring)](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601685314578_Screen+Shot+2020-10-03+at+10.35.00+am.png)

## appendix H - client interactions
![figure h.1 - we informed Cian with our progress and he described the next task we need to do (add custom signs to the simulator)](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601687530798_Screen+Shot+2020-10-03+at+11.12.05+am.png)

![figure h.2 - Cian answers all questions we had for the cancelled Friday meeting on week 5](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601687676133_Screen+Shot+2020-10-03+at+11.14.28+am.png)

![figure h.3 - Cian clarifies our questions regarding tensorflow versions in the donkeycar envirionment](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601687972663_Screen+Shot+2020-10-03+at+11.19.28+am.png)

![figure h.4 - Cian provided us with project scope and description via email](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601696667392_Screen+Shot+2020-10-03+at+1.44.07+pm.png)

## appendix I - example individual progress summary
![our group members kept their weekly progress updated on their own individual summary page](https://paper-attachments.dropbox.com/s_856DC0097927EC11C9A3D0A6C22C7A01531421EDE54128175E021A3817015A13_1601697829862_Screen+Shot+2020-10-03+at+2.03.33+pm.png)

## appendix J - wiki page layout
![this is what our wiki home page looks like](https://lh3.googleusercontent.com/LId9DMpNRD6Z_kFX_XOAudfWrKpFx1MYtVc_YAHW05ocwVbxfes0Ty9nfY_dWsmEjZc56EDdZxce2RVZ3MJdZN6GSorT2LmP9OEw9IFpOiWtHSHbb-wVh5enyMSKsThgXhop4Hor)

![we make every document a direct link on the home page s.t. they are easy to find](https://lh4.googleusercontent.com/5RkZWoZoZ4z8Wf91_NZ2i6AjiuZGWwECxv2Lk-ttD3Onuak204ttfQPydUCMvk0X7fERaRpQv4trSAnFimH7RSycPqkukxqzmkfZQsFGrZWJ4XxUvN4jQEHfFt-BP21ck5i9nm4O)

## appendix K - daily communication on Discord
![our daily communication](https://lh6.googleusercontent.com/xJAK1EohLzqx_zu7XpjFKyJCLZGRKV-44BWl0K1gVcwaJ0U4wpGd5NIFbnv6OJulpZPR1fk62DzbFeb1dG5d90WhXwXhxEOQ1x60Jgo_29c3VGgK9lz--RXpTj-TkfMQSWz550N5)

## appendix L - weekly individual‘s video demo

[weekly video demo wiki page link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Weekly%20Video%20Demo)

![weekly video demo](https://paper-attachments.dropbox.com/s_BE3187F6030E9EA61C4FAB7F9489553DC178709D6F1BDCF8F2A9EEC94B6002C7_1601703566853_54401601703203_.pic_hd.jpg width="100" height="100")

## appendix - Acceptance tests

**Run test case of CNN model**
Firstly, unzip test_data.zip within test-CNN folder, then run following code in terminal:
[the link of test-CNN folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/test/Test-CNN/ )

     $ cd Test-CNN
     $ python3 sign_detection_test.py

**Track physics** 

- **Test description**
    We will test whether the track we built responds to user input(via keyboard for driving)/object collision reasonably using the physics in Unity. To do this, we will divide the test into normal/abnormal test cases, where the normal test case looks at how accurate the donkey car responds to user inputs and manages to drive around the map. This will involve driving in a straight line turning and braking. In the abnormal case, we will intentionally drive the donkey car to hit the poles of traffic lights/signs, and walls to check the object collision. 
- **Test result** 
    The footage is [available here](https://youtu.be/h16BiZ5xd50) . The donkey car’s response to keyboard input is sound, it managed to drives in a straight line, turning and braking. Object collision is tested with all the traffic signs and traffic lights, most of the object collides as expected, except for the parking sign. 

**Self-driving test** 

- **Test description**
    To start experimenting with sign detection models, we need first build a simple autonomous vehicle in the simulator. We will test the performance of such vehicle by measuring the duration for which the donkey car can self-drive without hitting any obstacles. 
- **Test result**
    The footage is [available here](https://youtu.be/N-Cc1OrBDno). On average, the donkey car is able to drive without hitting obstacles for about 35 seconds. The best result we recorded is 1 minute and 31 seconds. 

**Real-time sign detection in simulator**

- **Test description** 
    Given the accuracy of the CNN model is tested, the next step in our plan is to test whether the model when fed into a data stream of camera images, is able to predict the label class in real-time. The input space can be partitioned into images containing [stop, left, right, park, no sign] signs. We will test whether these camera images are correctly classified, by printing the class label to the console in real-time.  
- **Test result** 
    The footage is [available here](https://youtu.be/-Ea1S9x55oQ). The test was successful, our model correctly classifies and prints out the class values (stop, left, right, park, other) to the console in real-time. 

**Donkey car response to the sign**

- **Test description**
    Donkey car should stop by reducing the throttle value, after a stop sign is detected. Similarly, the donkey car should turn left/right when a left/right sign is detected. This can be tested by running the image detection model and self-driving model at the same time in the custom map containing traffic signs. Then, we will print out the actual throttle and angle values received by the donkey car, and observe the behaviour of the donkey car.
- **Test result** 
    The footage is [available here](https://youtu.be/hWSs6zBgu_s), the terminal output is [available here](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/test/Driving%20and%20Sign%20detection/out)  We saw a decrease in throttle value below zero after a stop sign is detected, and observed the stopping behaviour of the donkey car. A positive (closer to 1.0) steering angle, and a small negative steering angle is outputted when right/left signs are detected respectively. Donkey car managed also to make the left/right turns.