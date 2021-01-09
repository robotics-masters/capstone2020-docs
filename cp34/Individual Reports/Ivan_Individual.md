# Individual Report

This is the individual report for Yufan XU as the first project report. All hyperlinks in this report direct to the relevant evidence and some work done can be proved by links in a different part, which will not be listed again.

## Introduction

For this project, our team decided to fix XP roles instead of rotating every week. So, my role in this project is tester throughout these weeks. My responsibility is implementing and running Functional Tests rather than Unit Tests that programmers will do. In other words, when other team members upload their code work or simulation model, I will run them to see if they meet the expectations and make sure people know if the test results decline. Apart from that, I also take technical roles as an experimental tester and programmer.

## Week-by-Week Work

However, as our project is still in the early-stage that works from different parts haven’t been able to combine, my major work for these weeks follows team distributions other than exactly XP roles. I will explain it week by week as following.

### WEEK 2

Week 2 is the first week of our project. Primarily this week’s focus is getting familiar with team members and getting connected with the client. We made our group contract this week, which states some basic agreements on staffs such as meeting times, XP roles distribution, solutions to team conflict, and so on.

During the meeting, I choose to take the role of the tester as I am more expert in problem-finding. But as programmers will do their Unit Tests before uploading their code, I was also saying to help write minutes every week.

Apart from the above, our client also gave out ahead work to do. We were trying to get the simulator working on our computers.

### WEEK 3

Week 3 is the first week that we officially started the project. Works allocated to me on that week include:

* Gazebo running in all environments on Ubuntu 18.04
* Work on weather simulation

As I stated before, I was able to get Gazebo work on my Desktop with Ubuntu 18.04 during week 2. However, our team members were struggling with Virtual Machine, WSL, and Linux as the simulator cannot work under the Windows environment. So, I tried all three environments in order to choose a common platform we were going to use. After a few days’ test, I found out that Virtual Machine would result in a performance loss which is unacceptable due to the high system resource requirement by the simulator. Also, WSL causes extra steps to open the GUI of the simulator which is complicated as we usually need to open 4-5 GUI in order to monitor and control the behavior of the drone. Besides, I installed both Ubuntu 18.04 and 20.04 to check if there is a specific requirement on the OS version. The result was that the simulator, Gazebo, was not compatible with the higher version of Ubuntu after version 18.04. I shared the findings with the group and as a result, we decided to choose Ubuntu 18.04 as our project platform.

My second work for this week is weather simulation. I did plenty of researches about drone simulation and Gazebo and wrote a document about how to achieve this in our project. Generally speaking, the only factor we will consider in simulation is the wind, and we can set the parameter in SITL. Also, I listed ideal test values that would be used in testing after the code of the algorithm is ready. Detailed work can be seen here: Weather Simulation.md

### WEEK 4

From Week 4, our team divided into two groups that worked on Gazebo simulation and algorithm code separately. I was one of the simulation group. The work of ours was:

* Gazebo - looking into rendering Worlds.
* Gazebo - modeling charging stations in the simulator. Creating its symbol for this object with collision detection.

During this week, we discussed creating our own world from real map data. However, we concluded that it was difficult to get 3-D city data and model that into a world file. So, we decided to look for an existing world model to perform our demo which can be viewed here: test_drone.world.

Later, I learned how to make building model in the Gazebo simulator and created multiple model options. But after communication with the client, he clarified that we were only required to make a simple box with an identical symbol for detection. So, we began with a simple model and wait to see if it will be necessary to change to a more complete model in the later project progress.

### WEEK 5

The work plan for week 5 includes two parts:

* 1-minute video summary of work for each individual.
* Simulator - Modelling Buildings, Trees (optional), and Other objects into the World.

With the world file ready, my responsibility this week is to perfect the file, including modeling buildings, trees, and other objects that will be necessary for simulation. All these things have been added into the world file with the link above. Although further modification may be needed in the later test.

Besides, we are also required to randomly generate a charger station in the world, and my job is to find out the relevant code in the world file and how to modify them in order to change the position of the station and create new ones.

### WEEK 6

This is the last week of this report. During this week, I mainly work on the group report, demos, and presentation.

## Quality of technical work done

To ensure the quality of my work done, I will run several tests before pushing to the bitbucket. The major aspects I will test are:

* If the code works with both PX4 and ArduPilot.
* If the code works with different world file.
* If the code works after changing the position of the object in the world.

Also, other group members will run my code after and give me feedback on any issues in order to check if the code works on different computers.

## Other contribution to group processes

Apart from each weeks’ specific work, there were also works that I did throughout all these weeks:

* Take part in writing Meeting Minutes, including client meetings, team meetings, and tutorial meetings.
* Weekly Summary Vides from week 4 that shows work done every week and plan for next week.
* Collaboration and teamwork are throughout every zoom meetings and can also be reflected by meeting minutes and slack.

## Reflection

During this project, I really learn a lot from helpful teammates and the client. Although I can basically use git before the project, I get more skilled and a deeper understanding of version control through the project. Also, I was not used to writing very comprehensive comments for my code. But during these weeks, I began to write brief and easy-to-understanding comments by learning from other team members’ work. They have a very good style, and standard variable and function name, which helps a lot in reading.

As a software engineer, my code is mainly about the model object in the simulator. My experience with Unity helps a lot in this work, as the world file editing and model insertion are pretty like things in Unity. Also, the format of the world file looks similar to JavaScript which is also mastered before. The code experience in this project extends my understanding of visualization of the code of the project and the implementation of code of models.

Overall, the whole project operates well, and the team is very nice. Teammates learn from each other and help each other. While for the following weeks, I think I should communicate more with the programmers, especially regarding their code. As far as I am familiar with their code design and function design, I can plan test earlier rather than after their pushing, which hopefully could make the most use of time and also help them with code test.

## Links to relevant work

Weather Simulation.md

https://bitbucket.org/DylDupe/comp3888_t15a_group1/src/master/Weather%20Simulation.md

test_drone.world

https://bitbucket.org/DylDupe/comp3888_t15a_group1/src/master/worlds/test_drone.world

Meeting Minutes

https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Minutes

Weekly Summary Videos

https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Videos

Slack

comp3888t15agroup1.slack.com