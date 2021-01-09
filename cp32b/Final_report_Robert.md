# COMP3988 Final Individual Report
# Unikey: sjia0385
# SID: 480391405
# Group Name: COMP3988_T17B_Group1
# Project Name: Sign Detection with Tensorflow
# Client Name: Cian Byrne

## Clear Statement of Work Done
### XP roles, other responsibilities and contributions
Manager - From week 5 onward (last cycle), I became the permanent manager for our team, I have been writing 2 to 3 meeting minutes per week until the end of week 12. Normally, 2 of them are for the client meetings on Monday and Friday, and the other is for the group meeting on Tuesday.  

## Programmer - 
During this cycle, I have been involved in designing and implementing simulator track objects and car models. I discussed with my group members during a meeting and we decided what objects we need for the F1 tracks, and what the car model should look like, then I completed the car model and the start gates by using Blender.

## Image Classifier - 
In this cycle I kept on classifying images when my team member asked for my help. I manually classify the track images collected by my team members into different signs and non-signs.

## Customer - 
I asked questions to our client on Discord or during the meeting when I’m not clear about how we should do for some task.

## Slack expert (retired) - 
In the beginning of our project we were required to use slack for communication, I created our slack channel and managed to add our tutor and client in our channels. But I retired from this cycle since we don’t use slack anymore.

## Weekly plan (Week 7 - 13)


## Week 7
1. Classified 30000+ track images to different colours of stop, turn_left, turn_right, park and traffic light for training, the data can be found here: https://drive.google.com/drive/folders/1z43C6RBGayumv_euhthvmi-rP1XCNgn1  
2. Found a free Ferrari F1 car model online, informed Peter and Nicole
3. Wrote 3 meeting minutes  
**video: https://youtu.be/fGYtrB7iZmA**  

## Week 8
1. Completed the Ferrari F1 model shape + colour finshings and exported it to Peter and Nicole
2. Wrote 3 meeting minutes  
**video: https://youtu.be/UZG1vpD1AS0**

## Week 9
1. Discussed about the F1 car model appearance with Cian, and put various different sponsor images onto the car model, the exported fbx and original blend file can be found on our github: https://github.sydney.edu.au/moxu7046/COMP3988_simulator/commit/d7704d088df8e0486c77570acb36df67d553d2e5  
2. Wrote 3 meeting minutes  
**video: https://youtu.be/tltSKE9agMs**

## Week 10
1. Classified about 14000 new Shenzhen track images to different colours of stop, turn_left, turn_right, park and traffic light for training and testing, the data can be found here: https://drive.google.com/file/d/1eSvReJYCR_RNjYhNNuFL03FqIJLRijX9/view  
2. Discussed with Peter and Nicole about track objects, and made two start gates for Shanghai and Melbourne F1 tracks, the exported fbx files can be found on our github: https://github.sydney.edu.au/moxu7046/COMP3988_simulator/commit/5b6255bf5a0ed7ec0e9fcbf060ccce1492021919  
3. Wrote 3 meeting minutes  
**video: https://youtu.be/b1Enooe4wRc**

## Week 11
1. Followed a tutorial, and used Google Earth to look up the elevations of the Shanghai and Melbourne tracks, then discussed the result with Peter and Nicole. The tutorial can be found here: https://www.youtube.com/watch?v=NE2oY9FMAKk&feature=youtu.be thanks to: Joseph Pham  
2. Wrote 3 meeting minutes  
**video: https://youtu.be/iSuoB33_i0A**

## Week 12
1. Recorded the demo video about group process and contributed to the relevant slides (slide 16 - 22) for the presentation. The slides can be found here: https://docs.google.com/presentation/d/1D2ldYPLLpUOHR_xMz1kFZU-CrPrlHsQyow-lb2i1E0Y/edit#slide=id.g9cd4b9b3fd_0_18. The demo video can be found on Canvas.  
2. Wrote the 360 degree peer review, can be found on canvas  
3. Wrote 2 meeting minutes (no second client meeting)  
**video: https://youtu.be/J37EGAt-KQs**

