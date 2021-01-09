# Individual Report - Martin Chai #

This is the individual report for @mcha3431 for the First Report due Sunday 4th October 2020.

---

During the past few weeks, I have been delegated the following XP roles on a rotational basis:

* Manager: Oversaw the progress and completion of the earlier tasks such as the group contract and project scope statement.

* Programmer: No coding was required at the time as only setup tasks were required.

* Tester: Checked the functionality of setup code.

Other responsibilities:

* ML expert: As being one of the team members with prior experience in practical machine learning, I have taken the role as one of the specialists regarding the machine learning aspects of the project.

---

## Weekly Plan ##

### Week 2 ###
Plans:

* Set up Gazebo in both the PX4 and Ardupilot environments following documentation provided by our client.

* Complete the group contract.

Issues:

* I was on MacOS and on old hardware. Despite the presence of documentation for setting up Gazebo with PX4 and Ardupilot on MacOS, I was not able to get it working. Other group members have had similar experiences so we decided as a group to shift to Ubuntu 18.04. However, hardware limitations prevented me from being able to dual boot or run virtual machines and thus I had to upgrade machines.

Achievements:

* Shared the group contract template with the group and also wrote a significant portion of it. Made sure each group member was happy with its contents.

### Week 3 ###
Plans:

* Install Ubuntu 18.04 on new system

* Set up Gazebo in both the PX4 and Ardupilot environments following documentation provided by our client.

Achievements:

* Installed Ubuntu 18.04 on the new system and set up Gazebo as planned for the upcoming client meeting

### Week 4 ###
Plans:

* Gather training data

* Build a Tensorflow model

* Set up GPU integration for TensorFlow

Issues:

* The dependencies required for GPU integration were fairly large which caused me to run out of root storage space to complete the GPU integration. Hard drive needed to be re-partitioned.

Achievements:

*  Gathered three external datasets and started building the initial training model locally.

### Week 5 ###
Plans:

* Continue gathering training data

* Test initial training model on the training data

* Set up GPU integration for TensorFlow

Achievements:

*  Re-partitioned the hard drive and set up GPU integration.

*  Manually cleaned the data that was retrieved from the previous week.

*  Tested the initial model on the new data

*  Began research and implementation of the VGGNet model

### Week 6 ###
Plans:

* Finish implementing VGGNet model.

* Write up group report sections.

* Prepare demo slides and speech

Achievements:

* Written introduction of group report as wells as section relating to TensorFlow in the tools, information search and reflection sections.

*  Presented introduction of demo video and written Tensorflow related portions of System overview.

---

## Contributions ##
### Technical ###

I [gathered various external datasets](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/6359f1b9d18dad0800add7a86b90dceb68887816) that would be used to train our neural network. Then [manually sorted and selected the images](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/7f1361589b1626c5ecc50ac6ec339613b7c03731) that would be relevant as training data for our project. After compiling the various datasets I [merged them into a single training dataset](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/2bdde92af697a9d655c57022656ae95755edfaba).

I [implemented an additional object classification model](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/2bdde92af697a9d655c57022656ae95755edfaba) to improve upon our initial model. This was done through research on models that are currently being used for object classification on traffic signs. From there I decided on VGGNet which has a good balance between accuracy and simplicity. I then looked through various repositories of implementations of VGGNet and found one that could be adapted for our use case. I have then refactored the code to suit our data.

### Non-technical ###

I [started an an informal communication channel](https://i.imgur.com/rMihrUE.jpg) for all TensorFlow related discussions  between two other members designated to to the neural network component of the project. From there we discussed updates on status and shared tips.

I [prepared and managed all collaborative documents](https://i.imgur.com/2bPwduW.png) within a Google drive folder which were all shared with the group and completed within Zoom calls.

I wrote the introduction of the group report and all the TensorFlow related content in the system overview, tools, information search and reflection sections. I then imported the content from the Google Doc into the wiki and [performed the final formatting and editing](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/history/reports/group/report).

---

## Reflections ##
### Programming ###
The project did not involve much programming until the last few weeks where scripts, plugins and back-end models became relevant. Due to my previous experiences, I gravitated towards programming the TensorFlow models. Much of the work involved refactoring code from external sources and thus it was a struggle at times trying to understand certain lines of code. However, this was usually pretty easily resolved as the TensorFlow library is pretty well documented.

### Version Control ###
Git commits and branches were used appropriately on BitBucket so it was always easy to review the progress made by fellow team members and implement materials into my own code. Much of the commit activity were made later on in the project as the initial weeks were dedicated to setup.

### Extreme Programming ###
Since there wasn't a lot of programming involved in the earlier stages of the project, some of the extreme programming roles such as programmer and tester were not very necessary. As the project diverged into separate components based on strengths and backgrounds, it also became difficult to properly designate and rotate roles as a complete group as we would often focus on performing all the roles individually. As rotation becomes less feasible it may be necessarily to fix all the roles going forwards. 

### Thoughts and Improvements ###
Admittedly, my contributions were lacking during the earlier weeks due to troubles in setup stemming from incompatible software and hardware. However, once the project diverged into the simulator and object detection components, I was able to find my place within the team became more confident with my setup and my abilities. One substantial area of improvement I will need to make is documentation. From both prior experiences in machine learning projects the nature of this university course, I have learnt that properly documentation is vital in supporting both my teammates and myself. Thus, I plan to write more wiki pages to document the neural network architectures that I use and their parameters. Additionally, I need to use the BitBucket environment and user stories more frequently. Oftentimes, I would informally address my issues and ideas through direct message rather than addressing them appropriately on as issues on Bitbucket or under user stories on Trello, where they can be formally documented.