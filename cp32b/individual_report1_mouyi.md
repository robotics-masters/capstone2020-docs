# Individual Report #
## Roles and Contributions ##

- Manager for Week 4: For some reason, we changed our project at week 3, so we actually started this project from week4. As the manager for week 4, I held the group meeting as well as the first two meetings with our new client in week4. During these meetings, we developed a general picture of our new project and started to work on that. 

- Programmer: I take the role of Programmer for other weeks. In those weeks, I helped my teammates with some coding problems. However, as our project haven't involved too much coding yet, I didn't do much work.

- Unity Expert: I am the only one in my team who has experience using Unity. Therefore, I take the responsibility of creating new tracks using Unity together with Nicole, who is Blender Expert for building the 3D Objects. Any work involving the use of Unity under my administration including create new scene, link the new track to the menu, etc.

In addition to these work, I also keep record of my [individual work](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Mouyi) in Wiki every week as well as upload a Youtube video describing this week's activities. The link to youtube videos were also included in my individual Wiki page.

## Extend of Work ##
### Donkey Environment Setup ###
I set up the donkeycar environment in my local computer in week 4, as described in the weekly individual report. I followed the tutorial given by the client to compete this work. A conda virtual environment was created to run the donkeycar. In this virtual environment, some packages such as donkey, gym-donkey and tensorflow were installed to make sure the car can run perfectly. Also, a simulator was used to provide a graphic interface.

### Meeting for week4 ###
I held three meetings in week 4, two meetings with client and one within the team. The team meeting was held on Tuesday wthin the tutorial. We discussed about what we had done, what was in progress and what we were going to do. The first meeting with client was held on Monday. We talked about what we already done and asked some questions. The client also gave us scopes for week 4. The second client meeting was held in Friday, which was just a 15-minutes meeting talking about what's in progress. As this meeting was just for client to make sure we were working so I didn't write a meeting minutes for it. The links to the other two meetings were listed below and also in my individual report on Wiki:

- [Meeting Minutes Group](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/MeetingMinutes_Tut_Week4)

- [Meeting Minutes with Client](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/MeetingMinutes_Week4_Client1)

### Simulator ###
Unity was used to build the simulator. There was a built Unity project in github and I use that as a template. The map picture from our client as well as some 3D sign objcets (fbx file) from Nicole were used to built the track. Also, a new button was added to the menu and linked to our new track scene so that users can access the new track by a simple click. Furthermore, we also changed the car model to make it more fancy. Following are two Youtube videos that describe my work on the simulator.

- [Youtube Video](https://youtu.be/2FwnLP4FiB0)

- [Youtube Video](https://youtu.be/adVbw1as3VE)

## Quality of Technical Work Done ##
I and Nicole took the responsibility of the simulator part. Though we have divided the work, I did unity part while she did Blender part, we had a general idea of each other's work. So, we held zoom meetings during our work and tested each other's work throughout the progress. I checked the Sign objects she made and gave feedbacks on aspects such as size and materials while she watched me driving my car in the scene and gave me advice. This ensured the quality of our final simulator.

Also, after the simulator was built, we sent it to other teammates. They drove donkeycar on it, both using the model or by hand, and gave us some advices. There were two main issues they found and told us to update. One is that the picture captured by the car was blurry and the other one is that the sign was too height for the car to detect. The chat messages were listed below.

![1.png](https://bitbucket.org/repo/G6xBMXK/images/464357884-1.png)

![2.png](https://bitbucket.org/repo/G6xBMXK/images/3610975247-2.png)

![3.png](https://bitbucket.org/repo/G6xBMXK/images/2486781220-3.png)

![4.png](https://bitbucket.org/repo/G6xBMXK/images/2056069156-4.png)

## Other Contribution to group process ##
I attended all three meetings every week and involved in other discussions in discord. I asked some questions in discord as well as answered my teammates questions and help them to solve the problem. The evidence of my involvement in discord is listed above in the quality of work part.
Also, I did data collection for my teammates to train the model. I drove the donkeycar in my simulator and collect thousands of pictures. Also, I did the data split work of stop sign and non stop sign in week 4. There is a commit in bitbucket as an evidence.

## Reflection ##
### Extreme Programming ###
We are asked to use XP throught the progress of our project. However, as our project is more similar to a research not a software development, it seems really hard to use the concepts of Extreme Programming in our work. For example, works on Unity and Blender doesn't invovle much coding.

### Version Control ###
We use bitbucket's reporsitory to control the version. We created three branches, a master branch, a simulator branch and a model branch. When we work saperately, we control our own version. For example, in the simulator branch, Nicole did some pushes of 3D objects and I also pushed the newly updated simulator even there was just some small changes. Then, when we think our simulator was perfect, we merged it to the master branch. I think this progress makes us work clear and efficient. It is also convenient to check the previous work.

### Challenges ###
One challenge I met was the OS System. My computer is windows so the simulator I built can only be used in Windows. However, my teammates have MacOS and Linux. So I googled the approach to export Unity project to other platform and found that I need to install some supports. I then followed the instructions and finally solved the problem.

Another challenge is to use GPU to train the model. I followed the tutorial and installed all required packages. However, it kept warning me that a file was not found and because of that, I cannot use GPU to run the process. AFter searching on the net and discussed with my teammate Hao, who had the same issue, we fianlly solve the problem. We found that it was caused by the version of cudatoolkit, cudNN, tensorflow, tf-nightly and donkey. Donkey can only support tensorflow 1.x but the code we used involves some function from tensorflow 2.x. Also, tensorflow 1.x asked for cuda 10.1 while tensorflow 2.x required cuda 11.0. Wrong corresponding version of different packages was the main reason. 

### role ###
My role in this project is programmer. I help my teammates with coding issues they met. However, as our project doesn't have much coding work, I don't think it's necessary to have a programmer role. Issues can be solved through group discussions in Discord or in meeting and coding is just for some small functions.

### Current Process ###
Our team is now working well on this project. We have clear division of tasks and each of us are willing to help other teammates when they had some problems. Also, we have sufficient communications with our client. We chats in discord with him as well as held two meetings every week to talk about what's in progress and what to do. Nothing need to be improved yet and I am glad to work with my great teammates.