# COMP5615 Group 2 Report: Implement Sign Detection using TensorFlow

Group Members:

- Aradhika Guha (490267956)
- Thomas Porcaro (309207274)
- Joko Wijaya (470317361)

Tutor: Adhish Panta

## Executive summary

*Project Title: Implement Sign Detection using TensorFlow*

Our system allows for a small vehicle to drive autonomously in a simulator and act upon visual detection of specific traffic signs. This is achieved using a machine learning (AI) solution, specifically a library called TensorFlow.

Acknowledgements go to Google for the development of TensorFlow, as well as a variety of contributors to a wealth of open source code that is leveraged in our solution.

## Introduction 

### Problem statement 

Our main project is to drive a car in a simulator autonomously and take necessary action when detecting traffic signs or lights in the simulator. The car will drive on its own and turn when it detects right/left turn signs, stop when it detects stop sign and act accordingly to other signs and traffic light.

### Description

The project extends an existing solution that has been built for donkey car, we have to extend the current solution by modifying the following:
1. Python donkey car module. Add code to the module so that it can integrate with the machine learning part.
2. Simulator (Unity). Create new tracks and add traffic signs and lights. 

On top of that we will also be inserting machine learning code into the self driving car so that it can recognize traffic signs and lights.

## Overview of System

Below are the user stories from the point of view of all users of the system (which includes completed and incomplete user stories):

- *Story 1*. As a user, I would like to be able to drive around track1 and track2 in the simulator. If it is possible please ensure track 2 is 7.0 metres by 10.0 metres and track 1 is 15 metres by 9 metres in the simulator. (see appendix A)
- *Story 2*. As a user, I would like to be able to see signs such as stop signs inside the simulator and it has been of a certain size. (see appendix B)
- *Story 3*. As a user, I would like to be able to see traffic lights inside the simulator.
- *Story 4*. As a user, I would like to be able to drive automatically around the circuit with AI
- *Story 5*. As a user, I would like to be able to have a system where the car (AI enabled) can detect traffic signs/ lights and do necessary action whenever it detects the sign/light.
- *Story 6*. As a user, I would like to have the documentation about how to add track and asset into the simulator.

## Evaluation

### Overview

As with the nature of the project, it is hard to design the acceptance test with techniques such as equivalence partitioning and boundary analysis as most the test is done by eyeballing.

Below is the set of of acceptance test for each user story:

| User Story No. | Acceptance Test |
|----------------|-----------------|
| User story \#1  | \#1 Able to drive around track1 and track2 in the simulator |
| User story \#1  | \#2 Can see that the size of the track1 and track2 is as indicated in the requirement |
| User story \#2  | \#3 Can see the signs implemented in the simulator (in this case they are stop, right, left and parking signs) |
| User story \#3 | \#4 Can see that the traffic light is inserted into the simulator and it changes colour between red, yellow and green. |
| User story \#4 | \#5 Can see that the car is driven around the circuit by AI and circle around the circuit multiple time |
| User story \#5 | \#6 Can see that the car is driven around the circuit by AI and can detect signs and traffic lights and do necessary action whenever it detects the sign/light. |
| User story \#6 | \#7 Documentation on how to add tracks and assets into the simulator should be present on the wiki |

### Details of Tests 

| Acceptance Test \# |Type | Test |
|--------------------|-----|------|
| \#1 Able to drive around track1 and track2 in the simulator | Normal | Start simulator and drive around track1 and track2 and see if it can be driven at as expected |
| \#2 Can see that the size of the track1 and track2 is as indicated in the requirement | Normal | Check the size of the track according to the size of the donkey car |
| \#3 Can see the signs implemented in the simulator (in this case they are stop, right, left and parking signs) | Normal | Check if the signs is implemented correctly and the sign can be seen in the simulator and it is clear |
| \#4 Can see that the traffic light is inserted into the simulator and it changes colour between red, yellow and green. | Normal | Check if the traffic light is implemented correctly and the traffic light can be seen in the simulator and it is clear. Also check if it can switch colour between red, yellow and green
| \#5 Can see that the car is driven around the circuit by AI and circle around the circuit multiple time | Normal | Start the car using python code and see if the car is driven around by the AI
| \#6 Can see that the car is driven around the circuit by AI and can detect signs and traffic lights and do necessary action whenever it detects the sign/light. | Normal | Start the car using python code and see if the car is driven around by the AI and take necessary action when it see signs and traffic light |
| \#7 Can see that documentation about how to add track and asset into the simulator in wiki | Normal | Check if the documentation is as expected |

#### Usability Testing

