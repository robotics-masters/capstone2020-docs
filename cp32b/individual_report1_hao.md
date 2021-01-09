# Individual report
Note: All evidence is available on team wiki page or Canvas submission.

## Clear statement of work done

(Due to a transfer of project in week 3/4, my report will start from week 3)

**This part of the report only provides an overview of work done. Details will be provided in the following sections (in particular, “extent of that work”)**

 ****
**XP roles:**

This section states works done related to XP roles on a weekly basis.
 
**Week 3:**

I am the customer contact point in this week.

In this week a preference for a transfer of project is submitted. As the point of contact with the client (and the supervisor). I arrange meeting with the clients and notify our group members.

**Week 4:**

I am the tracker this week.

I keep track of the deadlines and progress of the team and summarize them in a weekly status report and submit them to Canvas and wiki page. I record the risks and problems associated with teamwork and handle them over to the manager as well as record them on the status report. Improvements and corrections of mistakes are expected to make in weeks after, based on the items on the status report.

**Week 5, 6:**

Since everyone in our team has been the manager or tracker at least once as required by the project, so we have decided not to do a rotation every week anymore. I will be the tracker for the rest of the project unless a group decision is made. My responsibilities related to XP roles will pretty much remain the same as a tracker.
 
**Other responsibilities and contributions**

This section states work done that are not related to XP roles but closely to the project itself.

 ****
**Set up TensorFlow virtual running environment on local machines**

A virtual environment is set up for TensorFlow 2 on my local machine for model training and image classifications later used in the project.
 
**Set up TensorFlow GPU supports on local machines**

TensorFlow comes with build-in CPU support but a CPU is very slow at machine learning (model training). Under the expectation of our clients, I successfully set up a GPU supports on local machines, which greatly enhances our training speed.
 
**Set up Donkey Car simulator environment on local machines**

A simulator (implemented in Unity and C#) is set up on local machines so that models can be tested without any hardware support. After models (signs) are set up in the map as 3D models, training data can be collected from the simulator.
 
**Train and run models in simulator**

I downloaded images (as initial training data) from the internet and performed data cleaning manually (along with members of the team as the amount of data required is huge). A basic model is trained and can auto-pilot itself in the standard map.
 
**Complete classification of simple images**

Following the TensorFlow classification tutorial, complete a classification of images task .
 
**Report writing, Wiki editing, Demo**

These works are performed by all team members as required.
 ****
**Weekly plan:**

 ****
**Week 3:**

Communicate with clients and supervisor.
Start to investigate into TensorFlow and Donkey car simulator.
Reading project scope statement, client expectation, etc.
set up a communication channel, Discord.
Submit a status report.
 
All works are done for this week.
 
**Week 4:**

Join BitBucket
Read project proposal and scope
Set up TensorFlow and Python virtual environment on local machine
Set up TensorFlow GPU supports on local machine
Set up Donkey car simulator on local machine
Submit a status report.
 
All works are done for this week.
 
**Week 5:**

Continue to set up and fix issues with GPU supports.
Go through TensorFlow image classification tutorial with stop, left and right signs.
Set up Donkey car simulator; train and run a model on it.
Submit a status report.
 
I was going to improve the image classification algorithms with Yiran, but I was sick for the second half of the week so that was not done.
 
**Week 6:**

As instructed by the client, this week is mainly for preparing reports and demonstration; no actual work related to the project are mandatory.
 

## Extent of that work

**XP roles:**
**Customer contact points:**
This task is done mainly by email, I will attach some screenshots below, the rest are cc’d to the tutor.

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816764519_image.png)

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816776683_image.png)


**Tracker:**
Tracker reports can be found on Canvas and Wiki. A screenshot is attached as an example.

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816790241_image.png)


**Set up TensorFlow virtual running environment on local machines**
This task cannot be seen from the repository as it is mainly related to environment set up and no code is actually required. (installation guide is at

https://www.tensorflow.org/install/pip


This task involves setting up Python virtual environment on local machines as well as tools like Microsoft C++ redistributable.

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816803391_image.png)


**Set up TensorFlow GPU supports on local machines**
This work is done on local machines which have a Nvidia graphics card installed. This task was very complicated and time-consuming but considering the speed boost it can provide it is all worth it.
Nvidia machine learning enabling drives, software, platform are configured as advised by the manual.

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816813427_image.png)

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816820539_image.png)


This task is crucial in increasing efficiency of our project.
The following is a speed comparison of a training with a CPU and a training with a GPU.
CPU:

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816834320_image.png)

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816841224_image.png)


GPU:

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816847263_image.png)


 

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816852932_image.png)


