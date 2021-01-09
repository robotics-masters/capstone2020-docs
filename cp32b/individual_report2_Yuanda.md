# Individual Report - Yuanda Dong 

## Clear statement of work done 

### XP roles, other responsibilities and contributions 

#### Manager - Leadership role 

We decided early on in the project to fix the role of a manager to @Robert. He is responsible for making sure the work allocation for each group member is agreed upon, and taking meeting minutes. However, i took the responsibility of allocating works for both client deployment and the final report. 

#### Programmer 

I have been involved in implementing the sign detection algorithm using a hybrid of OpenCV and Tensorflow, and modifying a python library rmracerlib which is used to cause the responses of donkey car when a sign is detected. Collaborating with @Yiran, we used OpenCV (colour based) to extract region of interest (ROI), then manually filtered the signs out. Then using this data, we have tuned a neural network that classify different traffic signs in the simulator environment. I have also trained an autonomous driving model using the donkey car framework. These two models coupled with the modified rmracerlib library that is able to extract signs in real-time, really forms the basis for the sign detection part of our project. More details and evidence will be detailed later. 

#### Data collector 

I have collected > 30000+60000 images of donkey car driving in our custom map for training both autonomous vehicle and sign detection model. The first dataset is available [here](https://drive.google.com/drive/folders/1vLOvwvZ5vTzoEmqTWa_bW7E8tnUB5eSE). The other is available [here](https://drive.google.com/file/d/1NrvSqs_RhgehOVQ6FbTWBztKjMc-MPes/view?usp=sharing). In addition, together with @Robert, we manually classified ~20000 real-world Shenzhen images for model training, and shared this with other groups. [link](https://drive.google.com/file/d/1G0Cl2cZ8bEwPntNO22A2nFECbLNySn4q/view?usp=sharing)

#### Tester 

Collaborating with @Yiran, we have continuously tested based on the accuracy and confusion matrix of the sign detection model, and improved our model based on that. I have written a test script to automate this process. The test checks the diagonal/off-diagonal entries of the confusion matrix and precision,recall and f1-score of our models’ performance on different sets of test data. This is later used in the Bitbucket pipeline by LanHao. In addition, I ran five major tests that looks at the correct behaviour of donkey car using the autonomous driving and accuracy of sign detection models. More details and evidence will follow later.  

#### Doomsayer and customer 

I have monitored the progress of the project and raised any potential blockers, deadline concerns with the team. I have communicated with my team the objectives, which the client has conveyed to me personally on discord. 

#### Discord expert 

Instead of using Slack, our group has decided to use just one main communication platform with the client, Discord, which is also client’s preference. I have been using Discord to actively communicate with our client about our weekly progresses, and technical difficulties regarding to the project. [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/client.png) There will be more evidence below.

### Weekly plan (Week 7 - 13)

Most of my weekly plan has gone as expected. Please checkout previous individual report for my weekly plans for week 1-6. 

**Week 7 (Initial Client Deployment)**

| Task                                                         | Status | Support Evidence                                             |
| ------------------------------------------------------------ | ------ | ------------------------------------------------------------ |
| Updated to Donkey car 4.0 module, and fixed some related bugs with simulator | DONE   | [pic1](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/donkey4.0png.png) [pic2](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/donkey4.png) |
| Attended Venture Cafe event online with @Mouyi               | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/venture.png) |
| Discussed with my team and we made decision to make another 2 maps with signs of different colours (to overcome the issue with having too many signs on one map) | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/more_map.png) |
| Collected training data from the new maps for both autonomous driving and sign detection module | DONE   | [link](https://drive.google.com/file/d/1NrvSqs_RhgehOVQ6FbTWBztKjMc-MPes/view?usp=sharing) |
| Trained an autonomous driving model that is able to continue driving after hitting walls for new maps | DONE   | [link](https://bitbucket.org/Yuanda4228/comp3988-client-deployment/src/master/Fast_driver_but_unstable_sign_detection_for_all_three_map/) |
| Worked with Yiran to improve the sign classification model, I mainly do testing in the simulator | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/improve.png) |
| Wrote deployment documentation for client                    | DONE   | [link](https://bitbucket.org/Yuanda4228/comp3988-client-deployment/src/master/Documentation/) |
| Moved everything for client deployment from google drive, Bitbucket site, to the dedicated repo for client deployment | DONE   | [link](https://bitbucket.org/Yuanda4228/comp3988-client-deployment/src/master/) |
| Wrote the client deployment presentation slides with Hao Lan | DONE   | [link](https://docs.google.com/presentation/d/10QSsLILYQtDHuWbn9pgKHpGeMvQFAfwOsJA2IhQwKgM/edit#slide=id.g9d1917a7a0_0_69) |
| Attended the client deployment, and presented the introduction section before we start the actual Demo | DONE   | [link](https://www.youtube.com/watch?v=_W_JX03uFBE&ab_channel=RoboticsMastersLimited) |
| Demoed the sign detection + self-driving in simulator        | DONE   | [link](https://www.youtube.com/watch?v=_W_JX03uFBE&ab_channel=RoboticsMastersLimited) |

**Week 8**

| Task                                                         | Status | Support Evidence                                             |
| ------------------------------------------------------------ | ------ | ------------------------------------------------------------ |
| Attended a inter-group meeting with the other CP32 teams, to exchange results, and set up server for data sharing | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/inter.png) |
| Tested sign detection model without ‘other’ class, and concluded it’s better to have ‘other’ class for full-frame detection | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/other.png) |
| Tested sign detection model without sub-classing, and concluded it’s better to not bother with sub-classing for full-frame detection | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/other.png) |
| Discussed with the client and CP31, to decide the next feature (to be implemented) for sign detection. We decided to adapt existing openCV code to extract the full-frame images, and do classifications on the extracted images. Assigned work between Yiran and myself to implement this feature. In summary, Yiran will be working on building the image classification model; I’ll use that model and make it work in the simulator | DONE   | [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/MeetingMinutes_Week7_Client2) |
| Discussed with client, @Wilson, Yiran on how to adapt the openCV code | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/wilson.png) [pic2](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/pic2.png) |
| Looked at an alternative approach (other than openCV), which uses tensorflow only + Unity perception packages to generate synthetic data at scale. However, decided our team don’t have enough time to do this from scratch | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/approach.png) |

**Week 9**

| Task                                                         | Status | Support Evidence                                             |
| ------------------------------------------------------------ | ------ | ------------------------------------------------------------ |
| Continue Discussion with client, Yiran on how to adapt the openCV code | DONE   | [pic1](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/continue.png)[pic2](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/continue2.png)[pic3](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/cotinue3.png)[pic4](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/continue4.png) |
| Yiran built a prototype model for sign detection(using openCV), and i used the model, and made it work in the simulator | DONE   | [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/ebcd60b91cd0e303db11859a792fc5c8d523aac2) |
| Attempted to draw real-time bounding boxes for signs in the simulator camera, but had some issues (to be discussed next week with the client) | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/back.png) |
| Manually classified 20000 images for Shenzhen track with Robert. Shenzhen track images will be used as the main test for our sign detection model | DONE   | [link](https://drive.google.com/file/d/1G0Cl2cZ8bEwPntNO22A2nFECbLNySn4q/view?usp=sharing) |

**Week 10**

| Task                                                         | Status | Support Evidence                                             |
| ------------------------------------------------------------ | ------ | ------------------------------------------------------------ |
| Had a coding meeting with the client to try fix the bounding box issues, however it was not resolved, but the issue is posted to Donkey Car Discord. | DONE   | [pic1](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/code.png)[pic2](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/q.png)[pic3](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/s.png) |
| Fixed the bounding box issue with the suggestion from @MaximeEllerbach | DONE   | [link](https://www.youtube.com/watch?v=UvBLPZw6Trc&feature=youtu.be) |
| Added pytest for model accuracy that will be used later on in testing pipeline. The test involves checking the diagonal/off-diagonal entries of the confusion matrix and precision, recall and f1-scores of the models’ performance on different test data. | DONE   | [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/9102470a4416cabbe05db241468bda866e35f14d) |

**Week 11**

| Task                                                         | Status | Support Evidence                                             |
| ------------------------------------------------------------ | ------ | ------------------------------------------------------------ |
| Gave help to give to @CP32-aradhikaguha  and @CP32 - Thomas with their TensorFlow work | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/pick.png) |
| Collaborate with @Yiran, we found a method (using colour picker) to change the upper/lower bound of OpenCV color filters,to overfit to given signs, and produce very good OpenCV extraction. | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/help.png) |
| Using the new filters, We were able to get great sign detection results on F1 tracks, which shows the generalisation capabilities of our approach. | DONE   | [link](https://youtu.be/1rpVVS2q54A)                         |

**Week 12 (+ Final Client Deployment)**

| Task                                                         | Status | Support Evidence                                             |
| ------------------------------------------------------------ | ------ | ------------------------------------------------------------ |
| Together with @Yiran, @LanHao, we created the demo for testing section of our project. Also I compiled everyone’s video together to produce the final demo video. | DONE   | [link](https://youtu.be/eCw6QChhvj4)                         |
| Created Github Repository dedicated for the final client deployment, and added final rmracerlib to the repo | DONE   | [link](https://github.com/Yuanda-Dong/Client-Final-Deployment) |
| Together with @Yiran, we created a showWeel for the sign detection part of our project | DONE   | [link](https://drive.google.com/drive/folders/18mV71fDfvLSkojq61_i8B7IqWVVNC85p?usp=sharing) |
| Present the project introduction and sign detection in simulator part of the client deployment. | DONE   | [link](https://www.youtube.com/watch?v=6H6geVCDLH8)          |
| Wrote the testing section of the group report, as well as doing some additional testing of sign detection. | DONE   | [link](https://docs.google.com/document/d/1pPQTqB6OSCoV3mSsRMsvVmgs9b68zqMQP2TM0W_YBM4/edit#) |



## **Extent of that work** 

### Evidence in links of the above statement

All the links are entered in the weekly plan table so that it’s easy to find. Here, i provide more links for completeness. 

1. Code repository: https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/
2. Commit history: https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/
3. Discord channel: https://discord.gg/fVUS2wA 
4. Wiki homepage: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home
5. First client deployment codebase:https://bitbucket.org/Yuanda4228/comp3988-client-deployment/src/master/
6. Final client deployment codebase:https://github.com/Yuanda-Dong/Client-Final-Deployment

### Technical development work and XP roles  

The technical work i have undertaken has been outlined in statement of work section, here i repeat for completeness. 

> I have been involved in implementing the sign detection algorithm using a hybrid of OpenCV and Tensorflow, and modifying a python library rmracerlib which is used to cause the responses of donkey car when a sign is detected. Collaborating with @Yiran, we used OpenCV (colour based) to extract region of interest (ROI), then manually filtered the signs out. Then using this data, we have tuned a neural network that classify different traffic signs in the simulator environment. I have also trained an autonomous driving model using the donkey car framework. These two models coupled with the modified rmracerlib library that is able to extract signs in real-time, really forms the basis for the sign detection part of our project. More details and evidence will be detailed later. 

I have played the role of manager, programmer, data collector, tester, doomsayer, customer and Discord expert. The evidence for these can be found in the weekly plan table, here i want to highlight my role as a tester. 

1. For each user stories, i have written the acceptance criteria that assess whether the user story is delivered and their outcomes.

   [Acceptance Test](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/t1.md) 

2. Created 6 testing plans that assess the accuracy of the CNN model and behavioural aspects of the donkey car model in the simulator based on bounding boxes drawing, throttle, angle measurements, console output, and observation of the donkey car behaviour. 

   [Testing plan](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/t2.md)

3. Create usability testing plan 

   [Usability testing  plan](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/t3.md)

4. Actually running the 6 tests. 

   [Test result](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/t4.md)

### Summary of the measures taken to ensure code quality

* To ensure the correctness and good style of the model function, I did **Pee Code review and pair programming** via Zoom and Discord with @Yiran. See our final [codebase for client deployment](https://github.com/Yuanda-Dong/Client-Final-Deployment). There is documentation written nicely in markdown for each of folder(module). we are following a consistent style and well-documented, and there are lots of improvements based on peers’ feedback. 

* As i mentioned above, I have done rigorous testings on the accuracy of the CNN model and behavioural aspects of the donkey car model in the simulator based on bounding boxes, throttle, angle measurements, console output, and observation of the donkey car behaviour, the links to evidence are provided above. 

* There was some refactoring of our code at the end of our project, mainly converting jupyter notebook files to python scripts for client deployment. 

## **Other contribution to group processes**  

### All group activities with links to the evidence.

* I have adhered to the group contacts in the following sense: 
  * Attended all group meetings among ourselves and with clients 
  * Fulfilled my delegated tasks for each weeks 
  * Communicated with my team member and the client on a regular basis outside group meetings 

* I took the responsibility of allocating works for both client deployment and the final report. [link](https://docs.google.com/presentation/d/10QSsLILYQtDHuWbn9pgKHpGeMvQFAfwOsJA2IhQwKgM/edit#slide=id.g9d1917a7a0_0_23)

* I have been involved together with my whole team in drafting the group contract and client contract early on during the project. [client contract](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Scope_Statement_overall) 
* I have been involved in preparing and presenting the testing section of final report.[Report](https://docs.google.com/document/d/1pPQTqB6OSCoV3mSsRMsvVmgs9b68zqMQP2TM0W_YBM4/edit#)
* I have been made a prototype demonstration video of sign detection in action. [video](https://youtu.be/4KhhqXZcjRE)

### Evidence of collaboration and teamwork

1. Our team has a lot of collaboration and teamwork, it is evident from our weekly meeting minutes and status report which outlines the allocation of group tasks to each member and progresses. [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home)

2. To ensure the correctness and good style of the model function, I did **Pee Code review and pair programming** via Zoom and Discord with @Yiran. See [my repository folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yuanda/) and [Yiran’s folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/) of CNN model, we are following a consistent style and well-documented, and there are lots of improvements based on peers’ feedback. 

###   Issues created on bitbucket 

Our team has used Bitbucket Issues to track all the user stories that are either TO DO or DONE. The user stories are set of clients’ requirements written from the perspectives of a potential stakeholder. Credited to @Peter and @Nicole, who have nicely prepared the user stories and uses Trello board to visualise the remaining tasks. I have updated the issues tracking in Bitbucket to reflect the status of each tasks and user stories. [Trello](https://bitbucket.org/RobertJia/comp3988_t17b_group1/addon/trello/trello-board) [Bitbucket Issues](https://bitbucket.org/RobertJia/comp3988_t17b_group1/jira?site=be859735-9bb3-4a0d-a5cb-b2a285747fd9&statuses=new&statuses=indeterminate&statuses=done&sort=-status&page=1)



## **Reflection** 

###  Reflections on version control, coding styles, XP; challenges 

#### Version control  

Our team uses Bitbucket-git to manage our code base. We have used the branching features, by having main branch on TensorFlow sign detection and another branch on simulator improvement. The process of managing branches and version control went quite smoothly, without major issues. There was a minor issues with irrelevant system-specific files and large data set files. This was solved by adding a .gitingore file. 

[link to repo](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/) [link to commits](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/) 

However, the size of our repository has at one point grown over its limit of 2 GB, because the dataset we used for training, and binary executable file of simulator for different computer system were quite large. I had submitted a ticket to Atlassian to bring the size down so that later commits can be made. [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/size.png) In addition, we have decided to move the simulator part to another [github repository](https://github.sydney.edu.au/moxu7046/COMP3988_simulator). 

#### Coding style 

We have been using mainly the TensorFlow library to implement our sign detection model. TensorFlow website offers a [tutorial](https://www.tensorflow.org/tutorials/images/classification) on image classification, which our team has followed closely in our own code. As for the OpenCV extraction code, we have been mainly using the code provided by the client with modifications to the filter ranges to suit our purposes.

We have been using primarily Jupyter Notebook to write our sign detection code, as it allows us to store the state of computation such as loading/pre-processing the dataset and trained model (in comparison to python script). This saves a lot of computational times. In addition, it allowed us to present our models/findings among ourselves and to the client more easily. However, for the final client deployment, @Yiran has converted these files into python scripts together with automatically generated documentations [link](https://github.com/Yuanda-Dong/Client-Final-Deployment/tree/main/SourceCode/doc). 

#### XP 

We have tried our best to follow XP practices despite the physical restrictions that we all experience. This involves

* Scope planning: We have a meeting at the beginning of each iteration cycle with our client to decide and approve the features wanted for that iteration and the sprint scope. 

* Close interaction with client: we have two 15-minutes group meetings with the client each week, and communicate with the client on Discord on a daily basis. 
* Pair programming and code review: I did **Peer Code review and pair programming** via Zoom and Discord with @Yiran. This has been really helpful in improving our models’ accuracy, and understanding how our code are going to interact with each other, specifically, the OpenCV + TensorFlow sign detection model drives the behaviour of the donkey car in the simulator.   
* Incremental releases: In developing our sign detection model, and the simulator map we have taken the approach of continuous improvements, in the sense that we will first have a working model (which maybe a primitive map, or classifier with low accuracy), then continuously improve on that. 

#### Challenges 

* late start: We changed from *Object Oriented Architecture design for bioreactor user interface and control software system* to CP32 at the end of week 3. This has caused some challenges in schedule, we had to work hard to deliver the user stories for each sprint on a timely manner. 
* Software environment: To actually start experimenting and developing models for donkey car self-driving and sign detection, we need to install the required environment including TensorFlow, Donkey car, Gym Donkey, Donkey car simulator, Unity and Blender(for building tracks). Now, this has posed some significant challenges for us early on in the project, because the documentation on donkey car was not accurate and due to different computer platform Windows, Linux, Macos that we have in the team. 
* Using existing OpenCV code: the OpenCV code used to extract signs were provided by the client, however, there was little documentation, and we didn’t have previous experiences working with OpenCV. We had many meetings with the client to discuss the code before we can fully use it for our purposes. 
* Data cleaning and labelling: We had to manually label the class label (stop, left, right, park, other) for >100000 images, so that we can train our model on that. This require a lot of time and patience devoted. 
* Computational demand: training the image classification and self-driving neural network with a large dataset demands a lot of computation. Not everyone in our group has a dedicated Nvidia graphic cards that can be used to speed up the training process. We have to either trained slowly with our CPU or to resort to Google colab for cloud computing. 

### How the team has improved performance based on feedback from client, tutor, and team members

We have received overall quite positive feedback from the client for our first client deployment. However, he mentioned mainly two issues with our project: 

1. The simulator track was not as polished as he would like 
2. The sign detection model was not stable enough

Based on these feedback, we had group discussion on how to improve. Specifically, we have added more assets including trees, stadium, lake and really polished up the track for our new Melbourne, and Shanghai track. Check out our [releases](https://github.sydney.edu.au/moxu7046/COMP3988_simulator/releases), they can be downloaded and run on Windows, Linux and Macos. To address the problem with stability of sign detection model, we have proposed to use the hybrid OpenCV sign extraction and Tensorflow classification. This was proved to produce a more stable result and has generalisation (works on different maps) capabilities. Check out this [short demo video](https://youtu.be/4KhhqXZcjRE). 

We have also received feedback on testing methodologies from our Tutor. It’s important to write test cases to ensure that every new features that we have implemented doesn’t break previous functions of the system. We have written automatic python test scripts that test the accuracy of our sign detection model and is built into the [Bitbucket pipeline](https://bitbucket.org/RobertJia/comp3988_t17b_group1/addon/pipelines/home). This actually helped us before the final group demo to identity an issue with left/right sign detection, as some test cases were failed. It turns out the some left/right signs data were mixed up, and we were able to fix that. 

### Role in the group and as a software engineer

As mentioned before, my role as a software engineer involve coding (TensorFlow image classification, modification to rmracerlib), and testing (planned and executed 6 sets of tests). In addition to that,

* i have been discussing with clients the scope requirement each week to decide the acceptance criteria for user stories. 
* written documentations on installing donkey car/TensorFlow environments [ Link - 16/09/2020](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Tensorflow and Donkey Simulator Environment Setup Guide), and training models with colab  [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Training%20neural%20network%20using%20google%20colab).
* written documentations on using the modified rmracerlib for sign detection in simulator [link](https://bitbucket.org/Yuanda4228/comp3988-client-deployment/src/master/Documentation/)
* compiled a list of dependencies and documentations for using our codebase for sign detection [link](https://bitbucket.org/Yuanda4228/comp3988-client-deployment/src/master/Documentation/)
* collaborating and helping my team members to deliver the user stories. 



### Further Improvements 

The project has been quite successful considering the short time frame that we’ve got, delivering the key aspects of client‘s requirement, which is a working sign detection model, and a variety of tracks in donkey car simulator. The team dynamics for our group also has improved a lot during the project duration so far, specifically we have practised XP as a group with diverse range of skill sets and learnt how to combine everyone’s contribution to a unified product. In terms of technical improvement of sign detection model, i would really like to try using Unity perception and Tensorflow object detection, which i believe will have better scalability and generalisation capabilities than our current approach.  

## Wiki  

* Link to our home page: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home 
* Link to my weekly individual report: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Yuanda
* Link to my previous individual report: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Yuanda