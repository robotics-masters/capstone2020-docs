| COMP3888/COMP3988/INFO3600/SOFT3888/COMP5615 PROJECT STATUS REPORT | 13/10/2020 |
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
| **Project point person** | Steven Condell |
| **Report Date** | 13/10/2020 |

| **Quick description** | Using neural networks and/or computer vision to implement object detection for simulated drones. |
| --- | --- |

| **Status item** | **Status up to last week** | **Planned for next week** |
| --- | --- | --- |
| **Scope** | Implement a working sign and obstacle detection algorithm for drones within a simulated environment (Gazebo) ||
| **Time**| Up to date ||
| **Quality** | Up to standard so far ||
| **Planned Activities** | Have a working demo of basic sign detection and navigation.GPS or waypoints navigation demo.Make a TensorFlow model using Cian/'s dataset of sign images.Extract frames from a Gazebo video, where the video has signs in view. Sort these frames in directories labelled by which (single) sign is visible, then use it to train the model.Implement traffic lights throughout the test world (city) and add in traffic signs | Have a client demo with Cian.Make a better Tensorflow model using frames captured by drone  camera.Add in more traffic signs into the simulator world for the drone to detect.|
| **Achievements** |- City model uploaded and integrated with traffic light controls- Traffic light control via network||
| **Major deliverables** | Complete the traffic lights throughout the test environment | Add additional traffic signs for more signs to detect during simulation. |
| **Major issues** | OpenCV - unable to extract sections of the frame where the sign exists | OpenCV may continue to be an incompatibility issue for us which may hinder the accuracy |
| **Major risks** | Feeding the neural network with frames including the background - there is a risk that this may reduce the accuracy of the NN for sign detection | Sign detection with Tensorflow is not accurate |
| **External dependencies**| No external dependencies for this week | No external dependencies for next week|
| **Estimated effort (h)** | 15 hours | 15 hours |
| **Recorded effort (h)** | 15 hours |
 |
| **Overall Status (RYG)** | Green |
 |

\*project status report should be brief but informative – may use dot points where appropriate

|
 |
 |
| --- | --- |
| COMP3988\_T17B\_GROUP5 | 13 October 2020 | 0 |