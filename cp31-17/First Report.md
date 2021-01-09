# **COMP3888 First Report Group 5 T17A**

Team: Patrick Delaney, Winson Chen, Jordan Koukides,

Kevin Wong, Joseph Pham, Julian Jee

Tutor: Abdallah Lakhdari

Date: 4th October 2020

# Executive summary

Project Title: Implementing Sign Detection using Computer Vision

Members: Patrick Delaney, Winson Chen, Jordan Koukides, Kevin Wong, Joseph Pham, Julian Jee

The aim of this project is to implement effective sign, path and object detection algorithms for self-driving cars by solely relying on the OpenCV library. The algorithms will be tested using data collected from DonkeySim, a virtual car simulation environment. A robust system of tracks, models and scenarios will also be implemented into the simulator to achieve thorough testing of our algorithm, indicative of the real world testing environment.

## Table of Contents

[TOC]

# 1 Introduction

## **1.1 Overall objective**

Our group was tasked with the implementation and improvement of computer vision object and sign detection in a simulated environment. Additionally, our team will also improve the Unity-based simulator and, along it, our understanding of Unity.

## **1.2 What will the project achieve**

The project aims to improve on an already established codebase and algorithms aimed at detecting road signs whilst providing Robotics Masters with a long term solution for customizing simulation environments for testing purposes; especially during this pandemic. Utilising OpenCV as our computer vision model and Unity as the engine for modelling re-creations of real-world driving environments, we will use DonkeyCar Simulator as a virtual environment in which to test and train our sign detection algorithm. Ultimately, this project will solve sign and path detection challenges faced by stakeholders in both the DonkeyCar and OpenCV community, as well as provide a basic computer-vision-based sign detection algorithm for use in autonomous vehicles.

## **1.3 Stakeholders**

The primary stakeholders of this project are Robotics Masters (the client), as well as the DonkeyCar, OpenCV and autonomous vehicle communities. Cian Byrne, the co-founder and lead developer of Robotics Masters, is acting as our main point of contact for this project; as well as setting sprint goals and monitoring progress in our bi-weekly meetings, Cian is also the stakeholder that we turn to for any project specific questions. Alongside being beneficial to Robotics Masters and their clients, our project is also designed to make progress on many of the issues faced by both the DonkeyCar and OpenCV communities, many of which revolve around difficulties in sign and path detection when machine learning techniques are not an option. As of halfway through this semester, our early progress videos have already been shared with the DonkeyCar Discord community, inviting their feedback and answering any questions posed by them about our algorithm. By design, we aim that our final deliverable will also be beneficial to these stakeholder communities.

## **1.4 Tools and Resources**