## week 13
1. Contributed to the group process part in the group report
2. Wrote individual report and put it on my wiki page
3. Edited client deployment showreel video for Nicole’s, Peter’s and my part


## Extent of That Work
### Technical development work and XP roles
As described above, as a programmer in the XP roles, I have been involved in designing and implementing simulator track objects and car models, including:
Designing and building the Ferrari F1 model as close as possible to the real world Ferrari F1 SF1000 model
This involves building the car model shape first, which I found a free F1 model online (see week 7 evidence 1) without any finishing touches. 

After that I need to paint the car in Blender to red colour, for that I used texture paint, see appendix 1, which is a functionality in Blender to quickly edit the UV texture to paint the whole mesh object, see this tutorial here.

Then I need to put the car body sponsor images and logos onto the car surface, this involves first retrieving them online as PNG format images, see appendix 2. Then press Shift-A in Blender to add them to the world, after a bit of dimension and rotation adjustment, we add 2 modifiers on the car body, which are subdivision surface: adjust the surface rendering smoothness, and shrinkwrap: wrap another object onto the main object, see appendix 3.

Designing and building the start gates in the Shanghai and Melbourne F1 tracks
This mainly involves using the “edit mode” in Blender which allows me to edit points, surfaces and their combination precisely. Given a simple cube, I can extrude a region on one surface of the cube, doing this while selecting 2 opposite surfaces, I can get the horizontal bar on top of the gate, and with the help of loop cut, I can select which part of a surface that I want to extrude specifically, see appendix 4.


## Quality of Technical Work Done
### Measures Taken to Ensure Code and Work Quality
To ensure that we have clear and readable sign images from the tracks when they are collected, I manually classify them to different signs as mentioned above. If some signs are blurry, I put them into another folder named “other”, which basically collects all images that are not signs (other track images), if an image contains more than one sign, then I put it into a folder named “ambiguous”, which suggests that the sign detection code cannot extract only one sign using OpenCV, see Appendix 5 for details.

To ensure that our simulator repository on github does not track files that could cause merge conflict (such as the local .DS_Store files from different computers), I added a gitignore file which contains the files that should be untracked, see Appendix 6.

### Use and Application of Discipline Knowledge
I used my knowledge in computer networking to tackle down the leaderboard requirement that were withdrawn by the client later on, it requires our donkey car server to be able to put up a scoreboard that shows the information about the lap times and best score for each player, this information needs to be sent from the server to each client racer through a web interface, which requires socket and web programming and networking knowledge, which is eventually decided as “out of scope” by Cian since it requires too much work. 

Before its cancellation, I successfully let the local area client-server framework to function on the localhost web interface when the donkey car started. Basically I need to let the client side change the SIM_HOST value on myconfig.py to the LAN address of the server and change the port number to 8889 which is used specifically for client-server interaction in donkey car, see Appendix 7.

I further applied my knowledge of network programming to enable the client and server to communicate truly remotely. What I need to do is to configure the server side computer’s firewall and enable the port forwarding ability which allows that incoming request from the remote client to be forwarded by the firewall to some computer that has the application the client requested on its outgoing port number bit, see Appendix 8.

### Challenges and Complex Problems
One of the biggest challenges I faced is to manually classify dozens of thousands of track images to different signs, this would take a lot of time and it can be hard with some images since either they have bad quality (very often), or they are ambiguous (contain different signs), doing this for one image at a time is not desirable and efficient at all (probably takes forever), therefore I have to sort the images by examining dozens of them at once. The reason that this helps is because when the camera on the donkey car captures some track images, they usually have high similarities (for example 40 consecutive images might all be stop signs captured, but some are close and some are far from the car) since pycamera’s capture rate is about 10-20 images per second. This method helps me speed up the classification process a lot, see Appendix 9 for the efficiency of this method.


## Other Contribution to Group Processes
### Group Activities and Evidence of Collaboration
I have adhered to our group contract in different aspects involving:
fulfilling my duties as a manager
completing my assigned work each week
communicating with my group members and the client during each meeting and on discord or wechat
contribute to any group reports or demo video/slides that are to be submitted on canvas or delivered to the client.

