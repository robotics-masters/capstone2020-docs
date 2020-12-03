# Individual Report - Yuanda Dong 

## Clear statement of work done 

### Project changes 

Before i start the following statements of individual contributions, i would like to account for the changes in project from CP4 *Object Oriented Architecture design for bioreactor user interface and control software system* to CP32 *Implement Sign Detection using TensorFlow*, which occurred at the end of week 3. 

### XP roles, other responsibilities and contributions 

#### Manager - Leadership role 

I have played the role of a manager during the second week of the project, during which i organised and facilitated group meetings, and has taken meetings minutes. However, we decided later on in the project to fix the role of a manager to @Robert. He is responsible for making sure the work allocation for each group member is agreed upon, and taking meeting minutes. 

#### Programmer 

I have been involved in implementing the sign detection algorithm using TensorFlow, and modifying a python library rmracerlib which is used to cause the responses of donkey car when a sign is detected. In addition, collaborating with @Yiran, we have used our sign detection model to develop and continuously tuned a neural network that classify different traffic signs in the simulator environment. I have also trained an autonomous driving model using the donkey car framework. These two models coupled with the modified rmracerlib library, really forms the basis for our prototype demonstration. More details and evidence will be detailed later. 

#### Data collector 

I have collected >30000 images of donkey car driving in our custom map for training both autonomous vehicle and sign detection model. The dataset is available [here](https://drive.google.com/drive/folders/1vLOvwvZ5vTzoEmqTWa_bW7E8tnUB5eSE). 

#### Tester 

Collaborating with @Yiran, we have continuously tested based on the accuracy and confusion matrix of the sign detection model, and improved our model based on that. In addition, I ran four major tests that looks at the correct behaviour of donkey car using the autonomous driving and sign detection models. More details and evidence will follow later.  

#### Doomsayer and customer 

I have monitored the progress of the project and raised any potential blockers, deadline concerns with the team. I have communicated with my team the objectives, which the client has conveyed to me personally on discord. 

#### Discord expert 

Instead of using Slack, our group has decided to use just one main communication platform with the client, Discord, which is also client’s preference. I’m responsible for any technical difficulties that occurred during the transition from Slack to Discord. In addition, i have been using Discord to actively communicate with our client about our weekly progresses, and technical difficulties regarding to the project. There will be evidence below.

### Weekly plan  

Most of my weekly plan has gone as expected, so my actual tasks done is exactly the same as my plan. 

**Week 3**

| Task                                                         | Status | Support Evidence                                             |
| ------------------------------------------------------------ | ------ | ------------------------------------------------------------ |
| Communicate with course co-coordinator, tutor and clients to change our project from CP4 to CP32 | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/2020-10-04_09-00.png) |
| Established communication with new client                    | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/2020-10-04_09-03.png) |
| Updated the format of Wiki page                              | DONE   | [link1](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/commits/bb137a8e54b79001673085e60256b86576cab4af) [link2](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/commits/f47b1bfb53320eee42d39592f14b0538a9881b6d) |
| Attended group meeting with client to discuss the project scope | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/2020-10-04_09-09.png) |

**Week 4**

