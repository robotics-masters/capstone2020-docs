# Contributions:

Similarly to week 1-6, from 7-12, all members took on the role of developer and tester while
members of the group took turns rotating the other XP roles. In week 11, I took on the role of
tracker and recorded minutes for the team meeting, and submitted weekly reports to Canvas weeks
7, 8.

Evidence: https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Minutes/Landing

In regards to our weekly plan vs. what I actually did, I achieved the allocated tasks, especially since
the nature of our project had milestones such as “Improve sign detection” rather than a finished
product goal. As such, most of the work from a week to week basis was refinement and
improvements on existing detection, with the exception of adding and implementing sign responses,
which were implemented in week 10. The following section will go into detail of the specific
technical work done, with evidence.

## OpenCV:

My programming contributions came mainly in the form of coding sign detection and response with
OpenCV. Throughout weeks 7-12, we were mainly tasked with improving and refining our sign
detection from weeks 1-6 to better work in our simulator, which was changing due to the changing
scope requirements from our client, as well as a software upgrade mid-project, in which we changed
from DonkeyCar version 3 to DonkeyCar 4.0 and eventually DonkeyCar 4.0.1. This actually
required us to make changes in some files, reinstall and even troubleshoot directly with the
DonkeyCar developer.

In weeks 7, I pair-programmed and worked on my code to try and reduce false positive detection for
the turn sign detection I worked on before the middle of semester break. Unfortunately, the exact
commit on Bitbucket cannot be found because we deleted many of the experimental work branches
due to reaching the 2GB repository limit on Bitbucket.
Evidence of pair programming work done: https://gyazo.com/
740c1525d9672cc6861d808e1eed501c
Evidence of sharing my progress with the team: https://gyazo.com/
1c3a8139db5c849036179fd3c7fa

In week 8 and 9, I added further refinements and tested it in the new environments our simulator
team made. Further more, in week 9, I pair-programmed with a group member to clean up the
Bitbucket, as we had many different branches; testing sign detection was very experimental in
nature, and a lot of trial and error, so we made multiple experimental branches to share work. Our
Bitbucket was reaching the repository limit of 2GB, so we had a planned pair-programming meet up
to cleanly merge our code from various experimental branches. Again, unfortunately we do not
have evidence of the branches that we worked on previously because we deleted them, and at the
time, did not have the foresight to save evidence for the report. As such, after deleting many of the


branches due to a space issue, I continued some work locally and shared progress/results and ideas
with my team.
Evidence of sharing my progress with team: https://gyazo.com/
ab2b8b6f2fc1f90e866e2d2ea8dc017e

In Week 10, I implemented the pair programmed and worked on again improving the current turn
sign detection, helping with the circle sign, as well as implementing the turn response.
Evidence: https://gyazo.com/780123a1603d327658a2b9e0700e2a0c
Since we were at this point working on the main branch, the evidence for these commits remain on
the Bitbucket: https://gyazo.com/8482b9566b22409a346d540a09a

The last bit of coding work I did was in week 11, where we were preparing for the final demo and
deployment. In this week, I worked on cleaning up the code and making it more readable for the
client upon deployment. Here is evidence of my commit: https://gyazo.com/
9fdab23d0a9d1a7f12a4fba5304bfff

## Demo:

For my work on the demo, I wrote and recorded the section for group processes, in which I
described what tools we used for collaboration, how we utilised XP in our work, and our systematic
work/issue creations. I documented how we ran our team meetings in regards to planning and task
allocation, and client communication.
Evidence: https://gyazo.com/1e48a25a67f6f10fd0467dfac0a912e

## Showreel Video:

For our final deployment, our client requested a showreel to summarise and showcase our car’s
capabilities as well as show the progress throughout the course of the project. I provided 2 videos
for our team to choose from to present as our final deployment showreel.
Evidence: https://gyazo.com/b58f64fd92b6ff53eda037a0c951c
https://gyazo.com/315ae9b2bf25ac371c7bdae5a6be59c