### Details of the above group activities:
As the manager of our group, I have written all meeting minutes in this cycle, these can be found in the above weekly plan’s evidence column (with direct links to the minutes so no need to look for them on wiki :)).

As a group member, I completed all my assigned work in each week, these are described in detail and can be found in my individual weekly updates: Robert's individual work each week (or in the above weekly plan table).

### Communication
I communicated with my group members on different matters, such as providing updates (Appendix 10, figure 10.1), reminding them of an upcoming meeting (Appendix 10, figure 10.2), or pointing out important things we missed (Appendix 10, figure 10.3).
I communicated with the client on requirements that we are not clear about on Discord, see Appendix 11.
Contribution on group assignments (as described in the above weekly plan table)
I contributed to the final group report on the group process part, our report is written here
I contributed to the final demo video and slides, see above weekly plan on week 12’s evidence column for detail.

I discussed with my group members during a meeting and we decided what objects we need for the F1 tracks, and what the car model should look like, then I completed the car model and the start gates by using Blender.


## “Issues” created and progress
### Issues
Unity does not recognise the paints on the model
Elevation is hard to implement on Unity

### Progress
I painted the model manually then baked the whole material during export, then the unity programmer (Peter) can manually put the paints on the models, appendix 12 displays a critical step during the export step in Blender.

I checked the elevation profile for both Shanghai and Melbourne F1 tracks using Google Earth Pro, then found out that the elevations are not significantly different from point to point, so it’s not really useful to implement them on the tracks, see the above weekly plan on week 11’s evidence column (1b) for detail.

## Reflection
### Reflections on Version Control, Coding Styles, XP, Challenges
### Version control
Our team used both bitbucket and github for our development on sign detection and simulator respectively, we have different branches on both repositories to distinguish different subparts of the work, for example, the simulator branch and the blender branch on github. We use git commands such as git commit (commit our change to the code) and git push (updating the remote repository), git pull (retrieve new changes) to deal with different versions of our files. Overall, we did good on version control without any major issues, except that our bitbucket repo once exceeded its 2GB limit then we opened up the github repo).

### Coding styles
We used the tensorflow library to implement our sign detection algorithm, which is based on image classifications, although I am in the simulator squad, I learned how the tensorflow sign detection code works from the tensorflow image classification tutorials. We used blender to create track objects which are assembled on Unity, which takes the exported blender fbx files. Blender is powerful and not hard to use, we can create objects with great details such as the lighting on different view angles and the decomposition of an object to multiple parts that can be modified separately. The only inconvenience is the rendering process of an fbx file on Unity, Unity won’t directly recognise the object with full detail but rather break it to different parts because they are implemented separately, for example, the paintings on the object would need to be added to the object manually.

### XP
Scope planning and task allocation

We followed the XP framework well, in the beginning of each week, we have a client meeting to reflect on what we did last week, then receive new requirement information from the client. Then we will have another meeting on Tuesday to allocate the tasks to do for everyone in the group.

### Client interaction
We interact with the client directly on Discord since this is much more efficient than only using emails, so that we can get quick responses from any questions we have or suggestions on what we should do next.
Continuous Integration

We follow the CI method from Agile, each week we have something improved and different from last week’s work, so that they match the new requirement given by the client in each week, this involves the updates on our simulator tracks and the result accuracies of our sign detection algorithm using the new features of the tracks.

### Challenges
#### Project change
We initially got selected by the client that offers the object oriented architecture design with bioreactor and control system, this sucks for us since none of us have experience with bioreactor and architecture design related, plus we needed to produce something very abstract and no coding is involved, which is not what we wanted to do. Therefore we switched to this sign detection project on week 3, which was challenging for us since we had a late start. But then we worked hard and diligently on that and we did catch up with what other groups were up to. 

#### Image classification
Before we start training and testing the model with the track images, we need to first sort them out manually to different classes of signs we wanted. This is a bit challenging since it requires a lot of time and patience, I was involved in this process 3 times during this semester, and classified about 40000 + 30000 + 15000 = 85000 images to various signs and non-signs. I feel like this process should be simplified with some other technologies maybe we are not aware of.