The usability testing for this project are:
1. Able to start the code easily and the code can be understood easily, this is achieved by good structure of code and follow coding guideline
2. Signs and traffic lights are placed correctly on the track and can be seen easily while driving around the track.
3. Documentation can be read and understood easily by asking the end user to give a score for the documentation.
4. Image classification is easily comprehensible and run.

### Conclusions 

We have been able to successfully import tracks and signs into the simulator.

The tests demonstrate the system is working as expected. As most of the test is done by eyeballing, it is hard to set a standard but if it is confirmed by the end user then it should be good enough to function.

The limitations of the system is that accuracy may not be 100% (it is around 85% with 20 epochs)  because of the nature of machine learning. Detecting signs and traffic lights using machine learning may not result in 100% accuracy therefore it may need to be accompanied by other type object recognition algorithms such as computer vision but since this project only focused on machine learning, it may be hard to achieve the expected result.

Overall, by keeping the number of epochs to 20 and batch size to 32 , we are able to achieve an accuracy of around 85% which is considered a very good result for stop sign detection. Our algorithm is able to accurately detect stop signs and we are able to save this training model successfully.

Currently we have used the sigmoid activation function for binary classification (stop sign or not). We have extended this by using softmax activation for multiclass classification to be able to detect various types of signs.

## System structure overview 

The systems used for this project can be divided into three subsystems:

### 1. Python donkey car module 

DonkeyCar is being used by us as a client to connect to the Unity simulator. Once DonkeyCar is installed in a Python environment (we are using Anaconda) it is used to create a “car”, which is essentially a directory with some code to run the client. The two main CLI functionalities in the “car” directory are “drive” and “train”. “Drive” connects the client to a running simulator/server instance. Once connected, we are able to drive the car around virtually by connecting to a web server that is run. The driving is controlled in a browser. When we drive, we are able to capture images from the camera, and other data which are stored in a data directory called a “tub” (the data store). The tubs can then be used by the “train” command, to train a neural network to drive around the track autonomously. Once we have a trained neural network, we can use the “drive” command again, specifying a saved model file, and the car will drive around the track automatically.

The vehicle executes a series of “parts” with a certain specified frequency. A “part” can take input from the environment in which the car is driving, and act based on it. Parts are executed in a perpetual loop. For example, we have implemented a “StopPart” that takes in camera image information, checks if a sign is recognised in the image, and performs the “stop” action accordingly (i.e. it kills the car’s throttle).

For the most part, our work involves making a part/parts in which an image can be checked with a trained TensorFlow model and an action taken. During initialisation in the “drive” method of manage.py we add our part, providing it with a path to the trained model from the configuration file. This path is used to load the saved model, and the saved model is then used by a “TfDetect” object which is stored as a field on the StopPart which is added to the parts of the car. As we continue development, this StopPart will either become one of many parts (e.g. we will want a “TrafficLightPart” and a “TurnSignPart”) or we may consolidate all of the functionality into a single “SignDetectionPart” which will be able to detect signs and act accordingly. A more detailed depiction of the DonkeyCar architecture is present in the figure below.

