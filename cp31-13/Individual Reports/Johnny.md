Roles, Responsibilities and Contributions
=========================================

I have worked in a number of roles throughout the project and my responsibilities continue to evolve as the project progresses. In the beginning, we were given two systems which interacted with each other; the donkeycar environment and the simulator software.

Early on the project I undertook the role of **Existing Systems Researcher** which led to an understanding of how the donkeycar driver interacted with the simulator. In particular, we learnt early on how certain properties like which track to load are sent to the simluator from the donkeycar program.

I also took on the role of **Software Researcher** on the simulator side, establish workflow within Unity's development environment and bringing team members up to speed with external software we needed such as Blender for the modelling of new assets.

As for XP roles the ones I undertook were:

-   **Week 2 - Tester:** While week 2 didn't have many programming tasks, I had to make sure the new tracks and signs we modelled were set up correctly and to client specification

-   **Week 3 - Doomsayer:** Highlighting major issues that we were falling behind on (we had nothing major that week)

-   **Week 4 - Tracker:** Keeping track of meeting minutes, making sure people were on track especially on the simulator side. Discussing what we should be doing if things started to go off-track.

Weekly Planned Tasks & Extent of Work
=====================================

**Weekly Update Videos**

-   [Week 2 & 3](https://drive.google.com/file/d/1x1USLvkOTlh7QacpMFdXISg3_5msts_m/view?usp=sharing)

-   [Week 4](https://drive.google.com/file/d/12TnAvUCR9Ek7jN_izCWXjzT4i7Xir5Mv/view)

-   [Week 5](https://drive.google.com/file/d/1EbwY6i80am8qoB-wXy4OEmQm_LhmPR7h/view?usp=sharing)

Since the beginning of the project, I have mainly been on the simulator side, focusing on delivering much needed improvements as specified by our client. Our team also made 1 minute week update videos which are relevant to this section and show the end results of each week's work.

During **week 2 & 3**, we were tasked to get two tracks layouts provided by Robotics Masters into the simulator as well as some road signs. In accordance to my role as tester that week, I was also responsible for quality control of these new assets as previously mentioned. I was tasked with getting one of the two tracks into the simulator ([Commit\#b100633](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/b100633a003cc738479d7b8daf277de03dcd39b4)), helping out the modelling team with their task by walking through the creation of one of the signs and making sure our new assets were registered and recognised on the donkeycar side of things ([Commit\#305d773](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/305d77340163675cea7e26f694a7550429d61568)).

**Week 4** for me was modelling & programming traffic lights to be used for the OpenCV detection code the team will work on. As there was no existing traffic light in the simulator, all modelling and programming was completely new to the project and the work done can be found in [Commit\#35ff1a6](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/35ff1a6c19069af7675ba2827204d689bf87e0e7).

In **Week 5**, I started laying the foundations for users to be able to edit properties within a scene without having to rebuild the entire simulator project every time they want something changed. I did this in the form of having the traffic lights read .json file and changing its properties based on the values in that file. The work done can be found in [Commit\#885015c](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/885015cabfdda4265d74c3a2cbc5be3ad9f27f25). I wish to extend this and add a fully-featured editor mode so tracks can be added and shared in a way independent of the Unity project however, this might end up being out of scope as I'm limited by the university's time constraint currently.

Quality of Technical Work Done
==============================

Much of the work early on in the project did not involve code however, we employed pair-programming like practices early on to ensure the quality of our models and track designs were consistent. At the start, I was responsible for the Unity project and as such made sure to run through tasks with other members doing simulator things.

As the person mainly responsible for the simulator side of the project, I was also tasked with making sure commits involving the simulator project were satisfactory and didn't break when other team members. I made sure to review these pull requests and give feedback where appropriate as evidenced
[here](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/6/stop-sign/diff#comment-176246975).

Unit tests were also employed on one of the more recent extensions I've been working on. We used unit tests to ensure we knew what inputs and outputs to expect before any code was written and because this simulator extension relies on user-input, unit testing is useful in ensuring we keep a library of regression tests to make sure known bugs / exploits don't re-emerge when further developments are made. We make sure to test as many branches of execution as we can, from expected / regular functionality to edge-case exploits such as trying to access a directory you're not meant to be allowed in. We haven't decided on the best way to commit Unity tests to the repository yet as major alterations to the project structure are required for unit testing to be run within Unity.

Other (Non-Technical) Contributions
===================================

As previously mentioned, I looked after pull-requests that involved the simulator, making sure to test the new features and make sure project structure was maintained before giving the OK to Osama to merge. In addition to that, I have recorded the meeting minutes during my time as the tracker, divvied up tasks when the project first started and established the Unity workflow within the team.

Also as previously mentioned, I did research into the existing systems we were given and helped out team members understand how each piece connected and helped team mates get adjusted with Unity & Blender.

Reflections
===========

Programming
-----------

It was really hard for the team and I to get programming right off the bat as the client had provided us with a pre-existing project to improve upon. Much of the initial stint was spent doing research on the existing systems and their interactions with one another as well as learning new tools.

On the simulator side, documentation was non-existent and everything we learnt was done by manually tracing through the existing code-base which was time consuming. There were also classes in the code-base which were depreciated (eg. PID controller and the Path Generator) but not mentioned anywhere until asking the maintainers / client which made it hard to self-sufficiently understand what was going on. It would have made the first stint of the project much easier if the code-base even had some documentation.

We also didn't do much programming on the simulator side of the project in the initial stint, as the client's requirements stated there were more important things (modelling in the requested objects) to be done before simulator improvements were made and as such, actual XP programming hasn't really kicked in until recently for simulator work. It is only until week 4 that I started programming and laying the foundations for some improvements to the simulator. From the lessons learnt in the above paragraph, I'll make sure to document the new functionalities I will implement for future developers to improve upon as I don't believe everything I want done can be completed within project time-frame.

Version Control
---------------

Early on in the project, we were debating whether we wanted to have the Unity project in the same repository as the OpenCV code-base as the existing Unity code-base along with the models meant we could be pushing on Bitbucket's file size limit in future. Ultimately, the benefits of version control outweighed this potential risk and I took on responsibility to make sure the Unity project didn't get too out of hand. Any changes to the simulator, especially new models go through rigourous review before being pushed and I make sure the team doesn't commit any unnecessary bloat to the repository.

Extreme Programming
-------------------

As previously stated, as someone mainly working on the simulator side of things, there hasn't been much need for XP until recently. The work on the simulator early on didn't lend itself to XP methodology as it was non-programming tasks however, once I am able to get the green-light for my proposed simulator improvement, we can pull another team member to follow XP methodology provided it doesn't hinder the main OpenCV side of the project.

I also had to be reminded of a testing-first approach which XP methodology establishes. As a programmer, I've found it difficult to write precise test-cases before thinking of program structure. I can think of the inputs and outputs but edge-cases that can break a program I usually think of as I trace through source-code and come up with attack vectors. As such I've usually written test-cases after I can trace through source-code but I've been reminded to come up with some preliminary test-cases for this project and have been trying to adhere to that.

Challenges
----------

-   **Lack of Documentation:** As previously mentioned, there was pretty much no documentation for the systems we were given by the client. To understand the existing code-base, we had to trace source-code as well as resort communicating with maintainers of the project.

-   **Knowledge-Gaps:** At the start of the project, non of our team had experience with OpenCV and Unity was foreign to most members as well. A lot of time was initially spent on research and getting up to speed with the project.

-   **COVID:** The pandemic going on has been a challenge keeping the team and client away from meeting in person. We've worked around this and adjusted through various online communication channels and the team as well as the client has been very responsive on these channels however, I'm sure some of us would have liked to meet in person. COVID has also changed up the project as the donkey car simulator only came into prominence due to this and we aren't able to run our sign detection algorithms on actual hardware. I would have personally liked to work on actual hardware and build the car.

-   **Code Version:** As this is a project that external developers who are also working on the code, we have to consider updates on their end and whether we can integrate our code. We also have to make sure to communicate to the client and ensure that improvements we make on the simulator aren't already being worked on by someone else.

Role in Group and as a Software Engineer
----------------------------------------

As mentioned previously, I've been mainly involved on the simulator side of the project, making sure to review all pull-requests that concern the simulator as well as make further developments for the simulator. I'm able to answer any questions the team might have with regards to the workings of the simulator.

As a software developer, I've begun work on isolating scenes from the Unity project so complete rebuilds aren't required every time an edit/new track is added ([JSONReader.cs](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/885015cabfdda4265d74c3a2cbc5be3ad9f27f25#Lsdsandbox/sdsim/Assets/Scripts/JSONReader.csT1)). It is also important to adhere to OOP Design Principles, especially for this proposed improvement, and have only just begun planning out Design Patterns to be used. I'll make sure this new system is well documented unlike the rest of the code-base.

General Thoughts
----------------

The team has been on-track with implementing features and keeping up with the client's requests. Our communication has been solid with fast replies however, we could be using Slack a lot more as its meant to be the official channel of communication we are being marked on. Osama has really put in a lot of research on the OpenCV side of the project and Keenan has really been helpful bridging the DonkeyCar work to the simulator work. Oscar, Tamara and Chengdong have done their share of work and have been reliable members and this has been why the team has managed to stay on schedule thus-far.

For the non-technical tasks of the project, the team has done a great job at managing. Meetings have had a maximum of 1 absent member on the rare occasion. Minutes have always been recorded and we would always come out of meetings knowing what our tasks were. Solid team work all round.

Moving forward, we're expecting the client to drop a second scope document soon and I'll need to discuss the scope of the improvements I'm proposing for the simulator.