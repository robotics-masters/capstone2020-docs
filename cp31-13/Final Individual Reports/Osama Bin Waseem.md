# COMP3888 - Final Project Report (Individual) #

## Introduction ##

This document lists the individual contributions made by **Osama Bin Waseem** to the ‘_CP31 - Sign Detection using Computer Vision_’ project. The aim of the project is to improve the original code provided for detecting traffic signs and traffic lights and to also include new tracks and new traffic signs in the simulator. Throughout the semester, I had a chance at experiencing different XP roles including Programmer, Tester, Doomsayer and Manager. Having the most work experience as a developer, I was the one responsible for setting up and managing the Bitbucket repository and the project, in general. I led the team by dividing up tasks amongst the team members during each week’s meeting and catching up with everyone on their progress. I also made sure that each team member’s progress didn’t block anyone else on the team. I was heavily involved with improving the four turn (left and right) traffic signs, the traffic lights detection code, improving the actions the car takes upon a detection and getting everything to work altogether for both our first and final client demo.

## Statement of work done ##

This section covers the technical and non-technical work I did over the semester and the evidence to support my claims. There is also a summary of the quality of technical work done.

### Technical work done ###

- Set up the Bitbucket repository and ensured everyone had the correct access level. Restricted the team's ability to push to the master branch directly and granted myself the permission to merge other branches to master. This makes it so each branch must be reviewed before being merged to master and allows us to avoid conflicts as the project grows over the coming weeks. [Bitbucket repository](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/src/master/)
- Set up issue tracking on Bitbucket so each team member could be assigned an issue they were working on so progress could be tracked easily. [Bitbucket Issue Tracking](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues)
- Wrote a script to allow us to generate results given detection code. This was used with the original code provided by the client to generate baseline results. [Script](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/src/master/opencv/run_tests.sh) - [Baseline results](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/src/master/opencv/Results)
- Pushed the initial code to the repository and shared instructions with the team on how to run it. [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/39c82853b2d5cd498eca3d2d79a926b2b785f710)
- Reviewed and familiarised myself with the original code to get a better understanding of how the original detection algorithm worked for turn signs. [Original code](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/src/master/opencv/)
- Proposed and programmed the first iteration of the solution that would improve the turn sign detection algorithm. The baseline code detected the turn sign once in 140 frames, whereas the first iteration of the improvement detected the turn sign 7 times in the same 140 frames. [Issue #5](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues/5/refined-working-solution-of-provided-code) - [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/cd2de0ebfce010b46268dd2410326ae356863c15)
- Continued improving the turn sign detection algorithm by researching into feature matching. Implemented the SIFT algorithm (Introduction to SIFT (Scale-Invariant Feature Transform), n.d.) and recorded a significant improvement to the detection count. The improved code now detects the turn sign 31 times as compared to only once when using the baseline code. [Issue #12](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues/12/improvements-to-turning-signs) - [Video](https://youtu.be/AzwAmBrw02E) - [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/055ccc610028ac490e053b2407c731ebc36b3e14)
- Helped with the integration of all the parts of the project including the simulator, the traffic sign detection code and the Robotics Masters library to see everything work together as requested by the client. [Demo video](https://www.youtube.com/watch?v=KUbAHsUcolg&feature=youtu.be)
- Helped other team members set up their development environments and debug coding related problems through pair-programming sessions. [Pair programming evidence](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/Pair%20Programming%20Evidence/Osama-Oscar-26-09-2020)
- Reviewed pull requests set up by team members and merged them to the master branch. [Pull request #1](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/5) - [Pull request #2](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/7) - [Pull request #3](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/8) - [Pull request #4](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/9)
- **Week 6 onwards**
- As the real-world solution for the turn signs didn't work well with the simulator, the client requested we focus on the simulator rather than the real world. This meant that I had to change and improve my turn sign detection code to work in the simulator. [[Issue #15]](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues/15/find-a-solution-for-detecting-turn-signs) [[Pull request]](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/21)
- Fixed a bug related to the `templates` folder that the SIFT algorithm uses for the turn signs. [[Pull request]](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/22)
- Cleaned up the code and removed unnecessary files. [[Pull request]](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/24)
- Added detection code for black background turn signs. [[Issue #19]](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues/19/add-detection-code-for-turn-signs-with) [[Pull request]](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/25)
- Reviewed, tested, and merged various different pull requests throughout the semester. [[Links here]](#)

### Quality of technical work done ###

All code that was written is divided into functions and so is easily testable. To measure the performance of the improvements made to the traffic sign detection algorithms, it was essential to have a baseline. This led to the creation of a script that would generate results given a traffic sign detection algorithm. This allowed us to use the script to measure how the changes to the detection algorithm we make affect the results. For the first few weeks, most of the team was working with Unity and modelling assets which would be used in the simulator, we didn’t make much progress with the OpenCV code. During the last week, we were able to do a few pair programming sessions helping each other out and programming together. I was also responsible for reviewing all pull requests, requesting changes on them and advising team members on how they could refactor the code to be more efficient and readable. The main testing I did was comparison and performance testing on the code I wrote for the turn signs, which involved running the modified code and comparing the results against the baseline results and ensuring the code I wrote was performant and wasn’t computationally expensive. 

### Non-technical work done ###
- Ensured the [Wiki](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/browse/) on our Bitbucket repository is well-maintained and all information is easily accessible.
- Helped the team complete weekly meeting minutes, project status reports, and all other documentation on the [Wiki.](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/browse/)
- Helped write some of the [user stories.](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/User%20stories)
- Divided the tasks amongst team members and caught up with everyone’s progress during our team meetings. [Issue tracking](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues)
- Reviewed the documentation shared by the client on OpenCV. [Video](https://www.youtube.com/watch?v=JX95Cmp-lno) - [Slides](https://cdn.discordapp.com/attachments/751798747922432010/752142762694148136/2_Morphologoical_Image_Processing_.pdf) - [Documentation](https://docs.opencv.org/trunk/d9/d61/tutorial_py_morphological_ops.html)
- Researched into existing techniques being used by others for the same problem - traffic sign detection and recognition. [Research paper #1](https://ieeexplore.ieee.org/document/7033810) - [Research paper #2](https://www.irjet.net/archives/V4/i4/IRJET-V4I4275.pdf)
- Drew a [high level system architecture diagram](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/System%20Architecture%20Design%20(High%20level)) to visualise how all components of the project work together.
- **Week 6 onwards**
- Planned out how the first and final demo would take place and rehearsed it with the team. Prepared the presentation slides for the demo and participated in the demo. [[Slides]]() - [[Demo recording]]()

## Reflection ##

- **Version control**: This is managed through Bitbucket. The team is using an existing code base provided by the client. I have set up the repository such that no one can push directly to the master branch except me. This allows us all to work on separate branches related to the task assigned and then set up a pull request to merge that branch into the master branch after at least one other person has reviewed it. This means the team can pick up on issues, solve conflicts and request changes before the work is made available to everyone through the master branch.

- **Coding styles**: The code written by me follows the PEP 8 style guide (PEP 8 - Style Guide for Python Code, n.d.) and is written in a testable fashion. All functions follow the single responsibility principle from SOLID principles (Wikipedia, n.d.) which means each function is responsible for only one thing. I also made sure to add comments to explain what a certain function did. This makes the code easy to read and test. It should also help us when we set up the continuous integration pipeline on Bitbucket. 

- **Extreme Programming**: The team has been trying its best to follow the XP principles throughout the weeks. This means that the project is being developed in increments based on the priority of the user stories. During our team meetings, the user stories would be divided between team members by creating issues on the issue tracker set up on Bitbucket. This way, everyone was aware of what others were working on. It also meant we knew who was responsible for a given user story. By doing so, we had something new to show to the client every week so we kept the client satisfied. The role rotations were successful in all weeks and everyone was happy with the roles assigned to them. However, it is worth noting that the client preferred us having a single role throughout the semester rather than switching roles on a weekly basis.

### Challenges faced ###

- **Insufficient knowledge and experience**: as the team had little to no experience with the tools and technology required by the project, it was difficult getting started. A lot of time was spent researching and reading documentation to figure things out. The team is in a much better position now as compared to the earlier weeks.

- **Team dynamics**: All team members have never met before. It was difficult at the start to figure out everyone’s strengths and weaknesses, so dividing the tasks for the first few weeks was a challenge. However, it was essential to get to know each other and the strengths and weaknesses of each other so we could work effectively and efficiently. This was done by arranging a Zoom call and getting everyone to talk about themselves and their expertise. 

- **Communication**: There are four different tools used for communication. Zoom for voice and video meetings, Slack and Facebook messenger for daily chats among the team, and Discord as the client, most of the support staff and other groups are on there and prefer to use that. This made it really hard to communicate as no one was sure of what platform to use. However, we all decided to move away from Facebook messenger and use Slack for our daily chats. We also added the client to our Slack channel so he is always aware of our communication and can chat with us there instead of on Discord.

### Role in the group and as a software engineer ###

As stated in the introduction, I have had quite a few roles over the last six weeks.

**Week 2 - Programmer**: came up with user stories from the project specifications and ensured that the client provided code ran without any issues and added it to the repository so it is accessible by everyone. 

**Week 3 - Tester**: came up with a solution to compare our improvements against the original code using comparison testing.

**Week 4 - Doomsayer**: made sure everything was on track and reported back to the team if we were lagging behind.

**Week 5-12 - Manager**: communicated with the team and arranged a meeting time and recorded the information needed for meeting minutes to help the Tracker. 

As a software engineer, I implemented the script to generate results given a traffic sign detection code. This was essential as it would allow us to validate our improvements to the algorithm. I wrote testable and well-documented code for the turn signs detection. I also reviewed pull requests and ensured everyone’s work met the standard of quality I was following. I had two pair programming sessions last week, one to help a teammate debug some algorithm related issues for the stop sign and one to help integrate everything together for our first client demo. All the links to the information mentioned in this paragraph are shared above in the ‘Statement of work done’ section.

### Going forward ###

At the start of the project, there were quite a few tasks associated with Unity and modelling assets which limited the number of people working on the OpenCV code. As most of those tasks are completed, I would like to get more team members involved with the OpenCV code so we can improve all traffic sign detection and also look into adding detection code for the traffic lights. I would also like to set up a continuous integration pipeline which would run the tests and show coverage on every commit so the team focuses on writing tests and maintaining a high coverage as we get more people involved with the OpenCV code.

## References ##

Introduction to SIFT (Scale-Invariant Feature Transform). (n.d.). OpenCV. Retrieved September 24, 2020, from https://docs.opencv.org/3.4/da/df5/tutorial_py_sift_intro.html

Wikipedia. (n.d.). SOLID Principles. Retrieved September 9, 2020, from https://en.wikipedia.org/wiki/SOLID

PEP 8 - Style Guide for Python Code. (n.d.). Python.Org. Retrieved September 9, 2020, from https://www.python.org/dev/peps/pep-0008/