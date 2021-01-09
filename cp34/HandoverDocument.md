# Client Handover Document
## CP34 - Optimal Path for Drone Delivery
**COMP3888_T15A_Group1**

## Project Description

This project assumes we are flying drones at high and low altitudes. At high altitudes, the drone is expected to be constantly calculating battery level, nearest charging station and distance to destination. The final goal of the project is to allow a fleet of drones to deliver any number of parcels to destinations in the most optimal way autonomously.

A key component for simulation is modelling the battery life, weather conditions and accurate distances. This project is not too concerned about object detection but focused on the algorithms for path finding. Collision Avoidance between drones and buildings should be considered.

---
## Documents

[Requirements Document](https://github.com/wallarug/capstone2020/raw/master/requirements/CP34%20-%20Scope%20and%20Requirements%20Document%20September%202020.pdf).

## Code & Respository
[BitBucket Repository Link](https://bitbucket.org/DylDupe/comp3888_t15a_group1/src/master/).

There is only 1 branch, the master branch.

---
## Team Members & Tasks

| Name | Primary Email | Core Role(s) Tasks |
|--|--|--|
| Dylan Duplessis | ddup5819@uni.sydney.edu.au | World Rendering and Object Creation |
| Justin Lee | jlee2180@uni.sydney.edu.au | Drone Navigation |
| Nicholas Hui | shui3677@uni.sydney.edu.au | Document Controller and Tester |
| Ivan Xu | yuxu6642@uni.sydney.edu.au | Weather Implementation |
| Jimmy Liu | dliu2530@uni.sydney.edu.au | Algorithm Implementation and Testing |
| William Wu | xiwu9085@uni.sydney.edu.au | Algorithm Design |

## Video Summaries

### Weekly Updates

Weekly Update Videos can be seen [here](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Videos).

### Major Milestones

Demonstration Videos can be seen [here](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Demos).

---
## Documentation

Link to the README file with links to all the documentation can be found [here](https://bitbucket.org/DylDupe/comp3888_t15a_group1/src/master/Docs/).

| Specific Documents |
| -- |
| [Deploying \ Environment Setup AND running the solution](https://bitbucket.org/DylDupe/comp3888_t15a_group1/src/master/) |
| [World Rendering and Object Creation](https://bitbucket.org/DylDupe/comp3888_t15a_group1/src/master/worlds/) |

---
## Goals & Deliverables

| Deliverable | Achieved |
| -- | -- |
| Install and Configure Gazebo Simulator Tools with ArduPilot | Completed |
| Model charging station as a marker (landing zone) in Gazebo simulator | Completed |
| Show how to control the drone using code/scripts (backend) | Completed |
| Show how to create worlds and drop assets | Completed |
| Build a large simulated city / CBD environment in the simulator | Completed |
| Install and Configure Gazebo Simulator Tools with PX4 | Completed |
| Documentation for placing objects (signs, traffic lights, objects) | Completed |
| Autonomous drone flight possible and demonstrated | Completed |
| Multiple drones in the simulator at the same time | Completed |
| Show primitive detection / model working on initially provided 4 signs (stop, turning, parking, traffic lights) | Uncompleted |
| Autonomous flight with detection active | Uncompleted |
| Demo in simulator (different environments/ worlds) | Uncompleted |
| All outlined signs and objects (total 12 unique objects in table) detected and corresponding action response from the drone | Uncompleted |
| Demo in the simulator (different environments) | Completed |
| Show working for both PX4 and ArduPilot environments | Uncompleted |
| Simulator improvements completed and demo / video showing process to import new objects and create worlds | Completed |
| Usage documentation (as per each Milestone) | Completed |
| Demo of working solution in simulator | Completed |
| Meets all ‘test conditions’ | Completed |
| Deliverables as per ‘Hand-over deliverables’ section | Completed |

Algorithms Testing Framework video can be found [here](https://youtu.be/5wQY8h6KiDs).