## Quality of Work Done:

To ensure that we had good code quality, we utilised many good practices and standard measures,
such as frequent pair programming, constant testing, and recording minutes for any activities.
Evidence for minutes: https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Minutes/
Landing
Evidence for frequent pair programming: https://gyazo.com/46beb5130080d617b43ae86da1700d7c
Evidence of code review and refactoring: https://gyazo.com/646596b594217cf034729ec59840dea5,
note the timestamp discrepancy is due to the different timezone’s we live in.

Computer science discipline knowledge also helped us in this project. One notable practice we did
well was testing, in which we were able to create a very elaborate test code which could help us test
our detection in a fast manner while collecting data on detection rates (false positive/negative,


correct positive/negative etc...). Through this, we were able to do unit tests, and extensive white
box testing. This was particularly helpful in this project since the aim of the project was to develop
and improve sign detection without the use of AI. Therefore, our project resulted in a lot of trial and
error work with testing our detection, and creating a good method of testing was extremely
beneficial. Examples : https://gyazo.com/8aef5fd649b364a9c2d9d904d7ad98c6,
https://gyazo.com/be21b4d9b5b3cfad407c26e45bf

One particular challenge that wasn’t necessarily an individual’s work was the fact that we had to
change our working system during the project, as our client wanted us to upgrade from Donkey
version 3 to Donkey 4.0. This caused a lot of issues in getting our code to work, as we needed to
update to the new software, reinstall it to work (even though the new version was buggy and not
truly compatible with every OS) and refactor our code to work well with it. Even then, through our
client, we set up a meeting with the Donkey developer to help troubleshoot Donkey 4.0. Here is an
example of trying to help another member getting the new update to work on his computer: https://
gyazo.com/0cf30a5e101d2807793e97e75266083b
In pair programming, if my partner had poor detection results, we would work together to test
solutions, and specific ranges to try, share a same data set to test on and troubleshoot it together. As
a team, we were all receptive to feedback and criticism, following XP guidelines, sharing feedback
and showing the courage to share our progress even if not as good as we expected. Here is evidence
of me and a teammate in a call together, and i share with him a data set of images we can use, a
suggested range for our colour mask, and suggest HSV ranges to try troubleshooting with:
https://gyazo.com/0483cd08a527efb91ff77801989c

## Group Processes:

As a group, we met up twice a week, and once with the client, and once again for the tutorial. After
each meeting with the client, we would have another mini-meeting after, to decide new tasks or
changes to our goals based on client feedback and requirement changes. We took turns for tracker
and manager. All meetings had minutes taken and evidence of meetings + weekly progress/tracker
work can be seen on our Bitbucket wiki.
Evidence to all meetings: https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/
Minutes/Landing

Our team frequently pair programmed and collaborated, here is evidence to my individual
contributions to pair programming and collaboration.
Evidence to collaboration and pair programming: https://gyazo.com/
1a401532e403b45a49bbbafef69c
https://gyazo.com/e0403f6b9a8af1aa3ee112b0e25673af
https://gyazo.com/705ab72eec63dafe3c493dc469b
https://gyazo.com/fde73f4626b364f9cbc69ab4dfff676b

Our team used the Bitbucket integrated Trello to plan and allocate tasks. Here are my individual
contributions on Trello.


Evidence to work done on Trello: https://gyazo.com/361e320ad7c5d15d070f2138822f086d
https://gyazo.com/c0a15621c36da628c4e8f9854528d
https://gyazo.com/272577ca8d7128b4406262623d

## Reflection:

