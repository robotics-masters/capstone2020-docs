# Individual Report – Joseph Pham

---

**Table of Content**

[TOC]

---

# Work Done

## Roles

This is the individual report for @jpha6542 for the final report.

I have undertaken several roles for the project so that our team can maintain an efficient and straightforward project. The main roles I was assigned throughout the semester:

* **Unity Expert**: I was tasked to understand the whole unity component for the project this included understanding the program given to use to update but also what tools to use for a smoother project. This also included explaining the simulator to the rest of the group this was done through the documentation of the map and signs. I was also in charge of what was going to be placed in the simulator and if anyone wanted anything in the simulator, I was the first line of contact to achieve their needs. 
* **Wiki Expert**: As the wiki expert, I was in charge of keeping the wiki up to date but also to have consistent formatting for all pages. This can be seen through my edits. I was also in charge of getting the layout of the wiki so that all information was easily accessible from the home screen and that all information was readily available through only a couple links. Everything can be accessed from the home page. The edit can be seen in the Appendix A4.

Not only was I tasked with these specialised roles I was also undertaken certain XP roles throughout the project. Initially as a team we had decided to rotate roles in the beginning of the project so that everyone could have a hand at every role while having more defined roles later on in the project.

* **Tracker**: I was the tracker for week 4, some of the task were to ask how everyone was going in their respective part of the project and if they need assistance if they were struggling. I was also in charge of the weekly report since I was able to talk to everyone and see where their progress was.
* **Customer**: Throughout the whole project I was the secondary customer with the client, as I would often update the client with our smaller updates and conveyed to our group with the demands the clients wanted that week. I would also ask any question our team had for the clients about the unity components. I also ensured that our group stayed on track with the scope and requirements of the project. The interaction can be seen in the Appendix A3. Note: The reason why we have two customers for the project was due to us having two ‘separate’ teams one for OpenCV and one for Unity. 
* **Programmer (Unity)**: I was in charge of implementing the simulator’s user stories for the project ensured that all quality of work in unity was of excellent quality and always delivered on time. 

## Task/Work Completed
Our project had us split into teams, one team for OpenCV and one team for Unity/Simulator. I was assigned to the unity team with Julian. Throughout the project I have completed a majority of the unity and project task which include:

*Note: Some hyperlinks are missing this is due to the Unity branch being deleted and so we can only see the commits locally but not on the servers. The history of the ‘deleted’ commits can be seen in the Appendix A1 (manually have to find the search if you want).*

* Implementation of 4 maps (2 flat and 2 F1 Tracks)

Commits: 5f4d633, 2e40916, 645bc86, 9dc0e2a, 1856854, c9db661, 2bf5409, db6110c, d42d795, 96dd81b, 259c6ca, 90da144, 90da144, d533a7d, 88d3e61, d6f9572

* Implementing camera resolution to config file

Commits: [Meeting Minute for Week 9](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Minutes/Week09_Client_1), 72dc944

* Improvement of menu screen in simulator

Commits: c57291d, 5d101f7, 8db07e6, 53a422c, 81fbe8f, 4967611, d533a7d, 5c0de24

* Helped implement another car into the simulator

Commit: 2a9918b

* Workshop for Client

* Documentation of Map and Sign Implementation

Commits: 5ad2d64, 5f4c45a, 854ab05, cf143cc

* Documentation of Camera Resolution

Commit: cf143cc

* Report, Presentation and Demo

Commits: [Week 11 Individual Progress](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Weekly Individual Progress/Week 11), [Week 12 Individual Progress](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Weekly Individual Progress/Week 12)

## Weekly Plan

|     Week    |     Planned for the week    |     work achieved |
|-|-|-|
|     Midsem    |     Implement new car model    |     Help integrate second car model into simulator (understanding how to spawn it).Started research on Hockenheim track |
|     7    |     Start working on F1 track, documentation of map implementation    |     Finish off making the layout of the Hockenheim F1 track    |
|     8    |     Elevation of F1 Track (Hockenheim) |     Implemented height elevation to Hockenheim track. Camera resolution from config    |
|     9    |     Fencing for F1 Track (Hockenheim)    |     Fixed up Hockenheim’s road width and add fencing (Using new asset)    |
|     10    |     Finish off Hockenheim map    |     Improved fence texture created new menu and finished the road layout for Monaco F1 track. Workshop for track creation   |
|     11    |     Unity user stories presentation    |     Finish off my writing of the presentation and did   the Hockenheim track lining.    |
|     12    |     Unity user stories presentation    |     Recorded my part of the presentation and did part my part of the demo. Start on client deployment    |
|     Stuvac    |     Finish Handover sheet for client and another extra. Finish off Report    |     Finished handover sheet, looked over the wiki one last time and changed anything out of place. Documentation for camera resolution. Helped write sections of the report    |

