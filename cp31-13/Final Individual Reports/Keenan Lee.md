# COMP3888 - Final Project Report (Individual) #

## Introduction ##
This document lists the individual contributions made by Keenan Lee to the ‘CP31 - Sign Detection using Computer Vision’ project. The aim of the project is to improve the original code provided for detecting traffic signs and traffic lights and to also include new tracks and new traffic signs in the simulator. During weeks 7 - 12, I continued my XP role as the client point of communication, asking any relevant questions to the client, and relaying information back to the team. During these weeks, I largely focused on implementing the brake into the Donkey Car system, making general improvements to the simulator and the AI, controlling the demo, and working on creating a testing framework.

## Statement of work done ##
This section covers the technical work and non-technical work I did over weeks 7 - 12 and the evidence to support my claims.


### Technical work done ###

- Implementing the Donkey Car brake system into the simulator with Johnny. [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/0003b539b9f4cfc54b314add4c3f8b98d277fa0a).

- Changing the camera resolution that is used when the Donkey Car stores images in the simulator. [Pull Request](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/23).

- Training and improving the AI for this new camera resolution. [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/25eccd7d0ecae4fbb206356802f7495a51960611).

- Adjusting and improving the actions the Donkey Car takes while in the simulator upon detecting signs.
 [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/529ccb118dc3af26dd8b2277119cff84e342336c) and [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/b3dbf2c18bb96e9ecd4a94f580767069a93fca99) and [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/0003b539b9f4cfc54b314add4c3f8b98d277fa0a).

- Upgrading our Donkey Car version model to 4.0.0. Helping other teammates bugfix issues they were encountering with the new version. [Pull Request](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/26)

- Creating a testing framework (implemented as a Python script) that can be used to measure and compare the accuracy of our new OpenCv detection algorithms. [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/43559bf6bc432cda847c2f746af603d717dccb93).

- Collected data and created test cases to be used in our testing framework [Pull Request](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/32)

- Helped other teammembers debug using the simulator on their systems. [Pair Programming evidence]. The pair programming sessions I was involved with will have my name. The outcome of each pair programming session and what we talked about can be found by clicking on the particular link. (https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/browse/Pair%20Programming%20Evidence)
 
