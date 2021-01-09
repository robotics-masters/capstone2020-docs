Introduction {#introduction .unnumbered}
============

For this project I have been assigned numerous roles in order to help
achieve a high level of organisation and quality of work. These roles
include team manager, Bitbucket expert, and document controller. 

As the Bitbucket expert I created and maintained both repositories, the group
wiki and the source repository. This entailed uploading the weekly
client, tutorial, and team minutes, as well as the pdf versions, and the
creation and updating of links and other relevant documents to create a
central point of access. In addition to this, I was in charge of making
sure everybody has correct access and rights on the repository.

The XP roles undertaken were not rotated weekly. Instead, members were
allocated the role they were suited for at the beginning of the project.
For me, I was allocated the team manager. As the team manager I was
responsible for communicating the date and time for team meetings that
suited all (or the majority at best) team members. I often posted
reminders, summaries of work to be completed, and monitored the work
being produced by other team members to ensure it was at a high
standard.

In addition to the team manager, I was the document controller.
This role encapsulated the revision of documents added to the Bitbucket
repositories and fixing typos, structural errors, and other flaws. Often
the minutes produced for a meeting were written on a google document by
all team members. It was my job to convert these documents to markdown
form for easy viewing on the Bitbucket wiki.

Statement of Completed Work {#statement-of-completed-work .unnumbered}
===========================

**Week 2:** During the second week of the semester, there was first
contact with the client for which a sprint was held and we were all
assigned to install the relevant tools on our computers and gather a
sense of how to use them. There was no list of work items to be
completed, rather a general setup period and some time to familiarize
oneself with the environment. As the Team Manager, I communicated a time
and date to convene and discuss, as a team, our collective understanding
of the task itself and catch others up on tool setup as there were many
issues at the beginning of this project regarding installation and setup
of the environment. 

[Client Meeting [1
02/09/2020]](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Client%20Meetings/Client_Minutes_1)
[Team Meeting 1
[07/09/2020]](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Team%20Meetings/Team_Minutes_1)

**Week 3:** Going into the next week, installation issues persisted
hindering early progression of the project. Through communication with
other groups from the University, I was informed that installing Ubuntu
was the easiest solution. As the document controller, manager, and
Bitbucket expert, I made it my job to install the operating system and
environment and write up a full [installation
guide](https://bitbucket.org/DylDupe/comp3888_t15a_group1/src/master/Installation_Guide.md)
for my team and others who were experiencing similar issues. The email
sent out by the client highlighted a number of tasks, some of which
built upon the previous week’s tasks. These included autonomous drone
navigation using MavSDK, running both flight stacks (i.e. PX4 and
ArduPilot) together with Gazebo, and simulating weather. From these
tasks, taking into consideration the installation issues and the need to
install an entire operating system, I was not able to achieve autonomous
drone flight. I did however manage to install PX4 and ArduPilot and
connect them both to the ground control software QGroundControl.
Simulation of the weather was allocated to Ivan Xu. 

[Team Meeting 2
[13/09/2020]](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Team%20Meetings/Team_Minutes_2)

**Week 4:** For week 4, we were required to submit a [1 minute video
presentation](https://www.youtube.com/watch?v=ysOZhEe95d8) of the work
completed for the previous week. During this week’s sprint with the
client, the tasks set out for us were to gain further experience
navigating the drone with MavSDK, rendering worlds, modelling charging
stations, and thinking about the algorithm. As the manager I delegated
these tasks to team members most suited to them. For example, I assigned
William and Jimmy the tasks that were algorithm related - they became
the algorithm development team - as they are currently based in China
together and both could not setup the proper Linux environment to
complete the other tasks. During the team meeting for this week, Justin,
Nicholas and I explored the compatibility of code made for PX4 and
ArduPilot employing techniques of paired programming which ultimately
enhanced my understanding of the code and MavSDK. Additionally, we
looked into the basics of world rendering but there was little to no
exploration into the modelling of objects. 

[Client Meeting 2
[14/09/20]](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Client%20Meetings/Client_Minutes_2)
[Team Meeting 3
[17/09/20]](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Team%20Meetings/Team_Minutes_3)
[Client Meeting 3
[18/09/20]](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Client%20Meetings/Client_Minutes_3)

**Week 5:** The tasks set out for this week by the client in the sprint
were to model objects into the world and use way-points to navigate the
world. This week however I allocated the drone flight automation to
Justin and the modelling to Nicholas and Ivan and set myself the task of
developing a program to randomly spawn charging stations into any given
world. This program absorbed most of my time and a demo can be seen here
in the [1 minute video
presentation](https://www.youtube.com/watch?v=hyzNpVydzBk). The team
meeting for this week was concerned mainly with world rendering as we
planned to catch up on that as it was last weeks task and a primary
subtask for my program to tackle. 

[Team Meeting 4
[20/09/20]](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Team%20Meetings/Team_Minutes_4)
[Client Meeting 4
[21/09/20]](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Client%20Meetings/Client_Minutes_4)
[Client Meeting 5
[25/09/20]](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Client%20Meetings/Client_Minutes_5)

**Week 6:** I spent the majority of this week developing the program to
randomly spawn charging stations. The client was mainly concerned with
the progression of the reports and thus no tasks were set to be
completed for the coming week. As a result of this, there was no 1
minute presentation made as each team member focused solely on the
reports due.

[Team Meeting 5
[26/09/20]](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Team%20Meetings/Team_Minutes_5)
[Client Meeting 6
[28/09/20]](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Client%20Meetings/Client_Minutes_6)

Extent of Completed Work {#extent-of-completed-work .unnumbered}
========================

**Technical Development** The setup of the environment consumed a lot of
my time in the earlier stages of the project. It involved learning about
many different packages and software and writing the relevant
documentation for those to be able to reproduce our experiments and
procedures later on. These included:

-   Installing Gazebo, PX4, and ArduPilot onto my machine proved to be a
    difficult task, it was undocumented and took around a week to
    complete. There were issues with the installation of python on
    Ubuntu as PX4 and ArduPilot required python2 for some program and
    python3 for others. Doing a fresh installation of Ubuntu came with
    no installation of python and thus when installed, the binary file
    is named python3 rather than just python. The program files for the
    flight stacks specified the binary file “python” to run the code so
    it was defaulting to python2 if it was installed. The solution to
    this was to create a symlink of the binary “python” to “python3”.

-   Compiling many python2 and python3 packages such as pymavlink,
    dronekit, and MAVProxy.

-   Generating objects in worlds also took a few days to complete. World
    files are formatted as XML files and objects in these files are
    children of the main tags. There are specific placement of these
    children throughout the files which required me to learn how to use
    the xml.etree.ElementTree library in python3. The methods in this
    library allowed me to place these objects in the right positions but
    the tricky part was knowing which combination of properties to set
    for the objects to spawn correctly. At first, they would spawn with
    random values of yaw, roll, and pitch, see this [video
    demonstration](https://www.youtube.com/watch?v=zJaSMwK0zO4) of that.
    It wasn’t until a day later that I’d discovered the right
    combination of values to assign the properties of the charging
    station object. Here’s a [video
    demonstration](https://www.youtube.com/watch?v=cgtDnoudIR8) of the
    working program.

-   Created an image of the software so that others could easily install
    the required environment without the troubles the team and I faced.

**Non-Technical Development** I played a pivotal role in the development
of the project as the Team Manager and Bitbucket expert. It was my job
to maintain the wiki as you can see I’ve done in the [wiki commit
history](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/history/Home.md?page=1).
I spend on average 3-5 hours per week converting meeting minutes into
markdown documents, uploading them and the pdf files, and fixing typos
and structural errors to ensure a higher quality of work. In addition to
this I created and maintained a Jira project which I linked to the main
repository to track commits and set issues for other team members. This
was integral to the organisation and time management of the project. As
the manager, I opened multiple slack text channels in order to
communicate prioritised information in its own channel, this way team
members could easily find the time and dates I set for team meetings and
other important information pertinent to project issues or development.
In summary, my role in the project was essential to the development of
the project as I provided structure and acted as the supervisor of
subtasks that were assigned to team members. I employed principles of XP
throughout the project thus far creating a backlog of tasks to be
completed within the week for each sprint and encouraged team
communication by setting meetings and performing regular check-ins with
team members.

Quality of Technical Work Completed {#quality-of-technical-work-completed .unnumbered}
===================================

Considering that only half of the semester has been completed, and the
early stages have not involved a great deal of programming, there hasn’t
been the need for testing in many areas. However, once the majority of
the team had the environment set up, team meetings were spent reviewing
code from online sources such as GitHub or communities for PX4 and
ArduPilot. We employed techniques of paired-programming via zoom to
generate a collective understanding of the basic code building blocks.
From this, we were able to build our own scripts using the pieces of
code we understood. The scripting, however, was not my area of focus and
thus was not tested by myself. Recently my focus has been on developing
a python script to add objects to Gazebo world files and procedurally
generate their locations. There has been little to no testing of this
program as it has only been recently developed into a beta stage. The
source code of this program can be viewed
[here](https://bitbucket.org/DylDupe/comp3888_t15a_group1/src/master/StationSpawner/randomize.py)
and as you can see it has structure and comments where necessary, but
will require re-factoring as the functions are becoming extensive, which
is not very pythonic or efficient. In summary, there has been little
technical work completed given the duration of the project up until now.
This has been due to unforeseen technical difficulties with installation
and tool setup. However, in recent weeks, technical development has
picked up and will continue to rapidly progress as the subtasks are
being completed at a much faster rate due to our increasing knowledge of
the software.

Other Contribution to Group Processes {#other-contribution-to-group-processes .unnumbered}
=====================================

As previously mentioned, I created a Jira project and linked it to the
project in order to link issues to commits which can be found
[here](https://bitbucket.org/DylDupe/comp3888_t15a_group1/jira?site=b95f0f0b-0d5c-4c02-9317-ac9d14f0d9b8&statuses=new&statuses=indeterminate&statuses=done&sort=-updated&page=1).
I assigned team members to work items from the backlog of each sprint
and as per the group contract, tried to create several tickets per week.
For further evidence of collaboration and teamwork, our slack channel
can be reviewed [here](comp3888t15agroup1.slack.com) where there is
currently over 1800 messages sent. On this slack channel it can be seen
that I, as the manager, have consistently been organising team meetings
and providing summaries of work items still be completed.

Reflection {#reflection .unnumbered}
==========

**Programming** The earlier stages of the project required little to no
programming as they were mainly concerned with setup of the environment
and basic usage of the tools which are all pre-written. When It came to
scripting for autonomous drone flight, using pre-written code from
various GitHub repositories and communities online was difficult as it
was often undocumented. Much time was spent just reading through
relevant documentation until common ground was found between all of the
code written by others online. From there, it was just a matter of
understanding the simple functions and putting them together to get
basic point-to-point navigation. If there was some more concrete
information as to how to get the simulator running and controlling it
with both PX4 and ArduPilot, that would have sped up the project
immensely. When it came to developing the program which randomised the
charging station location, I had to do a lot of heavy programming and
research into the relevant algorithms. There is a built-in function of
Gazebo to spawn *populations* of objects randomly within a given map,
but this was flawed at it didn’t take into consideration minimum
distance between objects, from the drone, or object collision. The main
reason I didn’t use this feature was because there was no way to
procedurally generate objects. That is, each charging station spawned
increases the area of possible locations for the next. This growth in
spawning area is essential to the project as it represents the maximum
distance the drone can travel as opposed to a single set radius which
cannot be pre-determined as the drone can be recharged. It would have
been nice if there was some room to adjust the population generation
feature of Gazebo or some more documentation on it at the least. If
future software projects could spend more time writing more specific
documentation, all other projects would greatly benefit from this.

**Version Control** Bitbucket was the version control system used. The
team relied on a repository I created and shared which began with
nothing. I found Bitbucket to be very simple to use and that it provided
a great amount of organisation. However, it would have been a nice
feature if we could link our Jira issues to specific commits and view a
timeline of these together. The Bitbucket can be found
[here](https://bitbucket.org/DylDupe/comp3888_t15a_group1/src/master/),
it includes the majority of the work I completed and documentation
written.

**XP** Many of the principles of XP were employed throughout
the lifespan of the project thus far as this project does lend itself to
them very well. My XP role as the manager was to organise the team and
encourage communication and collaboration. As XP emphasises teamwork, it
is my belief that we achieved synergy through constant communication,
SMART bite-sized goals and work items, weekly team meetings, and an open
environment to discuss issues and ask for feedback or help. However, an
improvement we could make is to document things as we go rather than in
chunks, when things are completed. I’d like to note that with the
generous help of the client, an inviting and honest environment was
created which motivated me to stay on tasks and not be afraid to ask for
help if I was unsure. The reinforcement of the clients needs in specific
detail for subtasks greatly improved the quality of work and I believe
went a long way in ensuring that the final product will be one of
satisfaction to the client.

**Challenges** Throughout the duration of the
project thus far, the challenges have been surmountable due to the help
of the client and online communities. The main challenges have been:

-   *Installing the tools and environment:* The early stages of the
    project was plagued with installation issues taking me weeks to put
    together a stable environment and gather knowledge on using it
    efficiently. It took a lot of trial and error, re-installations, and
    debugging source code to get some applications to work. However, by
    going through this early on, myself and other team members learnt a
    lot about the software and became familiarized with the online
    forums, learning where to look when there were issues.

-   *Lack of Documentation:* There was little documentation on SITL
    (Software In The Loop) simulation with PX4 and ArduPilot. While
    there was basic installation guides, there lacked any extensive
    documentation on usage but mainly troubleshooting. If there had been
    a more active online community with FAQs to refer to, I think this
    would have helped a lot. Much of the documentation that was
    available was also outdated, using python2 instead of python3. This
    was not a huge problem, but another hurdle to jump over certainly
    didn’t speed things up.

-   *Gaps in Knowledge:* This perhaps was the biggest and most
    frustrating problem. Not a single team member had any experience
    with drone simulation at this level and as a result, lacked any sort
    of idea as to how the software worked or the high-level ideas behind
    the design of these software and their relationships. For example,
    coming to understand the way PX4 and Gazebo worked together with
    QGroundControl or MissionPlanner was a big hurdle that took a few
    weeks to wrap my head around and came with experience.

**Improvements** Some areas that could be improved include
documentation; consistently documenting the work being completed at the
time of doing it. If this problem could be reduced, we would have more
time to spent on development rather than assigning chunks of time to
writing the documentation which has a higher change of being incomplete
as information tends to go missing the longer you leave it undocumented.
We plan on moving forward by keeping up-to-date on documentation through
giving it a higher priority from here on out. 

**Role as a Software Engineer** Besides reading through code repositories and debugging
source code, my role as a software engineer was displayed through
discussions with the client about requirements such as specific world
rendering for trees and buildings and whether a custom city was required
or if just a basic world and features would suffice. These discussions
occurred during sprints with the client. As previously mentioned, I had
the individual job of developing the charging station spawner from
scratch. This required my software development skills and agile
methodologies in order to produce a software that was functional and
efficient.