| Task                                                         | Status | Support Evidence                                             |
| ------------------------------------------------------------ | ------ | ------------------------------------------------------------ |
| Set up Tensorflow, Donkey car and Donkey car simulator environment on my PC, written on guide on how to do that. | DONE   | [ Link - 16/09/2020](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Tensorflow and Donkey Simulator Environment Setup Guide) |
| Using the simulator, I trained a self-driving Donkey car model. See the video here | DONE   | [Video](https://youtu.be/d9mRQXM1_dc)                        |
| Learned about how to use TensorFlow to train a neural network that classifies images | DONE   | [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/074dddb69e4f2e68fe7e7721c3722a1bab7a3ba6) |
| Using the [tutorial!](https://www.tensorflow.org/tutorials/images/classification), i built a classifier that is able to classify stop/non-stop signs | DONE   | [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/074dddb69e4f2e68fe7e7721c3722a1bab7a3ba6) |
| Looked into how to run model training on Colab and has communicated with client about the speed of Colab training compared to local CPU. | DONE   | [link](https://colab.research.google.com/github/robocarstore/donkey-car-training-on-google-colab/blob/master/Donkey_Car_Training_using_Google_Colab.ipynb) [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/2020-10-04_09-16.png) |

See my weekly summary video here: https://youtu.be/1o-RmwG3IqA

**Week 5**

| Task                                                         | Status | Support Evidence                                             |
| ------------------------------------------------------------ | ------ | ------------------------------------------------------------ |
| Trained a neural network using the same model from last week, to classify [dataset](https://discordapp.com/channels/750412538637975633/753894317138903120/757404530915803177), and observed low accuracy measures ~ 20%. | DONE   | [link](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/sign.ipynb) |
| Written documentation on training neural network using Colab | DONE   | [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Training%20neural%20network%20using%20google%20colab) |
| Looked into and experimented with setting up servers for running donkey car races. Managed to get it working in LAN, but unable to host it on WAN due to ISP issues. | DONE   | [pic1](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/2020-10-04_09-24.png) [pic2](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/2020-10-04_09-24_1.png) |
| Implemented the code to classify a given directory of images, and write the class label on the image. Also, was able to produce a video from the labelled images. | DONE   | [link](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/glue.ipynb) |
| Modified rmracerlib so that the image detection code would work in the simulator, and printing out the class labels in real-time. | DONE   | [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/060831765bbc8e3561e05825b533948b2a11d9c2) |

See my weekly update video here: https://www.youtube.com/watch?v=-Ea1S9x55oQ&feature=youtu.be

**Week 6**

| Task                                                         | Status | Support Evidence                                             |
| ------------------------------------------------------------ | ------ | ------------------------------------------------------------ |
| Collected more image data by manually driving in our custom map. | DONE   | [link](https://drive.google.com/drive/folders/1vLOvwvZ5vTzoEmqTWa_bW7E8tnUB5eSE) |
| Trained an self-driving model using donkey car framework for our custom map. | DONE   | [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/0c5e31d31697472aa254f261c4d8f32eadf1fff5) |
| In collaboration with @Yiran, Experimented and improved on the sign detection models for our custom map which has (stop, left, right, park, other) signs. | DONE   | [link1](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/2d653adb773c43683e5cff1af0ee9df491ebee8f) [link2](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/c213ca75451d290507d410fedd076f747c1507ec) |
| Continued to modify rmracerlib so that the donkey car reacts to the sign detected, involving stop, turn left, turn right behaviour. | DONE   | [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/096f4cc6d1012826b5c8f80c7a9e2504e6b3fbd2) |

See my weekly update video here: https://www.youtube.com/watch?v=hWSs6zBgu_s&feature=youtu.be



## **Extent of that work** 

### Evidence in links of the above statement

All the links are entered in the weekly plan table so that it’s easy to find. Here, i provide more links for completeness. 

1. Code repository: https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/
2. Commit history: https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/
3. Discord channel: https://discord.gg/fVUS2wA 
4. Wiki homepage: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home

###Technical development work and XP roles  

The technical work i have undertaken has been outlined in statement of work section, here i repeat for completeness. 

> I have been involved in implementing the sign detection algorithm using TensorFlow, and modifying a python library rmracerlib which is used to cause the responses of donkey car when a sign is detected. In addition, collaborating with @Yiran, we have used our sign detection model to develop and continuously tuned a neural network that classify different traffic signs in the simulator environment. I have also trained an autonomous driving model using the donkey car framework. These two models coupled with the modified rmracerlib library, really forms the basis for our prototype demonstration. 

I have played the role of manager, programmer, data collector, tester, doomsayer, customer and Discord expert. The evidence for these can be found in the weekly plan table, here i want to highlight my role as a tester. 

1. For each user stories, i have written the acceptance criteria that assess whether the user story is delivered and their outcomes.

   [Acceptance Test](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/t1.md) 

2. Created 4 testing plans that assess the behavioural aspects of the donkey car model in the simulator based on time, throttle, angle measurements, console output, and observation of the donkey car behaviour. 

   [Testing plan](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/t2.md)

3. Create usability testing plan 

   [Usability testing  plan](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/t3.md)

4. Actually running the 4 tests. 

   [Test result](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/t4.md)

### Summary of the measures taken to ensure code quality

* To ensure the correctness and good style of the model function, I did **Pee Code review and pair programming** via Zoom and Discord with @Yiran. See [my repository folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yuanda/) and [Yiran’s folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/) of CNN model, we are following a consistent style and well-documented, and there are lots of improvements based on peers’ feedback. 

* As i mentioned above, I have done rigorous testings on behavioural aspects of the donkey car model in the simulator based on time, throttle, angle measurements, console output, and observation of the donkey car behaviour, the links to evidence are provided above. 

* There has not been major refactoring of our code base because we were building the prototype model at this moment. 

## **Other contribution to group processes**  

### All group activities with links to the evidence.

* I have adhered to the group contacts in the following sense: 
  * Attended all group meetings among ourselves and with clients 
  * Fulfilled my delegated tasks for each weeks 
  * Communicated with my team member and the client on a regular basis outside group meetings 

* I have played the role of a manager during the second week of the project, during which i organised and facilitated group meetings, and has taken meetings minutes. [Meeting minutes](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/Meeting%20Minutes%20Tempate_Date%20-%20UG%20Capstone%20Projects-3.pdf)

* I have been involved together with my whole team in drafting the group contract and client contract early on during the project. [client contract](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Scope_Statement_overall) 
* I have been involved in preparing and presenting the testing section of Report 1.[Report](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/COMP3988_T17B_Group1%20First%20Project%20Report)
* I have been made a prototype demonstration video. [video](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/Car_action.m4v)

### Evidence of collaboration and teamwork

1. Our team has a lot of collaboration and teamwork, it is evident from our weekly project report which outlines the allocation of group tasks to each member and progresses. [Week2](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Week2) [Week3](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Week3) [Week4](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Week4) [Week5](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Week5) [Week6](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Week6) 

2. To ensure the correctness and good style of the model function, I did **Pee Code review and pair programming** via Zoom and Discord with @Yiran. See [my repository folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yuanda/) and [Yiran’s folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/) of CNN model, we are following a consistent style and well-documented, and there are lots of improvements based on peers’ feedback. 

###   Issues created on bitbucket 

Our team has used Jira Issues to track all the user stories that are either TO DO or DONE. The user stories are set of clients’ requirements written from the perspectives of a potential stakeholder. Credited to @Peter and @Nicole, who have nicely prepared the user stories and uses Trello board to visualise the remaining tasks. I have updated the issues tracking in Bitbucket to reflect the status of each tasks and user stories. [Trello](https://bitbucket.org/RobertJia/comp3988_t17b_group1/addon/trello/trello-board) [Bitbucket Issues](https://bitbucket.org/RobertJia/comp3988_t17b_group1/jira?site=be859735-9bb3-4a0d-a5cb-b2a285747fd9&statuses=new&statuses=indeterminate&statuses=done&sort=-status&page=1)



## **Reflection** 

###  Reflections on version control, coding styles, XP; challenges 

#### Version control  

Our team uses Bitbucket-git to manage our code base. We have used the branching features, by having main branch on TensorFlow sign detection and another branch on simulator improvement. The process of managing branches and version control went quite smoothly, without major issues. There was a minor issues with irrelevant system-specific/IDE files being generated and stored in our repository. This was solved by adding a .gitingore file. 

[link to repo](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/) [link to commits](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/) 

However, the size of our repository has grown almost at its limit of 2 GB, because the dataset we used for training, and binary executable file of simulator for different computer system were quite large. We will later move these to a cloud storage. 

#### Coding style 

We have been using mainly the encapsulated TensorFlow library to implement our sign detection model. TensorFlow website offers a [tutorial](https://www.tensorflow.org/tutorials/images/classification) on image classification, which our team has followed closely in our own code. 

At the moment, we have been using Jupyter Notebook to write our TensorFlow code, as it allows us to store the state of computation such as loading/pre-processing the dataset and trained model (in comparison to python script). This saves a lot of computational times. In addition, it allowed us to present our models/findings among ourselves and to the client more easily. However that also incurs some problems with code modularity, we intend to modularise our code base for the client deployment later on.  

#### XP 

We have tried our best to follow XP practices despite the physical restrictions that we all experience. This involves

* Scope planning: We have a meeting at the beginning of each iteration cycle with our client to decide and approve the features wanted for that iteration and the sprint scope. 

* Close interaction with client: we have two 15-minutes group meetings with the client each week, and communicate with the client on Discord on a daily basis. 
* Pair programming and code review: I did **Pee Code review and pair programming** via Zoom and Discord with @Yiran. This has been really helpful in improving our models’ accuracy, and understanding how our code are going to interact with each other, specifically, the TensorFlow sign detection model drives the behaviour of the donkey car in the simulator.   
* Incremental releases: In developing our sign detection model, and the simulator map we have taken the approach of continuous improvements, in the sense that we will first have a working model (which maybe a primitive map, or classifier with low accuracy), then continuously improve on that. 

#### Challenges 

* late start: The project scope for CP4 *Object Oriented Architecture design for bioreactor user interface and control software system* was deemed as not suitable for our group as an advanced computer science project. So we were assigned to CP32 at the end of week 3. This has caused some challenges in schedule, we had to work very hard to deliver the user stories for each sprint on a timely manner. 
* Software environment: To actually start experimenting and developing models for donkey car self-driving and sign detection, we need to install the required environment including TensorFlow, Donkey car, Gym Donkey, Donkey car simulator, Unity and Blender(for building tracks). Now, this has posed some significant challenges for us during week4, because the documentation on donkey car was not accurate and due to different computer platform Windows, Linux, Macos that we have in the team. 
* Data cleaning and labelling: We had to manually label the class label (stop, left, right, park, other) for >40000 images, so that we can train our model on that. This require a lot of time and patience devoted. 
* Computational demand: training the image classification and self-driving neural network with a large dataset demands a lot of computation. Not everyone in our group has a dedicated Nvidia graphic cards that can be used to speed up the training process. We have to either trained slowly with our CPU or to resort to Google colab for cloud computing. 

### Role in the group and as a software engineer

As mentioned before, my role as a software engineer involve coding (TensorFlow image classification, modification to rmracerlib), and testing (planned and executed 4 sets of tests). In addition to that,

* i have been discussing with clients the scope requirement each week to decide the acceptance criteria for user stories. 
* written documentations on installing donkey car/TensorFlow environments [ Link - 16/09/2020](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Tensorflow and Donkey Simulator Environment Setup Guide), and training models with colab  [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Training%20neural%20network%20using%20google%20colab). 
* collaborating and helping my team members to deliver the user stories. 

### Further Improvements 

The project has been quite successful considering the short time frame that we’ve got, delivering the key aspects of client‘s requirement, which is the TensorFlow sign classification model, and usage in donkey car simulator. The team dynamics for our group also has improved a lot during the project duration so far, specifically we have practised XP as a group with diverse range of skill sets and learnt how to combine everyone’s contribution to a unified product. In the future, we will continue to apply these successful development methodologies and work more closely as a team by involving everyone in the group discussion and development work. 

## Wiki  

* Link to our home page: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home 
* Link to my weekly individual report: https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Yuanda