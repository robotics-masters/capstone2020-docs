# Individual Report -- Zhiyi Song #

XP roles I have taken

 - Tester -- test works done by other group members.
 - Programmer -- do the development, writing documents for completed items.
 - Doomsayer -- find the risk our group are facing and help to solve it.

## Contribution ##

### Technical ###

Although this project is mainly about objection detection, we need a working simulator and world to simulate the process.
The project can be diveide into 3 parts, simulatior setup and simulation world development and maintance, OpenCV objection detection and TensorFlow objection categraization.

Weekly breakdown:

 - **Week 2**
   - setup development environment
 - **Week 3**
   - [setup px4 and mavsdk-Python](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/Set-Up%20(Ubuntu%2018.04)) (px4, mavsdk-Python and streaming with QGC section)
   - some traffic sign modelled
 - **Week 4**
   - [All traffic sign modelled](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/268deb9a6d128f51ec721f7af3776f83b85b8bb2)
   - [demo video](https://youtu.be/LvALBdcM4KA)
 - **Week 5**
   - Traffic Light Controller
     - [the controller itself](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/41864fa1609582e540d01fb289c9ca3ecab0c5ce) also [PR #5](https://bitbucket.org/zson5784/comp3988_t17b_group_5/pull-requests/5)
     - [Documentation for controller](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/Traffic%20Light%20Control%20Plugin.md)
     - [demo video](https://youtu.be/Ds3Da5b4x38)
 - **Week 6**
   - integrating video capture, drone and world together and Start up script for simulation.
     - [commit 08459c6](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/08459c632d8772f85e70425c7ac5de1c307dbffe) also [PR #7](https://bitbucket.org/zson5784/comp3988_t17b_group_5/pull-requests/7)
     - [wiki for startup script](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/Start%20Simulation.md)
   - [Start development precise drone control](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/44e3c6fbd2005a90b1d85af9c4488eb1cbcfe329)
   - Improve traffic sign model
     - commit [d9853af](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/d9853af4e25bbac65415d83255ed0355ff7dde17), [c1ea742](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/c1ea7426b0fa74aad6a5309042c1aa2d55c366a5) and [6fc3fd9](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/6fc3fd9bd8aeb7846a03ea674fd2d30cb79dd9e5)
 - **Week 7**
    * Manual Controller [66be9b9](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/66be9b9e975e706878f8066ed6645c41bc056caf)
 - **Week 8**
    * Manual Controller [6ac7c29](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/6ac7c29e5c6fe027c321ef5ba06ad0da558a3ea3)
 - **Week 9**
    * collecting data for trainning model [data](https://drive.google.com/drive/folders/1NeOuPnEkn5OfmxDkQvhphWcYZutKVZ_Q?usp=sharing)
 - **Week 10**
    * Intergration test framework [465995f](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/465995f39447fd1e4ee90f57f4999f0cf353e790)
 - **Week 11**
    * opencv filter [c745d58](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/c745d5879d3226f5407bc2d26b5cfe9934033e09), [demo video](https://youtu.be/MTeDqtkY4a0)
 - **Week 12**
    * collecting data for trainning model [data](https://drive.google.com/file/d/1gN5BMscKR1PJ1508m4aI2EIglZJvHEyJ/view?usp=sharing)

### Non-technical ###

 - [managing team wiki](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/history/Home)
 - [Week 3 status report](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/Project%20Status%20Report/week03.md)
 - [Writing user stories](https://trello.com/b/Y8qWmnWG/user-story)
 - Some Client communication (Most are done by Gio)
 - Client deployment
 - present on Final Client Demostration


## Reflection ##

### Programming ###

The first 2 weeks are for are for setting up development environment and make sure it is working, therefore, there are not much programming involved.
The 3rd week I spend my time on modeling traffic signs to  be used in simulation.
My programming  starts at the end of week 4, where I am writing a c++ plugin for our simulatior to control traffic light exterally.
On week 6, I started writing startup script for simulation and precise control for drone.
The code style for my c++ code is Linux coding style and for python is PEP-8 style.
We are using code reviewing and testing by other group member to ensure code quality.
Every branch to be merged have to be reviewed.
Issues will be created by reviewer as comment and I need to fix it before merge.
However, testing is hard to implemented as our project is GUI oriented and based on neural network.

On week 7 and week 8, as we find it is not convient to collect trainning data from the simulator by snapshot the popped up opencv window.
And it is not convinent to move drone with script or move by gazebo's builtin 3D editor.
I developped a drone controller allowing manual controling and snapshot using keyboard.
The controller fasten the process for collecting trainning data for our project.

On week 11 and 12, I worked on implementing OpenCV filter for TensorFlow model.
Because images from the raw video stream contains too much noise for the TensorFlow model,
It is essential to filter out some noises before images were fed into TensorFlow model.
The OpenCV approach in this project is quite strait forward, as we do not need a very good
accuray with the OpenCV filter and all traffic signs are some polygon or circle with some
noticable color. We can filter traffic signs by applied a color filter follow by a shaple filter.

### Version Control ###

Version control for this project is managed on bitbucket with git.
We are using bitbucket as an issue tracking system as well.
All new development is conducted on branches and merge into master after code review.

### Extreme Programming ###

Our project did not involve with much programming in the first few weeks.
So, the extreme programming concept are not that helpful for our project.
We tried our best to follow the principle.
I am as tracker one week 2, however, on this week all of us are trying to setup development environment.
We have role rotation which is documented [here](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/Role%20Rotation.md).

### Communication and collaboration ###

Communication is done mainly on messenger group chat for instant messaging.
Group members can reached out each other quickly.

The client created a discord server and [channel](https://discord.com/channels/750412538637975633/751799048914206732) for every groups working in drone simulation.
There is also channels for all tensorflow teams, and resource sharing channel on that server.
This server is the perferred communication way of client.

---

### Challenges ###

#### Hard to setup development environment ####

The simulator and the development environment are hard to setup, as the documentations are too Linux-distro specific, ubuntu 18 is only tested Linux-distro for our development environment.
Virtualization is not a good solution for this issue, because our development requires dedicated Nvidia graphic card with recent Cuda support for both 3D acceleration and training neural network.
I must install a new Ubuntu 18 on my computer.
Meanwhile the documentation is poor as many issues involved during the setup.
There is no good solution for this, but spend more time trying.
Boswell and I spend some time on setup and write our own setup guide to save other group members’ time.

#### No knowledge on this domain ####

In this project, we are using OpenCV and TensorFlow as object detection backend.
I have never used there two tools before.
Aside from this, I also have to learn modelling 3D model, making textures for 3D model,
the SDFormat which is used for Gazebo rendering 3D mode, Gazebo plugin framework for traffic light controller.
As drone industry is new and everything are under active development, documentations for tools in this area are poor.
I need to dig into source code to find documentation I needed.

Computer vision and neutral network are completely two new domain to me.
After this project, I have a basic knowledgement of OpenCV,
but still, because lack of time, I don't have time to learn TensorFlow.

#### Insufficient Time ####

The duration for this project is only 13 weeks, which is not sufficient considering all group member has other courses and the complex natura of this project.
The project involved with many domains, software development, machine learning and many other miscellenous skills such as 3D modeling, image editing.
