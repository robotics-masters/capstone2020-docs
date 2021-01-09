# Week 5 Project Status Report

| **Unit of Study**        | COMP3988                                                                     |
| ---                      | ---                                                                          |
| **Team name**            | COMP3988\_T17B\_Group5                                                       |
| **Project Name**         | CP33 - Implementing Object Detection (Object Detection for Simulated Drones) |
| **Project start date**   | Monday, 24/08/2020                                                           |
| **Project end date**     | Friday, 20/11/2020                                                           |
| **Project point person** | Steven Condell                                                                   |
| **Report Date**          | 29/09/2020                                                                   |
| **Quick description** | Using neural networks and/or computer vision to implement object detection for simulated drones. |

| **Status item** | **Status up to last week** | **Planned for next week** |
| --- | --- | --- |
| **Scope** | Implement a working sign and obstacle detection algorithm for drones within a simulated environment (Gazebo) | |
| **Time** | Slightly behind | |
| **Quality** | Up to standard so far | |
| **Planned Activities** | Build a simulated residential environment in the simulator. Extract frames from gazebo simulator.| Have a working demo of basic sign detection and navigation. GPS or waypoints navigation demo. Make a TensorFlow model using Cian’s dataset of sign images. Extract frames from a Gazebo video, where the video has signs in view. Sort these frames in directories labelled by which (single) sign is visible, then use it to train the model. Implement traffic lights throughout the test world (city) and add in traffic signs |
| **Achievements** | City model uploaded and integrated with traffic light controls Traffic light control via network | |
| **Major deliverables** | Traffic light control and integrated it into our test world | Opencv detection of traffic signs. Complete the traffic lights throughout the test environment and add traffic signs |
| **Major issues** | Tensorflow parameters are difficult to tune | Additional models are required for improved accuracy but could run into similar problems |
| **Major risks** |Models produced may include errors that are difficult to catch | Implementation of object detection program into Gazebo may be difficult |
| **External dependencies** | No external dependencies for this week | No external dependencies for next week |
| **Estimated effort (h)** | 15 hours | 15 hours |
| **Recorded effort (h)** | 15 hours | |
| **Overall Status (RYG)** | Yellow | |