# Table of Content
[TOC]

# Scope Outline

**Project Name: **CP31 - Implementing sign detection using Computer Vision  
**Project Period: **Semester 2 2020  
**Sponsor(s) or Client: **Cian Byrne  
**Organisation: **Robotics Masters  
**Project Supervisor: **Abdallah Lakhdari  

|Topic|Discussion|
|-|-|
|Background _Context of Project_|Cian and the employees at Robotics Masters have provided us with a work-in-progress signal detection codebase using OpenCV exclusively and we have been tasked to develop improvements and document these. Due to coronavirus the testing of these algorithms needs to be performed on a simulation which is to be on the donkey platform with modification made by our team.|
|Aim  _Purpose of the project_|To develop algorithms and associated testing environment for the implementation of automated car driving|
|Objective (SMART) _Goals of the project_ |The objective of the project is to develop improvements to the computer vision codebase to see a marked improvement within the modified/improved donkey simulator in signal detection consistency prior to delivery of the final product in Week 12.|
|Success Criteria _What does success look like and how can it be measured_|Success is a fully working simulation environment which reflects all required tracks in the desired ratio. Additionally, implementing all sign detection algorithms to a high level of accuracy and efficiency.|
|Deliverables  _List of outputs as part of the project include final product_|Fully implemented simulation environment; All signs modelled virtually; Signs, path and object detection using Computer Vision (OpenCV) exclusively.|
|Scope _The work that needs to be done to deliver or complete project_|A working algorithm that is able to detect a set of given signs from either live video or simulated feed via DonkeyGym using the OpenCV library only. Expansion of the simulator through the implementation of new tracks and sign assets. |
|Out Scope _Work not required to deliver as part of the project_|This included error fixing of DonkeyCar 4.0, since it was an experimental build, multiple issue appeared when using the new software. Improvement of simulator documentation.|
|Milestones _Key checkpoints_|**Milestone 1:** implementing 2 new tracks to simulator and adding appropriate objects **Milestone 2:** Improve and document quicker way to import new tracks, add in 2 more tracks through automatic generation and improve method of adding in objects - **Milestone 3:** Improve existing algorithmic solution, research and document improvements, demonstrate changes on sample data, add extra objects for detection - **Milestone 4:** All outlined signs detected and corresponding action response, demo on sample data and in simulator - **Milestone 5:** Demo of working solution in simulator, usage documentation, demo of working solution on real-world track, all deliverables completed and handed over.|
|Human Resources _Any specialist staff or subject experts that will participate_|N/A|
|Other Resources _Other resources used for the project including data and equipment_|Unity, Blender, OpenCV, Bitbucket, Sourcetree, Trello, Slack, Discord, academic resources surrounding colour morphology, computer vision testing data and map provided by client.|
|Reporting/Meeting frequency _How often will the team meeting and report to client_|Team meetings will occur twice a week (once during the tute and again on Thursday mornings), we will meet with the client twice a week on Monday and Friday afternoon. Updates will be given to our client through these meetings and other communications via email and discord.|

# User Stories

## End User

* I am an end user and I want an autonomous car to be able to recognise signs from a given database and perform a specific correlated action accordingly.
* I am an end user and would like to see real world tracks implemented in the simulator such as F1 tracks to test my car on more realistic tracks.
* I am an end user and would like the option of customising the vehicle I drive in the simulator.
* I am an end user and would like a model of a working traffic light in the simulator that replicates our real world light.

## Admin

* As a developer, I want to be able to test my detection algorithm by running the simulator, being able to return the results of the test and choose a variety of different test maps.
* I am a map developer and I want a given .png file to be implemented as a new track into the simulator with the correct scale.
* I am a developer and I want all the source files to have succinct documentation.
* I am a map developer with a list of traffic signs and I want to be able to place them in a given map in the simulator.
* I am a map developer and I want a F1 track implemented into the simulator with a 1:10 scale with correct elevation and width changes.

## Other Stakeholders

* As a car manufacturer, I want to be able to use this detection algorithm for use in automated cars
* I'm a DonkeyCar developer and would like the implemented code changes to be easily merged with current branches for each of integration
* I’m a DonkeyCar developer and would like the ability to modify the resolution of the camera used in real time.