Our group managed version control quite well. Due to the nature of our project and milestones, we
experimented with different approaches for sign detection and tried to improve on the ones we
found success with. As such, we ended up using different branches for different computer vision
approaches (such as binary masking, colour masking, edge detection etc...). This worked well,
however, our group ran into trouble due to BitBucket’s 2GB limit, since we also required to create a
simulator to run our car in, which took up a lot of space in the repository. When we hit this limit, it
became impossible to continue with multiple experimental sign detection branches, and we had a
pair programming session where we reviewed the code, cleaned it up and merged our best method
for each sign to the master branch. Unfortunately, due to this space constraint, subsequent work was
also done on the master branch without great version control, however, it was near the end of the
project so it didn’t end up being too consequential. In a professional setting, we likely would not
run into this program since we would have a fully licensed Bitbucket with a larger repository.

For coding styles, we managed and agreed on a lot of our differences in the first half, such as agreed
good variable names, comments and 4 space indents. In the second half of the semester, we did not
have too many problems with this, and the code was easy for one another to read and work on.

Our group used XP since the beginning, and it was rewarding to follow the XP guidelines.Although
we rotated some roles such as tracker for the sake of learning, the practice of having a tracker/
doomsayer/manager, recording minutes every meeting helped us gauge our progress and give
proper feedback to ourselves, in order to set and create meaningful tasks and issues. In turn, this
made following the principles easier; we created meaningful tasks on Trello, and we could
guarantee that by allocating those tasks, we would be finishing what we need to be done, and
nothing more. Since we adopted extreme programming as our work methodology, we had a
systematic approach to working on the project. We had minimum 2 weekly team meetings since the
start. We used these meetings to discuss our progress and to create new tasks/sprints. Additionally,
upon planning new tasks, we would also plan times for specific task group work, like pair
programming. In between days of meetings, we communicated using Discord to share progress and
receive feedback from one another. We also aimed to have workable/showable products each week
to get client feedback. Even if we didn’t make the progress we aimed for, we showed courage in
sharing our individual progress and sharing our problems faced. All members showed respect for
one another, and each member was valued.

My role in the group from weeks 7-12 was a standard programmer and tester. I did not handle too
much work with client emails/communication. At times it was difficult for me to take the role of the
tracker since the client meetings were usually held around 4am for me (since I live in the Eastern
Standard Timezone). I mostly worked on developing the code required to achieve the milestones,
working with others, and extensively testing the code that we had.


The final project was delivered above our expectations, especially considering the road blocks we
faced. In particular the major roadblocks I feel we faced were the software change mid-project in
regards to upgrading our Donkey version, and working around my different timezone. Our team
tackled each of these problems well. For the Donkey upgrade, we had one member of our team get
in contact with the Donkey developer, and troubleshoot our issues. We were then able to all learn
how to fix and change our Donkey-related issues. The team was very accomodating to my
timezone, since the group meetings in week 1-6 were all planned in the Australian morning, but it
was still difficult for me to attend the client meetings, because of a less flexible time slot. As such, a
team member would often relay updates to me right after the client meeting, for me to catch up on
when I woke up. My reflection feedback for the first report mentioned that I could improve on
pushing more proactively to the branch and working less locally, and sharing my thoughts and
progress more. I believe that I improved on that greatly in the second half, as I pushed a lot of
experimental sign detection approaches to the Bitbucket, which resulted in me getting more
feedback from my group members. Evidence: https://gyazo.com/
a7716221bc2e65dd5a72142bbbafcd

As for further improvements, I think I would greatly benefit from more pair programming, as I
could receive instant feedback and ideas.

I believe the team greatly improved from the first half, as the main factors for improvement
included more Bitbucket commits and uses, and more promptness for team meetings, which were
achieved in the second half. Links to previous individual reports for said improvements: https://
bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/First%20Individual%20Reports/
Landing
Our team also took weekly feedback from the client and tried to change to our client’s needs, for
example when we changed to Donkey 4.0.

## Writing and wiki use quality:

The wiki was a joint effort from all members of the team. Each member has contributed a
substantial amount to making and adding to it. The wiki uses an organised, simple structure to
ensure ease of use for any member or client navigating through it.

## https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Home