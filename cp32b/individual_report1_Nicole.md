# Individual_report1_Nicole
This is the individual report for @Nicole Huang for the First Report due Sunday 4th October 2020.

---

# Clear statement of work done

To ensure that everyone has experienced different roles, we have a XP role rotation in week 2 to week 5. The main XP roles I have undertaken are listed below:

* Manager: I am responsible for organising meetings and write the minutes for week3. All meeting minutes can be found on our [Wiki pages](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home). I have also created Trello board for manage user stories.
* Customer: I represent the group and communicate with the client through meeting to ensure the project scope are met. Evidences can be found in **appendix A**. 
* Programmer: I have been involved in creating Blender 3D models and collaborating with @Mouyi to create track using Unity. 
* Data collector: I have collected images of donkey car driving in our custom map for training sign detection model. Evidences can be found in **Extent of that work** section. 

Also, I have been assigned the role of blender expert to ensure the overall quality of our project, expecially with improving the donkey simulator environment. 

* Blender Expert: ensuring the quality of signs and format of signs can be built and exported correctly and also making sure they can be successfully implemented in Unity. Evidences can be found in **appendix B**. 

The following table is my **weekly plan** (Consider we have changed a project, the new project started at week 3): 

|       | Plan                                                                                                                                                   | Work Done                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| week3 | Set up environment for new project according to Client’s requirement.                                                                                  | 1. Discussed changing project from cp4 to cp32 with coordinator/client and tutor. 2. Joined discord channel. 3. Uploaded [week 3 meeting minutes](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/MeetingMinutes_Tut_Week3) to wiki page. 4. Set up Donkey car simulator and Tensorflow environment.                                                                                                                                                                                                                                                                                                                                       |
| week4 | Start the new project and learn through the materials (Tensorflow image classification tutorial and donkey car training tutorials) provided by client. | 1. Wrote the Scope Statement for cp32. 2. Learned about TensorFlow image classification through the [tutorial link](https://www.tensorflow.org/tutorials/images/classification). 3. Train Donkey car model using gen_track_user_drv_right_lane && gen_track_usr_drv_recovery data files. Here is my [video link](https://youtu.be/totA3HmxinM).                                                                                                                                                                                                                                                                                                          |
| week5 | Improve donkey car simulator environment by creating signs models on Blender and creating new track on Unity.                                          | 1. Collaborate with Mouyi, working through the document "Map and Sign implementation" and create our new track on Unity and successfully run the donkey car on the map. 2. Create multiple signs (including Stop, left turn, right turn and parking) and objects using Blender, which then Mouyi has imported them to the new track.                                                                                                                                                                                                                                                                                                                       |
| week6 | 1. Teach the team for new track environment set up. 2. Prepare for the group report/demo and invidual report.                                       | 1. Write the guide for setting up the environment on donkey simulator for new track. [Wiki page Link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Donkey%20car%20environment%20for%20new%20created%20track%20SetUp%20Guide). 2. Write the wiki page for first project report. As well with the pdf format submitted to Canvas. [Wiki page link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/COMP3988_T17B_Group1%20First%20Project%20Report). 3. Write the individual report. 4. Contribute to the video demo. 5. Help to collect raw image data for sign detection. 6. Organize Trello board for manage User Story. |

**More about my weekly works can refer to my** [**individual weekly report**](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Nicole)**.** 

---

# Extent of that work

**Technical and XP roles**

The technical compotents of the project can be broken down into two parts: 

1. Improving donkey car simulator environment.
2. Writing sign detections code using tensorflow. 

I majorly work in part 1. To improve the donkey car simulator environment means we required to create our own tracks and need to enable the car to run on it. As a role of a **programmer**, I collaborate with Unity expert Mouyi. We built two tracks on Unity individually. In order to improve efficiency, we assigned different tasks, which he will focus on building tracks on Unity while I will focus on creating signs using Blender. 

After my signs are ready to export to Unity, I sent to Mouyi straight away. I pushed them to bitbucket under the simulator branch as well. 

![Sign models - evidences of push](https://paper-attachments.dropbox.com/s_9EA5BC4E79877F64D092DB5A77EDCCFAAF52827B6D474ABE38B625E6E0C7CFFC_1601790511351_Screen+Shot+2020-10-04+at+4.48.24+pm.png)

![Other models on track - evidence of push](https://paper-attachments.dropbox.com/s_9EA5BC4E79877F64D092DB5A77EDCCFAAF52827B6D474ABE38B625E6E0C7CFFC_1601790063389_Screen+Shot+2020-10-04+at+4.40.17+pm.png)


While Mouyi implemented my models to Unity, we also communicated on models’ size/light adjustment. For example, we need to adjust the size sign the Unity to real world size is 8.79 to 1m. While the track is ready to use**,** I also helps in driving donkey car to see whether the signs can be detected by the car’s camera.  

After that, I also wrote a [documentation](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Donkey%20car%20environment%20for%20new%20created%20track%20SetUp%20Guide) to help the team with implement tracks to their local simulator. 

In part 2, as a **data collector,** I was involved in driving car on new tracks to collect raw data of sign images. This was to collect datas for other members who involved in writing sign detection codes. 

![Evidences of my raw data, pushed by Yiran](https://paper-attachments.dropbox.com/s_9EA5BC4E79877F64D092DB5A77EDCCFAAF52827B6D474ABE38B625E6E0C7CFFC_1601791398313_Screen+Shot+2020-10-04+at+5.02.55+pm.png)


In addition, I also helped @Robert with testing out the network settings for virtual server for leaderboard. 

---

# Quality of technical work done


- To ensure the quality of the track environment, which includes image resolution of the signs and tracks. I and @Mouyi collaborated with @Yiran and @Yuanda, where we all tried on the new tracks on simulator and collect images of signs. They helped in providing us with the images collected, so we can see whether we need to improve the signs or tracks’ size and clarity. Evidences in **appendix C**. 
- Since Unity and Blender does not involve much coding, we do not have any peer code review.  But I and @Mouyi have peer reviewing with each other, in order to improve quality of signs (from blender) and quality of tracks (from unity). For example, to improve the quality of signs, @Mouyi would give me feedback when he imprement my signs models in Unity, which allowed me to make further modification. 

---

# Other contribution to group processes

**All group activities with links to the evidence.**

- I finished all tasks that allocated to me each week. 
- I have been allocated a role of manager for week 3. I was responsible for organizing meetings. Also to record [meeting minutes](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/MeetingMinutes_Tut_Week3). 
- I created Trello board and managed User story using the board for our group. 
![Evidences of Trello board](https://paper-attachments.dropbox.com/s_9EA5BC4E79877F64D092DB5A77EDCCFAAF52827B6D474ABE38B625E6E0C7CFFC_1601792155033_Screen+Shot+2020-10-04+at+5.15.49+pm.png)

- I wrote a [documentation](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Donkey%20car%20environment%20for%20new%20created%20track%20SetUp%20Guide) to help the team with implement tracks to their local simulator. 
- I have been involved in writing the group scope statement during the project. [client contract](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Scope_Statement_overall)
- Additionally I also wrote the first project report in [Wiki pages](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/COMP3988_T17B_Group1%20First%20Project%20Report) format as well as pdf for Canvas submission. 
![Evidence of first project report](https://paper-attachments.dropbox.com/s_9EA5BC4E79877F64D092DB5A77EDCCFAAF52827B6D474ABE38B625E6E0C7CFFC_1601792371024_Screen+Shot+2020-10-04+at+5.19.26+pm.png)


 
 **Evidence of collaboration and teamwork**
 

- Collaborate with @Mouyi in “improving donkeycar simulator environment” through Zoom meeting and Wechat meeting. Our works are pushed to [bitbucket](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/?page=2). 



- Collaborate with @Yiran. [Collect data](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/2fff60ca3f5edd2857ef183377d8d2b59f0858c8) for her sign detection code. 

**“Issues” created and progress**

- I and @Mouyi has prepared the user stories and uses [Trello board](https://bitbucket.org/RobertJia/comp3988_t17b_group1/addon/trello/trello-board) to visualize the remaining tasks. Our team also has used [Jira Issues](https://bitbucket.org/RobertJia/comp3988_t17b_group1/jira?site=be859735-9bb3-4a0d-a5cb-b2a285747fd9&statuses=new&statuses=indeterminate&statuses=done&sort=-status&page=1) to track all the user stories as well as status of any remaining tasks.  [Here is one evidence of a issue created by me](https://yuanda-dong.atlassian.net/browse/CP-6).

---

# Reflection

**Version control**

Our team have used [bitbucket](https://bitbucket.org/RobertJia/comp3988_t17b_group1/branches/?sort=name) for version control. For the two major parts of the project “improving simulator environment” and “detect signs using tensorflow”, our bitbucket also has branches “master” and “simulator” for them respectively. The bitbucket went well except an issue that we are reacting the repository’s limit size.

**XP**

Our team have followed the XP practices, which involving: 

- Communication: We are unable to do  face to face discussion due to the covid-19. But we ensure our effectiveness of communication by frequently meet online with group members and also with clients. We have meeting with client twice a week and also communicate with group members/client on daily basis on Discord. 
- Feedback: Our team constantly feedbacking about the previous efforts, and revising previous practices. Either through peer reviews and meeting. Achieving a continuous improvement process. 

 
**Challenges**

- Late start: Our team start the current project in week 4 as we left 3 week behind compared to other team. It is a challenge for us to catch up. We need to work very hard in each sprint and frequently communicate with cient. 
- Software environment set up: The current project has many software environment to set up. Since our team have different systems (Win, Mac, linux…), each of us also faced different set up issues. I had met an issue related to version constraints, such that I had downloaded tensorflow v2 before, while its module has not attribute ‘app’, thus I cannot use that attribute. The solution is to use tensorflow v1. However, it became a great challenge as many of these set up issues happened. To tackle that, our team members chat on Discord and seeked help. 
- Learning new software: Within limited time, we need to learn new software. For example, I had never used Unity and Blender before. But in order to finish my work, I need to learn them from the very begining. It created challenges for me along with the time pressure. To tackle that, I spent lots of time on learning them and simplified documentation for other group members. 

**Role in the group and as a software engineer**

- As already stated above, I have been involved with creating 3D models using Blender and created track using Unity according to client’s requirement. 
- Other activities I’ve been involved in as a software engineer included collecting data for sign detection on donkey car simulator. Writing documentation for new track set up on donkey simulator. [Wiki page Link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Donkey%20car%20environment%20for%20new%20created%20track%20SetUp%20Guide)
- In addition, I have gone through the sign detection code base that @Yuanda and @Yiran are working with. 

**Future Improvement**

Our group is doing well so far, especially considered with the 3 weeks delay. Our tensorflow code is able to detect stop signs and stop the donkey car in the simulator.  I will continue work on Blender and Unity, as in the later day, more signs and tracks are required by client. At the same time, I will also assist with detecting other signs using Tensorflow. 

---

# Wiki
- [Link to Our Wiki home pages](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home)
- [Link to my individual weekly report](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Nicole)
- [Link to group first project report](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/COMP3988_T17B_Group1%20First%20Project%20Report)

---

# Appendix

## appendix A - Collect questions from the groups and record answers from client (previous project)

![](https://paper-attachments.dropbox.com/s_9EA5BC4E79877F64D092DB5A77EDCCFAAF52827B6D474ABE38B625E6E0C7CFFC_1601798136302_Screen+Shot+2020-10-04+at+6.55.29+pm.png)


## appendix B - Blender signs 
- 3D models to be implemented in Unity must be in fbx format
![3D models to be implemented in Unity must be in fbx format](https://paper-attachments.dropbox.com/s_9EA5BC4E79877F64D092DB5A77EDCCFAAF52827B6D474ABE38B625E6E0C7CFFC_1601798380125_Screen+Shot+2020-10-04+at+6.59.30+pm.png)

- For a FBX model to have color, it must be in copy path mode + embed texture
![For a FBX model to have color, it must be in copy path mode + embed texture](https://paper-attachments.dropbox.com/s_9EA5BC4E79877F64D092DB5A77EDCCFAAF52827B6D474ABE38B625E6E0C7CFFC_1601798470649_Screen+Shot+2020-10-04+at+7.01.01+pm.png)


## appendix C - Evidences from Discord.
- Evidences of Yuanda tested out the track and gave feedback to us.
![Evidences of Yuanda tested out the track and gave feedback to us.](https://paper-attachments.dropbox.com/s_9EA5BC4E79877F64D092DB5A77EDCCFAAF52827B6D474ABE38B625E6E0C7CFFC_1601800369095_431601800321_.pic_hd.jpg)

- Evidences of we modified the size of signs
![Evidences of we modified the size of signs](https://paper-attachments.dropbox.com/s_9EA5BC4E79877F64D092DB5A77EDCCFAAF52827B6D474ABE38B625E6E0C7CFFC_1601800438803_441601800354_.pic_hd.jpg)