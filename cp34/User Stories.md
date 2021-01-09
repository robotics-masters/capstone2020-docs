# Developers #
## Goals and plan for the project as a developer ##
- As developers, they should be able to have working simulators with both ArduPilot and PX4 environments so that the model can be tested in two different environments.
- As developers, they should have the ability to do path navigation based on coordinates or point to point in the simulators because it is an important first step for further research of optimal paths.
- As developers, they should be able to model the battery life of the drone into the simulator or the algorithm to achieve more accurate and relevant information in real-world scenarios.
- As developers, they should be able to model weather conditions into the simulator in order to derive more accurate and relevant information in real-world scenarios where there are complex environmental variables.
- As developers, they need to have a plan on how to achieve the optimal path and include base stations and proof of concepts in the simulator.
- As developers, they are expected to properly document the process of development. Meeting minutes, status reports, and weekly video reports. This helps to keep track of the progress and provide insights on what to do in the following week.
---
# Users #
## The expectations of the User and what the User wants from the project ##
1. As a user, I want to be able to use both ArduPilot and PX4 drones for delivery so I have a broader choice of drones.
1. As a user, I want the Gazebo simulator to be fully functional and configured with PX4.
1. As a user, I want the Gazebo simulator to be fully functional and configured with ArduPilot.
1. As a user, I want to be able to install and set up the software and environment for the project easily.
1. As a user, I want to be able to control the drone by doing coordinate based or point to point navigation in the simulator.
1. As a user, I want to be able to have different weather conditions in the simulator so that I can simulate the delivery in different environments.
1. As a user, I want to have a plan of how to achieve the optimal path and include base stations and proof of concepts in the simulator.
1. As a user, I want to have a charging station model in the Gazebo simulator so that I know what a charging station looks like.
1. As a user, I want to be able to control the drone using code/scripts so that I don’t have to manually control the drone.
1. As a user, I want to be able to create worlds in Gazebo with variable spawning locations for charging stations and delivery waypoints.
1. As a user, I want an autonomous drone flight to be possible so that the whole delivery process is automated.
1. As a user, I want documentation for placing objects such as signs, traffic lights, objects so that I can place objects myself.
1. As a user, I want to have multiple drones in the simulator at the same time so that I can use multiple drones for delivery.
1. As a user, I want a primitive detection/model working on 4 signs (stop, turning, parking, traffic lights).
1. As a user, I want the drone to be able to do an autonomous flight with detection active so that it does not crash into anything.
1. As a user, I want the drone to be able to fly to any number of destination and return home so that it can deliver multiple packages on one trip.
1. As a user, I want landing pads to be modeled into the simulator so that I know when the drone is landing at a destination.
1. As a user, I want the drone to stay on the charging station for a period of time so that I know the drone is being charged.
1. As a user, I want the Gazebo world generator to pass the location of the charging station and landing pads (destinations) to the optimal path algorithm so that the algorithm knows the coordinates it needs to work with.
1. As a user, I want a way to charge the drone's battery in the simulator when it is at a charging station so that an accurate representation of the drone's battery is shown.
1. As a user, I want the battery to be enabled in PX4 so that I can see the battery percentage.
1. As a user, I want the system combined and have a single point of execution so that all components will work together automatically.
1. As a user, I want all 12 unique objects that were outlined in the table to be detected so that the drone can recognise the objects.
1. As a user, I want the drone to take appropriate corresponding action when it detects an object so that it behaves in a specified way.
1. As a user, I want instructions/demo videos showing the process to import new objects and create worlds so that I can create environments myself.
1. As a user, I want a completed project demo showcasing all functionalities so that I know the project meets the requirements.
---
# Acceptance Criteria

| User Story | Acceptance Criteria |
| -- | -- |
| 1 | Be able to configure ArduPilot and PX4 without errors. |
| 2 | Be able to open Gazebo through PX4. Be able to use Gazebo and with all it's functionality with PX4. |
| 3 | Be able to open Gazebo through ArduPilot. Be able to use Gazebo and with all it's functionality with ArduPilot. |
| 4 | Be able to run the installation script without errors. Be able to follow the documentation and run Gazebo and intended without errors. |
| 5 | Be able to use the mission script to control the drone without errors. Have the drone fly as it is intended to bypassing the desired coordinates and locations. |
| 6 | Have the drone be affected by the weather in the simulator. Be able to control the weather parameters in Gazebo. |
| 7 | Have clear documentation on the algorithm and it's techniques. Have phases of algorithm documents describing the evolution of the algorithm which explain how it computes the path. Have videos demonstrating proof of concepts such as the drone navigating the optimal path as computed by the algorithm. |
| 8 | The model should be a distinct object recognisable as a charging station. The model should be spawnable in any Gazebo world. The drone should be able to land on this object. |
| 9 | Have a script to connect to the drone and have it fly as desired. Have a script that can take in a computed path and have the drone navigate the path as directed. |
| 10 | Be able to generate destination objects and charging stations either randomly or at specified locations in a given Gazebo world file. Have the drone navigate within this generated world. |
| 11 | Have the drone by completed automated and follow a given route. Have the drone drop down to the desired height in order to simulate either charging or dropping off a package. |
| 12 | Have documentation on how to use the world generator. Have documentation on how to place objects in Gazebo. |
| 13 | Be able to control multiple drones in Gazebo with scripts, one at a time, and simultaneously. |
| 14 | Be able to identify signs in Gazebo. Be able to differentiate the different types through a notification message or output. Be able to make the drone do something depending on which object it sees. |
| 15 | The drone should stop when it reaches an object standing in its path and make a decision as to where it should go next. The drone should automatically decide on its route and complete the given path regardless of the obstacles in the way. |
| 16 | The drone should visit the waypoint(s) in the order it is told, lower down, and rise back up, making its way to the next waypoint or home, and charge at a charging station when necessary. The drone should return home when it has completed it's route. |
| 17 | Landing pads should be visible in Gazebo. Landing pads should be spawnable at a random location or given coordinates. The drone should be able to land on these landing pads. |
| 18 | The drone should wait at these charging stations for a short period of time before taking off again. |
| 19 | The generated coordinates of the waypoints and charging stations should be written to a file. The file should be readable by the algorithm. |
| 20 | The drone waiting time should vary depending on the current battery length to simulate accurate relative charging times. |
| 21 | The battery should be visible in the hub of Gazebo or QGroundControl. The battery should increase and decrease when appropriate. |
| 22 | There should be a single script that generates the waypoints and charging stations and starts Gazebo. There should be a single script which connects to the drone and flies it. |
| 23 | Each object should be placeable and recognisable by the drone. A notification or terminal output should be seen when one of these objects is recognised. |
| 24 | The drone should be able to react to any specific object in the most appropriate way. |
| 25 | Videos explaining how to create objects and spawn objects in Gazebo. Videos getting the viewers familiar with the Gazebo file directory structure, i.e. the worlds file and models file. |
| 26 | A video demonstrating the project working in full with voice over guiding the user. |