#### Donkey car environment
The setup for the donkey car + simulator environment was challenging, different systems have different setup steps, I followed the tutorial from the linux tutorial, which caused me a lot of time since I made some mistakes in the middle such as downloading the old version of the simulator which had different startup interfaces when started, that leads me to question what I did wrong.

#### Out of scope requirements
There have been some out of scope requirements during the projects such as the leaderboard and the elevation on tracks. These were eventually cancelled by the client due to their difficulties and the short time we had. When we were given them, we were confused about their implementations since they seem like very complex work to do, so we did well on asking the client for their clarifications and explaining to him that we may not be able to finish them.


#### Role in the Group
My role in the group is mainly as a software engineer but involving various works. This is already mentioned and explained in the Quality of Group Process part.

#### Team Performance
Our team performed quite well in the first cycle, our client provided the feedback from our first client deployment that said we did well on both the simulator tracks and detecting the signs. The imperfection he noticed is that our tracks were not in a very high quality, the track can be scaled to a better proportion regarding the car size (the track we used was too small for the car), plus our sign detection is not stable enough to detect signs and react to them consistently (e.g. the car would hit the wall if not turned right immediately after recognising the sign). Our improvement on that in cycle 2 is that, first we adopted the sign extraction method based on the region of interest (aka the actual sign without the track environment), by using opencv, we are able to achieve a more consistent model with higher accuracies on different signs with more colours (achieved by adjusting the colour filters). For the track improvement, we did much better this time since we enlarged the F1 tracks that we need to build so that the Ferrari F1 would fit into the track just like the real world tracks. Moreover, we have more track objects including lake, stadiums, trees, and start gates, etc., which brings the tracks more variety and makes them look more like the real world tracks. Our recent release on github can fully demonstrate that: simulator releases.

Beside that, in the last cycle we did not have enough unit test cases to test the basic functionality of our sign detection code although our project is different from the traditional software development, our tutor pointed that out for us during the tutorials. We did better this cycle by writing the unit tests for each individual function and using a bitbucket pipeline
to automatically test the code.

## Wiki
### wiki home page
### Robert individual work