- Reviewed pull requests by other members by looking through their changed code and occasionally downloading their branch and running the simulator to ensure everything was working. [Pull Request #1](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/20), [Pull Request #2](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/30), [Pull Request #3](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/29), [Pull Request #4](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/31), [Pull Request #5](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/33), [Pull Request #6](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/28), [Pull Request #7](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/34), [Pull Request #8](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/36), [Pull Request #9](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/35)


### Quality of technical work done ###

For the braking action, to ensure quality I did pair programming sessions with Johnny so that we could get multiple perspectives on how to solve the problem. We also did pair programming sessions with the client where we showed him the code we changed, and got his opinions and feedback. Our changed code was then put through roughly 100 test cases created by the creators of Donkey Car. This was to ensure that our changes didn't break the existing system in any way.

For the other modifications I made to the simulator such as the actions of the Donkey Car and the camera, I mainly ensured quality through acceptance and usability testing. For acceptance testing, I would run the simulator and visually observe that things were working as expected without breaking. For example, after implementing the stopping action, I would run the simulator and verify that the Donkey Car did indeed stop, before a stop sign.

I also conducted usability testing by having other group members run the new changes on their systems, and fix any issues and bugs that arose for them through pair programming.

For the testing framework I wrote, the key things I tried to accomplish was modularity of the code, and ease of access when creating new cases. This would ensure that any changes to the testing framework could be done easily, as well as allowing for the efficient creation of new test cases.

Finally, I made use of pull request reviews both for myself and my teammates code, to get multiple perspectives on our changes and identify any bugs that were missed.

### Non-technical work done / Other contributions to group processes ###

- Preparing the [demo](https://drive.google.com/file/d/1MUSE49xbEUOnpXftkg5nXmfjzvoCpZip/view?usp=sharing) for our presentation.

- Adding documentation for how to run the [Donkey Car system](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/Documentation/Running%20the%20software).

- Helping the team complete [status reports and meeting minutes](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/browse/Meeting%20minutes), and submitting the status reports to Canvas.

- Helped write the [user stories](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/User%20stories).

- Read the [Donkey Car documentation](https://docs.donkeycar.com/) carefully so that I could make useful modifications to the simulator.

- Communication with the [client](https://comp3888t13agroup5.slack.com/archives/C019US118KC/p1601789717012200).

- Created [video / show reel] (https://drive.google.com/file/d/16IPZNoWgUFzOvtR3zwyFxTLPtpxRACwB/view?usp=sharing) for client

## Week-by-week explanation ##
NOTE: Evidence for any claims below should be covered in one of the hyperlinks below; this will act as more of a summary.

- Week 7: In this week I intended on implementing the brake system into the simulator so that the car stops properly. I was able to complete this with a lot of help from Johnny. H really helped a lot and there's no way we would have functioning brake without him.

- Week 8: In this week I intended on changing the camera resolution of the simulator to 240 x 240, and training a smarter AI. I was successful in changing the camera, however, my results on the AI were mixed. While it was smarter than the previous iteration, it still had issues of driving into walls and acting unpredictable/

- Week 9: In this week I planned on upgrading Donkey Car to the latest version and improve how the car turns in the simulator. I was able to achieve this.

- Week 10: In this week I planned on creating the testing framework as requested as the client. I was successful in getting a working prototype of it, but still had further refinemetns I wanted to complete.

- Week 11: In this week I planned on creating more test cases for some more of the signs in our testing. I was successful in doing so, and ended helping Oscar getting his parking sign detection code working in the simulator.

- Week 12: In this week I planned on creating more test cases specifically for the traffic lights, and implement the stopping action for the Donkey Car when it detects a parking sign. I was successful in completing this.

## Reflection ##

- **Version Control**: For this project, our team used Bitbucket for version control. Reflecting on this, I'd say that we did a good job of utilising the various features provided such as Pull requests and issue creation, especially when compared to the first 6 weeks of the project. 

- **Coding styles**: For the code I wrote throughout the project (the testing framework), my aim was to make the code as modularised and easy to use as possible. I prioritised modularity as a way to make quick changes to the code, and I prioritised ease of use so that we could create multiple test cases quickly. I also heavily documented the code so that other teammembers can use it if needed.

- **XP**: For this project, I think we did a much better job of following the XP guidelines for weeks 7 - 12 compared to the first 6 weeks, where we did far more pair programming sessions with each other, user story driven development, documentation and testing. The areas where I think we could have improved were focusing more on creating test cases before developing features as well as following the XP roles more strictly, such as having a doomsayer, tester, etc...

### Challenges faced ###

The largest challenge in this project was our lack of familiarity with Unity and OpenCV. None of us had any strong prior experience with any of these tools, causing us to conduct lots of research to just understand the basics. This added time pressure onto our project and slowed down our efficiency.

Regarding my XP role of being the client point of contact, a challenge I faced was feeling like my role was fairly useless for the last few weeks of the project. In the first few weeks of the project when we were primarily communicating using email my role felt useful, where I could summarise any questions our team had and send them to the client. However, in the final few weeks as we began using communication channels such as Slack and Discord, it became far more practical for members to just send their questions directly to the client instead of to me, as this would generate a faster response for them.

### Role in the group and as a computer scientist ###

As a computer scientist, the main skills I drew on was my understanding of algorithms and code modularisation, as well as the ability to analyse existing code and determine its functionality and purpose. My understanding of algorithms and modularsation was most effectively used when I created the testing framework, where I used these principles to create an easy to modify code base that could quickly generate tests. My ability to analyse existing code was most useful for the simulator related work. This is because the Donkey Car framework had a pre-existing code base, so if we wanted to make changes, we would first have to understand their existing code so that we can effectively implement our changes.


## Closing remarks ##

As a team, we were overall able to meet all the key user stories given to us by the client in a timely manner. We did so by using a divide and conquer strategy, where we would each tackle different user stories, and then combine and merge them together once completed. To improve, we could have followed the idea of test driven development more closely. While we did create tests, we did so after producing the code, so following test driven development more closely could have guaranteed us a more streamlined development process from the onset, where we would be able to immediately fix any bugs. We also could have followed the XP roles more closely, as while we did follow some roles like the tracker and manager closely, we neglected other roles such as the tester and doomsayer. Following the XP roles more closely would have provided each of us with a more specialised skillset, providing greater efficiency and productivity in the long run.

Reflecting on our workflow compared to the first 6 weeks, I think we made major improvements. The biggest improvement was the use of more rigorous test cases (though they were mainly created after the code instead of before, so it was not test-driven development). In the first 6 weeks we were using a very minimal amount of testing, but towards the later weeks, we had a large ensuite of tests that allowed us to measure and evaluate our algorithms. Our communication was also drastically improved, where we focused more on using tools like Slack for communication, so that it's easier for everyone involved in the project to monitor our work. We also made use of far more pair programming sessions, which was especially useful when integrating our work together. In the first few weeks of the project, we would do roughly 1 pair programming session every fortnight. This is in contrast to the final weeks, where we averaged about 2 pair programming sessions per week.

We also made large changes in response to client and tutor feedback. For client feedback, this came in the form of our testing framework, which came as a request following our client deployment. Evidence of planning for the creation of this testing framework can be found [here](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/TwoTasksDone/Tasks%20to%20be%20done). For our project, the main feedback from the tutor came in the form of more careful planning for our user stories, and the use of more pull request reviews. As a result, we created this [spreadsheet](https://docs.google.com/spreadsheets/d/1QlM02P0Eom47eLy5DrVxL1XlPOsksqbIIIxj-WNMf_w/edit#gid=0) which detailed how we were going to distribute pull request reviews. 

For his specific feedback regarding individual reports, he suggested that we follow Osama's individual report structure more closely, which I have attempted to mimic in this report.