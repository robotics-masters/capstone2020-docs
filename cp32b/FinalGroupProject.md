# COMP3988 Final Group Report 


# Introduction #
This report serves as a final summary for deliverables and outcomes of the project at the end of the semester. It also summarizes the group work done by the team, difficulties and challenges faced.

We take a look at the client’s requirements and the actual outcomes of the project; the goals and scope of the projects; system specification; group work and collaboration, communication, interaction with relevant parties and a collection of technical documentation of the project in the following sections.

To help you easily understand the scope of the project, we have made a showreel for you [here](https://youtu.be/VxKC9a5ixNI).

## The overall project vision, goal, purpose or objective ##

Autonomous vehicles and related technology have evolved rapidly in recent years. Among all of them, the most popular and crucial player is autonomous driving, which is essentially what differentiates manual and autonomous vehicles.

Many components jointly make the vehicle intelligent so that it can automatically drive itself; Obeying traffic rules is one of the priorities. Traffic signs detection, an important part of traffic rules, is what we are implementing in this project. 

We employ existing technology(TensorFlowNeural Networks, and OpenCV) to create new software solutions to detect some predefined traffic signs(e.g.stop, turn-left, turn-right signs). We build classifiers of signs by feeding cleaned data collected in a racing car simulator into a model; train the model, and collect a classifier. The goal is to build more accurate and reliable classifiers using a better simulator, better data and a combination of various techniques to employ their complementary benefits, as well as applying better data cleaning techniques and more efficient classification algorithms.

The team has been closely working with the clients and other teams to fully understand the evolving requirements of the client and harvests the progress of other teams working on relevant projects.

At the end of the project, the team has demonstrated its simulator and the sign detection algorithm in front of the client and many industry experts and satisfactorily fulfil the client’s expectation.

## What the project has achieved ##

The team has built multiple virtual and real-world tracks replicating F1 tracks in the city of Shanghai and Shenzhen. The team has also built a F1 racing car model replicating a Ferrari F1 car.

Although the algorithm is not capable of detecting all traffic signs outlined in the initial group report, it still achieved a satisfactory result, considering our team starting late. The algorithm manages to give high accuracy rates on common signs such as the stop sign or turning sign.

## The key stakeholders, what do they do, and how they interact ##

- Robotics master(the client):

The robotics company builds autonomous obstacle avoiding and auto-piloting robots. This sign detection algorithm can assist in auto-piloting of the robots(vehicles)in real traffic.

The client gives requirements to the team on a weekly basis. The team implements the client’s requirement with consultations to the clients and online documentation for professional advice. Ultimately the team is building the project for this stakeholder.


- Human drives

Human drives are highly relevant to this technology as it can release humans from this dangerous and sometimes tedious job of daily driving. Autonomous vehicles provide safer, more efficient solutions to existing error-prone, dangerous, congested traffic caused by inherent disadvantages in human’s characteristics and minds.

Autonomous driving is expected to partially and eventually fully replace human drives for safer and less congested commuting traffic environments for all road users. Sign detection is a crucial component of any practical auto-piloting.


- Car manufacturer

Since autonomous vehicles will become the trend of the future, current car manufacturers must evolve their technologies and manufacturing process so they won’t be left behind.

Car manufacturers need to either develop their own technology like Tesla, or purchase or invest into other companies to acquire such a technology.

- Other road users

Other road users include: cyclist, pedestrian, etc. Currently they share roads with cars which are manually controlled. Human drives can be distracted or have bad judgements which can pose danger to them. Once autonomous vehicles are widely used they can use the roads much more safely.

Autonomous vehicles must be able to detect the existence of other road users and place their safety as the first priorities(since they are usually more vulnerable than people sitting in vehicles)


- Governments and regulators

Autonomous vehicles require different regulation and coordination as they are controlled by computers. The effectiveness, safety, and security of computers must be carefully monitored and tested before they are legally allowed on-road. How to thoroughly test the effectiveness and safety is to be considered by the governments and transportation regulators.

## Identification of resources and risks involved in the project ##

### Resources: ###

- **Donkey Car Simulator**

The algorithms will be tested in a simulator provided by Donkey Car simulator, which is an open source project available for download and contributions on GitHub.

It allows teams who don’t have a physical donkey car or robots to develop and test their algorithms in a cost-efficient and easy way. It also saves time from building physical robots. We use donkey car simulator to collect training data which we feed into the model; to test our auto-piloting and sign detection model in the simulator for its effectiveness, etc.

- **TensorFlow**

TensorFlow is an open-source platform for machine learning. It provides comprehensive tools, libraries for developing machine learning models and testing machine learning algorithms.

We use TensorFlow to write the logic for our classifier using encapsulated algorithms provided by TensorFlow. We also use tutorials provided by TensorFlow to start our project from scratch.

- **Unity**

We use Unity to build new testing tracks in the simulator as well as new car models. What’s most important is that we use Unity to build models of traffic signs in existing and new tracks. 3D modeling allows easy collections of training data(e.g. pictures) in a track from different angles, scenarios, and speed.

### Risk ###

Since team members collaborate remotely on the project, there won’t be any risks relating to the current pandemic. Simulations are used instead of physical models so there are no physical risks associated with the project.


# System Specifications and Design

## User Story
Our project is mainly divided into three parts. Part 3 is added in by the client during the project as a new scope.

- Part 1 is improving the donkey car simulator environment for us to capture training data as well as test our model visually. 
- Part 2 is writing auto sign detection code for the car using tensorflow and OpenCV. 
- Part 3 is creating two F1 tracks as well as a SF1000 car model. 

According to the functional diversity of our project, we are going to write user stories separately for these three parts. 

### **Part 1. Simulator for Sign Detection**
We consider two types of users for part 1: 

- Tester (People who drive the car using the designed track on simulator): 
    - Tester 1: As a tester, I want the track to include as many signs as possible. So that I can write codes to detect many signs by using one track. 
    - Tester 2: As a tester, I want  the setup of the environment for the track as easy as possible. So that I can easily set up the environment and focus on writing codes for detecting signs.
    - Tester 3: As a tester, I want the raw images taken when I drive the car as clear as possible. So that I can improve my sign detection codes. 
    - Tester 4: As a tester, I want to have multiple tracks. So that I can use some for training and others for testing.
    - Tester 5: As a tester, I want to have different types of signs. So that my model can be trained to detect different kinds of signs.
    - Tester 6: As a tester, I want to have different colors of the same signs. So that my model can be trained to detect the same sign with different colours.

- Maintainer (People who is going to maintain the track for later use):
    - Maintainer 1: As a maintainer, I want to add more signs and build new tracks to the track easily in the later day. So that the maintenance job can be more efficient.  

### **Part 2. Sign Detection Model**
We consider two types of users for part 2: 

- Automotive industry:
    - Business 1: As a business, I want to know if the certain sign detections algorithm is reliable, so that I can decide whether or not to adopt the technology.
    - Business 2: As a business, I want the sign detection model to detect as many kinds of signs as possible so that the car will not break the traffic rules.
    - Engineer 1: As an engineer, I want the system to have a high adaptability so that we can use the system inside our own system without worrying about compatibility.

- Researcher for Driver Assistance System:
    - Researcher 1: As a researcher, I want to have documentation about the limitations and benefits for certain signs detection code, so that I can clearly understand the code and make improvements in  the future.  
    - Researcher 2: As a researcher, I want to have data on the certain algorithms for the sign detections, such as the percentages to clarify the signs correctly. So that I can decide how to make improvements in  the future.  
    - Researcher 3: As a researcher, I want to have a tutorial on how to build sign detection models so that we can do further training based on the results.

### **Part 3. F1 tracks and SF1000**
We consider two types of users for part 3: 

- 3D game developers:
    - Developer 1: As a 3d game developer, I want to have a clear documentation of how to design the f1 track, so that I can know how to develop similar tracks in my game.
    - Developer 2: As a 3D game developer, I want to have detailed documentation about how to design the F1 car model in Blender, so that I can know how to develop similar car models based on that.

- F1 Virtual Racer
    - Racer 1: As a virtual F1 racer, I want to have some textures and buildings around the track so that the racing will not be boring.
    - Racer 2: As a virtual F1 racer, I want to have a start line and a start gate so that my model will know where to start.
    - Racer 3: As a virtual F1 racer, I don’t want the front of the car to be seen from my first person angle so that my model can well detect the road.
    - Racer 4: As a virtual F1 racer, I want some spiky corners to be widened so that my car will be able to turn without  going out of track.

### Part 4. Out Scope
Besides these user stories, we also have some user stories related to requirements that are no longer needed by the Client. That is, these user stories are out of scope. These out scope user stories can be split into two parts:

- Leaderboard (anyone who race donkey car on leaderboard):
    - Racer 1: As a racer, I want to know if the racing environment is easy to set up on my computer. So that I can focus on the race rather than spend time on set up.
    - Racer 2: As a racer, I want to know whether or not the racing environment will be affected by computer configuration . So that I can know the fair of the racing environment.
    - Racer 3: As a racer, I want to see a scoreboard of the current race with lap times and personal best, so that I can know my current place in the game and other competitors’.
    - Audience: As an audience of the racer league, I want to watch the live show of the race from my own computer so that I do not have to go out.

- F1 Track:
    - Audience: As an audience, I want the track to have elevation so that the virtual race League looks like a real one.
    - Racer: As a racer, I want to have barriers along the track so that my car won’t drive out of track.
    - 3D game developer : As a 3D game developer, I want to know how to get the elevation for a game map so that I can be aware of the difficulty of adjusting my game environment based on that.

## Technical and other constraints

### Collaborating Blender and Unity
Some fbx models export from blender to Unity are without colour. We find out that this is due to the limitation of material surface. Unity is unable to recognize some material surface from Blender. Solution is to bake the whole material (which is a tool in a blender). However, we spend lots of time manually recoloring the model using hexadecimal values and choosing the similar surface that’s available in Unity.

### Technical issue of simulator
The wheels of our car model look unstable when the car is driving using manage.py. This remains  unfixed as this problem is due to the simulator template that we are given.

### CNN algorithm constraints
Our sign detections used convolutional neural networks only. While we may encounter some constraints from using CNN, such that CNN does not have a built-in understanding of 3D space. It means CNN requires tens of thousands of examples to achieve good performance. This increases difficulty in our data collection process. Also, CNN does not encode the position and orientation of the object, which means to CNN, both images are similar if they contain similar elements. This may bring up a reliability issue for those similar signs in the sign detection process. 

### Tensorflow Version constraints
There are some version constraints we encountered when we use tensorflow for sign detections. For example, tensorflowv2’s module has no attribute ‘app’,thus we cannot use that attribute if we downloaded tensorflowv2. The solution is to use tensorflowv1. 

Also, if we want to use GPU to train the model, we should install two packages, cudatookit and cuNN. The version of these two packages should also be restricted to the version of tensorflow. For example, tensorflow 2.1 requires cuda 10.1 while tensorflow 2.3 asks for cuda 11.0. 

### Limitation of OpenCV code
1. In the OpenCV findContours function, it is unable to draw the expected contours around some signs based on the given color filter and the area shape.
2. OpenCV code is unable to identify regions of interest with small signs due to the fixed resolution required by the client.


## **System Architecture**

Essentially, our system can be split into two parts: Sign Detection System and F1 Racer League. The Sign Detection System includes tracks with different types and different colours of signs, which are used for data collection and testing. It also contains the most essential element, the model, which should be able to detect which sign the car is facing at and does the corresponding behaviour. The F1 Racer League includes two F1 tracks, the Shanghai tack and the Melbourne track, as well as a Ferrari SF1000 car model. Virtual Racers will be able to drive the SF1000 car on both F1 tracks to have a competition.

### **Sign Detection System**

![final1.png](https://bitbucket.org/repo/G6xBMXK/images/3975877054-final1.png)

#### The Initial System(Platform)
Initially, we have a donkeycar platform, which includes the simulator and the donkeycar+gym-donkey. This allows us to set up a donkeycar in our local machine or in a virtual environment and drive the car in the simulator. There are four maps in the simulator with different environments, as shown in figure 2.a, and tracks so that we can choose one based on our requirement. Also, users can easily start Donkey simulation by entering one simple command as well as change some settings based on the comments in the myconfig.py file. Furthermore, if users want to train a model and build a self-driving car, they can use the code provided by the platform to train the model. However, to further develop the system, such as adding tracks and building our own models,requires more familiarity with Unity and in-depth research on neural networks.

![final2.png](https://bitbucket.org/repo/G6xBMXK/images/1772529712-final2.png)

#### The Track
Five tracks with the same map (Robotics Masters Challenge Track) were built for data collection and model testing. Images captured from four tracks were used as training sets and the other track was used for testing. Each of the five tracks had all types of signs, including left-turing, right-turing, stop, and parking. However, the colours are different. For left-turning signs and right-turning signs, they had black and blue respectively. For parking signs, it had three colours, green, yellow and blue. 

#### OpenCV
We use OpenCv as a preprocessing tool for gathering training data and for real-time sign detection. The approach is color-based ROI extraction. 

Training data: Using the camera images that we gathered from Robotics Master Challenge track, we apply OpenCv ROI extraction. It returns contours of the same colour. These will be manually filtered and labelled as stop, left/right turnin, parking etc. signs. These data can then be used for training the Neural network. 

Real-time sign detection: The camera image will be processed using openCv in real-time as camera streams. The extracted ROI will be fed into the neural network for classification. If a sign is detected, then bounding boxes will be drawn on the ROI, and class labelled will be printed to the console. 


#### The Model
Our model involves two components 1. OpenCv extraction + neural network classification 2. autonomous driving model.
- The neural network model is trained using python (Tensorflow). It involves a pre-processing layer (image resizing etc.), 3 hidden layers, 3 max pooling layers and a dense layer. The training data were gathered from a simulated donkey environment using OpenCv for pre-processing. 
- The autonomous driving model is trained using the training code provided by the donkey platform. The training data are in the form of JSON packets, that specifies the angle/throttle value for each camera frame. They are gathered as we drive around in the simulator. The model predicts the angle/throttle value based on the camera stream.


### F1 Racer Tracks

![final3.png](https://bitbucket.org/repo/G6xBMXK/images/2666138612-final3.png)

#### Pre-process jobs
Pre-processing jobs including map creation and car model creation. 
1. Map creation: Photoshop for drawing tracks ensure the angles and orientation of the tracks follow the real-world track designs. The creation of map objects in Blender and exported to Unity, make sure the easier management of materials in Unity. 
2. Car model creation: A basic racing car model was used from online resources. Then parts of the car are redesigned and restructured for the release of the final car model required by the client. 

#### Unity
The origin unity project was used as a template to build the tracks. The maps from the pre-process jobs were used as a texture of the ground-surface plane. The car model’s wheel collider system was built based on the origin donkey car model.  

#### Release
Some release versions were created and released to the github repository once we finished a specific requirement. We provide the simulator on three platforms, Windows, macOS and Linux. It can be directly downloaded from the release page.

## **Quality of Work** ##

### Overview of user stories and test results

| **Requirement**                                                                                                                                                                                                      | **Acceptance Test**                                                                                                                                                                                                                                                                                                                                                                    | **Results**                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. As a tester, I want the track to include **as many signs as possible**. So that I can write codes to detect many signs by using one track.                                                                        | The track is implemented in Unity as in the given specification, including stop, turn left/right, and parking signs.                                                                                                                                                                                                                                                                   | [Releases](https://github.sydney.edu.au/moxu7046/COMP3988_simulator/releases)                                                                                                                                                                                                                                                                                                                                                                           |
| 2. As a tester, I want the **setup of the environment** for the track as easy as possible. So that I can easily set up the environment and focus on writing codes for detecting signs.                               | There should be clear documentation on how to set up the environment for the track we built in the simulator                                                                                                                                                                                                                                                                           | [Link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Donkey%20car%20environment%20for%20new%20created%20track%20SetUp%20Guide)                                                                                                                                                                                                                                                                                                              |
| 3. As a tester, I want **the raw images taken when I drive the car as clear as possible**. So that I can improve my sign detection codes.                                                                            | The camera resolution of the image taken by the donkey car in simulator should be of 240 * 240 pixel values.                                                                                                                                                                                                                                                                           | Passed                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 4. As a tester, I want to **have multiple tracks**. So that I can use some for training and others for testing.                                                                                                      | There should be 5 variations of the Robotics Master Challenge track, as well as Shanghai and Melbourne F1 tracks.                                                                                                                                                                                                                                                                      | [Releases](https://github.sydney.edu.au/moxu7046/COMP3988_simulator/releases)                                                                                                                                                                                                                                                                                                                                                                           |
| 5. As a tester, I want to have **different types of signs**. So that my model can be trained to detect different kinds of signs.                                                                                     | The simulator should contain at least: stop signs, left/right turing signs, speed-50 and parking signs.                                                                                                                                                                                                                                                                                | [Releases](https://github.sydney.edu.au/moxu7046/COMP3988_simulator/releases)                                                                                                                                                                                                                                                                                                                                                                           |
| 6. As a tester, I want to **have different colors of the same signs**. So that my model can be trained to detect the same sign with different colours.                                                               | Stop signs, left/right turing signs, speed-50 and parking signs in the simulator should have different colour variations.                                                                                                                                                                                                                                                              | [Releases](https://github.sydney.edu.au/moxu7046/COMP3988_simulator/releases)                                                                                                                                                                                                                                                                                                                                                                           |
| 7. As a maintainer, I want to **add more signs and build new tracks** to the track easily in the later day. So that the maintenance job can be more efficient.                                                       | The process of adding signs and building new tracks in Unity should be well-documented, quick and easy to follow.                                                                                                                                                                                                                                                                      | [Link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/Docs/Map_and_Sign_Implementation.pdf)                                                                                                                                                                                                                                                                                                                                            |
| 8. As a racer, I want to know if the racing environment is **easy to set up** on my computer. So that I can focus on the race rather than spend time on set up.                                                      | There should be clear documentation on how to set up the donkey car environment and simulator.                                                                                                                                                                                                                                                                                         | [Link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Tensorflow%20and%20Donkey%20Simulator%20Environment%20Setup%20Guide)                                                                                                                                                                                                                                                                                                                   |
| 9. As a racer, I want to know whether the racing environment will be affected by computer configuration. So that I can know the fair of the racing environment.                                                      | During the race, the race conditions for each racer should ideally be identical, including internet connection, computational speed.                                                                                                                                                                                                                                                   | Out of scope                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 10. As a business, I want to know if the **certain sign detections algorithm is reliable**, so that I can decide whether or not to adopt the technology.                                                             | 1. The correct prediction rate of each class is high and stable in multiple runs 2. If the model cannot detect the sign or unsure about the sign, then classified to “other” (i.e. no action)                                                                                                                                                                                          | [Accuracy result](https://bitbucket.org/RobertJia/comp3988_t17b_group1/addon/pipelines/home#!/results/21)                                                                                                                                                                                                                                                                                                                                               |
| 11. As a researcher, I want to have documentation about the **limitations and benefits** for certain signs detection code, so that I can clearly understand the code and make improvements in the future.            | There should be a description about the employed sign detection model (Neural network), and also other possible alternatives.                                                                                                                                                                                                                                                          | [Sign detection code](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_Unity.ipynb) [Limitation of CNN model](https://yuanda-dong.atlassian.net/browse/CP-11?atlOrigin=eyJpIjoiNmJiOWYzNjhlOGUxNGRlZmFjOWI4YWJhNDU4NjlhM2QiLCJwIjoiaiJ9) [Benefits of CNN model](https://yuanda-dong.atlassian.net/browse/CP-12?atlOrigin=eyJpIjoiYTVhNDQyYzI2MTNmNGRmZmI2MTA2MTM0MmE0ZjdhNWMiLCJwIjoiaiJ9) |
| 12. As a researcher, I want to have data on the **certain algorithms for the sign detections**, such as the percentages to clarify the signs correctly. So that I can decide how to make improvements in the future. | 1. Model accuracies tests should be performed on the employed model. This includes the percentage of correctly classified signs as a single number, and the confusion matrix. 2. Model should have low misclassification cost: If the model cannot detect the sign, then classified to “other”(i.e. no action) 3. No overfitting: ensure the model can perform well on the new images. | [Explanation of evaluation algorithm and accuracy tests for CNN model](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/CNN_model_Evaluation)                                                                                                                                                                                                                                                                                                  |
| 13. Audience: As an audience of the racer league, I want to watch the live show of the race from my own computer so that I do not have to go out.                                                                    | The actual race shall be streamed live, so that the audience can view it from anywhere.                                                                                                                                                                                                                                                                                                | Out of scope                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 14. As a business, I want the sign detection model to detect as many kinds of signs as possible so that the car will not break the traffic rules.                                                                    | 1. Sign detection models should be accurate in predicting the traffic signs including (Stop, left, right, park, other) with at least 90% accuracy. 2. Donkey car should be able to respond accordingly to the sign detected.                                                                                                                                                           | [Accuracy result](https://bitbucket.org/RobertJia/comp3988_t17b_group1/addon/pipelines/home#!/results/21)                                                                                                                                                                                                                                                                                                                                               |
| 15. As a researcher, I want to have a tutorial on how to build sign detection models so that we can do further training based on the results.                                                                        | There should be documentation written on how to build a working sign detection model, including 1. Data collection and cleaning using simulator 2. Building the model using tensorflow 3. Train the model using tensorflow with the option for parameter tuning                                                                                                                        | [Simulator Documentation](https://docs.donkeycar.com/guide/simulator/) [Build and train model using tensorflow](https://www.tensorflow.org/tutorials/images/classification)                                                                                                                                                                                                                                                                             |
| 16. As a racer, I want to see a scoreboard of the current race with lap times and personal best, so that I can know my current place in the game and other competitors’.                                             | A web-based leader-board that displays the lap time and personal best. 1. It should be able to collect Json packets from the server machine. 2. It should be able to interpret this information and display with a user friendly interface                                                                                                                                             | Out of scope                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 17. As an engineer, I want the system to have a high adaptability so that we can use the system inside our own system without worrying about compatibility.                                                          | The system should have a fixed list of dependencies and should work across platforms, with clear documentation on how to install the environment required. Preferably in the future, the system will be deployed with a docker container.                                                                                                                                              | [Dependency List](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Dependency%20List)                                                                                                                                                                                                                                                                                                                                                          |
| 18. As a 3d game developer, I want to have a clear documentation of how to **design the f1 track**, so that I can know how to develop similar tracks in my game                                                      | There should be detailed documentation on how we used Unity & Blender to design the F1 tracks. The documentation should be easy to follow, so anyone can use it to reproduce the same results as ours.                                                                                                                                                                                 | [Documentation](https://github.com/Yuanda-Dong/Client-Final-Deployment/blob/main/Simulator/Documentation_F1/README.md)<br>[Blender](https://github.com/Yuanda-Dong/Client-Final-Deployment/blob/main/Simulator/Documentation_Blender/README.md)                                                                                                                                                                                                         |
| 19. As a 3D game developer, I want to have detailed documentation about how to **design the F1 car model** in Blender, so that I can know how to develop similar car models based on that.                           | There should be detailed documentation on how we used Blender to design the F1 car model. The documentation should be easy to follow, so anyone can use it to reproduce the same results as ours.                                                                                                                                                                                      | [Documentation](https://github.com/Yuanda-Dong/Client-Final-Deployment/blob/main/Simulator/Documentation_F1/README.md)                                                                                                                                                                                                                                                                                                                                  |
| 20. As an audience, I **want the track to have elevation** so that the virtual race League looks like a real one.                                                                                                    | Shanghai and Melbourne F1 tracks should have elevation that mimics the real-world data.                                                                                                                                                                                                                                                                                                | Out of scope                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 21. As a virtual F1 racer, I want to **have some textures and buildings** around the track so that the racing will not be boring.                                                                                    | Both F1 tracks should contain vegetation (trees/grass), stadium buildings, and start gates. The Melbourne F1 track should have a lake in the middle of the map                                                                                                                                                                                                                         | [Releases](https://github.sydney.edu.au/moxu7046/COMP3988_simulator/releases)                                                                                                                                                                                                                                                                                                                                                                           |
| 22. As a virtual F1 racer, I want to **have a start line and a start gate** so that my model will know where to start.                                                                                               | The F1 tracks should have a start line and a start gate with corresponding ‘Shanghai/Melbourne’ text engraved on it.                                                                                                                                                                                                                                                                   | [Releases](https://github.sydney.edu.au/moxu7046/COMP3988_simulator/releases)                                                                                                                                                                                                                                                                                                                                                                           |
| 23. As a virtual F1 racer, I don’t want **the front of the car to be seen from my first person angle** so that my model can well detect the road.                                                                    | The camera needs to be placed at the front of car to avoid the capturing the car itself.                                                                                                                                                                                                                                                                                               | Passed                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 24. As a virtual F1 racer, I want **some spiky corners to be widened** so that my car will be able to turn without  going out of track.                                                                              | White & red strips should be placed around spiky corners of the F1 tracks.                                                                                                                                                                                                                                                                                                             | [Releases](https://github.sydney.edu.au/moxu7046/COMP3988_simulator/releases)                                                                                                                                                                                                                                                                                                                                                                           |

### **Details of Tests**

### Testing plan

#### Test 1: Autonomous driving in the simulator

To assess the reliability of sign detection models in self-driving cars, we need first build a simple autonomous vehicle in the simulator. We will test the performance of such a vehicle by measuring the duration for which the donkey car can self-drive without hitting any obstacles.

#### Test 2: OpenCV testing for image pre-processing (success rate of detect correct ROI) 

Since the mid-semester break, we switched to a hybrid approach of OpenCV and neural network to sign detection. In the first step, we build a color-based filter algorithm using openCV to abstract the traffic sign area(region of interest ROI), and then train the model on the sign area only. 

To ensure our openCV function can abstract the ROI, we define the function “test_iamges” and every time when we run image preprocessing using Object_Detection_Unity.py, it can calculate and automatically print the success detection rate of each class (folder). By doing so, we easily monitor our openCV functions’ performance under different cases (controlled by the input folder).

#### Test 3: Simulation-based Evaluation for the image pre-processing time using openCV

We also care about the efficiency of our algorithm, to ensure our new hybrid method can give the real-time prediction in the simulator without latency. Thus, we monitor the image preprocessing time for the whole dataset, and calculate the average running time, to ensure the algorithm can process more than 10 thousand images within 1 min. 

#### Test 4: Simulation-based model evaluation for the CNN model accuracy (simulator signs[F1], real-world signs [Shenzhen])

We choose the CNN model, as it is the most successful model for image classification in recent years.
Our model can classify the input images (collected by the donkey car) into 5 classes: Right-turning, Left-turning, Park, Stop and speed_50.
By choosing the proper number of convolutional layers and epochs, we train the model using more than 4855 images, and test the model performance using extra 1621 (886 images on unity maps and  735 images on real-world shenzhen track) images (test data), which are not used in the model training.
Firstly, we test the model has no overfitting, which means that the test accuracy using new images (test data) is close to the evaluation accuracy achieved during model training. Secondly, we test our model structure to achieve the highest test accuracy based on the hyper-parameter tuning result. Thirdly, we test the misclassification ratio on the raw images, combining the openCV pre-processing and confidence level using function test_missclassification_images in TFmodel_helper_function.py. We also visualize the misclassification images using draw_misclassification_images. 
The complete model training and testing process can be found in [Sign_Classification_Unity.ipynb](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_Unity.ipynb)

#### Test 5: Automatic CNN model accuracy test

We test the accuracy of our CNN model through its performance on different sets of test data. The accuracy will be tested based on the confusion matrix and other statistical measures such as precision, recall and F1-score. There are [3 different sets of test data](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/tests/) involving [stop, left, right, park, speed-50] signs as well as different colour variations collected from our custom tracks (Robotics Challenge Track and F1 tracks), real-world images, Shenzhen track (provided by client). The test script will be run each time a ‘push’ is made to our repository, this is detailed in the pipeline section. 

#### Test 6: OpenCV draw bounding box correctly in simulator 

It’s important that the openCV (based on sign colours) can extract the correct region of interest (ROI), before feeding into Tensorflow for sign detection. We will test the performance of OpenCV extraction in the simulator by drawing bounding boxes around the detected ROI. We will run the simulation and draw bounding boxes in real-time to see how much ROIs were extracted correctly. 

#### Test 7: Stable testing result in different map (Robotics Challenge and F1 tracks) 

Given the accuracy of the CNN model, and openCV extraction is tested, the next step in our plan is to test whether the model when fed into a data stream of camera images, is able to predict the label class in real-time. We will test whether these camera images are correctly classified, by printing the class label while drawing bounding boxes to the console in real-time.

#### Test 8: Custom built track has the correct physics

We will test whether the track we built responds to user input(via keyboard for driving)/object collision reasonably using the physics in Unity. To do this, we will divide the test into normal/abnormal test cases, where the normal test case looks at how accurate the donkey car responds to user inputs and manages to drive around the map. This will involve driving in a straight line turning and braking. In the abnormal case, we will intentionally drive the donkey car to hit the poles of traffic lights/signs, and walls to check the object collision.

#### Test 9: Donkey car can respond accordingly to the sign

Donkey car should stop by reducing the throttle value, after a stop sign is detected. Similarly, the donkey car should turn left/right when a left/right sign is detected. This can be tested by running the image detection model and self-driving model at the same time in the custom map containing traffic signs. Then, we will print out the actual throttle and angle values received by the donkey car, and observe the behaviour of the donkey car. 

## **Relevant testing techniques**

### Usability testing 

Usability test is an important aspect of our testing process, once the acceptance conditions for each functional requirement have been met. We aim to build a usable system with clear documentation, so that a user with little prior knowledge in autonomous vehicles can use the tools that we provide in our repository to train a self-driving car capable of sign detection, and compete in races. 

1. User can produce the image dataset required for training their model by manually driving in the simulator map
2. User can create their own custom map if needed by following the documentations that we provide
3. User can create their own car models
4. User can build a neural network model for autonomous driving in the simulator easily
5. User can learn about how to use the combination of openCV and tensorflow to produce a more stable image classifier 
6. User can build an traffic sign/light classification model and has the option for fine tuning of their model
7. User shall be able to learn more about the model that we use by reading our documentation

All of the above mentioned tests will be primarily conducted with our client after the deployment, to ensure the usability of our system. There is a separate repository containing the final version of codebase and documentation dedicated for the client. 

### Sign detection accuracy through confusion matrix

The input space can be partitioned into images containing [stop, left, right, park, speed-50, no sign] signs. We test the diagonal entries of the confusion matrix is larger than the specified threshold and off-diagonal entries less than a specified threshold. In addition, we test the precision, recall and f1-score of the model. 

### Autonomous driving and sign detection in real time inside simulator

We have built a prototype implementation of the models using Tensorflow and OpenCV. Since the requirements related to autonomous driving and sign detection in simulator focus more on the behaviour aspect of the donkey car, i.e. whether it can drive without hitting obstacles, classifies signs and responds accordingly. We have devised our testing techniques to test the behaviour of the donkey car:

1. We will test the performance of self-driving model by measuring the duration for which the donkey car can self-drive without hitting any obstacles.
2. We will test the correctness of the image classifier by printing the class label and bounding boxes of the camera image in real-time inside the simulator.
3. We will test the responses of the donkey car to the traffic sign, by measuring the throttle and angle values after a traffic sign is detected, and by observing the movement of the donkey car in the simulator.

### Quality of Dataset used for CNN model training
The train and test data were collected by a donkey car simulator given by different drivers, and we use this dataset to train and test the CNN image classification model.

- Data folder [data](https://drive.google.com/drive/folders/1jGSZPrPlZ2ET9jY1pk_Af7OcWhweIO3J)
- Train data (4855 in total): 428 stop images; 768 park images; 1080 right turn images; 1869 left turn images; 710 speed_50 images
- Test data on unity map (886 in total): 23 stop images; 322 park turn images; 130 right turn images; 373 left turn images; 38 speed_50 images
- Test data on shenzhen track (735 in total): 577 stop images; 6 park turn images; 17 right turn images; 135 left turn images
- Within the train data, we separate 20% data as the evaluation data to validate the hyper-parameter turning and avoid overfitting.

**A summary of details of acceptance tests are in the appendix section**.

## **Discipline knowledge used in quality assurance**

### Convolutional neural network (CNN) algorithms

A convolutional neural network (CNN, or ConvNet) is a class of deep neural networks, which is commonly used for image classification.

- `Convolution layers`: the core building block of a CNN. Our model has 3 hidden layers.
- `Number of filters`: the dimensionality of the output space (i.e. the number of output filters in the convolution). Our model choice 16, 32, 64, and 128 as filters in each layer.
- `Epochs`: the number of passes of the entire training dataset the machine learning algorithm has completed. The low epoch value can result in under-fitting, high epoch value can result in overfitting. The proper number of epoch choices is necessary. Our model using epoch = 7.
- `Activation function`: determine the neuron should be activated (“fired”) or not. Our model uses `relu` as an activation function, as it is computationally efficient.
- [CNN model evaluation algorithm](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/CNN_model_Evaluation)


### Performance and reliability consideration

The computational demand of training a performing neural network model can be high if the given dataset is large. However, this is not so relevant in the testing section, and we provide a free method for training the model using [Colab](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Training%20neural%20network%20using%20google%20colab), which provides cloud computations with server-grade GPU. Therefore, the emphasis should be placed on computational costs of running both self-driving and image classification models in real-time while rendering the graphics of the donkey car simulator environment. Now, this depends on the CPU and the graphic cards of the computer. Performance issue is further We expect to see some discrepancies on the model’s performance among computers of different spec, especially in race condition.

The model should be reliable in the sense that it should minimise FP (false positives). False positive occurs when the model predicts a signed class label, while the image contains no signs. In such cases, the donkey car would behave abnormally. We will test this behaviour alongside with the previous part ‘sign detection in real time inside the simulator’. Here, we provide one possible solution in pseudocode to increase the reliability.

`if 100 * score (aka. confidence level) > 95:`
    `return class_name`
`return None`

In addition, we maintain a queue of size 10 for the detected signs, to improve the reliability of our model. Each time an image from the simulator is classified in real-time, its label is added to the queue. Our model will take the majority vote over the queue and predict that being the sign of the frame. 



## **Tools and additional processes to ensure quality** ###

#### Testing pipeline

Continuous integration is a crucial part of software engineering. In the earlier stage of the project, we did not establish a correct CI tool. This leads up onto many wrong tracks, wasting precious time and resources. Later, as required by the tutor, we integrated a CI tool called Pipeline into our Bitbucket repository. It automatically starts a build to run a newly pushed commit against a set of pre-written test cases.

![Screen Shot 2020-11-28 at 6.49.28 am.png](https://bitbucket.org/repo/G6xBMXK/images/1074845301-Screen%20Shot%202020-11-28%20at%206.49.28%20am.png)
(Failed build caused by failed test cases)

If there is a failed test case reported, the build will fail and the person responsible for the push will be notified and should correct any mistakes in the code that leads to the failure.

After the responsible individual corrects the bug(s) in the code, he/she can rerun the build.
![Screen Shot 2020-11-28 at 6.49.59 am.png](https://bitbucket.org/repo/G6xBMXK/images/674545938-Screen%20Shot%202020-11-28%20at%206.49.59%20am.png)
(If all test cases passes, the build will be successful)


We mainly use the Pipeline to test the accuracy of our machine learning model. If the accuracy of the model does not meet the lowest requirements, the test will fail and the programmer needs to check if the problem is caused by newly added code or contaminated training data.

By employing the benefit of CI and regression testing, the possibility of buggy code being pushed to the repository is eliminated. This saves the trouble of finding the initial source of the bug, resulting in code with high quality.

#### Bitbucket version control ####

Version control is another critical aspect of software engineering.  With the help of version control, we can revert the project back to a previous checkpoint. It could be that we need to restore a previous stable version or we want to abandon some experimental features.

Version control also allows team members to develop features on branches. This ensures the robustness of the master branch and there is always a working software ready to be delivered.

![Screen Shot 2020-11-28 at 6.51.00 am.png](https://bitbucket.org/repo/G6xBMXK/images/563459755-Screen%20Shot%202020-11-28%20at%206.51.00%20am.png)
(Team members developed features on different branches and merged them into the master branch)


Version control, together with continuous integration, ensures the quality of the code.

#### Dedicated repo and documentation for client deployment ####

There is a [separate repository](https://github.com/Yuanda-Dong/Client-Final-Deployment) containing the final version of codebase and documentation dedicated for the client. 

#### ShowReel ####
We produced an extra handover showReel for the client. [Link to the show reel](https://youtu.be/VxKC9a5ixNI)

## Quality of Group Process ##
### Setup of tooling for development 
#### Bitbucket and Git
Our team uses Atlassian Bitbucket for the collaboration and documentation of our project. This is the repository of our code base: https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/

With Bitbucket, we can update our code and inform other team members as soon as we push our code onto the repository and they can see it by pulling it down to their local branch. We have two branches in the repository: master and random_background_image. The master branch mainly stores our updated code of sign detection and improved donkeycar model, and the other branch keeps some background sign images for sign detection.

We use git to achieve a version control of our code. Git separates every different change made to the repository with a distinct commit object that represents a new change, such that we can distinguish which team member wrote which piece of code, and the effect of the change. Below is a part of our commit history:

#### Bitbucket Wiki
The wiki page of Bitbucket allows us to record and track any documentations we have regarding the project. Our group uses the wiki page to record our meeting minutes with the client and within our group, scope statement, blender and unity documentations, status reports and our personal weekly update videos, appendix B is a snapshot of our homepage.


#### Discord
Discord is our main communication tool for the project, we use Discord to discuss anything related to the project (questions, thoughts, etc) within our group and with the client to ask for any clarifications regarding the deliverables of each week and sometimes for help on the implementation. Discord allows users to create their servers for communication and multiple channels can be used in one server, we are in the server: Sydney2020 and our team channel for the project is: cp32-17b1, appendix C is a snapshot of our daily communication.


#### Slack (not used anymore)
We initially use Slack for communication amongst our team members, client and tutor, but our client prefers using Discord to communicate due to its convenience of communicating with multiple groups and sharing useful information amongst us due to the similarity and dependency of the projects we are doing.


#### Github
We also use github as our simulator and Blender/Unity codebase since bitbucket only supports 2GB of storage space, so we have to move our simulator-related work to a new github repository, appendix D is a snapshot of our github repository. The link to the repo is:
https://github.sydney.edu.au/moxu7046/COMP3988_simulator


### **Management and Allocation of Tasks**
Since our project is composed of the simulator and sign detection parts, we decided to ‘split’ our team into two squads: 

1. **sign detection squad** (Yuanda, Yiran, Hao) 
2. **simulator squad** (Peter, Nicole, Robert)

The sign detection squad is responsible for training and improving our sign detection model with various signs collected weekly from different training tracks, and test it against the test tracks. Yiran, Yuanda and Hao are in charge of developing/improving sign detection algorithms and fixing issues they met. Appendix E is a discussion on Discord amongst the sign detection people. Hao is also in charge of building the CI pipeline on our bitbucket repository as mentioned earlier, so that our code can be tested automatically.

The simulator squad is responsible for developing new tracks as required by the client plus the car model and other objects on the track (e.g. stadium, lake, tree, etc).  Peter is responsible for assembling all the objects on the track and adjusting the track using Unity so that everything in it is in the correct scale. Nicole and Rober are in charge of building different track objects on the tracks and improving the car model using Blender, so that they are close to the real world situation.

Besides that, sometimes we also need to manually classify track images collected into different signs, this job has been done by different squad members, including Hao, Yiran, Yuanda and Robert.

Below is our weekly plan for our process of task management:

1. Client meeting on Monday for requirement update  
2. Group meeting on Tuesday for allocation of work  
     1. Sign detection squad: Hao, Yiran, Yuanda  
     2. Simulator and models squad: Nicole, Peter, Robert  
3. Client meeting on Friday for progress update    
4. Occasional meetings amongst each squad on Zoom during the weekend  
5. XP roles allocation:  
     1. Manager - Robert  
     1. Tracker - Hao  
  
Although we split the work into the above two parts, they need to be merged together so that our work can be evaluated. This is done in the below workflow:

1. Simulation squad builds track objects in Blender as required  
2. Simulation squad assembles the objects in the track in Unity  
3. The simulator is deployed to different OS versions where the sign detection squad can collect  
4. Sign detection squad improves the detection algorithm and train the model using the newly updated tracks  
5. Sign detection squad tests the model using the new tracks and reflect on the result accuracies  

### **Collaboration and Teamwork**
Besides the above description of the sharing of actual tasks, we also adopt the extreme programming framework from agile development, that is, we define our scope statement for the project first, which can be found on our wiki page:
https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Scope_Statement_overall Appendix F is a snapshot of what it looks like.

After that we elicit user stories for a more specific description of what the client expects our product to achieve, our user stories can be found in the system specifications part. 

During Tuesday’s group meeting, our team separates the tasks to do for each week on different team members so that we can share the workload, appendix G shows the work separation of week n’s tasks given by the client on Monday’s client meeting.

Our team communicates and collaborates on Discord and occasional voice calls. During collaboration, we ask any questions and clarify them, and sometimes does pair programming, where one member shares their screen and does the programming, the other member watches and gives directions and clarifications, or raises issues. **Appendix H** describes some of our collaborations on Discord regarding result updates (figure H.1), algorithm discussions (figure H.2) and collaborative pair programming to solve issues (figure H.3).

During the second development cycle, we do not assign strict XP roles to each group member since our project is ML-oriented and does not fit to the traditional software development roles, but rather keep the XP roles flexible, therefore we have the following XP roles in our team:   
- manager: organises meetings and writes the minutes, an example of our meeting minutes can be found in appendix I.  
- tracker: track team progress and write status report, an example of the status report can be found in appendix J.  
- programmer: does the coding on sign detection, everyone in the group is programmer - this can be everyone in the sign detection squad that improves the detection algorithm (python code) or anyone in the simulator squad that builds the track objects (Blender operations) and assembles them in unity (Unity operations).  **Appendix K** shows the work of finishing the F1 car model in Blender, as a programmer’s task.  
- tester: test the implementation code and provide feedback - Hao is in charge of maintaining the pipeline unit testing on bitbucket but Yiran & Yuanda also tests the model detection accuracy which corresponds to the actual meaning of tests in ML.  
- doomsayer: provide warnings and advices on future issues/risks to group members - anyone can be doomsayer as soon as they are concerned about some certain issue  
- customer: represents the team to communicate with the client, due to the speciality of our project, everyone can directly asks the client their questions on Discord, however the customer role can still be adopted when communicating with the client on major events (e.g. meeting times) through email, an example can be found in **appendix L**.  


   - role: The XP roles that we adopt with variations included, we redefined these roles in this cycle, the manager and tracker are since some members are more familiar with some particular role and other XP roles are described above with different work:

- manager: Robert  
- tracker: Hao  
- Wiki maintainer: Yiran  

Since our wiki page determines our overall documentation style and therefore is critical when our supervisor (tutor) reviews it, we decided to add the wiki maintainer role to manage our wiki page to make it look more professional and organised.  

### **Risks and Constraints**
We encountered with the following risks and constraints during this development cycle:  

#### Issues and Constraints
1. Our sign detection algorithm had a low accuracy  
2. Unity does not recognise the paints on the model - this is a constraint that we have to work in another way to solve this  
3. Our Bitbucket repository once exceeded the limit of 2GB  

#### Progress
1. We use OpenCV to extract Region of Interest in a picture (**appendix N** displays our discussion on this)  
2. We adjust colour filters to get better accuracy  
3. We paint the model manually then bake the whole material during export, then the unity programmer can manually put the paints on the models, appendix O displays a critical step during the export step in Blender
4. We rolled back commits and put all simulator work on Github (**appendix M** displays our simulator release page on github)

### Client Interaction
We have the following client interaction methods:  

- Discord  
   -- Daily communication  
   -- ask questions and provide progress update  
- Email  
   -- Receive major requirement updates and client deployment information  
- Meetings
   -- Twice a week - on Discord  
   -- Monday - demonstrate work done and get new requirements  
   -- Friday - Show progress and ask questions  

We interact with the client frequently on Discord to ask any related questions and clarifications, **appendix P** (figure p.1 - figure p.2) documents a few client interactions.  

Other than direct communication on Discord, we also used emails to receive updates about new requirements or client deployment information, this can be found on **appendix Q**.  

**Appendix I** shows an example client meeting minutes on Monday, week 11.  

#### **Reflections on client interaction**:  
We work closely with the clients by responding to client’s new requirements promptly. The client replies to our request for consultation and discusses our questions actively. Overall, we believe we maintain a good interaction with the client.

### **Critiques and Reflections**

#### Communication 
Our team performed well in communication, both to fellow members using mainly Wechat and the client. Apart from discord (which is mainly used for client consultation and discussion), we communicate daily in our WeChat group chat to discuss any issues. Yiran and Yuanda performed very well on communication, Yiran will always remind group members about certain issues or events and provide her sign detection updates on Discord. Yuanda is very active on Discord since he communicated with the client a lot about sign detection issues he encountered or asking for clarifications.


We hold video conferences on Zoom meetings or voice calls regularly to discuss issues that require collaboration or teamwork. Communication between group members always gets fast responses and good solutions to issues. Robert, Nicole and Hao need improvements during the zoom conferences, since they don’t speak as much as Yiran does, despite them paying attention to the meeting very well. However, talking during the meeting can really make the meeting efficient since we will have different opinions.


Overall, our communication has no major issues.


#### Group process
Group members work closely together. Work loads are divided among members as discussed above and each member does what they are most good at to achieve the best efficiency. When a member has other commitments in a week, his/her workload is reduced and shared among other members. We ensure everyone is having a workload that they are comfortable with.

Everyone performed very well in their assigned tasks since there are no major delays for the handover of the work between each squad, despite that we are all busy with other assignments.

#### Progress update
As required by the client, we update our weekly progress with an individual weekly report page on wiki containing a summary video attached to it, each member updates their status frequently, this can be found on appendix R. The progress is also documented briefly in each week’s status report and submitted to Canvas. We believe that our progress update is thorough and effective both to our supervisor (Canvas) and to the client (Bitbucket).

Robert did well on updating the 3 (or 2) meeting minutes every week as his manager task, Hao did well on updating the weekly status report as his tracker task, and Peter and Nicole did well on updating their individual progress report each week and never delay them for too late.

#### Agile practice
All of us did better for adopting the XP framework than the last cycle. For example, our role allocation is very clear in this cycle since everyone is aware of what they should do each week, plus, we focused on updating our wiki page since the meeting minutes contain what we should achieve for each week. Moreover, we did well on organising every major event such as client deployment or demo videos. For example, everyone finished their part on the demo video slides in a timely manner and no delay occurred before the submission date.


We also did well in terms of daily agile practice. We have meetings with the client on the first working day of the week to reflect on our progress from last week to the client. We also demonstrate deliverables (if any from last week) to the client. On the last working day of a week, we have another meeting with the clients to discuss any difficulties we have during the week and report the plan for the weekend and the week to come.


## **Appendices**
Team member’s individual report on Wiki:  
Mouyi: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Mouyi  
Hao: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Hao  
Yuanda: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Yuanda  
Yiran: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Yiran  
Robert: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Robert  
Nicole: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Nicole  

### appendix A - Acceptance tests details   
#### Test 1: Autonomous driving in the simulator [Yuanda] 

Test description: To start experimenting with sign detection models, we need first build a simple autonomous vehicle in the simulator. We will test the performance of such a vehicle by measuring the duration for which the donkey car can self-drive without hitting any obstacles.

Test result: The footage is available here. On average, the donkey car is able to drive without hitting obstacles for about 40 seconds. The best result we recorded is 1 minute and 31 seconds.

#### Test 2: Automatic CNN model accuracy test[Yuanda] 

Test description: We test the accuracy of our CNN model through its performance on different sets of test data. The accuracy will be tested based on the confusion matrix and other statistical measures such as precision, recall and F1-score. There are 3 different sets of test data involving [stop, left, right, park, speed-50] signs as well as different colour variations collected from our custom tracks (Robotics Challenge Track and F1 tracks), real-world images, Shenzhen track (provided by client). The test script will be run each time a ‘push’ is made to our repository, this is detailed in the pipeline section. 
Test result: The following threshold values are used:  
true_positive = 0.85  
false_negative = 0.15  
precision = 0.95  
recall = 0.95  
f1 = 0.95  
Our model passed 3(datasets) × 5(statistic) tests. However, we relaxed the testing conditions for Shenzhen track, the precision, recall and f1-scores are tested using the weighted average over all signs, instead of testing these statistics for each type of signs.   
Structure of test data:
![Screen Shot 2020-11-27 at 21.56.07.png](https://bitbucket.org/repo/G6xBMXK/images/3972860528-Screen%20Shot%202020-11-27%20at%2021.56.07.png)

First set of test data result: 
![Screen Shot 2020-11-27 at 21.56.43.png](https://bitbucket.org/repo/G6xBMXK/images/3004057491-Screen%20Shot%202020-11-27%20at%2021.56.43.png)

Second set of test data result: 
![Screen Shot 2020-11-27 at 21.57.03.png](https://bitbucket.org/repo/G6xBMXK/images/3876158333-Screen%20Shot%202020-11-27%20at%2021.57.03.png)

Shenzhen track result: 
![Screen Shot 2020-11-27 at 21.57.23.png](https://bitbucket.org/repo/G6xBMXK/images/1850576267-Screen%20Shot%202020-11-27%20at%2021.57.23.png)

#### Test 3: OpenCV testing for image pre-processing (success rate of detect correct ROI)  
#### Test 4: CNN mo![Screen Shot 2020-11-27 at 22.10.16.png](https://bitbucket.org/repo/G6xBMXK/images/2551128326-Screen%20Shot%202020-11-27%20at%2022.10.16.png)del accuracy (simulator signs[F1], real-world signs [Shenzhen])  
#### Test 5: OpenCv draw bounding box correctly in simulator 

Test description: It’s important that the openCV (based on sign colours) can extract the correct region of interest (ROI), before feeding into Tensorflow for sign detection. We will test the performance of OpenCV extraction in the simulator by drawing bounding boxes around the detected ROI. We will run the simulation and draw bounding boxes in real-time to see how much ROIs were extracted correctly. 

Test result: OpenCV is able to successfully extract the signs if the sign is the largest area contours based on colour filters. However, since we added the black filters, it introduced a lot of noises to openCV results. OpenCV will return many non-sign ROI to CNN models. The footage is available here. However, our CNN model is able to distinguish between sign and non-sign ROIs.  

#### Test 6: Stable testing result in different map (Robotics Challenge and F1 tracks) 
Test description: Given the accuracy of the CNN model, and openCV extraction is tested, the next step in our plan is to test whether the model when fed into a data stream of camera images, is able to predict the label class in real-time. We will test whether these camera images are correctly classified, by printing the class label to the console while drawing bounding boxes in real-time.

Test result: The footage is available [here](https://youtu.be/4KhhqXZcjRE). The test was overall very successful. It shows the generalisation capabilities of our current approach (OpenCV + CNN). Our model has stable sign detection results in F1 tracks, despite the fact that the training data is gathered from the Challenge track.  

#### Test 7: Custom built track has the correct physics 
Test description: We will test whether the track we built responds to user input(via keyboard for driving)/object collision reasonably using the physics in Unity. To do this, we will divide the test into normal/abnormal test cases, where the normal test case looks at how accurate the donkey car responds to user inputs and manages to drive around the map. This will involve driving in a straight line turning and braking. In the abnormal case, we will intentionally drive the donkey car to hit the poles of traffic lights/signs, and walls to check the object collision.

Test result: The footage is available [here](https://youtu.be/h16BiZ5xd50). The donkey car’s response to keyboard input is sound, it managed to drive in a straight line, turning and braking. Object collision is tested with all the traffic signs and traffic lights, most of the object collides as expected, except for the parking sign.

#### Test 8: Donkey car can respond accordingly to the sign 
Test description: Donkey car should stop by reducing the throttle value, after a stop sign is detected. Similarly, the donkey car should turn left/right when a left/right sign is detected. This can be tested by running the image detection model and self-driving model at the same time in the custom map containing traffic signs. Then, we will print out the actual throttle and angle values received by the donkey car, and observe the behaviour of the donkey car.

Test result: The footage is available [here](https://youtu.be/hWSs6zBgu_s), the terminal output is available [here](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/test/Driving%20and%20Sign%20detection/out) We saw a decrease in throttle value below zero after a stop sign is detected, and observed the stopping behaviour of the donkey car. A positive (closer to 1.0) steering angle, and a small negative steering angle is outputted when right/left signs are detected respectively. Donkey car managed to make the left/right turns.

### Appendix B - wiki page layout
![Screen Shot 2020-11-27 at 22.02.21.png](https://bitbucket.org/repo/G6xBMXK/images/1687274361-Screen%20Shot%202020-11-27%20at%2022.02.21.png)

### Appendix C - Discord daily communication
![Screen Shot 2020-11-27 at 22.02.49.png](https://bitbucket.org/repo/G6xBMXK/images/651227640-Screen%20Shot%202020-11-27%20at%2022.02.49.png)

### Appendix D - Github simulator repository
![Screen Shot 2020-11-27 at 22.03.12.png](https://bitbucket.org/repo/G6xBMXK/images/131683973-Screen%20Shot%202020-11-27%20at%2022.03.12.png)

### Appendix E - Sign detection discussions
![Screen Shot 2020-11-27 at 22.03.31.png](https://bitbucket.org/repo/G6xBMXK/images/3085793659-Screen%20Shot%202020-11-27%20at%2022.03.31.png)

### Appendix F - scope statement
![Screen Shot 2020-11-27 at 22.04.10.png](https://bitbucket.org/repo/G6xBMXK/images/81842237-Screen%20Shot%202020-11-27%20at%2022.04.10.png)

### Appendix G - task allocation
Week 9’s task allocation after week 9 tuesday’s group meeting.  
![Screen Shot 2020-11-27 at 22.04.47.png](https://bitbucket.org/repo/G6xBMXK/images/1290479609-Screen%20Shot%202020-11-27%20at%2022.04.47.png)

### Appendix H - Collaborations
(figure 1 - result updates)  
![Screen Shot 2020-11-27 at 22.05.13.png](https://bitbucket.org/repo/G6xBMXK/images/452345770-Screen%20Shot%202020-11-27%20at%2022.05.13.png)

(figure 2 - algorithm discussions)
![Screen Shot 2020-11-27 at 22.05.34.png](https://bitbucket.org/repo/G6xBMXK/images/2104685981-Screen%20Shot%202020-11-27%20at%2022.05.34.png)

(figure 3 - collaborative programming to solve issues w/ liveshare on VSCode)
![Screen Shot 2020-11-27 at 22.05.52.png](https://bitbucket.org/repo/G6xBMXK/images/410235059-Screen%20Shot%202020-11-27%20at%2022.05.52.png)

### Appendix I - Meeting minutes (Week 11)
![Screen Shot 2020-11-27 at 22.06.14.png](https://bitbucket.org/repo/G6xBMXK/images/3473889635-Screen%20Shot%202020-11-27%20at%2022.06.14.png)

### Appendix J - Status report (week 10)
![Screen Shot 2020-11-27 at 22.06.34.png](https://bitbucket.org/repo/G6xBMXK/images/133084583-Screen%20Shot%202020-11-27%20at%2022.06.34.png)

### Appendix K - Blender car model work
![Screen Shot 2020-11-27 at 22.06.57.png](https://bitbucket.org/repo/G6xBMXK/images/1703779483-Screen%20Shot%202020-11-27%20at%2022.06.57.png)

### Appendix L - Email communication (meeting info update from client)
![Screen Shot 2020-11-27 at 22.07.16.png](https://bitbucket.org/repo/G6xBMXK/images/724975766-Screen%20Shot%202020-11-27%20at%2022.07.16.png)

### Appendix M - Simulator repository on Github
![Screen Shot 2020-11-27 at 22.07.33.png](https://bitbucket.org/repo/G6xBMXK/images/2003845890-Screen%20Shot%202020-11-27%20at%2022.07.33.png)

### Appendix N - Sign extraction with OpenCV discussions
![Screen Shot 2020-11-27 at 22.07.53.png](https://bitbucket.org/repo/G6xBMXK/images/429034359-Screen%20Shot%202020-11-27%20at%2022.07.53.png)

### Appendix O - Blender export step
![Screen Shot 2020-11-27 at 22.08.21.png](https://bitbucket.org/repo/G6xBMXK/images/714567110-Screen%20Shot%202020-11-27%20at%2022.08.21.png)

### Appendix P - Client interactions on Discord
(figure p1 - Discussion about an online GPU rendering application with the client)
![Screen Shot 2020-11-27 at 22.09.56.png](https://bitbucket.org/repo/G6xBMXK/images/3660615588-Screen%20Shot%202020-11-27%20at%2022.09.56.png)

(figure p2 - Client explaining about the ROI (region of interest) functionality on OpenCV)
![Screen Shot 2020-11-27 at 22.11.26.png](https://bitbucket.org/repo/G6xBMXK/images/2122976673-Screen%20Shot%202020-11-27%20at%2022.11.26.png)

### Appendix Q - Client interactions with email
(Client providing information about the final client deployment)
![Screen Shot 2020-11-27 at 22.11.46.png](https://bitbucket.org/repo/G6xBMXK/images/196287057-Screen%20Shot%202020-11-27%20at%2022.11.46.png)

### Appendix R - Individual weekly report
(Extracted from Peter (Mouyi)’s report on week 11)
![Screen Shot 2020-11-27 at 22.12.08.png](https://bitbucket.org/repo/G6xBMXK/images/1702936708-Screen%20Shot%202020-11-27%20at%2022.12.08.png)