Evidence for this is in my weekly videos which can be found [here](https://www.youtube.com/playlist?list=PLD3U35be682fLG9l8n8aJ1Yvim3ZCfuKe) and further evidence for week 7 and onwards can seen [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Weekly Individual Progress/Landing). The reason why we only have week 7 and onwards was because we only started this up after we got feedback for our initial individual report per our tutors’ advice.

---

# Extent of work
I will now go through each of my task completed and how I achieved them and how far I went to them:

## Implementation of Maps
Creation of the maps was the main thing I had to do for this project and took up most of my time. I initially created the flat maps; I first tried to create the tracks in blender and model out the road from the picture with the width this can be seen through my fbx (3d model) file I pushed [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/2e409160e2910a1702fb8dbce22fa196c78ad30c#chg-Assets/Map%20Trial.fbx). However, I discover a much simpler and cleaner looking way of implementing flat maps. 

This was done by essentially duplicating a scene already in the simulator and then changing the textures to our tracks design. It was a very simple and easy solution to our user story. While for the scaling of the map I was unsure about the actual scale of the plane, so I was unsure how long our track was initially. I however found a solution to figure out the scale of unity by utilising the actual donkey car since I knew the dimension of it. I had to confirm the scale with the client just in case, this confirmation can be seen here.

![Figure 1.png](https://bitbucket.org/repo/48xyAqR/images/1732750765-Figure%201.png)

*Figure 1: Interaction between me and the client about dimensionality for unity*

Now that I knew how the scale of unity, I was able to correctly scale the map, as I now knew that for a cube asset in unity the scale was 8.79 for every 1 m. So, I kind of had a ‘ruler’ for dimensionality so I was now able to correctly scale the dimension of the map. I then added the walls where specified and scaled them correctly too. This meant that we were also able to quickly complete the second flat map as well as I already knew the steps of how to make the first one and just copied the same steps just changing the texture for the map. I did both maps within a day using this new method and they can be seen [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/583e72debe8adeddab1b0e9828e785533a729749).

The next thing I had to do was figure out how to get the maps to work in the gym so that we could get images/snapshot for our algorithm. I had to read a lot of the codes to figure out how the environments were created and used in the gym while Patrick tried to ask the donkey car discord for help, but no one replied. 

![Figure 2.png](https://bitbucket.org/repo/48xyAqR/images/3279064831-Figure%202.png)

*Figure 2: As we can see we asked the donkey car discord but we didn’t get a response back so we had to figure it out on our own*

This meant that we were kind of on our own. I however figured out the solution by going in the codes and search for the ‘env-name’ and from there I was able to understand how the environments are created and so created the environment for the newly added tracks. I then made a video for the client as he requested how the environments were made:

![Figure 3.png](https://bitbucket.org/repo/48xyAqR/images/3690334948-Figure%203.png)

*Figure 3: Interaction between me and client to show him how to create the environments for the gym (link to YouTube: https://youtu.be/IOb12vrP5xQ)*

I then pushed it to the repo so that our OpenCV team could use the new maps for their algorithm testing, the push can be seen [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/9dc0e2a0e21ef2bb7238aeb41feffec5311dd663). All of this is talked about in my documentation which I will go through later. 

I then helped Julian with placing the signs into the second map of the simulator, this was due to the specification of our client. We initially had issue with the signs as the signs texture was not showing up in the simulator, we however discovered that we forgot to put the texture inside with the simulator. This issue however was resolved quickly that we didn’t raise an issue with the team. Sign implementation was however quite easy, it was just to drag and drop the sign into the map. The main issue we had was the scaling of the signs. We initially scaled the sign’s pole wrong which cause problems for our OpenCV team as the sign was out of frame. We only figured this out when we were talking to our client as seen from the reminders [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Minutes/Week05_Client_2). This was due to our client not specifying the pole length comparative to the sign but after that meeting, I was then able to quickly fix the scale and show it to him.

![Figure 4.png](https://bitbucket.org/repo/48xyAqR/images/2004604290-Figure%204.png)

*Figure 4: Communication between me and client about the scaling of the pole*

I had to yet again change the scaling of the signs as he had made another mistake when he wrote the specifications of the signs in our initial scope. I brought it up to him in the discord.

![Figure 5.png](https://bitbucket.org/repo/48xyAqR/images/853022625-Figure%205.png)

*Figure 5: Discussion about the final scaling of the sign*

After this all the scaling was done for our signs and I pushed the new scaled signs to the repo which can be seen [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/8e6b37266bad1d5205ed59731a52d0dbf26c7c3e). 

After week 6, our client updated our scope so that the group was to create a two F1 track which included Hockenheim and Monaco. I started working Hockenheim track in week 7, I initially used a free asset in unity called ‘Beizer Path Creator’ by Sebastian Lague. This method was very usefully when creating the [roads](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/c9db66165ffc0d64ddef710869580defa9679d50) and [elevation](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Weekly Individual Progress/Week 08) as all you had to do was draw out the path and it would create the roads for you. Initial video of the track is seen [here](https://youtu.be/Zut9YYVZB6E).

![commit 1.png](https://bitbucket.org/repo/48xyAqR/images/2716966704-commit%201.png)
*Note: One of our teammates deleted the branch for the simulator to save space on our repo this meant that all commits can no longer be seen on the server and can only be seen from my local machine.*

We however ran into an issue with implementing the fences and changing the width of the track as the ‘Beizer Path Creator’ did not offer this as part of its functionality. This is as if I had to manually add the fences one by one on the track it would take too long and wouldn’t look good around corners at is would look too stiff doing it by hand. This is why I decided to swap to another unity asset called ‘SplineMesh’ by Benoit Dumas. This asset had more functionality such as being able to create fences automatically and also change the road width automatically. So, we decided to swap to SplineMesh this meant that all the work done on Beizer Path Creator was scrapped which meant that 2 weeks where essential gone. However, I used the skill I obtained by using Beizer Path Creator on SplineMesh as they used very similar creation system just having different functionality. So, I was able to quickly create the Hockenheim track again with the fences and better transitions between track widths. I then pushed the new Hockenheim track with everything done to the repo. This is the map with the new asset [here](https://youtu.be/beiQuRtymx0). (Note: Julian did the terrain, but I did everything else) 

![commit 2.png](https://bitbucket.org/repo/48xyAqR/images/3043893832-commit%202.png)

I then started working on the Monaco track, creating the track layout with elevation and width changes. The creation method was now able to be done in a single sitting, as I was now more acquainted with the asset and because of that I knew exactly what and how to do things which allowed me to quickly finish off the Monaco track. While Julian was in charge of making the terrain for this map too. The Monaco layout can be seen [here](https://youtu.be/qfKMfmIKPIk). 

![commit 3.png](https://bitbucket.org/repo/48xyAqR/images/235480763-commit%203.png)

I also made the tunnel for the Monaco track as it has a tunnel in real life as well. This can be seen in the commit here.

![commit 4.png](https://bitbucket.org/repo/48xyAqR/images/684855176-commit%204.png)

With this the only thing I had to do left was to add the curb run off which was done by utilising the functionality of SplineMesh and then manually moving anything that looked out of place and this commit can be seen here. 

![commit 5.png](https://bitbucket.org/repo/48xyAqR/images/2239287694-commit%205.png)

With this done I had finished all of the map implementation, so 2 flat maps and then 2 F1 tracks. A screen shot of all the map can be seen in the Appendix A2.

## Implementing camera resolution to config file
Implementing the camera resolution was a task given to us by the client during our meeting with him which can be seen as it was given to us as a task [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Minutes/Week08_Client_2)(Action for improvement). This is as initially the only way to change the camera resolution was to change it the simulator which would take a lot of time since you would have to build and run every time you wanted to change resolution. So, me and Julian spent the weekend reading through the source code of the simulator and gym and trying to understand how the gym communicates to the simulator and vice versa, the communication log can be seen [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Communication Log) (25/10/2020). We were able to figure it out a bit and found another method of changing the camera resolution through another python file and we quickly informed the client 

![Figure 6.png](https://bitbucket.org/repo/48xyAqR/images/2574846474-Figure%206.png)

*Figure 6: Initial talk with the client about camera resolution fix*

We then got into a call with our client and told him our solution but while we were in the call, we figured out how to change it from the config file and gave him that solution as well. He decided to go with the solution from changing it from the config and so we were done with camera resolution. This success can be seen in the weekly report for week 8 [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Weekly Updates/Week 08). 

## Improvement of menu screen in simulator
Initially the menu for the simulator had only the maps that the initial simulator but as stated before we had implemented more maps into the simulator that also needed to be added to the menu, so this is what initially the menu looked like.

![Figure 7.png](https://bitbucket.org/repo/48xyAqR/images/2071233255-Figure%207.png)

*Figure 7: The initial menu*

So, I had to add our maps to the menu, so I moved the positions of the other maps to better suit the U.I. of the menu so that we are able to fit more maps into one menu. This menu was pushed to the repo [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/8db07e6e17f42f625de5a355428c4df799258e66).

![Figure 8.png](https://bitbucket.org/repo/48xyAqR/images/3330008274-Figure%208.png)

*Figure 8: The revised menu with our maps*

But later on, in the project we had to also add the F1 tracks to menu and as you can see from above there is no longer space for more maps, so I decided to create a second page to the menu. Since this was the first time, I had worked with unity I had no idea how to do overlays but upon watching a few tutorials, I figured out how to make a second page for the menu. We also added in map placeholder due to our client wanting the ability to easily add new maps from other groups to our menu. Which can be seen below

![Figure 9.png](https://bitbucket.org/repo/48xyAqR/images/2340514963-Figure%209.png)
![Figure 9B.png](https://bitbucket.org/repo/48xyAqR/images/1715996101-Figure%209B.png)

*Figure 9: The new menu with the second page, accessible through the next page button and vice versa*

This was pushed to the repo here.
![commit 6.png](https://bitbucket.org/repo/48xyAqR/images/1037878901-commit%206.png)
This was our final change to the menu.

## Helped implement another car into the simulator
As per part of our user stories we had to implement a new vehicle into the simulator, Julian did the building of the vehicles but did not understand how to implement it to the simulator. So me and him worked together to try to figure out how to place it into the simulator this can be seen through our communication log [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Communication Log) (9/10/2020). We figured out how to add it to the simulator which can be shown through this video [here](https://youtu.be/vifHMOugUYg) (0:00 - 0:56). We had successfully implemented it to the simulator it can also shown through the achievement we had for our mid-semester break [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Weekly Updates/Week 06B).

## Workshop for client
In the beginning of week 10, our client asked us to assist him in running a workshop to help other groups that were struggling in creating their F1 tracks.

![Figure 10.png](https://bitbucket.org/repo/48xyAqR/images/2692146742-Figure%2010.png)

*Figure 10: Our Client asking me to present in the workshop*

So, I participated in the workshop by showing the rest of the teams how I implemented the maps and took any questions they had about my technique and why I was using the asset in the first place. Overall, I presented in the workshop for around one hour and can be seen in the video our client has released here on [YouTube](https://www.youtube.com/watch?v=dI-CaKepWIA&ab_channel=RoboticsMastersLimited) (0:00:00 – 1:05:00). 

## Documentation of Map and Sign Implementation
I was also in charge of doing the documentation of the map and sign implementation as I was the one that implemented these things. However as stated above we had multiple ways of doing the implementation and so I was constantly changing the documentation to the easiest possible way of implementing map. So, I went through multiple iterations of the documentation. This can be seen through the multiple pushes I did for it. This is the [first iteration](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/5ad2d64edde44e702309920fc3299bcd2d52f163) of the documentation which showed doing the method of duplicating a scene and placing of signs. I also wrote how to create the environments for the donkey car gym as well. I then wrote the component for scaling the signs correctly which can be seen [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/0685447d09d1ecb3f66a52bd911b5e75a8f2eb87). While the [final iteration](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/cf143cc18f10bdb10e74af3dcaa52a909ba0a485) (Creating and modifying simulator) of the documentation changed a lot of the map implementation as we used a simpler method of creating flat maps and so incorporated that into the documentation as well. There is also documentation on how to make the elevated tracks and goes into details on how we created the F1 tracks and which function we used to get there. The link to the final documentation can be found [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/src/master/docs/Creating and Modifying Simulator.pdf) or can be found on the wiki [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Creating and Modifying Simulator).

## Documentation of Camera Resolution
I also created the documentation of camera resolution so anyone who wanted to change the resolution of the camera could read the documentation and change their files so that the resolution can be changed. Through this documentation I also talk about how the simulator and donkey car gym communicate with each other to give a better understanding of how the software works since our client also did not have a fully understand of how it worked as shown before. The link to the documentation can be found [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/src/master/docs/Camera Configuration.pdf) or can be found on the wiki [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Camera Configuration).

## Roles as a Customer
As stated, before I was the second customer for the project as I was the one mainly talking to the client for the unity component. Some of my roles including asking any question the Unity component had for the client and made sure that the unity component always keep up with the client’s requirement and that we were always on time with the deliverables. I would also constantly update the client on any big changes we had for the simulator through messages. Some interaction between me and client can be found in the Appendix A3. But not only did we message each other on Discord but I was always there in Client meeting to update him on smaller changes and if he liked what we did for the week or not.

---

#Quality of Technical Work Done
It is important to note that I didn’t do much coding throughout this project as Unity does not require you to code at all since, since I was building upon someone else unity program but instead I was mostly using the assets given to use by unity.

This meant it was very hard to check quality for the unity component as the unity component could not quantitively given a value but could only be done qualitatively. This meant that it was really up to my own opinion to see how good I actually did for the simulator component. 

So, for the beginning of the project I mostly worked alone for the unity component but would constantly update the client to see if my work was to his standard. While also showing him my weekly updates videos in the client meeting to see if quality was good. 

![Figure 11.png](https://bitbucket.org/repo/48xyAqR/images/3929279160-Figure%2011.png)

*Figure 11: One of the showcases I sent to the client to see if he liked it or not*

However, towards the middle and all the way to the end of the project, I did a lot of pair-programming with Julian this meant that I had another opinion on how I was doing the map as seen from our [communication logs](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Communication Log). So, we utilised a lot of user acceptance testing within the team, so we would constantly check the quality of the unity component with the team before we would show it to the client for his approval. So essentially we had a feed-back loop where we would get feedback on how good the maps looks to the teammate and so if they thought it was bad I would try to fix it and if they thought it was good we would show it to the client for his overall approval since the unity component is primarily for our client’s personal use and so in the end it really just matter on the if the client likes it or not. We also had a feed-back loop with our client so obviously if he thought it was good, we would continue doing what we were doing but if he wanted something changed, we would change it to his standard some of these interaction can be seen in the Appendix A3. This can be seen in multiple client meeting as he was often quite happy with the unity component as seen from the [weekly updates](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Weekly Updates/Landing) (If you check each week, normally it says the client is happy with the unity component).

This meant that I always kept a high quality of work since I was always trying to work off the advice given to me by both my teammates and client so that the quality was as good as it could possibly be.
I really didn’t use too much of discipline knowledge as stated before I didn’t code too much so this is not super applicable to me. However, I did have to understand the code given to use by the client in the unity component as I had to understand the gym created the environments. So, I had to go through multiple python files trying to understand the code how they were created so it was very useful to understanding how functions worked and how the import command worked and reading through a lot of someone else code would be difficult but because I understood how coding work I was able to track down how the gym and simulator communicate to each other. Here is evidence of me understanding the code of someone else [here](https://youtu.be/IOb12vrP5xQ). This is also true for trying to figure out the camera resolution as stated before I had to figure out how to get the camera resolution to work from the config by looking at the python code that run the simulator and the gym so I was looking through all the files and reading what was important and because I knew programming practices and had knowledge in functions and python I was able to understand how it worked and wrote documentation for it [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Camera Configuration).

Some of the challenges I faced was understanding environment id, menu creation, track implementation and working with blender.

Most of these challenges were due to me having zero prior knowledge in using unity, as this was the first time, I had ever used it so everything I did was pretty much a shot in the dark. To address this problem, I watched a lot of YouTube videos, but it was also just fiddling around with the unity program. So, I spent a lot of time trying different things until I finally found a method which would be very easy and simple to use. This is as I initially tried to make the track in blender as seen here 

![Figure 12.png](https://bitbucket.org/repo/48xyAqR/images/1053858100-Figure%2012.png)

*Figure 12: As you can see, I initially tried to make only the road in blender but then figured out another method*

But upon playing with unity more I was able to understand that I could use a .png as a texture instead of creating the roads in blender. This made it so that I could just drag and drop the images for the track I wanted and scale the dimension (I talk a bit about difficult in scaling here). 

![Figure 13.png](https://bitbucket.org/repo/48xyAqR/images/29967355-Figure%2013.png)

*Figure 13: The new map implementation*

One of the biggest problems was adding the new maps into the simulator so I asked the donkey car discord, but my question was ignored.

![Figure 14.png](https://bitbucket.org/repo/48xyAqR/images/4124911288-Figure%2014.png)

*Figure 14: (Hoeseph is me) As you can see my question was outright ignored by the users*

I then researched more into the donkey car GitHub repository and learnt how most of the simulator works and upon playing around with some reading of someone else coding I was able to figure out how to get the environment implemented into the as seen [here](https://youtu.be/IOb12vrP5xQ) (I’ve already talk about this problem a lot of time above). 

Another big problem we experienced was creating elevated tracks, as we had to have found our own way of creating the tracks and therefore we initially tried to creating it to using one asset known as ‘Beizer Path Creator’ but realized that it didn’t have enough functionality for the project as we had to manually place all the fences this would create a high time constraint and therefore we had to find another method for elevated track creation. I then found ‘SplineMesh’ which offer me more functionality but the only problem that we had was that we had to redo everything we did in Beizer Path Creator this meant that we lost a lot of progress since we had to start again. However, I believe that I still saved time as it could automatically do fences for me. This change can be shown in the [YouTube](https://youtu.be/sYmdjIXKRvw) video I had for the client. 

Working with blender was also difficult due to me never using blender before, but this wasn’t too much of a problem as there were multiple blender tutorials that I had used to try to get a better grasp of the program. This show evidently through my multiple iterations of signs as initially I had just a [basic sign](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/417ed28b9b021c47147f6c544aea11d2f8752ffa) but I would make improvement to the signs as I would understand more of how blender worked. As seen from the other iterations which include [this](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/8558f381c2492df08ab1094488621d369391e1c1) and [this](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/c73c3628b39ca26f81dd34975ab331a15f8e8ed2).

---

# Contribution
## Non-Technical 
My non-technical contribution involved understand the simulator, this includes figuring out how the simulator creates environment so that we could run the simulator through our web browser instead. After understanding this, I instructed everyone on how to run the new simulator with the new maps and how everything worked and guided them through the process in discord call. 

I played a major role in maintain the quality of the Bitbucket Wiki pages as the Wiki Expert, such as help creating templates, updating any pages and keeping all pages consistent. I was also in charge of placing links so that everything was easily accessible from the home page this included making the landing pages and constantly updating the wiki. The history of the Wiki can be found in the [Appendix A4](##A4)(show a lot of my edits). I also taken [minutes](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Minutes/Landing) and [weekly report](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Weekly Updates/Landing) for some of the meeting and weeks respectively. 

I’ve also attended [all group and client meetings](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Minutes/Landing), only missing two client meeting, to update our client with our project but to also always know what our client expects of us that week. Also stated above I was the second point of contact with the client asking him questions and letting him keep updated with the changes we thought were important. These are some images of our interaction. While the meeting that I did miss I would check the minutes when they were up to see what I had missed out on.

While I have attended [every team meeting and tutorials](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Minutes/Landing) so that I stay up to date with what everyone is doing but to also ask questions to the tutor whenever we felt stuck.

I was also pair-programming with Julian constantly as we were both working on the simulator and we always wanted to have a second opinion with anything we did for a quality reassurance. It can demonstrated in our [communication log](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Communication Log). 

One of the other contributions I had for the team was something called [VentureCafe](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Minutes/Week07_Team) for our group project. So, Patrick and I went to the VentureCafe to speak to industry professionals and allow them to provide insight into our work and what we could better for our project, and we tried to incorporate what they said to us for our own project. 

An issue I had as a wiki expert was that people would often have different naming conventions for their wiki pages and so would not link to the wiki landing page correctly. The fix to this was to always check the wiki page after they were done to see if they had correctly named the page or not and if they didn’t, I would edit it. This can be seen as now all our [meeting minutes](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/browse/Minutes) having the same naming scheme.

Another issues I had was that I would often have big assignments due throughout the semester since I was doing another project alongside this one. This is shown evidently in [week 11](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Weekly Individual Progress/Week 11) when my other project was due as I was doing the bare minimum. However, after my project was due then I would put it my all for this project this can be shown as I did almost all of the [client handover sheet](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Handover) which include creating the documentation and other files. 

This also meant that I had to pick up my slack by helping in the creation of the final group report and presentation. For the presentation I was in charge of creating and recording the [user stories](https://drive.google.com/drive/folders/1e5STrl2GYHfLVaO3nBWK1fi6bRfDJ_7_?usp=sharing) for the unity component but also creating the unity [demo](https://drive.google.com/file/d/1nRAYEPc85oMGlCr01UDtgHXyGe07cG_Z/view?usp=sharing) as well. While for the group report, I wrote a majority of the testing method, limitations, and pretty much anytime unity was mentioned I was writing and editing it. 

Like stated before I was often asked about unity map creations, so I was the group member who the group would talk to make certain training maps for them as seen here and the commit of the maps can be seen [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/770733b3987370453d690fc77d7c23b8151bfcce) 

![commit 7.png](https://bitbucket.org/repo/48xyAqR/images/2343923723-commit%207.png)

![Figure 15.png](https://bitbucket.org/repo/48xyAqR/images/666986944-Figure%2015.png)

*Figure 15:Winson ask me to make maps for him to use for testing*

![Figure 16.png](https://bitbucket.org/repo/48xyAqR/images/527134463-Figure%2016.png)

*Figure 16: Jordan asking for a map for testing purposes*

---

# Reflection
## Version Control
Version Control for the simulator was relatively easy to handle as it was just me and Julian working on the simulator component so we would often tell each other if we had changed something and if we did we would always pull the new changes before working on our stuff and later with pair programmed we would always have the same version as we were always working together. It was also a lot easier due to been able to track the changes through the source tree history menu to always see what each other did. I improved on version control by making my commits more explicit, so Julian always knew what I was pushing to the repo. However, we ran into issue because we were using two branches for the simulator, one being the master branch and the second being the experimental simulator. This wasn’t that much of an issue as I was always aware of what we changed in both and what we had to remove for our final client deployment. So overall version control was excellent for the simulator component.

## Coding Style
This really wasn’t an issue for the simulator component as most of the coding is just added extra lines in the already given code, so I would copy the formatting of the code so that it was consistent. As the rest of the ‘coding’ was done in unity, where it was more about the creation of new object and changing their properties through the menus. So, the coding style wasn’t really something we had to worry about for the unity component.

## Extreme Programming
We initially try to stick to our initial XP roles given in our group contract with success in the tracker and management roles but struggled with the programming roles with dual programming as initial everyone was just trying to figure everything out. However this change further into the project as me and Julian now ‘program’ in unity together quite frequently by sharing our screen and go through our thoughts process at each step so that we both get our ideas across instead of one person doing work one day and the other another day. We have now decided as a group to be stricter on the XP roles given to us and to follow the procedures more often. This is evident as Julian would become the manager while Winson was the tracker and constantly asked us biweekly what we did so that everyone now knew where we were at. While for me as a customer for the rest of the project allowed me to have stricter guidelines on where I wanted the unity component to go and was more in command of what we had to complete and by what time.

## Challenges 
We initially struggling with how was going to send in the weekly meeting every week, but upon just talking about how we want things to go we were able to decide how it was going to work. I also initially struggled with making the actual environments and maps and tried asking the discord as seen from above. In the end, I overcame this problem by doing some more resource into the GitHub of the donkey car and look into the code and in the end found the solution upon examining multiple files of code. We also struggled to decide where we would update each other as the university wanted everything to be done in slack but we preferred to use discord for updates. In the end we decided to use discord to speak to each other but slack for major updates and changes. Another major challenge we had was talking to one of group mates due to him living in Canada so was in a completely different time zone. So, communication with him was very tricky. However, to overcome this I would message him in the morning if I need anything from him. Probably the biggest challenge was working with a new software (Unity), as stated beforehand a lot of issue occur when using unity as I was unfamiliar with it but upon just spending more time on it and watching videos I was slowly able to fully understand its functionality and utilize it correctly.

## Roles 
As stated above the main roles I undertook for the group was tracker in week 4, customer and even a little bit of being a doomsayer. The customer role was very important as I was able to talk to the client about the requirement for unity and quickly ask him any problems that we had and because of this clear communication line I was always able to instruct my other group mates to what we had to do and what we need to improve on in Unity. While the main role I had for this group was to foresee the improvement of the simulator, so being the Unity Expert. This is by understanding the codes and objects but also testing how well our simulator mimics real life and constantly changing it so that it is life-like as possible. As the unity expert I was also in charge of creating anything the OpenCV team need and so was able to help the other team also increase their efficiency, this was done by making maps specifically for them to use for testing. While I also had to play the role of the Wiki expert so was in charge of cleaning up a majority of the wiki, I made it so the wiki would always be eligible and also consistent. I also made the any wiki page accessible from the home page and was also aesthetically pleasing.

## Overall 
I feel that most of my group has been amazing by constantly keeping each other up to date with where everyone is up to but also being honest when they feel like they are falling behind. It was also great that when someone was stuck, there was always someone there to help them out and work on it with them. Everyone has also been very friendly and constantly try to keep our group moral up as everyone is excited about this project. However, we did have some problem with a group member but try to push him as much as possible to do his work. We would also often give him the easy workload so he could at least do something. I believe that we could have approached this problem a lot harsh by being stricter with him instead of letting him off easy.

However even with this I believed that our team performed brilliantly as we were able to finish all the requirement set out for us by the client with excellent results. Our client was happy with what we achieved throughout the project and I believe that everyone tried to really push for the best. 

Some improvements for the overall project was to stricter on teammate that didn’t attend the meeting and also decide how we would communicate a lot earlier as a lot of us wanted to use discord, but we were meant to use slack. So, I think the best idea is to only use the communication that was required of us (Slack) instead of doing whatever we wanted this is so that communication can all be kept in one place but also so that the project could start earlier.

For the first 6 weeks I believed that we achieved a lot but lack a lot of evidence for the report as we were mostly talking in voice chat and not recording what specifically we were talking about so by the time we had to do our individual report, the evidence was really lacking. We also had a lot of XP role rotation in the beginning of the project. This was ok since everyone wanted to try their hands at all the roles but was difficult because we would often forget who was what role for the week so didn’t know who to talk to.

So from the mid semester break and onwards we starting keeping a [weekly individual progress](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Weekly Individual Progress/Landing) page so that we had evidence on what we did weekly but also we were able to see what everyone did. While we also started to do a [communication log](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Communication Log) for further evidence for our individual report. We also decided on more defined roles for each group member, so we no longer did XP role rotation, as we decided Julian was our manager, Winson was our tracker and Patrick and I were the customer. With everyone being a tester and programmer. This was a more efficiency way of doing the project as we now knew who exactly to talk to if we had problem and Winson always keep track of how everyone was doing so that no one was slacking. While Patrick and I constantly communicated with the client and each other about requirements we need to get done and if we need anything from the other team.

In conclusion, I believe that I have contributed a lot to this project and has allowed the project to be a great success. But I believe that that I was unable to do this alone and that my teammates have been a great help throughout the whole project. I have developed many skills and techniques, because of working as a team and using this agile method.

---

# Appendix
## A1 History of Experimental_Simulator (Deleted Branch)
![Figure 17.png](https://bitbucket.org/repo/48xyAqR/images/2142703212-Figure%2017.png)
![Figure 17B.png](https://bitbucket.org/repo/48xyAqR/images/2108372434-Figure%2017B.png)

*Figure 17: Just for evidence to show that we had an experimental simulator that was deleted*

## A2 Screenshot of Maps
![Figure 18.png](https://bitbucket.org/repo/48xyAqR/images/3971262066-Figure%2018.png)

*Figure 18: First flat track I created (Called Track 2 by our Client)*

![Figure 19.png](https://bitbucket.org/repo/48xyAqR/images/1559745089-Figure%2019.png)

*Figure 19: Second flat track I implemented into the simulator (Called Challenge Track by our client)*

![Figure 20.png](https://bitbucket.org/repo/48xyAqR/images/1670715091-Figure%2020.png)

*Figure 20: The F1 Hockenheim Track I implemented into the simulator. I had put in the road with elevation and width changes but also the fence which cannot fully see as we are at bird-eye view but there are fences around the track as well.*

![Figure 21.png](https://bitbucket.org/repo/48xyAqR/images/4237026748-Screenshot%202020-11-29%20221758.png)

*Figure 21: The F1 Monaco Track I implemented into the simulator, I made the road not the terrain. With the road having being the correct layout, scale and elevation. I also added the fences which yet again are hard to see due to being a bird-eye view but also the tunnel.*

## A3 Interaction with Client
![Figure 22.png](https://bitbucket.org/repo/48xyAqR/images/1053361184-Figure%2022.png)

*Figure 22: Interaction about map creation*

![Figure 23.png](https://bitbucket.org/repo/48xyAqR/images/1545327713-Figure%2023.png)

*Figure 23: Interaction about talking dimensionality of the map*

![Figure 24.png](https://bitbucket.org/repo/48xyAqR/images/3995672519-Figure%2024.png)

*Figure 24: Interaction about quality of the map*

![Figure 24B.png](https://bitbucket.org/repo/48xyAqR/images/2069325170-Figure%2024B.png)

*Figure 24 continued: Further interaction about changes to the map*

![Figure 25.png](https://bitbucket.org/repo/48xyAqR/images/2326502381-Figure%2025.png)

*Figure 25: Confirmation if he liked what I had achieved so far*

![Figure 26.png](https://bitbucket.org/repo/48xyAqR/images/1456451439-Figure%2026.png)

*Figure 26: Interaction about getting the new map into the gym*

![Figure 27.png](https://bitbucket.org/repo/48xyAqR/images/1653967062-Figure%2027.png)

*Figure 27: Asking the client about the approval of the menu screen*

![Figure 28.png](https://bitbucket.org/repo/48xyAqR/images/365074538-Figure%2028.png)

*Figure 28: Asking the client about the dimensionality of one of the signs*

![Figure 29.png](https://bitbucket.org/repo/48xyAqR/images/3372305875-Figure%2029.png)

*Figure 29: Updating the client on the progress of our sign scaling*

![Figure 30.png](https://bitbucket.org/repo/48xyAqR/images/3844371603-Figure%2030.png)

*Figure 30: Question to the client about scaling the signs*

![Figure 31.png](https://bitbucket.org/repo/48xyAqR/images/770651943-Figure%2031.png)

*Figure 31: Asking for feedback about the map*

![Figure 32.png](https://bitbucket.org/repo/48xyAqR/images/3086605079-Figure%2032.png)

*Figure 32: Questions about the F1 tracks in simulator*

![Figure 33.png](https://bitbucket.org/repo/48xyAqR/images/2686462057-Figure%2033.png)

*Figure 33: Interaction about installing our software*

![Figure 34.png](https://bitbucket.org/repo/48xyAqR/images/1153198688-Figure%2034.png)

*Figure 34: Question about the quality of the F1 track*

![Figure 35.png](https://bitbucket.org/repo/48xyAqR/images/3766181382-Figure%2035.png)

*Figure 35: Bringing up the solution we found for camera resolution (we joined the call after)*

![Figure 36.png](https://bitbucket.org/repo/48xyAqR/images/3155030785-Figure%2036.png)

*Figure 36: Asking advice about pruning our repo*

![Figure 37.png](https://bitbucket.org/repo/48xyAqR/images/2618764445-Figure%2037.png)

*Figure 37: Helping Cian with a presentation about map implementation*

![Figure 38.png](https://bitbucket.org/repo/48xyAqR/images/1204495056-Figure%2038.png)

*Figure 38: Asking Cian his opinion on the menu*

![Figure 39.png](https://bitbucket.org/repo/48xyAqR/images/2804066281-Figure%2039.png)
![Figure 39B.png](https://bitbucket.org/repo/48xyAqR/images/3009505150-Figure%2039B.png)

*Figure 39: Helping Cian figure out map implementation*

![Figure 40.png](https://bitbucket.org/repo/48xyAqR/images/1882060214-Figure%2040.png)

*Figure 40: Asking question about the documentation process for the map*

![Figure 41.png](https://bitbucket.org/repo/48xyAqR/images/2219520699-Figure%2041.png)

*Figure 41: Asking for our client deployment video to use for our handover*

![Figure 42.png](https://bitbucket.org/repo/48xyAqR/images/897615956-Figure%2042.png)

*Figure 42: Asking about Handover and what he wanted to do with it*

## A4 History of Wiki
![Figure 43.png](https://bitbucket.org/repo/48xyAqR/images/3400694097-Figure%2043.png)
![Figure 43B.png](https://bitbucket.org/repo/48xyAqR/images/3191827158-Figure%2043B.png)
![Figure 43C.png](https://bitbucket.org/repo/48xyAqR/images/3067931914-Figure%2043C.png)
![Figure 43D.png](https://bitbucket.org/repo/48xyAqR/images/3215975968-Figure%2043D.png)
![Figure 43E.png](https://bitbucket.org/repo/48xyAqR/images/978073006-Figure%2043E.png)
![Figure 43F.png](https://bitbucket.org/repo/48xyAqR/images/1645135091-Figure%2043F.png)

*Figure 43: This was the day I fully fixed the whole wiki so that it was consistent and looked overall more appealing.*

![Figure 44.png](https://bitbucket.org/repo/48xyAqR/images/1249178596-Figure%2044.png)

*Figure 44: Fixing the landing pages for the upcoming weeks*

There is more but they are smaller edits.