| COMP3888/COMP3988/INFO3600/SOFT3888/COMP5615 PROJECT STATUS REPORT | 03/11/2020 |
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
| **Report Date** | 03/11/2020 |
| **Quick description** | Using neural networks and/or computer vision to implement object detection for simulated drones. |
| --- | --- |
| **Status item** | **Status up to last week** | **Planned for next week** |
| --- | --- | --- |
| **Scope**| Implement a working sign and obstacle detection algorithm for drones within a simulated environment (Gazebo) ||
| **Time**| Up to date ||
| **Quality** | Up to standard so far ||
| **Planned Activities** |- Integration testing- Practical testing code for Cian: taking a video from a moving drone and testing in neural net| Complete the integration testing scriptsTrain a better model with tensorflowAccurate sign detection with openCV ||
| **Achievements** |- Snapshot support for the manual drone controller for better collecting data.||
| **Major deliverables** | Discussion of integration testing | Testing frameworking - integration testingDetect signs with low accuracy using openCV |
| **Major issues** | OpenCV unable to extract bounding boxesIntegration testing with CI pipeline unfeasible at this current stage - workaround is to still use the testing scripts and provide evidence | Too many false detections in both tensorflow and openCV |
| **Major risks** | Feeding the neural network with frames including the background - there is a risk that this may reduce the accuracy of the NN for sign detection.Training large dataset may cause out of memory. | Sign detection with Tensorflow is not accurateOpenCV code may be difficult to incorporate |
| **External dependencies**| No external dependencies for this week | No external dependencies for next week|
| **Estimated effort (h)** | 15 hours | 15 hours |
| **Recorded effort (h)** | 15 hours ||
| **Overall Status (RYG)** | Yellow |
|
|
|
| --- | --- |
| COMP3988\_T17B\_GROUP5 |3 November 2020 | 0 |