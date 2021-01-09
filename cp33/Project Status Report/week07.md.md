| COMP3888/COMP3988/INFO3600/SOFT3888/COMP5615 PROJECT STATUS REPORT | 20/10/2020 |
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
| **Project point person** | Boswell Lin |
| **Report Date** | 20/10/2020 |
|||

| **Quick description** | Using neural networks and/or computer vision to implement object detection for simulated drones. |
| --- | --- |
|
 |
 |

| **Status item** | **Status up to last week** | **Planned for next week** |
| --- | --- | --- |
| **Scope** | Implement a working sign and obstacle detection algorithm for drones within a simulated environment (Gazebo) ||
| **Time**| Up to date ||
| **Quality** | Up to standard so far ||
| **Planned Activities** | - Have a client demo with Cian - Make a better Tensorflow model using frames captured by the drone's camera. - Add in more traffic signs into the simulator world for the drone to detect. | Add snapshot support for the manual drone controller for better collecting data.|
| **Achievements** |- Manual drone control working in simulator -Large number of traffic signs now modelled in simulator|
| **Major deliverables** | - Add additional traffic signs for more signs to detect during simulation. - Manual control of drone in the simulator. - Demo to the client including explanation of which requirements have been completed and which have not | Improved TensorFlow model using frames from drone ||
| **Major issues** | OpenCV - unable to extract sections of the frame where the sign exists | OpenCV may continue to be an incompatibility issue for us which may hinder the accuracy |
| **Major risks** | Feeding the neural network with frames including the background - there is a risk that this may reduce the accuracy of the NN for sign detection | Sign detection with Tensorflow is not accurate
OpenCV incompatibility may mean we have to redesign our object detection code - can introduce technical debt |
| **External dependencies**| No external dependencies for this week | No external dependencies for next week|
| **Estimated effort (h)** | 15 hours | 15 hours |
| **Recorded effort (h)** | 15 hours |
 |
| **Overall Status (RYG)** | Green |
 |
|
 |
 |
\*project status report should be brief but informative – may use dot points where appropriate


| COMP3888/COMP3988/INFO3600/SOFT3888/COMP5615 PROJECT STATUS REPORT | 20/10/2020 |
| --- | --- |
|
 |
 |