As you can see, a GPU is highly effectively at machine learning than a GPU, although the setup does take days, but you can see how much speed boost it gives to model training. Training on the same data, a CPU takes 500 ms per step, roughly 50 seconds per epoch; **It takes the CPU 21 minutes to complete 26 epochs before an early stop; however, a GPU takes 15 ms per step, roughly less than 1 second per epoch,** which adds up to 43 seconds for 50 epochs (roughly 22 seconds for 26 epochs). **You get a roughly 50 times improvement in training speed when using a GPU. This greatly shorten the time we spend to train a model therefore gives us better abilities to configure our models.**
 
**Set up Donkey Car simulator environment on local machines**
A donkey car simulator is set up to train and test model as well as collecting training data.
 
**Train and run models in simulator**
A link to a small demo on training and running a model: [https://youtu.be/iPJreDFLsCs](https://youtu.be/iPJreDFLsCs)
Details can be found in the video so I will not add more textual explanation here.
This is a screenshot of data (image) collected from the simulator:

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816864748_image.png)

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816870232_image.png)


This image is collected using the on-board camera on the (simulated) car.
 
**Complete classification of simple images**
This is a practice on classifying images using TensorFlow 2 and the Keras module provided.

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816879871_image.png)

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816883109_image.png)


The code can be found in the repo.
Note: a TensorFlow environment with GPU supports need to set up before running the code
 

## Quality of technical work done

Most work I have done so far is not related to code but system set up and speed (efficiency) improvement.
The most effective technical work process I did, I believe was trying to set up the GPU support together with Peter. We worked remotely to collaborate on relevant issues including not matching versions or not found physical device.
We looked for solutions online and asked for help from the clients to tackle the problems. After one of us solved the problem, he documented it and demonstrated to the other person so that that person can replay the process on his machine. This saved time from both of us and the problem is resolved much faster than if only one person was working on it.
Evidence can be found on Discord.

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816890144_image.png)


 

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816897089_image.png)

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816904285_image.png)


The other thing is that team members will test code that has been pushed to the online repository on their own machines at their discretion, to make sure that the code is not machine dependent. The image classification code I pushed to the repo has not been reported any issues.

## Other contribution to group processes

**Group activities as customer contact points and tracker:**
Evidence can be found in cc’d emails as well as screenshots in earlier sections of this report. Tracker’s status report can be found on Canvas and Wiki.
 
 
**Adherence to group contract, collaboration and teamwork**
**Evidence of collaboration and teamwork**
Respond to communications promptly via email, discords and Wechat.
 

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816926890_image.png)

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816934044_image.png)

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816937489_image.png)


Other records can be found on Discord and in emails (the tutor should have access to both) as well as Slack.

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816942762_image.png)


 

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816946799_image.png)


Attend group meeting as set up on the agenda:

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816959228_image.png)

![](https://paper-attachments.dropbox.com/s_61519D26473A4D3DA4194246F29A1D15B9A7073B238C96A30BB955C60767ABAF_1601816965098_image.png)


**“Issues” created and progress**
The biggest issue I tackled was with another member Peter, when trying to set up a GPU support on our local machines. This issue was not part of the project source code so it was not documented on Wiki. I can provide some evidence on Discord related to our discussion with the client.
 
Details have been mentioned in earlier section.

## Reflection

**Version control:**
I haven’t been using the version control (git) as frequently as a software engineer will be required to do. I “saved up” lots of work and push to the repository at once. This is bad as it contradicts to the purpose of using a version control system in the first place.
In the second half of the semester, I should push to the repository as soon as a major feature is implemented, or a major issue is dissolved. Therefore, other members can benefit from improved code and added features; it also makes it easier to look back in history in case of a refactoring or similar events.
 
**Coding style:**
I should be putting more comments and documentation in my code so that other programmer can easily pick up my work and understand my code. Meaningful variable names should be used for better readability.
More functions should be used so the code is modularized and easier to maintain.
 
**XP:**
As a tracker, I should be tracking deadlines of task more actively for the team. Time management is not done well enough in our team in the past few weeks. I should communicate more frequently with members and understand their progress and difficulties from time to time.
 
**Challenges:**
I had been sick for one week and were a little bit behind the progress of our team. I need to spend more efforts in the following weeks to catch up with the progress of the team.
 
**Role in the group and as a software engineer**
As a software engineer in the group, I work closely and communicate to my team members. I respond to team member’s questions and requests promptly. I collaborate with members to solve complex issues and environment set up. I aim to write code that can be easily understood by other members. I help other members to understand and follow the work I do. I took part in the design of the software structure.
 
**How has the team being doing**
The team has been doing well. Although we were a bit left behind because late transfer into the project; but we managed to catch up with other teams under the assistance of the clients and close collaboration between team members. We aim to spend more time on the project later so we can be a leading team among all others working on the same project.
 
All documentations and evidence needed related to the team can be found on the team wiki.
[https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home)
 
 
No feedbacks has been provided on the presentation yet!