# Individual Report –

# Justin Lee

CP34 – OPTIMAL PATH FOR DRONE DELIVERY

### COMP3888 CAPSTONE PROJECT


## Table of Contents

- Role
- Contributions
- Other Contribution to Group Processes
- Quality of Technical Work Done
- Reflection
   - Programming
   - Version Control
   - Extreme Programming


## Role

For this project, I have been given the XP roles of programmer, tester and Doomsayer.

## Contributions

My contribution to the project can be broken down into two main parts, installation and configuration
of the simulation environment and developing an automated drone navigation script tailored to our
team’s needs.

The project began with the installation of the multiple drone simulators available for the team to choose
from and I was able to quickly set up and configure the simulation environments on my machine. Since
the other team members had trouble setting up the simulation environment, I was able to let my team
members see what the different simulators looked like and thus I helped the decision to use Gazebo
over jMavSim.

When the team members had trouble with installation, I also attempted to help by trying to install the
simulator in their environment (WSL, Ubuntu in VirtualBox) but also faced many obstacles. Ultimately,
the team decided to follow my setup (dual boot Ubuntu 18.04) as it was able to have all the required
tools installed correctly for the simulation environment.

During this time, I was also able to get a head start on my team members and start reading
documentation for both PX4 and ArduPilot flight control software and communicate to the team about
the basics and differences of these software.

I also did research on the several libraries available for automated drone navigation scripting and tested
them on the simulator. I started with the MAVSDK library, then moved onto DroneKit as it was the only
one that worked for both flight control software. I had to extensively research, test, trial and modify the
existing scripts in order to develop an automated drone script that works for both PX4 and ArduPilot as
they are coded differently for the two flight control software despite using the same library, and also
because the documentation was extremely scarce for PX4 and outdated for ArduPilot. See [Weekly
Update Video Week 4 & 5](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Videos).

I produced a short demo video briefly demonstrating how the automated drone script worked, as well
as a longer demo video that also acts as a tutorial with more in-depth details about how to use script so
that my team members can use it too. See [Mission Script Auto Navigation Demo 1 & 2](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Demos).

I also did testing on the automated drone script with several different input files containing varying
amount of way points and different length between each way point. See [testing](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Mission%20Script%20Testing).

I kept my communication lines open as well and tried to keep my team up to date on everything I’m
doing and letting them ask me any questions. I also attended almost all team meetings, missing out on
only one team meeting so far. See [Meeting Minutes](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/Minutes/Minutes).

## Other Contribution to Group Processes

As a programmer, I’ve been reading through the documentation for the flight control software and
automated drone script libraries and further relaying them to my team as well as answering any
questions they might have.

[User Stories](https://bitbucket.org/DylDupe/comp3888_t15a_group1/wiki/User%20Stories)

- Week 2 – Installation of simulator (as a team), user story #1, 2, 3
- Week 3 – Research and development of automated drone navigation, user story #4, 8
- Week 4 – Development of automated drone navigation, user story #8, 10
- Week 5 – Developing and Integrating automated drone navigation with optimal path delivery
    algorithm, user story #8, 10
- Week 6 – Testing and Report writing

In addition, I made sure that the code that I produced was readable, well-documented with comments
and docstring inside the code as well as providing a well-written readme file and necessary
demo/tutorial videos. See [Bitbucket Mission Script](https://bitbucket.org/DylDupe/comp3888_t15a_group1/src/master/MissionScript/)

## Quality of Technical Work Done

Pair programming was done when researching and testing existing scripts for developing an automated
drone script in order to have extra eyes on the modification of the existing code to ensure code quality.

Early testing of the automated drone script was conducted to ensure that it behaves correctly when
reading in input files with different way point configurations. Some edge test cases are omitted due to
the assumption that the optimal path algorithm would not have those sorts of output, however this
should be tested further in subsequent development cycles.

## Reflection

### Programming

The last team to work on this project did not complete much and our team had no foundation to build
on, leading to a lot of time spent researching on the software and tools that we were all unfamiliar with.

Developing with DroneKit was somewhat difficult as the documentations were incomplete or outdated
and there were no existing programs that are similar to something that the team needed. Hopefully this
shouldn’t hinder the project too much moving forward now that I’ve spent quite some time researching
and developing.

Pair programming did not seem to be very effective as the team members involved were all unfamiliar
with the DroneKit library and were unsure of how to proceed. This seem to be better suited for
development of code that the members are familiar with and just need extra pair of eyes to maintain
code quality. However, members involved in the pair programming were able to gain a better
understanding of DroneKit as a result.

### Version Control

Version control is managed through BitBucket and Git. All other team members have been following the
correct procedure of creating a separate branch for the feature they will implement, however I have not
been following that procedure. This is something I should improve on in subsequent development.

### Extreme Programming

It has been difficult to follow XP principles with our given project. The project is very open ended and
tends to leave a lot more freedom in development to the team as opposed to having the client list out
their specific requirements. This also resulted in our user stories taking a while until it can be explicitly
defined, and they tend to be quite broad and take a lot of time to complete. Furthermore, it is difficult
to do test-driven development when we don’t have a good idea of the product we’re developing.

In terms of the Doomsayer role, there was not much to do as the team will usually update progress and
forecast any obstacles together during team meetings.