## Appendices
### Appendix 1
(figure 1.1 - blender texture paint)
![Screen Shot 2020-11-25 at 20.27.57.png](https://bitbucket.org/repo/G6xBMXK/images/1875766261-Screen%20Shot%202020-11-25%20at%2020.27.57.png)

### Appendix 2
(figure 2.1 - the car body sponsor logos png files I found)
![Screen Shot 2020-11-25 at 20.28.30.png](https://bitbucket.org/repo/G6xBMXK/images/1280686105-Screen%20Shot%202020-11-25%20at%2020.28.30.png)

### Appendix 3
(figure 3.1 - subdivision surface + shrinkwrap)
![Screen Shot 2020-11-25 at 20.29.49.png](https://bitbucket.org/repo/G6xBMXK/images/56429344-Screen%20Shot%202020-11-25%20at%2020.29.49.png)

### Appendix 4
(figure 4.1 - loop cut + extrude region to get the basic gate first)
![Screen Shot 2020-11-25 at 20.30.08.png](https://bitbucket.org/repo/G6xBMXK/images/2174632252-Screen%20Shot%202020-11-25%20at%2020.30.08.png)

(figure 4.2 - then make the Sword of Melbourne)
![Screen Shot 2020-11-25 at 20.30.24.png](https://bitbucket.org/repo/G6xBMXK/images/3943944763-Screen%20Shot%202020-11-25%20at%2020.30.24.png)

### Appendix 5
(figure 5.1 - ambiguous folder, the image here contains the green traffic light and the stop sign, which we cannot use for training)
![Screen Shot 2020-11-25 at 20.30.39.png](https://bitbucket.org/repo/G6xBMXK/images/876304841-Screen%20Shot%202020-11-25%20at%2020.30.39.png)


(figure 5.2 - other folder, the image here contains a very blurry red traffic light, which we cannot use for training since it is not distinguishable from the stop sign (also red))
![Screen Shot 2020-11-25 at 20.31.06.png](https://bitbucket.org/repo/G6xBMXK/images/3975644135-Screen%20Shot%202020-11-25%20at%2020.31.06.png)

### Appendix 6
(figure 6.1 - .DS_Store would cause merge conflict so it needs to be untracked using gitignore)
![Screen Shot 2020-11-25 at 20.31.25.png](https://bitbucket.org/repo/G6xBMXK/images/2598221638-Screen%20Shot%202020-11-25%20at%2020.31.25.png)

### Appendix 7
(figure 7.1 - client and server on a same computer)
![Screen Shot 2020-11-25 at 20.31.39.png](https://bitbucket.org/repo/G6xBMXK/images/3253042836-Screen%20Shot%202020-11-25%20at%2020.31.39.png)

(figure 7.2 - client and server on the same LAN, simply change the host address to the private ip of the server)
![Screen Shot 2020-11-25 at 20.32.00.png](https://bitbucket.org/repo/G6xBMXK/images/717375826-Screen%20Shot%202020-11-25%20at%2020.32.00.png)

### Appendix 8
(figure 8.1 - configure the firewall’s virtual server to enable port forwarding on the server side)
![Screen Shot 2020-11-25 at 20.32.14.png](https://bitbucket.org/repo/G6xBMXK/images/388611074-Screen%20Shot%202020-11-25%20at%2020.32.14.png)

(figure 8.2 - and we can see the car from another network in the web interface)
![Screen Shot 2020-11-25 at 20.32.32.png](https://bitbucket.org/repo/G6xBMXK/images/2085368925-Screen%20Shot%202020-11-25%20at%2020.32.32.png)


### Appendix 9
(figure 9.1 - a conversation with Yuanda, see the time difference circled in white, 3 folders containing about 15k images classified into the folders in figure 9.2, only takes me 2.5 hours)
![Screen Shot 2020-11-25 at 20.33.22.png](https://bitbucket.org/repo/G6xBMXK/images/905836794-Screen%20Shot%202020-11-25%20at%2020.33.22.png)


(figure 9.2 - result folders for different signs (excluding data 4-6))
![Screen Shot 2020-11-25 at 20.33.41.png](https://bitbucket.org/repo/G6xBMXK/images/3487683330-Screen%20Shot%202020-11-25%20at%2020.33.41.png)

### Appendix 10
(figure 10.1 - providing updates)
![Screen Shot 2020-11-25 at 20.33.56.png](https://bitbucket.org/repo/G6xBMXK/images/2223833255-Screen%20Shot%202020-11-25%20at%2020.33.56.png)

(figure 10.2 - reminder of a meeting, providing the zoom link)
![Screen Shot 2020-11-25 at 20.34.15.png](https://bitbucket.org/repo/G6xBMXK/images/2973211316-Screen%20Shot%202020-11-25%20at%2020.34.15.png)

(figure 10.3 - pointing out group report stuff we missed)
![Screen Shot 2020-11-25 at 20.34.37.png](https://bitbucket.org/repo/G6xBMXK/images/1375720868-Screen%20Shot%202020-11-25%20at%2020.34.37.png)

### Appendix 11
(figure 11.1 - asking the client for car model clarification)
![Screen Shot 2020-11-25 at 20.34.56.png](https://bitbucket.org/repo/G6xBMXK/images/3423375517-Screen%20Shot%202020-11-25%20at%2020.34.56.png)

### Appendix 12
(figure 12.1 - blender export step)
![Screen Shot 2020-11-25 at 20.37.33.png](https://bitbucket.org/repo/G6xBMXK/images/79024641-Screen%20Shot%202020-11-25%20at%2020.37.33.png)

### Appendix 13
(figure 13.1 - showreel simulator part video editing)
![Screen Shot 2020-11-25 at 20.37.47.png](https://bitbucket.org/repo/G6xBMXK/images/2252590887-Screen%20Shot%202020-11-25%20at%2020.37.47.png)