# Final Individual Report
## Clear Statement of Work Done
### Roles and Contributions
- Simulator Manager: I take the role of Simulator Manager from week 7 to week 12. I decided the requirements and user stories of the simulator part to be done for the new week. Also, I split these works and assign to the other two teammates, Nicole and Robert, who did the simulator part with me.

- Unity Expert: I am the only one in my team who has experience using Unity. Therefore, I take the responsibility of creating new tracks using Unity together with Nicole, who is Blender Expert for building the 3D Objects. Any work involving the use of Unity under my administration including create new scene, link the new track to the menu, etc.

### Weekly Plan
I keep record of my [individual work](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Mouyi) in Wiki every week as well as upload a Youtube video describing this week's activities. The link to youtube videos were included in my individual Wiki page and the below figure is a screenshot of my individual weekly report from week 7 to week 12.

![1.png](https://bitbucket.org/repo/G6xBMXK/images/3605544460-1.png)

## Extend of Work
Robert, Nicole and I took the responsibility of the simulator part. And as mentioned before, I am the unity expert, so I mainly worked on all tasks related to Unity. Basically, these tasks can be divided into three part, tracks for Sign Detection, tracks for F1 and the F1 car model. 

### Tracks for Sign Detection
We built five different tracks with same map but different signs on it. Each track contains all types of signs including a left-turn sign, a right-turn sign, a parking sign, a stopping sign and a speed limit sign. However, the color of the same type of signs are different in different tracks. Turning signs, including both left-turn and right-turn signs, have two colors, blue and black. Parking signs, however, have four different colors, yellow, green, white and blue. The figure below is a vertical view of one of our tracks.

![2.png](https://bitbucket.org/repo/G6xBMXK/images/401064302-2.png)

### Tracks for F1 
We built two F1 tracks using F1 Melbourne map and F1 Shanghai Map. These maps were drawn by Photoshop and the models surrounded the track was made by Blender. These models and pictures were then be imported into Unity to build the track. The below two figures are the vertical view of our F1 tracks.

![3.png](https://bitbucket.org/repo/G6xBMXK/images/54492294-3.png)

![4.png](https://bitbucket.org/repo/G6xBMXK/images/1525584425-4.png)

### F1 Car model
Besides the tracks, I also build a F1 car model in Unity using the car model made in Blender as well as the origin donkey car as a platform. I replaced the donkey car model by our own model but keep the other settings such as the wheel collider. These invisible objects mainly wheel colliders were put in the right position to make sure our car can be run properly. As you can see in the below figures, the objects with green edges are those invisible objects which I made changes to, comparing to the origin donkey car.

![6.png](https://bitbucket.org/repo/G6xBMXK/images/4226781292-6.png)

![5.png](https://bitbucket.org/repo/G6xBMXK/images/355853903-5.png)

### Documentation
After we built the F1 tracks and the F1 car model, I also wrote a documentation explaining how to create the tracks, what adjustment should be made to create the F1 car based on the origin donkey car prefab and what tools are recommended to be used. The documentation was both uploaded in Google Drive and Wiki. Below is the links of the documentation and a screenshot of part of the documentation.

- [Wiki](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Documentation%20for%20F1%20tracks%20and%20car%20model)

- [Google Drive](https://drive.google.com/file/d/1HyIPBn4J6VmeVzhDO1gLaWJZvft6T_8e/view?usp=sharing)

![documentation.png](https://bitbucket.org/repo/G6xBMXK/images/2146151976-documentation.png)

## Quality of Technical Work Done 
### Sign Detection
I and Nicole took the responsibility of the tracks for sign detection. Though we have divided the work, I did unity part while she did Blender part, we both had a general idea of each other's work. So, we held zoom meetings during our work and tested each other's work throughout the progress. I checked the Sign objects she made and gave feedbacks on aspects such as size and materials while she watched me driving my car in the scene and gave me advice. This ensured the quality of our tracks for sign detection.

After these tracks was built, we sent it to other teammates. They drove donkey car on it, both using the model or by hand, and gave us some advices. Also, my teammates Yuanda and Yiran who did the model part gave us requirements about what signs they want to be put in the track and how many tracks they want. These tracks were then passed to them and be tested by their model which ensured the quality of our tracks.

### F1 Tracks
The requirement of F1 tracks were given after the study break and it was separated and independent from the whole Sign Detection requirements. The quality of this part was mainly ensured by two approaches, comparing to the real track and showing to the client. We used satellite image as the real track and mostly compared if the track is similar, as shown below.

![compare.png](https://bitbucket.org/repo/G6xBMXK/images/2223613360-compare.png)

Getting advice from our client, Cian, is also an essential to ensure our quality of the F1 tracks. We showed him our updated F1 tracks every week. Below is an screenshot on discord that we are planning to discuss the F1 track.

![with_client.png](https://bitbucket.org/repo/G6xBMXK/images/4131384490-with_client.png)

### Use and Application of Discipline knowledge
In this project, I use my knowledge in Unity to build the simulator. As mentioned before, I am the only one who had experience in Unity. This means that my knowledge and experience in Unity, particularly how to import the models, how to write code in C#, how to build the release, etc. 

### Challenges
Throughout the whole progress, I met with several issues. One big issue is when I trying to import Nicole’s model (made in Blender and export as .fbx file) to Unity, all colors vanished. It is due to the different spaces we used between Unity and Blender. At the end, we had to recolor the objects in Unity to fix this problem. Figures below show the issue.

![origin.png](https://bitbucket.org/repo/G6xBMXK/images/1545172995-origin.png)

(the origin car model from Blender)

![afterImport.png](https://bitbucket.org/repo/G6xBMXK/images/2431979749-afterImport.png)

(the model after imported into Unity)

![afterRecolor.png](https://bitbucket.org/repo/G6xBMXK/images/505360642-afterRecolor.png)

(the model after recoloring)

 

Another issue occurred when I was building the car model. Due to the wrong position of the wheelCollider object, the wheels rotated in a strange way. After searching on the internet and carefully compared the wheelColliders of origin donkey car prefab, I finally located the issue and fixed it. 

## Other Contribution to group process 
I attended all three meetings every week and involved in other discussions in discord. I asked some questions in discord as well as answered my teammates questions and help them to solve the problem. The evidence of my involvement in discord is listed above in the quality of work part. Also, when my teammates doing sign detection model and meet with issues, I discussed with them in our weekly meeting to provide them with some idea from my perspective.

Furthermore, I and my teammates, Nicole and Robert, who did Simulator part with me, collaborated our work using GitHub. As Bitbucket has a limitation of the size of repositories, during our work from week 7 to week 12, we move the whole simulator part to a new [GitHub repository](https://github.sydney.edu.au/moxu7046/COMP3988_simulator). The following screenshots are also evidence of our collaborate work as well as my individual work.

![evidence_github.png](https://bitbucket.org/repo/G6xBMXK/images/1434404388-evidence_github.png)

## Reflection 
### Extreme Programming 
In this project, we are asked to use XP to manage our project. It is a useful project management method. Using XP, we have clear task arrangement and well cooperation, which makes our work efficient.

However, as our project is more like a research not a software development, it seems hard to use the concepts of Extreme Programming in our work. For example, works on Unity and Blender doesn't involve much coding.

### Version Control 
We use GitHub and Tags to control the version. The evidence (screenshots and link) of our GitHub repository is already displayed in the previous part. Besides this, we also created some [released versions](https://github.sydney.edu.au/moxu7046/COMP3988_simulator/releases) of our simulator, as shown below.

![release.png](https://bitbucket.org/repo/G6xBMXK/images/2591717228-release.png)

I think it is useful to use these version control tools during our work. GitHub makes it possible for us to keep each change and roll back when bugs occurred. The tags in GitHub also helps us control the versions. Each time when we finished a milestone, a release was created. These releases kept a record of our work and showed our teammates who do the sign detection part that, they would not worry about bugs or other errors. That is, these released versions were well tested and can be used directly.

### role 
My role in this project is the Unity Expert. I help my teammates with issues related to Unity. However, as our project doesn't have much coding work, I don't think it's necessary to have a programmer role. Issues can be solved through group discussions in Discord or in meeting and coding is just for some small functions.

I am also the simulator manager, which I think is an essential role in our working. Every week after the client meeting and new requirements were given, we need somebody to carefully think about the requirements, transfer it to real works and assign them. This makes our cooperation efficient. 

Also, as a computer scientist, I think the project I did is a good chance for me to use the knowledges I learn to a real industry and improve the world. I feel very proud.

### final project delivery
Our final project delivery is a great success. Everyone works well both individually and with teammates. Although our work was split into two parts, the simulator part and the sign detection part, we have enough communication between two parts, and we trust each other’s ability to complete each part.

However, we still have something to improve. On big issue I think is the job arrangement. When we are given the new requirement on building the F1 tracks, as nobody had any experience on building a F1 track and a F1 car model, we thought it would be a great amount of job so we assigned three people, me, Nicole and Robert to take the responsibility of Simulator part. But when it came to week 10, 11 and 12, the works for Simulator part was almost finished and the Client was also more focusing on the sign detection part. In this three week, yuanda and yiran who take the responsibility of sign detection were doing far more works than we did. We tried to help them, but they were already started, and it was impossible to start at the middle. I think we should do more researches when assigning the jobs and also keep in track with others’ work so that we can step in if we were needed.