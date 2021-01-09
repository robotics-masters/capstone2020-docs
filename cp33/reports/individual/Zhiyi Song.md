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


### Non-technical ###
 - [managing team wiki](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/history/Home)
 - [Week 3 status report](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/Project%20Status%20Report/week03.md)
 - [Writing user stories](https://trello.com/b/Y8qWmnWG/user-story)


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

All group members are in a messenger chat which allow us to reach each other quickly.
As we can reach each other quickly, no issues are created so far, group member will contact the one who is developing certain component via messenger chat.

We divided our group into small teams to work on specific topic of our project.
Boswell and I are working on [developing world for simulation](https://bitbucket.org/zson5784/comp3988_t17b_group_5/pull-requests/6).

The client also created a discord server and [channel](https://discord.com/channels/750412538637975633/751799048914206732) for every groups working in drone simulation.
We contact our client on that channel as well.

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
Aside from this, I also have to learn modelling 3D model, making textures for 3D model, the SDFormat which is used for Gazebo rendering 3D mode, Gazebo plugin framework for traffic light controller.
As drone industry is new and everything are under active development, documentations for tools in this area are poor.
I need to dig into source code to find documentation I needed.


### future improvements ###

The progress of our project is bit behind, mainly due to the challenges we have in the fisrt two weeks. In the next half of the project, we need to speed up the development. And integrate OpenCV detection as soon as possible.
