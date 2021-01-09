# __Individual Report - Yexin Mao__ #

This is the individual report for @Yexin for the first report due Sunday
4th October 2020.  

Based on the rotation of XP roles, I have undertaken the roles of
Customer, Tracker, Programmer and Tester in the last few weeks.  

*Customer: Driving the project, writing user stories and deciding on
questions of these user stories.  

*Tracker: Talking to teammates, checking with their progress and giving
advice if they have trouble.  

*Programmer: Given the nature of the project, there was not much work
relating to programming. So basically I checked the codes provided by
our client and learned its functionality.  

*Tester: Checking if the data pushed by other teammates worked well.  
  
In addition to these XP roles, I have also been assigned the role of
Integration Tester. Since we have many modules in this project like the
simulator and different working environments, I integrated these modules
and verified the functionality and reliability of them.  
[Role
rotations](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/Role%20Rotation.md)

## __Weekly plan__ ##

### Week3 ###

I intended to set up Gazebo simulator with both ArduPilot and PX4
environments, but documents online for set-up were outdated and could
not apply to MacOS. I spent a lot of time looking for the best operating
system to support both the simulator and environments, I tried windows
10, installed Ubuntu20.04 as a dual-boot, used VirtualBox for testing
and finally I chose Ubuntu18.04. The installations were not smooth
afterwards because many packages and dependencies we needed are
inaccessible in china, so I learned how to set up VPN and changed the
mirror source of packages.  
By wasting the majority of time on issues irrelevant to this project, I
did not complete my goal of setting up both ArduPilot and PX4
environments. However, our client eased our burden on weekly tasks that
we only needed to configure Gazebo simulator tools with Ardupilot and I
reached that goal at last.

### Week 4 ###


I intended to set up Gazebo with PX4 environment, control drones using
scripts and create worlds in the simulator. I had the same network issue
of slow downloading at first, but by searching information online and
with the help of my teammates, I figured out how to speed up the
downloading and set up PX4 environment successfully. Drone control was
easy to implement, I could simply type some commands in the terminal or
use QGroundControl to make the drone arm, takeoff and land. I did not
create a whole world in Gazebo because our team had not agreed on what
kind of world we were going to build, but I learned how to insert models
inside the simulator which would be useful in the future work.  
[Set-up
guide for week3 and
week4](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/Set-Up%20(Ubuntu%2018.04).md)

### Week 5 ###

I intended to show primitive detection working on initially provided 4
signs (stop, turning, parking, traffic lights) with OpenCV, It was my
first time to use OpenCV and I spent the first half of the week learning
its functionality and reviewing the codes provided by our client. I
could use the existing codes to detect signs in sample data, but what I
wanted to do was using the codes to detect signs in the simulator.
However, I encountered difficulties in linking the codes with the camera
in the simulator. My teammate shared with me some codes by which I could
use the camera of drones in the simulator, but with these codes I could
only see signs instead of detecting signs. I also tried to combine both
codes provided by our client and teammates together, unfortunately, the
sign detection did not work at last.   
[Python codes for sign
detection](https://bitbucket.org/zson5784/comp3988_t17b_group_5/src/sign_detection/python/)

[video demo](https://youtu.be/9LmkGtMvqp4)

### Week 6 ###

Week 6 was more about report writing and demo video making. I attempted
to do some actual work on this project like building the world in the
simulator. Some of my teammates had already completed this part, but an
unusual issue occurred to me that I could not run the codes in our
Bitbucket repository successfully. However, following the suggestion of
my teammates, I re-downloaded the simulator and the issue was solved.  
[Pull requests](https://bitbucket.org/zson5784/comp3988_t17b_group_5/pull-requests/7/intergrate-gazebo-px4-video-capturing-and/diff)

[video demo](https://youtu.be/GfQQ_KQWgpc)

## __Quality of technical work done__ 


The technical work consists of primarily a number of key elements like
Gazebo simulator, Ardupilot, PX4 environments. We did not write as many
codes as other projects. To ensure the quality of the software, we
loaded a world called small_city into the simulator to test the
configuration of models. We also used some simple commands and scripts
in terminal to test if we could control the drones.   
[Path of the world
we
use](https://bitbucket.org/zson5784/comp3988_t17b_group_5/src/small_city/worlds/)

## __Other contribution to group processes__

### Wiki updates 


I created pages like minutes and status reports, uploaded some files in
our wiki, adjusted its structure and fixed some errors.   
[History of
wiki](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/history/Home)

### Communication with clients 

I encountered many difficulties in this project, so I talked a lot in
Discord with our client for help. Our client is excellent and eager to
help us, he provided plenty of useful information for the team.  
[Discord
channel](https://discord.com/channels/750412538637975633/751799048914206732)

### Issues created and progress 

We communicated and tracked our issues primarily on messenger at the
first few weeks, so we do not have many issues on Bitbucket. I opened 3
issues and they are all solved and closed right now.  
[Issues](https://bitbucket.org/zson5784/comp3988_t17b_group_5/issues)

### User stories 

One of my teammates have written nearly all the user stories in Trello.
To contribute a bit in this part, I fixed the format of user stories and
added some new user stories as well.   
[User
stories](https://trello.com/b/Y8qWmnWG/user-story)

## __Reflections__ 

### Version control 

As the nature of this project, we mainly focused on setting up
everything on local machines in the first few weeks. As a result, we did
not have many commits in Bitbucket. I think in the future working of
this project, we should commit more, open more issues and show more
evidence in the wiki.  
[Commits](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/)

### Coding style 

Coding style was not a big issue in this milestone, as we have not been
required to write any codes. However, it is good to keep in mind that we
should have consistent coding style in the future. The team will benefit
a lot from clear codes.

### Extreme programming 

The team have done many things related to XP, but I do not think I
totally understand the meaning of XP. So for me, it is important to get
more details of what it actually means to tackle its elements.

### Challenges 
#### Software version 

When we tried to install and configure Gazebo simulator tools with
Ardupilot and PX4, we had to figure out which operating system to use
and which version of Gazebo to use, because many packages and
dependencies required were incompatible. This was a great challenge for
us as we had to download, test and maybe re-install many times until we
found the most suitable version.

#### Communication and issue tracking

We were required to use Discord and Slack for communication and
Bitbucket for issue tracking. However, most of the time, we used
Facebook messenger to communicate with each other, and we asked for help
on messenger when we had difficulty in the project as well. This causes
a problem that we do not have as much evidence as what we actually
contributed to the project. And when some teammates faced the same
issue, they would waste a lot of time seeking for help instead of
checking the solved issues. I think we need to use Discord and Bitbucket
more in the following weeks, we can not only gain more marks from doing
this, but also learn to work as an XP team.

## __My role as a software engineer__ 
I have gone through all the codes on our git repository and have a good
understanding of how they work.  
I attempted to write my own python scripts to detect sign and objects
using OpenCV in gazebo.     
[Branch for sign
detection](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/branch/sign_detection).   

In the future, I expect to contribute more to Bitbucket, learn how to
use OpenCV and Tensorflow and work like an XP expert.