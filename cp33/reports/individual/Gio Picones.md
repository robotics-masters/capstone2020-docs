# __Individual Report – Gio Picones__ #

This is the First Project Report (Individual) for Gio Picones, due Sunday 4th October 2020.  

### XP Roles ###

- Doomsayer -- This role involved making sure that the team knew the risks involved with the project, and potential areas where we would have trouble. This includes the many different different layers of software this project would require, and the difficulty of setting everything up, and later integrating all the moving parts. These were discussed in the kick-off meeting.

- Manager -- This role involved making sure that each member of the team was up to date with the work so far, and ensuring that we were making progress, and assisting members where necessary. These are discussed during meetings.

- Customer -- This role involved leading team meetings with clients, updating the client on work done and work to be done, and ensuring that the team was clear with what the client expects, with these being translated to user stories.

[evidence_customer_1.png](https://bitbucket.org/repo/jkq4oxG/images/985925984-evidence_customer_1.png)

[evidence_customer_2.png](https://bitbucket.org/repo/jkq4oxG/images/222744918-evidence_customer_2.png)

[Role
rotations](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/Role%20Rotation.md) 


## Contribution ##

### Technical ###

The project has two main components - building a simulated world in Gazebo with traffic signs and a simulated drone with a camera, and building/training a neural network in TensorFlow which would make predictions based on the drone's camera feed. I played a key role in the TensorFlow component. 

### Week 3 ###

- Dual-booting Ubuntu 18.04

- Initial setup of development environment (Gazebo, PX4) using Zhi Yi/Boswell's setup guide.

- Note: Work done this week was what was actually intended to be done.

### Week 4 : Initial Neural Net Setup ###

- [Set up TensorFlow GPU locally](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/tensorflow_GPU_setup)

- [Initial neural network using Cian's data](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/bb2ffd943e2da4fc2d0dce324f1e0d3defa38f1b) also [PR #4](https://bitbucket.org/zson5784/comp3988_t17b_group_5/pull-requests/4/initial-neural-net-with-some-data)

- [Demo video](https://www.youtube.com/watch?v=ZnC8gs_pmeo&feature=youtu.be)

- Note: Work done this week was what was actually intended to be done.

- This week's work is linked to this [user story](https://trello.com/c/5lNadSI6/2-user-able-to-define-which-dataset-to-train-from-and-define-how-many-classes-there-are-when-choosing-to-build-a-neural-network-fr).

### Week 5 : Data Cleaning ###

- [Manually cleaned and categorised Cian's data](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/f11798d541ac953799707412971e9f02386cc4dd) and then re-trained the model.

- [Demo video](https://www.youtube.com/watch?v=3u_x2S2db4g&feature=youtu.be)

- This week's work is linked to this [issue](https://bitbucket.org/zson5784/comp3988_t17b_group_5/issues/6/data-cleaning).

- Note: Intended to start on integration this week but did not have the time, was done in the next week.

### Week 6 : Integration/Realtime Prediction ###

- [Python script](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/55fbefb4ae9ac2820d20a1d8570bb1ae8c5bba71) to extract frames from the Drone camera

- [Built dataset of training data](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/55fbefb4ae9ac2820d20a1d8570bb1ae8c5bba71) using the above Python script, and then re-trained the model, and saved the weights

- [Python script](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/55fbefb4ae9ac2820d20a1d8570bb1ae8c5bba71) to load in the saved model, and do predictions in realtime, based on input frames from the drone camera while the drone is active.

- This week's work is linked to this [issue](https://bitbucket.org/zson5784/comp3988_t17b_group_5/issues/5/sign-detection-integration) and this [user story](https://trello.com/c/V2fLbYZs/12-as-a-client-i-need-100-object-detection-rate).

- Note: Intended to train on images of signs this week but had trouble with Gazebo 9 (issue on their end - Gazebo 9 dependencies are recently broken on the Ubuntu apt repo), so I had to make do with Gazebo 11 which crashes when I load in specific models. This week I trained on images of fountains.


### Non-technical ###

- [TensorFlow GPU setup guide on the Wiki](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/tensorflow_GPU_setup)

- [Kickoff Meeting Minutes](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/minutes/week01-kickoff.md)

- [Week 4 meeting 1 minutes](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/minutes/week04-tuesday.md)

- [Week 4 meeting 2 minutes](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/edit/minutes/week04-friday)

- [User Stories](https://trello.com/b/Y8qWmnWG/user-story)

- Leading the agenda of all team meetings


## Quality of technical work done ##

To ensure code quality, we make sure to make a pull request and ask a team member to do a code review before merging branches into master. Here's an [example](https://bitbucket.org/zson5784/comp3988_t17b_group_5/pull-requests/4) where I made a pull request before merging the initial neural network branch. 

The nature of this project makes it hard to do traditional unit-testing for the section I'm in charge of. For example, given the exact same data to train on, training a neural network twice will result in different weights and thus a slightly difference accuracy. I considered writing a script that would rebuild a model from scratch then check that the accuracy was above some specified value, but I decided not to, because the final product would use the same pretrained model during every run, as opposed to building one from scratch each time. In other words, once the model is finalised, we can use the weights from that model and never build another one again.

Because of this, the team will have to figure out how to conduct User Acceptance Testing once the product is closer to being built. In the intermediate stage, once autonomous flight is achieved, we would have to test it manually by activating the drone and visually inspecting how it behaves.


## Other contributions to group processes ##

Our team makes use of [issues](https://bitbucket.org/zson5784/comp3988_t17b_group_5/issues) to keep track of bugs to be fixed or features to implement. As shown in the above section, most of my work in each week goes towards solving some issue or implementing some user story feature.

We also keep each other updated on our progress and help each other where needed. Since some members are working on the drone simulation part, and others are working on the neural network part, there needs to be communication between the two subgroups to be able to make integration work.

[evidence_collab_1.png](https://bitbucket.org/repo/jkq4oxG/images/1289542551-evidence_collab_1.png)

[evidence_collab_2.png](https://bitbucket.org/repo/jkq4oxG/images/1759338455-evidence_collab_2.png)



## Reflection ##

### Version Control ###

We used Bitbucket for version control. All members have experience with git, with some members being skilled enough to help the rest fix any issues, so using version control the way it was intended (merging branches, fixing conflicts, pull requests) was smooth sailing.


### XP ###

To be honest, the nature of our project doesn't lend itself very well to XP methodology, at least in the start, where the first few weeks was spent figuring out how to set up all the different software layers required for this project (and thus the Tester and Programmer wouldn't have had much to do). However we did stick them as much as possible, for example with the Manager and Customer roles still playing their part. For most of it though, we split the work and we were all Programmers every week.


### Challenges ###

One challenge we faced was the number of moving parts in the project, in terms of software. We needed Gazebo for the simulator, PX4 for the simulated drone and camera feed, MAVSDK to control the drone with code, and TensorFlow and OpenCV for the neural network and object detection. We had to figure out which software to use to begin with, how they would all communicate, and finally which Operating System supported them all, which was a lot of work.

We tackled this by splitting the team into 2 subgroups, with Zhi Yi and Boswell leading the simulator component, and myself leading the object detection component with Martin and Steven, with Ye Xin working on integration. Zhi Yi figured out and wrote an excellent guide on setting up the simulator components, while I figured out and wrote a guide on how to set up the neural network component. This saved time compared to if everyone had to figure out how to set up every component on their own.

We also decided to all install Ubuntu 18.04 to ensure software compatibility, which itself took a bit of time.

A challenge I faced personally was the broken Gazebo 9 dependencies on the Ubuntu Apt repo. I was having issues with Gazebo 9 and decided to uninstall and reinstall, but upon trying to reinstall, I was greeted with an error about unmet dependencies. I spent hours trying to fix this, manually installing packages, and even getting cached packages from my teammates to install it, but to no avail. In the end I installed Gazebo 11 as a temporary fix, which has compatibility issues with the models of traffic signs that we made in Gazebo 9, but I was still able to write the integration between the neural net and the drone camera, and trained it to detect other models which didn't cause crashes. 


### Role in The Group ###

My role in the group is essentially the neural net/object detection programmer/lead - I figured out how to set up TensorFlow with GPU acceleration and wrote a guide for it on the wiki for others to follow, I wrote the initial model trained on Cian's data, and I wrote the code that would extract frames from the drone camera and build a training dataset from it. I also wrote the code that would load a pre-trained model and then use that model with input from the drone camera to detect objects in realtime.


### Project Teamwork ###

In my opinion the team has been working excellently together so far. This project is no doubt a hard one, but we have rised to the challenge at each point. We are a bit behind schedule due to the challenges we faced in the initial setup, but at this point, we more or less have all working parts talking to each other (just need to integrate OpenCV now), so we can focus on fine-tuning the actual object detection and autonomous flight. We will be speeding up development.