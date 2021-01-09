# Final_individual_report_Nicole
This is the individual report for @Nicole Huang for the Final project report due Sunday 29th November 2020.

## Individual Information

**Unikey:** zhua4138

**SID:** 480359623

**Group name:** COMP3988_T17B_Group1

**Client name:** Cian from Robotics Master


---

# Clear statement of work done

We perform a XP role rotation in our group in week 2 to week 5. The main XP roles I have undertaken can be found in [my first individual report](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/individual_report1_Nicole). 

From week 7 to the end of the semester, our group did not perform any role rotation. However, after week 7, I have undertaken the role of tester, programmer and blender expert. 

* Programmer: I have been involved in creating Blender 3D models since the start of the project. From week 7 and after I also continue working with Blender to create models for new signs and objects on new tracks. 

Also, I have been assigned the role of blender expert to ensure the overall quality of our project, especially with improving the donkey simulator environment. 

* Blender Expert: I have been assigned the role of blender expert to ensure the overall quality of the models and also making sure they can be successfully implemented in Unity. Since I have the experiences in making models from the start of the project, so I have involved in teaching our members @Sipei Jia to use blender for model creation after week 6. I have also uploaded some blender tutorials on our project [Wiki page](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Useful%20Blender%20and%20Unity%20tutorial)


The following table is my **weekly plan** from week 7 - week 13 (The evidence before week 7 can be found on [my individual wiki page](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Nicole)): 

|       | Plan                                                                                                                                                   | Work Done                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| week7 | Build new signs according to the new scope given by the client.                                                                                  | 1. Build new signs required by the scope using Blender (Including traffic light red, yellow; blue and black turning arrow; green, yellow, white parking signs, speed 50). 2. Modify thickness of signs and height of signs according to testing group (@Yiran and @Yuanda). 3. Create a Blender and Unity tutorial document on [Wiki](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Useful%20Blender%20and%20Unity%20tutorial). 4. Research on new maps that we required to build for new scope and put it on [Wiki](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Useful%20Blender%20and%20Unity%20tutorial).                                                                                                                                                                                                                                                                                                                                      |
| week8 | Start the new tracks creation. (Two F1 tracks.) | 1. Make the picture for two new maps (required by the scope) a Higher resolution using lightroom.  2. Create two new map objects on Blender and collaborate with @Mouyi, who test the map objects on Unity. 3. Modify the Ferrari S1000 model on Blender. (Modification on tires).                                                                                                                                                                                                                                                                                                          |
| week9 | Create models for objects on the new tracks.                                         | 1. Make the model of the stadium for the two new tracks on BLENDER.  2. Make the model of the track barriers on BLENDER.                                                                                                                                                                                                                                                                                                                       |
| week10 | Improve F1 track models                                         | 1. Help to improve F1 track model, collaborating with Mouyi Xu and Robert Jia. For example, discussing adding lake to the track.                                                                                                                                                                                                                                                                                                                      |
| week11 | Document my model creation                                         | Create [Blender model documentation](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Blender%20documentation)                                                                                                                                                                                                                                                                                                                      |
| week12 | Final project presentation                                         | 1. Contribute to the group demo video (slide 6 - 11) for the presentation. The slides can be found here: https://docs.google.com/presentation/d/1D2ldYPLLpUOHR_xMz1kFZU-CrPrlHsQyow-lb2i1E0Y/edit#slide=id.g9cd4b9b3fd_0_18. The demo video can be found on Canvas. 2. Write the group review for the group members.                                                                                                                                                                                                                                                                                                                      |
| week13 | Final client deployment and report submission                                        | 1. Contribute to the client deployment for simulator section. Introduce track creation and model creation. 2. Contribute to the group report section: system specification.  3. Contribute to the creation and implement of the user story.  4. Write the final individual report.                                                                                                                                                                                                                                                                                                                      |


**More about my weekly works can refer to my** [**individual weekly report**](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Nicole)**.** 

---

# Extent of that work

**Technical roles**

The technical components of the project can be broken down into three parts with one addition from the new scope statement given by the client after week 6: 

1. Improving the donkey car simulator environment.
2. Writing sign detections code using TensorFlow. 
3. F1 tracks and F1 car model creation.

Started from week 7, I majorly worked in part 1 as well as the new scope component part 3 collaborating with @Mouyi Xu and @Sipei Jia. 

Part 1 is nearly done after the first project report. However, there were still some signs remaining need to be done after week 7. As the role of a **programmer**, I collaborate with Unity expert @Mouyi Xu. I built ranges of signs required by the client while @Mouyi Xu had created 4 extra test tracks such that each of them contains 4 signs selected randomly with different colours. This is one example of the test track:

![1.png](https://bitbucket.org/repo/G6xBMXK/images/1417077519-1.png)

The ranges of signs created after the new scope include:
![2.png](https://bitbucket.org/repo/G6xBMXK/images/2957323248-2.png)

After that, we start the work with two F1 tracks and F1 car models. Due to the heavy workload, @Sipei Jia had joined us for model creation. As a role of a **Blender expert** I involved in teaching our new partner for model creation. The documentation of the useful Blender tutorial link and 3d F1 car models can be found on our [Wiki page](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Useful%20Blender%20and%20Unity%20tutorial).

Works on F1 track model: 
There are two F1 track models we are required to create. One is the Shanghai F1 track and one is the Melbourne F1 track. We thanks our friend @Chunyue Zheng for repainted these two track maps on photoshop that eliminated insignificant elements on the map. I regenerated the picture into a higher resolution using lightroom and then used it in blender to create a track object. This object was later on export as fbx to Unity for the combination of the track and objects on the track.

![3.png](https://bitbucket.org/repo/G6xBMXK/images/366295697-3.png)


To made the F1 track closer to the one in the real world, I also created some objects on the track. For example, the stadium and the track barrier. A documentation of how I created the objects can also be found on the [Wiki page](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Blender%20documentation)

![4.png](https://bitbucket.org/repo/G6xBMXK/images/243131716-4.png)

![5.png](https://bitbucket.org/repo/G6xBMXK/images/3352792068-5.png)

Due to the size limit of our repo, the group members who worked with the simulator decided to start a new git repo. And our models and tracks are uploaded [there](https://github.sydney.edu.au/moxu7046/COMP3988_simulator/commits/master). 

Here are some evidences of my commit of models.

![6.png](https://bitbucket.org/repo/G6xBMXK/images/3000229926-6.png)

![7.jpeg](https://bitbucket.org/repo/G6xBMXK/images/730051615-7.jpeg)

Due to the size issue with some of the models, such as stadium. It is too large to upload. So I and @Mouyi Xu decided to use QQ drive to send through the models. 

![Screen Shot 2020-11-29 at 8.11.06 am.png](https://bitbucket.org/repo/G6xBMXK/images/2693677701-Screen%20Shot%202020-11-29%20at%208.11.06%20am.png)

---

# Quality of technical work done


- Sign detection: I and @Mouyi have peer reviewing with each other. We held zoom meeting together and tested each other's works, in order to obtain a good quality of sign models for delivery. For example, to improve the quality of signs, @Mouyi would give me feedback when he imprement my signs models in Unity, which allowed me to make further modification. 

- F1 tracks and models: We @Mouyi @Sipei improved the tracks by communicate through zoom meeting. For example, @Mouyi would do screen sharing while he drive the car in simulator. So that the rest of us who did model creation can give devices for the improvement in the implementation of the tracks. We also get devices from the Client Cian, to see his level of satisfaction. 


---

# Other contribution to group processes

**All group activities with links to the evidence.**

- I finished all tasks that allocated to me each week. 
- I created and implementeduser stories on Trello board for our group. 
![Screen Shot 2020-11-29 at 8.03.28 am.png](https://bitbucket.org/repo/G6xBMXK/images/1105947957-Screen%20Shot%202020-11-29%20at%208.03.28%20am.png)

- I collected a [useful blender tutorial](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Useful%20Blender%20and%20Unity%20tutorial) documentation for our group members who working on simulator part of the project with us. 

- I wrote a [Blender documentation](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Blender%20documentation) that documented how I created the models for signs, F1 tracks and objects on the tracks, such that other members can easily follow the steps for model creation in the future.  

- Additionally I also contribute to the final project report, client deployment as well as the project demonstration. These can be found in the links in our [Wiki pages](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home). 


 
 **Evidence of collaboration and teamwork**
 

- Collaborate with @Mouyi in “improving donkeycar simulator environment” through Zoom meeting and Wechat meeting. We worked together to create additional signs required by the client.

- Collaborate with @Sipei and @Mouyi in "F1 tracks and F1 car model creation" through Zoom meeting.

Our works are pushed to [github repo](https://github.sydney.edu.au/moxu7046/COMP3988_simulator/commits/master). 

Due to the size limitation of our original bitbucket repo, the pushes of our simulator parts were deleted from the bitbucket. The evidences of pushes are from github repo and the screenshot of bitbucket repo before deletion (Attached in the previous section "Extent of that work").

**“Issues” created and progress**

- I and @Mouyi has prepared the user stories and uses [Trello board](https://bitbucket.org/RobertJia/comp3988_t17b_group1/addon/trello/trello-board) to visualize the remaining tasks. Some new user stories for the new scopes are also created and managed by us. Our team also used [Jira Issues](https://bitbucket.org/RobertJia/comp3988_t17b_group1/jira?site=be859735-9bb3-4a0d-a5cb-b2a285747fd9&statuses=new&statuses=indeterminate&statuses=done&sort=-status&page=1) to track all the user stories as well as status of any remaining tasks.  [Here is one evidence of a issue created by me](https://yuanda-dong.atlassian.net/browse/CP-6).

---

# Reflection

**Version control**

Our team have used [bitbucket](https://bitbucket.org/RobertJia/comp3988_t17b_group1/branches/?sort=name) for version control. (The evidence of the repo was attached in the previous section). Due to the size limitation of our original bitbucket repo, we (the group members working on the simulator) also created a [github repo](https://github.sydney.edu.au/moxu7046/COMP3988_simulator/commits/master) that contains our simulator works only. 

**XP**

Our team have followed the XP practices, which involving: 

- Communication: We are unable to do face to face discussion due to the covid-19. But we ensure our effectiveness of communication by having weekly meeting among the development teams. During the meeting, we discuss the progress of each member. We also have meeting twice a week with the client. During the meeting The team would demonstrate new features to the client. The team also communicate with group members/client on daily basis on Discord. 

- Feedback: Our team constantly feedbacking about the previous efforts, and revising previous practices. Either through peer reviews and meeting. Achieving a continuous improvement process. 

 
**Challenges**

- Technical challenges: Some fbx models export from blender to Unity lose colour. We spend lots of time in manually recoloring the model using hexadecimal value and choosing the similar surface that’s available in Unity. We found out at the end that this is due to the limitation of material surface. Unity is unable to recognize some material surface from Blender. Solution is to bake the whole material (which is a tool in blender). 


- Time pressure towards the end of the semester: Group members are busy with other assignments while the client keeps adding new components to the existing scope. This created lots of pressure to us. However, our group members help each other a lot and through communication, we and the client reached an agreement with the final delivery. 

- Software environment set up: The current project has many software environment to set up. Since our team have different systems (Win, Mac, linux…), each of us also faced different set up issues. I had met an issue related to version constraints, such that I had downloaded tensorflow v2 before, while its module has not attribute ‘app’, thus I cannot use that attribute. The solution is to use tensorflow v1. However, it became a great challenge as many of these set up issues happened. To tackle that, our team members chat on Discord and seeked help. 

- Learning new software: Within limited time, we need to learn new software. For example, I had never used Unity and Blender before. But in order to finish my work, I need to learn them from the very begining. It created challenges for me along with the time pressure. To tackle that, I spent lots of time on learning them and simplified documentation for other group members. Same issue for @Sipei who started to learn Blender in week 7. 

**Role in the group and as a software engineer**

- As already mentioned above, I have been involved majorly with 3D sign models creation, simulator tracks creation and 3d objects creation according to client's scope requirement. My job was also to collaborate with @Mouyi and @Sipei to imprive simulator environment. 

- Other activities I’ve been involved in as a software engineer included writing documentation for new track set up on donkey simulator [Wiki page Link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Donkey%20car%20environment%20for%20new%20created%20track%20SetUp%20Guide); writing documentation for 3D models and track models creation [Wiki page Link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Blender%20documentation); collecting useful model creation tutorials and unity tutorial for group members [Wiki page link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Useful%20Blender%20and%20Unity%20tutorial). 

**Final project delivery**

Our final project is within a deliverable quality especially considered with the 3 weeks late start. Every group member was responsible and was communicated well with each other. 

The simulator team @Mouyi @Sipei @Nicole had delivered all requirements in the new scope and with a good quality. The algorithm team @Yiran @Yuanda @Hao did not completed detection codes for all traffic signs. However, they worked very hard to improve their detection models in many appraoches, such as from OpenCV. They were tried to stablize the detection accuracy rather than write many detection codes with low accuracy. 

Based on the feedback given from the tutor and the client, our team developed a continuous integration tools involved things such as testing. However, it was developed near the end of the project. For improvement, this shoud be implemented as early as possible. Also, there was also an issue with job assignment. Towards the end of the semester (Week 11, 12), the simulator team were nearly done with the jobs while the algorithm team were still having a lot to do. To adjust this, the job assignment should be done earlier, for example, these two teams would not spend extra time doing some jobs that only required one team to do.


---

# Wiki
- [Link to Our Wiki home pages](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home)
- [Link to my individual weekly report](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Nicole)
- [Link to group final project report](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/FinalGroupProject)