# __Individual Report - Yexin Mao__ #

This is the individual report for @ymao5456 for the final report due Sunday 29th 2020.

With respect to the software stack we have designed, I was assigned the role of integration manager in the second half of this project.

*Integration manager: This role involves coordination of all elements of project, including coordinating stakeholder, resources and tasks, in addition to reconciling contradictions between different aspects of the project.
  
In addition to the specialised role, I have also been assigned the XP roles of
tracker, programmer and tester. 

*Tracker: Talking to teammates, checking with their progress and giving
advice if they have trouble.  

*Programmer: Given the nature of the project, there was not much work
relating to programming. So basically I checked the codes provided by
our client and learned its functionality.  

*Tester: Checking if the data pushed by other teammates worked well. 

[Role
rotations](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/Role%20Rotation.md)

## __Weekly plan__ ##

### Week7 ###

For the sign detection using Tensorflow, we need a large number of frames to train a better model. However, before the first client demo, we could only drag the drone using mouse and place it at intended location to capture frames, which was inconvenient and might generate many duplicate frames. Our teammate ZhiYi wrote a python script to manual control the drone by typing in the terminal. I followed the instructions to set up the working environment of the control system and tested the functionality of these commands. I also wrote a simple wiki document for other teammates to have a quick understanding of the manipulation steps.

[Commits](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/a2c89d42efa9491411d339b1aac523174efb35ff)

[Wiki](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/Manual%20Control.md)

[Video Demo](https://youtu.be/YWK3NEBWJIU)



### Week 8 ###

Before week9, our team mainly focused on Tensorflow for sign detection. However, I had little knowledge in machine learning, so I could not contribute too much in this area. With the help of my teammates, I learned the basic ideas of data training and tried to train a model myself. Instead of training a model using GPU, I only had CPU setup, which is much slower, so the model we used later was trained by my teammates. What I did was driving the drone around the simulated world in Gazebo and taking photo of specific signs so that my teammates could have more data and train a better model. 

[Dataset](https://drive.google.com/drive/folders/1d6I6taDtUfT1dV4XS__XRssjiBLLU6Bd)

[Video Demo](https://youtu.be/2ZQExqvSmr4)

### Week 9 ###

Our model trained by Tensorflow was not ideal because there was too much background noise in the captured frames. We didn’t know how to solve it at that time, so I started to work on OpenCV, which is another method for sign detection. Teams like CP31 had been working on OpenCV from the start of their project, so they had elaborate codes at that time. Our client shared their codes with us and I spent a lot of time reading and modifying their codes to make them apply to our project. By the end of week9, I could detect stop signs and put a rectangle around it to indicate the detection. However, the detection accuracy was not very high, there were many false positives in the detection process.

[Commits](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/0d919c15e9a4cf411a5bfd14705d4a47e3af9fe3)

[video demo](https://youtu.be/oPDPv9TJZ2g)

### Week 10 ###

This week, I continued working on sign detection using OpenCV. To capture live video streams, we used a built-in camera on the drone called “Typhoon”, so it was necessary to integrate OpenCV with the camera so that we could feed OpenCV with images from the simulated world. Therefore, I combined the codes of video stream with OpenCV for stop, turn and parking signs.
However, I didn’t have enough time to adjust the filters used in turn and parking signs, although we could detect these signs, the detection accuracy was very low.
 
[Commits](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/ec8e6f7358f1853caafbac3d958d1f4155fb1abd)


### Week 11 ###

I intended to make perfect filters for each sign, but the result was not satisfactory. My teammate ZhiYi came to help that he reused the codes I wrote before and added in some new features. I helped in providing blue filters for turn signs and green filters for parking signs.  At the end of the week, we could detect all the signs required by our client with some potential errors. However, our client thought it was acceptable and we did a great job in sign detection.

### Week 12 ###

Week12 was more about the combination of OpenCV and Tensorflow. As we could detect and put a rectangle around the traffic signs, my teammate Gio trained a new model based on these new frames. We had high level of predictions for the speed limit signs while the predictions of left and right turn signs were still not very satisfactory.

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

The repository is recommended to remain small, ideally less than 1 GB. However, we accidently pushed many big files onto the repository, which made the repository reach 2GB. All the commits following were rejected because the repository is restricted to read-only access if the size is larger than 2 GB. As a result, we spent a lot of time reducing the size of the repository. In the future work, we should take care of the commits and only push valuable things.

### Coding style 

We don’t have many comments in our codes, which makes them a bit hard to understand by other readers. As we use many codes from the other teams and add new features in, the coding styles are not very consistent. It is acceptable for small scale project like this, but it is better to keep our codes clean and readable in the future.

### Extreme programming 

It is hard to follow the XP guidelines in this project because the project is too small and does not have many software development procedures related to XP methodology. However, we have tired our best to stick to the principles of XP through the whole semester. Some things the team have done are having sprints each week, documenting all the processes, testing the system adhering to the principles of XP.

### Challenges 
#### Degree of project difficulty

The scope of our project is very large, instead of running everything in unity, we had to set up our own environment in Gazebo, this part basically took one third of the total project time. Compared to other teams who worked either in OpenCV or Tensorflow, we had to use both methods to make a valuable product. This exponentially increased the difficulty of our project because none of us had any experience with these algorithms before.

#### Accuracy of sign detection

This is the main challenge we faced with. We used the combination of OpenCV and Tensorflow for the sign detection, but the detection result was not ideal. For the Tensorflow part, the data used for training were not pure signs but signs polluted by background noise, so when we used the trained model in live video stream, there were many false positives, we improved this by using more and better data. For the OpenCV part, the colour filters were good enough to detect required signs, but we could also detect objects with similar colour and shape. We made every effort to alleviate this in the whole semester, although it is better now, but still not as good as expected.

## __My role as a software engineer__ 
I have gone through all the codes on our git repository and have a good
understanding of how they work.  
I attempted to write my own python scripts to detect sign and objects
using OpenCV in gazebo.     
[Branch for sign
detection](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/branch/sign_detection).   

In the future, I expect to contribute more to Bitbucket, learn how to
use OpenCV and Tensorflow and work like an XP expert.