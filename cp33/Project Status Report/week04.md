| COMP3888/COMP3988/INFO3600/SOFT3888/COMP5615 PROJECT STATUS REPORT | 22/09/2020 |
| --- | --- |
|
 |
 |

| **Unit of Study** | COMP3988 |
| --- | --- |
| **Team name** | COMP3988\_T17B\_Group5 |
| **Project Name** | CP33 - Implementing Object Detection (Object Detection for Simulated Drones) |
| **Project start date** | Monday, 24/08/2020 |
| **Project end date** | Friday, 20/11/2020 |
| **Project point person** | Gio Picones |
| **Report Date** | 22/09/2020 |

| **Quick description** | Using neural networks and/or computer vision to implement object detection for simulated drones. |
| --- | --- |

| **Status item** | **Status up to last week** | **Planned for next week** |
| --- | --- | --- |
| **Scope**
 | Implement a working sign and obstacle detection algorithm for drones within a simulated environment (Gazebo) |
 |
| **Time**
 | Behind |
 |
| **Quality** | Up to standard so far |
 |
| **Planned Activities** | Have trees and plants in the customised world.Create assets of all signs and objects into simulators. install and configure gazebo simulator Tools with px4. Build a simulated residential environment in the simulator. | Have working demo of basic sign detection and navigation.GPS or waypoints navigation demo.Build a simulated residential environment in the simulator.
Make a TensorFlow model using Cian&#39;s dataset of sign images.
Extract frames from a Gazebo video, where the video has signs in view. Sort these frames in directories labelled by which (single) sign is visible, then use it to train the model. |
| **Achievements** |
- All sign models completed
- Tensorflow GPU running on one member&#39;s machine
- Able to connect Gazebo with OpenCV
 |
 |
| **Major deliverables** | All sign models completed
 | Traffic light control. Opencv detection of traffic signs. |
| **Major issues** | Some members do not have a Nvidia GPU, which is required for tensorflow GPU. We will get around this by delegating the majority of the tensorflow computation to those members who do have a Nvidia GPU and having the other members use the non-GPU version of tensorflow where needed. |
 |
| **Major risks** | Some members do not have a Nvidia GPU for tensorflow. | Tensorflow parameters may be difficult to tune |
| **External dependencies**
 | No external dependencies for this week | Need to get everyone up to speed with progress and any documentation/code Robotics Masters has given to us |
| **Estimated effort (h)** | 15 hours | 15 hours |
| **Recorded effort (h)** | 15 hours |
 |
| **Overall Status (RYG)** | Yellow |
 |