Unity: [https://unity.com/](https://unity.com/)
 Donkey Car: [https://github.com/autorope/DonkeyCar](https://github.com/autorope/DonkeyCar)

Donkey Gym Simulator (Unity): [https://github.com/tawnkramer/sdsandbox](https://github.com/tawnkramer/sdsandbox)

Initial OpenCV detection algorithm: Provided by client

Blender: [https://www.blender.org/](https://www.blender.org/)

Slack: [https://slack.com/](https://slack.com/)

Discord: [http://discord.com/](http://discord.com/)

Zoom: [http://zoom.us/](http://zoom.us/)

Google Drive/Docs: [http://docs.google.com](http://docs.google.com/) and [http://drive.google.com](http://drive.google.com/)

Bitbucket and SourceTree: [http://bitbucket.org/](http://bitbucket.org/) and [https://www.sourcetreeapp.com/](https://www.sourcetreeapp.com/)

Trello: [http://trello.com/](http://trello.com/)

## **1.5 Associated Risks**

### **1.5.1 Performance risk**

Based on the current research in computer based object detection, sign detection models without the use of machine learning are unreliable; ranging from 65% to 35% detection rates at 10% precision (Houben et. al., 2013). Thus it is a concern of the team that improvements we make to the detection algorithm are minimal, if any, due to the constraint of solely using computer vision techniques.Future performances can occur if the simulator does not imitate the real world well enough the algorithm could possibly fail to detect the signs in real-life.

### **1.5.2 Schedule risk**

As of the publication of this report, we have finished the current milestones on time. But, if any of thefuture milestones are not completed on time, we risk a compounding effect on every subsequent milestone, leading to a project which is either completed later than the original deadline or complete on-time but short of scope requirements.

### **1.5.3 Dependency risk**

Sign detection algorithm production and implementation cannot begin without the creation of Unity assets first. The use of the simulation environment is paramount to ensuring a high quality testing environment for the computer vision algorithm. Therefore, the completion of certain modules needs to be completed prior to moving onto future milestones and project requirements.

# **2 User stories**

## **2.1 User**

- I am an end user and I want an autonomous car to be able to recognise signs from a given database and perform a specific correlated action accordingly.

## **2.2 Admin**

- As a developer, I want to be able to test my detection algorithm by running the simulator, being able to return the results of the test and choose a variety of different test maps.
- I am a map developer and I want a given .png file to be implemented as a new track into the simulator with the correct scale.
- I am a developer and I want all the source files to have succinct documentation.
- I am a map developer with a list of traffic signs and I want to be able to place them in a given map in the simulator.

## **2.3 Other stakeholders**

- As a car manufacturer, I want to be able to use this detection algorithm for use in automated cars

# **3 Evaluation**

## **3.1 Overview of requirements**

| **Requirements** | **Acceptance test** |
| --- | --- |
| Map Implementation | Check simulator for working custom map |
| Sign Detection | Still image test\* |
| Sign Response | Unity unit testing |
| Documentation | Understable and detailed |

\* Still image test is compared to original code for evaluation of performance

## **3.2 Details of tests**

| **Acceptance test** | **Details** | **Test type (normal/boundary/abnormal)** |
| --- | --- | --- |
| Still image test | Test with high contrast between sign and background | Normal |
|| Test with low contrast between sign and background | Boundary |
|| Test with signs of shared features (e.g. red stop light and red stop sign) | Normal |
|| Test with ambiguous lighting | Abnormal |
| Unity unit testing Sign Response | Single sign, pass if vehicle has correct response to all signs | Normal |
|| Chain of sign, pass if vehicle has correct response to all signs | Normal |

## **3.3 Conclusion**

_what the tests demonstrate, their limitations and the_

_Limitations of the system_

Our tests firstly have been created to demonstrate the ability of our code to detect a variety of signs individually, performed with different conditions such as viewing angles, colour and lighting conditions to simulate how real vehicles can approach traffic signs in a variety of ways.

While test cases in the simulator offer more flexible ways of testing signs compared to real-life, it cannot account for the vast number of different signs present in the real world as well as the myriad of road conditions.

# **4 System structure overview**

![System structure.png](https://bitbucket.org/repo/48xyAqR/images/3583613547-System%20structure.png)

Our project focuses on making improvements to DonkeySim, a Unity based testing environment for DonkeyCar. Assets are created in the modelling software Blender and imported to Unity, where they can be placed accordingly in existing or new maps in the simulator.

With new assets/maps added, the simulator can be built and run as an executable. A virtual DonkeyCar can be placed in the simulator to be controlled by an autopilot driver to collect video data. This data will be processed in real-time by our OpenCV algorithms and sends an appropriate action back to the autopilot upon detecting a given object.

# **5 Tools used to build system**

| **Tool used** | **Why?** |
| --- | --- |
| Bitbucket | Bitbucket has high levels of integration with other project management software such as Trello and Sourcetree. It is very useful as it allows for the documentation of changes and allows for easier collaboration. |
| DonkeySim | A simulation environment for the donkey car platform that was the code base for our customized simulation environment. |
| Anaconda | A good tool for managing separate environments and packages that are necessary for the completion of the project. |
| Trello | Project management software depicting a signboard for easier issue and feature tracking of projects with higher numbers of people. |
| OpenCV | Is a Python library that allows for real-time computer vision to be able to notice traffic lights and signs so that it can perform the corresponding actions. |
| Python | Python was used for the majority of the simulation codebase as well as the sign detection and response algorithms, these were based in the Python module OpenCV. |
| C# | C# is the primary language that Unity is built upon and when developing certain assets (such as the traffic lights) which require additional functionality (changing the traffic lights). |

# **6 Information search**

The research you did into tools e.g. software and it's report/evaluations, literature

**Jira or Trello**

In terms of issue tracking, we selected Trello over Jira. This decision was made using a cost-benefit analysis. Jira had many attractive features for issue tracking, however, the integration into BitBucket had encountered too many issues relative to Trello's rather simple integration. The features offered by Jira over Trello did not provide too much benefit as our project scope was restricted enough to not require such a complex system.

**OpenCV: Sign detection algorithm**

We researched different methods of sign detection via a paper provided by the client and using reference chaining methods. We found that most methods required some sort of machine learning which we cannot use(Houben et al. 2013). One of the methods, however, does not use machine learning and performs better than the initial algorithm, but it still performs worse than the machine learning algorithm. As it performs better than what we currently have, one possible improvement we can make is to integrate the methods used in the paper. However, a limitation of implementation is the current OpenCV library capabilities. The OpenCV documentation and the associated tutorial was referenced and consulted on regularly for the understanding and implementation of functions.

**Blender and Unity Tutorials**

Since this was our first time using both Blender and Unity, YouTube was used as a starting point to learn the basics for things such as creating textures, making models, scaling images, adding collisions and basic scripting. If we ever got stuck on how to do something we would look at the Donkey Car discord for help.

**Donkey**** Platform Tutorials**

A majority of our Unity based simulator works off the open-source community project; Donkey. This community project provides a large amount of documentation with respect to setting up the simulator environment in its default settings.

**RmRacer Documentation**

RmRacer is a python module which enables the running of python scripts (OpenCV detection code) within the Donkey simulation environment

# **7 Group reflection and conclusions**

## **7.1 Challenges/risk analysis**

- Self-learning OpenCV and computer vision basics was quite a challenge, as none of our team members had done any work in this field before.
- Many team members had to re-familiarise themselves with Python, however this was not a significant challenge and was completed in our own time
- Team collaboration in a completely virtual environment. Initially, we found ourselves communicating through too many different collaboration tools (email, Slack, BitBucket, Trello, Messenger and Discord). However, as we found our rhythm as a team, we were able to reduce this list to just Discord, Slack and BitBucket. This change improved our productivity greatly, as it reduced the chances for a team member to miss a notification on one of the platforms and ensured that we weren't all working on the same thing at the same time.
- Different operating systems. 50% of our team operated on Windows and 50% on Mac OS. For some applications, this created functionality issues across platforms, particularly when running Donkey Car or OpenCV code. However by working in sub-teams based on OS, we were able to overcome this.

## **7.2 Functional limitations**

- Self-driving functionality is limited as we are not using AI or TensorFlow, but this was by design for this project.

## **7.3 Structure, design and implementation limitations**

- As the majority of test cases will be run in a simulation, the detection algorithms will not have to deal with the vast amount of various conditions present in real-world scenarios such as reflection, variations or partial obstruction of signs.

## **7.4 Primary strengths**

- Once issues communication channels were ironed out, we had excellent communication as a team, and updated each other on individual progress almost every day via Discord
- We did not exceed any client deadlines in terms of mini weekly-sprints
- From the start, we successfully identified the main components of the project, and delegated these amongst the team to improve efficiency. In the first sprint, the main areas of focus were OpenCV code, Unity implementation, and Blender design.

## **7.5 Programming practices**

### **7.5.1 Extreme programming**

- We consistently released the smallest useful feature set as seen when we released each sign asset as they are completed and uploaded improvements to the detection code after each coding session.
- Basic tests were created early on for the detection algorithm, however this occurred after the feature was created as a prototype of features was provided by the client.
- Pair programming was a helpful tool during the majority of the Unity and Blender creation. Knowledge between the pair was corroborated and improved both of our understanding of the programs.
- We all took collective code ownership of the code, any errors did not lead to the assignment to any blame and everyone was responsible for the creation of the fix/
- We had continuous communication with the client with meetings two times a week and regular updates on instant messaging platforms.
- We also assigned roles to each of our members (all members fell into the programmer role):

| Member | Roles | XP Roles |
| --- | --- | --- |
| Joseph Pham | Unity Expert | Week 4 Tracker; Doomsayer; Software Engineer; Tester |
| Winson Chen | Slack Expert | Week 2 Tracker, later Permanent; Doomsayer; Software Engineer; Tester |
| Julian Jee | Blender Expert | Week 4 Manager, later Permanent; Doomsayer; Software Engineer; Tester |
| Jordan Koukides | Bitbucket Expert | Week 3 Tracker; Doomsayer; Software Engineer; Tester |
| Patrick Delaney | Client Relations | Week 2 Manager; Permanent Customer; Doomsayer; Software Engineer; Tester |
| Kevin Wong | Wiki Expert | Week 3 Manager, International Relations |

### **7.5.2 Version control, issue tracking and coding style**

- Version control was successfully handled using Git through BitBucket
- Issues were tracked using Trello, which was integrated into BitBucket. Milestones and potential issues were discussed in team meetings or via Discord, which were then recorded into the minutes in the BitBucket wiki, and subsequently converted into Trello issues.
- Also everyone had a slightly different coding style, including our client, we successfully managed this through the use of branches in BitBucket. When a team member was experimenting with a new solution to an issue or milestone, they would branch this as to not impact the master code if the solution was found not to work; this also alleviated issues in conflicting coding styles.

### **7.5.3 Group aspects, product and processes**

- A significant portion of the allocation of tasks was done through a Trello board in which each member would assign themselves to tasks dependent upon their preferences and expertise.
- Our group had weekly meetings in-team, with the client as well as with the tutor in which we updated the appropriate people on our progress.
- There were numerous communication mediums used throughout the process including the use of formal emails between clients as well as discord and slack instant messaging for less formal matters.

# **8 Individual reports**

For our project, the group work was first split between making improvements to the client's detection algorithms in OpenCV and improvements to the simulator. Individual reports are located [here](First Individual Reports/Landing).

| Task | Completed by: |
| --- | --- |
| Modelling traffic signs in DonkeySim | Julian, Joseph |
| Implementation of client's maps into DonkeySim | Joseph |
| Documentation of map and sign implementation | Joseph |
| Script to cycle traffic light colours | Julian |
| Implementation of RMRacerLib | Patrick |
| Research sign detection methods | Winson |
| Stop sign detection | Winson, Jordan |
| Turn sign detection | Winson, Jordan, Kevin |
| Park sign detection | Patrick |
| Traffic light detection | Winson, Patrick |
| Unit tests for detection algorithm | Winson, Jordan, Kevin |
| Report | Everyone |
| Weekly Minutes | Everyone |
| Weekly Updates | Everyone |
| Presentation | Everyone |
| Demo | Everyone |

# Appendix

**Bitbucket Repository**

[https://bitbucket.org/comp3888-t17a/comp3888\_t17a\_group5/src/master/](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/src/master/)

**Individual Reports**

[https://bitbucket.org/comp3888-t17a/comp3888\_t17a\_group5/wiki/First%20Individual%20Reports/Landing](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/First%20Individual%20Reports/Landing)

**Installation of Software**

[https://bitbucket.org/comp3888-t17a/comp3888\_t17a\_group5/wiki/Installation%20of%20Software](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Installation%20of%20Software)

# **References**

Houben, S. (2011, June). A single target voting scheme for traffic sign detection. In _2011 IEEE Intelligent Vehicles Symposium (IV)_ (pp. 124-129). IEEE.

Houben, S., Stallkamp, J., Salmen, J., Schlipsing, M., &amp; Igel, C. (2013, August). Detection of traffic signs in real-world images: The German Traffic Sign Detection Benchmark. In _The 2013 international joint conference on neural networks (IJCNN)_ (pp. 1-8). IEEE.