![DonkeyCar module architecture](https://bitbucket.org/aradhikaguha/comp5615-group-2/downloads/1.png "DonkeyCar module architecture")

### 2. Simulator running on unity

This is the environment where the car is in and it is built using unity software. There is a TCP server built in the simulator so that the car can be controlled by TCP connection. The environment is 3D, assets and objects are inserted into the 3D environment. The architecture diagram of the simulator would be:

![Unity simulator architecture](https://bitbucket.org/aradhikaguha/comp5615-group-2/downloads/2.png "Unity simulator architecture")

The simulator consists of 
1. 3D environment and 3D assets
2. It is controlled by code inside the simulator such as camera and control
3. It also has built in TCP server that passes control action to controller

### 3. Machine learning (Tensorflow) code that detects sign and traffic light

This is the TensorFlow part that can detect sign and traffic light in the simulator. The TensorFlow code decodes an image array into classes (or types) of objects. Python donkey car module will pass the image array to the TensorFlow code and it is the job of the TensorFlow to decode the image array. Below is the information flow of the TensorFlow code:

![TensorFlow information flow](https://bitbucket.org/aradhikaguha/comp5615-group-2/downloads/3.png "TensorFlow information flow")

## Tools used to build system

To build the system, there are a variety of tools that are being used. Broadly speaking, the tools can be separated into management/collaboration tools, and technical/software tools.

*Management/collaboration*
- *Slack/Discord/Whatsapp*. These tools are used for messaging each other. Quick/trivial communication is done on WhatsApp, with more substantial correspondence done on Slack. Slack is built with software development in mind, and so is easier to manage and use if we wish to search through chat logs or share files. Discord is also being used for  a similar purpose, but less extensively.
- *BitBucket/Git/GitHub*. Git is a version control system. Git allows us to save “snapshots” of our development history, allowing us to make changes and retain a history of the codebase’s development. Git also allows for team collaboration. We have our main code code repository on BitBucket, providing a “remote” where team members can push code to and share. BitBucket also has other features that help with collaboration, particularly a “wiki” which we are using to write documentation and share other information. GitHub is being used for a similar purpose, but mostly just for retrieving relevant coebases for use in our project.
- *Incidental/common (email, Google Drive/docs)*. Email is being used sparingly for correspondence, particularly with the university. Google Drive/Docs are being used to share some large files, and for collaboration on writing documents (a draft for this report, for example).

*Technical/software*
- *Language*: Python 3. DonkeyCar is largely written using Python, and so most of the work we are doing is with Python. As a high-level interpreted “scripting” language, Python allows for rapid development and testing. Python is also extremely feature rich, with a lot of modern conveniences (lambdas, OOP, package management) and a variety of useful standard libraries. Additionally, TensorFlow has a Python client library that we are able to easily integrate into our codebase as necessary.
- *Unity*. Unity is being used for simulation. Unity is a versatile 3D modelling framework which is often used for developing computer games. In our case we are using Unity to extend the codebase for a driving simulator. Using Unity we are able to place virtual signs on a virtual track which we can drive a car around on. This is useful for rapid development, since we do not have access to a physical car to test with.
- *Anaconda*. Anaconda is a Python distribution. It assists with package management and easy set-up of an environment for developing our Python code.
- *Incidental/common (Linux/Windows/MacOS, light-weight text editors)*. We are using a variety of operating systems and code editors. Since our solution is cross platform, this introduces only minor issues that are easily managed.

*Library*
TensorFlow 2.3.0 (Open source). TensorFlow is a machine learning library. We are using it to train models for image recognition. The cars that we are driving around the tracks have a mounted camera that read in images. Images are passed to a trained TensorFlow model, the model examines the images as they come in, and we can make the car act as according to the sign that is recognised.

## Information search

The information search can be divided into three categories:

### 1. Python donkey car module

We are fortunate that DonkeyCar comes with a good amount of useful documentation at docs.donkeycar.com. The documentation outlines how to install the relevant DonkeyCar libraries into a Python virtual environment, how to create a “car” directory, and how to connect the car to a running Unity simulator using manage.py. The system cycles through “parts” that are added to the car during initialisation, each part able to control the behaviour of the car (throttle, angle, etc.). Parts can be passed a variety of data related to the running of the car (for example the current throttle value and images from the camera). We can then operate on the input data, and modify the behaviour of the car as we wish.

### 2. Simulator running on Unity

Below are the resources about the simulator and how research are done on each resources:
- Main github of the simulator (https://github.com/tawnkramer/sdsandbox)
This github provides the unity project that we can open and play on unity software. There is a readme on this github that provides helpful tips.
- Learning unity (https://unity.com/learn/get-started)
It is crucial to learn unity first before tinkering with the simulator, therefore we started by using unity get started tutorial, after understanding unity better then we import the project from the main github. While learning unity, it is also helpful to watch youtube videos for more details on how to accomplish certain tasks.
- Learning 3D asset creator using Blender (https://www.blender.org/support/tutorials/)
After learning unity, client would like some assets created and this is created by using Blender. By following tutorials, the assets have been able to be created and imported into unity.

### 3. Machine learning
Machine learning code that detects sign and traffic light using image classification based on convolution neural networks. We use TensorFlow open source library for this purpose.

## Group Reflections and Conclusions

### Group Reflection
The group has been functioning well, the XP roles are divided based on the character and personality of each team member and this has worked out well. The team has been able to move forward and complete tasks. Each team member is also comfortable with the roles that they have been assigned with.

The tasks are divided among the group depending on the experience and speciality of each team member. There are three of us and the task are mainly divided into:
1. Python donkey car module
2. Unity (Simulator)
3. Machine learning

This also worked out well, as each team member was able to tackle problems quickly and integrate their work.

The process found to be effective because the team is functioning and able to produce results.

One of the problems is to integrate machine learning code for image classification with the donkey car module and it is consuming a lot of time. The team member is unable to produce code to integrate with the donkey car module therefore the other team member needs to find the way and it is consuming a lot of time. This could be caused by a lack of experience of team members and it is a problem that is hard to avoid. This probably can further be improved by assigning multiple parallel tasks for each team member instead of one team member taking the whole subject field.

### Conclusion

The project will allow a small vehicle to drive autonomously in a simulator and act upon visual detection of specific traffic signs. The scope has been well defined by the client and the team has been able to produce results that the client needed. The architecture of the system has been well defined and understood by the team members. The information search for this project has been successful and a solution has been built.  The team has been functioning well under the XP methods with minor problems. 

## Individual Contributions

### Thomas

The main XP roles Thomas has filled have been developer, coach and tester. Thomas is relatively experienced in some aspects of this project (particularly in the use of Git and Python), and has therefore been able to develop code and assist others in their development.

Contributions:
- Initial import of a track into the simulator.
- Resolving technical issues around the use of BitBucket/git. This has proven to consume a lot of time, but has been useful in pushing us forward.
= Implementation of the StopPart and code for use of the TensorFlow model developed by Aradhika.
- Cleanup of TensorFlow training code so it can be run more easily. There were quite a few issues in running TensorFlow code on Aradhika’s machine. Thomas assisted greatly in setting things up so they could be run more easily.
- Documentation. Thomas has been largely responsible for writing the meeting minutes documentation.

### Joko

Main XP roles assigned for these few weeks:
1. Tracker: Organise document and put it on wiki
2. Programmer: Mainly working on the simulator: changing code, create assets, create tracks and export binary for the team to use
3. Tester: Testing simulator and asset objects and see if it looks and behaves as expected.

Contributions
- Import simulator to unity (https://github.com/tawnkramer/sdsandbox)
- Import track1 and track2 into the simulator (appendix C) (evidence: branch joko and trafficLight) 
- Create assets in 3d assets in unity (Issues #3)
- Create documentation on how to add track (Issues #1)
- Create documentation on how to create assets (Issues #2)
- Make simulator has menu(Issues #4)
- Make simulator startable (Issues #5)

### Aradhika
I have performed the following XP roles.

- **XP Programmer**:  I have estimated user stories and implemented the same in the form of tasks using python coding in Anaconda. I have implemented traffic light detection using LARA dataset and image classification using tensorflow 2.3.0.
- **XP Tracker**: Throughout the duration of the project , I have been responsible for setting up meeting with clients and keeping a track of project status and progress.
- **Doomsayer**: I have played the role of a doomsayer at times when I predicted the risk of decreasing epoch number and increasing batch size. While that significantly improved training speed , the accuracy was sacrificed in the process.
- **XP Manager**: For certain weeks I have served as the manager by reporting progress to the client/customer , setting up meetings with them and discussing releases.

I have also served as the document controller. The responsibilities involved constantly updating wiki with issues and their status(open or resolved) , updating wiki with project status on a weekly basis , updating user stories , adding necessary documentation for image classification , adding video reports , etc.
Throughout the process , I was the first point of contact with the client and responsible for setting up weekly meetings with the team and client on a regular basis.

#### Contributions

1. Written code for traffic light detection using tensorflow using LARA dataset
2. Written code for image classification for stop sign detection using Convolution Neural Network
3. I have also served as the document controller. The responsibilities involved constantly updating wiki with issues and their status(open or resolved) , updating wiki with project status on a weekly basis , updating user stories , adding video reports , etc.
4. I have also added documentation for image classification using tensorflow
5. I have added multiple user stories in wiki
6. I have regularly updated wiki with project status report on a weekly basis.
7. I have created multiple issue and currently they have all been resolved by me
8. Also I have performed code refactoring by simplifying the design through data augmentation and maxpooling. Data overfitting has been decreased by data augmentation.

## References

1. savyakholda, CNN | Introduction to Pooling Layer, Geeks for Geeks, 26th of August 2019. Accessed on 3rd of October 2020 [Online]. Available: https://www.geeksforgeeks.org/cnn-introduction-to-pooling-layer/
2. Shane Drumm, Extreme Programming for Beginners Made Easy - Roles and Practices. Accessed on 3rd of October 2020 [Online]. Available: https://pm-training.net/extreme-programming-beginners/

## Appendices

### A. Track images

![Track 1](https://bitbucket.org/aradhikaguha/comp5615-group-2/downloads/4.png "Track 1")
![Track 2](https://bitbucket.org/aradhikaguha/comp5615-group-2/downloads/5.png "Track 2")

### B. Traffic Sign Images

![Traffic Signs](https://bitbucket.org/aradhikaguha/comp5615-group-2/downloads/6.png "Traffic signs")

### B. Simulator Screenshots

![Driving on Track1 screenshot with parking sign](https://bitbucket.org/aradhikaguha/comp5615-group-2/downloads/7.png "Driving on Track1 screenshot with parking sign")
![Driving on Track1 screenshot with turning right sign](https://bitbucket.org/aradhikaguha/comp5615-group-2/downloads/8.png "Driving on Track1 screenshot with turning right sign")