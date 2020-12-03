# User Stories #

These are the user stories that are relevant to our team's project and are made more explicit in the Scope and Requirements Document provided to us by the client.

**Track Additions in the DonkeyCar Simulator**
As a user of the DonkeyCar simulator, I want four new track layouts incorporated into the simulator, so that I have more environments for driving and testing additional software.

**Automated Driving**
As a user of DonkeyCar simulator, I want to have a driving model trained on the new tracks using the ``gym-donkeycar'' software package so that the car can drive around the tracks autonomously.

**TensorFlow Sign Detection Data Collection**
As a machine learning developer, I want to be able to collect sign-tagged images from the simulated camera in the DonkeyCar simulator into large datasets, so that I can train neural network detection models.

**TensorFlow Sign Detection Training**
As a machine learning developer, I want to be ability to train my neural network on both simulated and real datasets of any reasonable size, so that the trained detection model can be easily adapted to have satisfactory performance on new data sources.

**TensorFlow Sign Detection Inference**
As a user of the DonkeyCar simulator, I want the car to use TensorFlow to accurately detect and report common traffic signs and objects, so that I time the initiation of corresponding autonomous behaviours.

**Creation of Traffic Sign Objects for the DonkeyCar Simulator**
As a user of the DonkeyCar simulator, I want traffic sign objects created with Unity and Blender and incorporated into the simulator, so that the environments I drive in are more realistic and facilitate testing of sign detection software.

**Simple Action Responses to Traffic Signs**
As a user of the DonkeyCar simulator, I want the model car to perform simple reactions upon reaching certain traffic signs in the simulator, including stopping at a stop sign, turning left at a left sign and right at a right sign, so that the car can exhibit autonomous behaviour.

**Autonomous Parking Response to Park Sign**
As a user of the DonkeyCar simulator, I want the model car to perform a simple parking routine when it encounters a park sign in the simulator, so that the car exhibits autonomous behaviour.

**Simple Collision Avoidance Response to Traffic Cones**
As a user of the DonkeyCar simulator, I want the model car to drive around orange traffic cones, without collision, when it encounters them in the simulator, so that the car exhibits autonomous behaviour.

**Traffic Light Responses**
As a user of the DonkeyCar simulator, I want the model car to react by stopping or slowing to standard red-yellow-green traffic lights when it encounters them in the simulator, so that the exhibits autonomous behaviour.

**Report Speed in Response to Speed Signs (Advanced)**
As a user of the DonkeyCar simulator, I want the model car to report its speed according to the numbers on speed signs when it encounters them in the simulator, so that this will support autonomous behaviour in the future.

**Detection of Other Vehicles (Advanced)**
As a user of the DonkeyCar simulator, I want the the simulator to report to me whenever a vehicle is detected within the line of sight of the model car, so that I can use this information for autonomous behaviours that may be implemented in the future.

**Random Traffic Cone Placement**
As a user of the DonkeyCar simulator, I want to be able to drive in an environment where traffic cones are randomly distributed on the track, so that I can test the performance of autonomous collision avoidance behaviours.

**Model New Donkey Car**
As a user of the DonkeyCar simulator, I want to be able to drive a new Donkey Car model in the simulator, so that I have more variety and options when using the simulator.

**Track and Object Import Automation Improvements**
As a DonkeyCar simulation developer, I want the track creation and object import pipelines to be more automatic, so that it takes less effort to create and improve simulation environments in the future.

**Real World Sign Detection and Reaction**
As a developer in the autonomous car industry, I want to be able to test the traffic sign detection and reaction software, developed for this project, on a real Donkey car, so that I can demonstrate real world capabilities.
