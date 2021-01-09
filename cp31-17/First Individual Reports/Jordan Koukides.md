460327798 - jkou3713

**JORDAN KOUKIDES - INDIVIDUAL REPORT I**



## **Statement of work**

Over the past 6 weeks, we have split our group in two sub-teams based on major work that was to be completed; the OpenCV team making a start on the algorithm and the Unity team building the simulator environment. Primarily I have worked as a member of the OpenCV team, however all team members have rotated XP roles as per our [group contract](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Group%20Contract). While week 2 was spent familiarising myself with the project and codebase, I rotated to the role of tracker in week 3; despite not having made many changes to the code as a group, I spent this time getting feedback from members on the code and the quality of the refactoring that we had done. In week 4, I began my role as a programmer and subsequently a tester in week 5. In week 6, the majority of my time was allocated towards the report (introduction and reflection sections), presentation (project background, stakeholders and demo). Additionally, I have also completed a rotation of taking the meeting minutes, which can be found [here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Minutes/Week04_Team).


## **Weekly plan**

| **Week** | **Work Intended** | **Work Completed** |
| --- | --- | --- |
| 1 | Group formation | Group formation |
| 2 | Project selection and delegation | Project selection and delegation |
3 | Initial client meeting, project familiarisation, refamiliarisation with python. Complete role as tracker. | Initial client meeting, project familiarisation, refamiliarisation with python and git. Got team feedback on code refactoring. |
| 4 | Get simulator running on local machine, make improvement to one of the signs. | Got simulator running locally, experimented with hues and contours for stop sign and turn sign, made slight improvement by using trackbar feature. |
| 5 | Train self driving model on track 2, implement canny edge detection for turn signs | Successfully trained self driving model, tried canny edge detection but didn&#39;t have much luck, did some research into Hough circles for turn signs |
| 6 | Work on report, presentation and project demo | Worked on report, presentation and project demo |



## **Extent and quality of work**

The majority of work I have completed over the past 6 weeks has been in understanding and experimenting with the sign detection aspects of the OpenCV code, in particular looking into Canny edge detection. Once we had refactored the clients code, fixed major bugs and made basic improvements on sign detection using traditional methods such as changing hues and contours, we ran into an issue detecting the turn sign as its background colour was a similar shade to the walls of the environment given by the client. Due to this, we researched more advanced methods of sign detection that were not dependant on identifying colours, this is where we came across Canny edge detection, which seemed promising for this application. I was delegated the role of looking into and experimenting with Canny edge detection to see if we could improve the code in respect to finding turn signs. [Here](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/branch/edge_detection_experimentation) is a link to my branch that was used for Canny experimentation. Although significant time was spend trialling this feature, I had hoped for an outcome that would have improved sign detection much more than it did. Due to this, I also looked into Hough Circles ([commit](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/41e1b4fb1e86e8d1761fdbd41d6c6a660df4c2d8?at=edge_detection_experimentation)), this was more promising and I expect to allocate more time to this feature in the second half of the semester. I have also found a research paper by Rong, Zhang and Sun (2014), that proposes an improvement to Canny detection when there is excessive noise present; I will also trial this in the coming weeks.

Although I expect that the majority of our code will be written in the second half of the semester now that we have our simulator up and running, there were still measures taken to ensure code quality. As a team, we have implemented code refactoring, pair programming and peer review before feature branches were merged. As we continue to make improvements to our code, I expect that more time will be spend in these areas, as well as writing more comprehensive testcases.



## **Other contribution to group processes**

I completed a rotation of taking the meeting minutes ([link](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Minutes/Week04_Team)) as well as been present in as many meetings as I could (we are currently meeting 4 times a week, 2 of these with the client). Further to this, I have also been an active voice on our communication channels Discord and Slack. For the group report, I contributed significantly to the introduction and reflection sections, and for the presentation, I completed the project background, stakeholders, and demo sections.



## **Reflection**

**Extreme programming**

We had 2 client meetings each which, which was good for XP as we could quickly iterate and deliver features of the product as the client needed them, rather than interpreting the brief ourselves and delivering a final product that was not what the client had in mind. Although we had slightly different coding styles to the client, we were able to overcome this challenge by refactoring the code early on. Also, since we had all used Git before, we were able to take advantage of version control in Bitbucket by created branches for new features and committing changes when they were made.

**Challenges**

For me, one of the biggest challenges was refamiliarizing myself with Python and Git, as well as learning how OpenCV worked as I had not touched computer vision before. However by putting time into learning this early on in the semester rather than jumping straight into the code, I feel like I have overcome this challenge.

Also, I found it challenging to dive into such a complex project with a team that I have only met under virtual circumstances. I find that getting to know each other is important for team dynamic, but having frequent meetings definitely alleviated this burden. Further to this, I found that we were attempting too many communication channels at the start of the semester, so it was easy for information to get lost. Realising this, we have since refined our channels to primarily Discord and Slack, as well as using Trello for task tracking.

Aside from these, there were small challenges in technical difficulties setting up some of the code and environments, but by working together as a team and with the help of the client, we were able to solve these quickly.

**My role as a software engineer**

As most of the work so far has been in familiarisation with the project and modelling of virtual environment, I expect my duties as a software engineer in the team to increase in the coming weeks as we push harder to improve our algorithm. To date, most of my time has been allocated to working with experimental features rather than more basic code improvements which have been made by the other team members working on OpenCV, however many of these have not increased the efficiency of our algorithm as much as I had hoped. I am also interested in opening my role to work more with the Unity environment, as this is a field that I do not have much experience in, but would like to explore more.

**Future improvements**

Overall, I am satisfied with our team&#39;s progress so far and am looking forward to progressing further in the second half of the semester. Despite this, I recognise that there are a few areas in which we can make improvements. Firstly, I think we should better use the issue tracking features of BitBucket, rather than just talking about issues informally in our Discord channels. Secondly, I believe that we can communicate better about the features we are working on individually in order to avoid doubling up and improve efficiency. Finally, I think it is important for us to continue rotating roles on a weekly basis, and potentially have more crossover of work between the Unity and OpenCV teams.

## **References**

W. Rong, Z. Li, W. Zhang and L. Sun, &quot;An improved Canny edge detection algorithm,&quot; _2014 IEEE International Conference on Mechatronics and Automation_, Tianjin, 2014, pp. 577-582, doi: 10.1109/ICMA.2014.6885761.