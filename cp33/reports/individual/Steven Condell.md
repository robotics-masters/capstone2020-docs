# Individual Report 1 -- Steven Condell

## XP Roles

Throughout the project, I have been responsible for the following XP roles:

* Tester: Responsible for implementing tests for code
* Doomsayer: Repsonsible for pointing out when things are going wrong
* Programmer: Responsible for implementing user stories

In terms of roles more specific to the project, I have been assigned to work primarily on the design and training of neural networks for classification of data, along with Gio and Martin. Full information on role allocations can be found [here](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/Role%20Rotation).


## Technical Contributions

* **Setting up the simulator (Weeks 3-4).** My initial focus was on getting the required software set up on my machine. This involved setting up a virtual machine with Ubuntu installed and then installing Gazebo, PX4 and other programs. I encountered issues with the VM being too slow and then had to relocate to a different device in order to get things running at an acceptable speed.

* **TensorFlow setup (Weeks 4-5).** I worked on trying to get TensorFlow set up and looked into using Google Colab as an alternative for using TensorFlow with GPU locally, finding that Google Colab was a viable alternative.

* **Neural network development (Weeks 5-6).** I worked with Gio and Martin on designing and building the initial neural network, including finding appropriate data to use for training of the network.


## Non-Technical Contributions

* **Writing meeting minutes.** Along with Gio, I have been responsible for writing meeting minutes at all group meetings. See, for example:
	- [Week 5 Tuesday minutes](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/minutes/week05-tuesday.md)
	- [Week 5 Friday minutes](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/minutes/week05-friday.md)
	- [Week 6 Tuesday minutes](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/minutes/week06-tuesday.md)

* **Creating report and presentation outlines (Weeks 5-6).** I created a rough version of the report and presentation due this week in the form of a scaffold tailored to our project with a dot point summary of all of the necessary content and helped allocate group members to complete the parts of the report/presentation that were most appropriate for them to complete.



## Quality of technical work done
As our system is primarily based around real-time movements of a drone, it is quite difficult to set up a rigorous testing framework. We are working to develop 
unit tests for our neural networks. A general acceptance testing framework is something that the group is prioritising in the coming weeks.


## Individual Reflections

### Version Control
We are using BitBucket for version control. In the early weeks of the project we did not make much use of BitBucket as our primary focus was on getting set up locally. However, as the project has progressed the group has started to make more use of it. Personally I have been struggling with contributing anything worthwhile in terms of actual implementation/code and so my history on BitBucket is quite lacking; this is something I am looking to improve on over the next two weeks.


### XP
As the majority of our time in the early weeks of the project was consumed by getting set up, we did not make very strong use of XP principles in terms of having distinct roles for each individual in the team. However, as the project has progressed into the stage where we are actively working to develop and complete user stories, the XP roles system is becoming more applicable. In particular, I think the customer role is a useful one, encouraging smooth communication with the client via a consistent group representative.


### Challenges
Probably the biggest challenge we encountered as a group was the difficulty in getting all of the required software set up on everyone's devices. There were compatibility issues with the software on different operating systems, and in the early weeks of the project, it was difficult to make progress as most team members were spending most or all of their time trying to get set up. We overcame this by getting everyone to run Ubuntu, either via VM or dual boot, as all of the software works well with this operating system.

A challenge for me personally has been trying to get acquainted with the neural network/TensorFlow background knowledge required to contribute effectively to the project. I have been overcoming this by doing my own research and discussing things with group members Gio and Martin when I am unsure, but this is a challenge that I am still struggling with.


### What I hope to improve
My contribution to the group on the technical side of things has been insufficient in the early weeks of the project. This is primarily due to the fact that, while I have chosen to be allocated to the neural network/TensorFlow aspect of the project, I have no experience in this area. Thus, while I have been contributing to discussions about this aspect of the project, I have not contributed much to the implementation/code for the project so far. I would like to change this over the coming weeks.

Another aspect of the project that I would like to handle differently is the way we communicate. So far, we have been alternating between a variety of channels for communication within the group: a Facebook Messenger group chat, a Slack channel, and a Discord channel run by the client. Communicating on all of these different channels has become confusing at times and makes it difficult to track where everyone is up to and what communications have occurred. Thus, going into the second half of semester we plan to focus our communication on our Slack channel and minimise communication via the Messenger chat, in order to keep our communication more formal, structured and unified.