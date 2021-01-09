# Traffic Sign Detection With TensorFlow

## Manfred Ai - Individual Report 1

**Tutor:** Abdallah Lakhdari

**Client:** Cian Byrne (Robotic Masters)


# Contributions/Tasks

The initial roles for week 2, 3 and 4 were assigned in the [Group Contract](https://bytebucket.org/jarodreynolds/comp3888_t15a_group4/wiki/Group%20Contract.pdf. The roles I took and tasks I completed are summarised below.

| Task | Week | Additional Notes |
|------|----------|------------------|
| Sign group contract | 2 | None |
| Write up minutes on 2020-09-08 (as designated tracker) | 3 | [Minutes-Tutorial-Week-3](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/minutes/Meeting-Minutes-2020-09-08.docx) |
| Complete group status report in week 3 | 3 | After I sent the report on slack, Calum helped submit it online. [Group-Status-Report-Week-3](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/progress_status_reports/Week%203%20Project%20Status%20Report.docx) |
| Get donkeycar simulator running on PC | 3 | In this week, concluding the XP-role rotations, I stepped back into a managerial role in addition to making technical contributions in a programming capacity. This managerial role took the form of leading task creation and delegation during our weekly meetings through the Trello task management system which we have used exclusively (evidenced later in the report). |
| Model new tracks into donkeycar simulator | 3 | None |
| Try NN driving in new tracks | 4 | NN model was created through training in the simulator, initially controlling the car manually. Once created, this could be run in the donkeycar engine. The video demonstrating completion is available in #weekly-videos |
| Tensorflow tutorial | 4 | None |
| Write User Stories in the Wiki | 5 | Wrote up a preliminary User Story regarding Stop Sign detection, which was expanded on and added into the group report. | 


## Modelling new tracks into donkeycar simulator

The task to model new tracks into the donkeycar simulator was assigned to Ben and I. The goal was to be able to build assigned tracks in Unity in order to simulate them in the donkeycar simulator. To add a track, a new scene had to be added in Unity. In order to learn how to use Unity, I took advantage of resources our client posted in the #resources channel and additionally researched online. We were struggling with this, until I copied an existing track and fiddled around with its contents. Ben created the necessary prefabs and pasted them onto the new created 'scene'. Both tracks were created in this fashion, and buttons were added to the menu. Once this was done, an executable was built in Unity, which could then be run in the simulator. Once these were able to be run in the simulator, Ben wrote up documentation on usage, and everybody was able to follow. An example of a track implemented (updated with signs now) is [Track 2](,,.images/track2_signed).

## Training a Self-Driving Car

A task which was assigned to all group members was to familiarise ourselves with the simulator and train a neural network model capable of driving on a track. Given that I was familiar with the simulator and tracks already, this was more simple, and the model simply had to be created for track 1. The video is available at [Trained Neural Network donkeycar](https://youtu.be/5F5hRLIS6aM).

## Group Report

In the group report, I was in charge of writing the sections on executive summary, Information Search, and Research. These were mainly based on slack chats and resources found by group members or the client.

### User Stories

User stories were implemented directly at the [User Stories Wiki](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/User%20Stories). I initially drafted a User Story regarding stop signs, which was expanded upon and added into the report.

### Meeting Minutes

I was responsible for meeting minutes during the tutorial in week 3.

# Work Quality

This project requires a higher level of collaboration and group understanding than other projects. As such, we have consistently attended meetings with the client to review progress/work, and receive feedback from the client. Given that we mostly received two different type of tasks each week, we decided to split up and tackle tasks in a pair/small group each time. Ben and I were able to work ideas off of each other to model new tracks in the simulator.

Each time an individual finished a task, they would share information and documentation with the group, and essentially other group members would validate the tasks, such as when assisting each other in setting up Unity or training a neural network. Furthermore, we shared videos in the #weekly-videos chat to show to the client. This additionally had the effect of providing information about a task for other group members.

# Reflections

Currently, I believe our team has progressed effectively and met the requirements set by the client. We have communicated well through slack which has ensured that no team members are left confused or behind. Programming technicalities have not been difficult, given that the team are all well-versed. With our wide knowledge base and understanding, anytime somebody requires assistance, other group members have stepped up and given appropriate advice. 

We have been extensively using Bitbucket for our version control for code and notes. Due to all of us being somewhat familiar with Git, this was not a difficult transition. However, there have been several difficulties with different environments, such as donkeycar and sdsandbox. This is because we have to manually replace files in the specific folders each time a group member has made an update. Although this is not difficult, it is not as automated as it could be, though it has not posed any issues for myself.

Personally, I have attended most of the meetings that we have, but have been late to a few, due to other commitments. However, for the latter half of the semester, I endeavour to attend every meeting (that I'm able to) on time, so that everybody is on the same page. However, I have noticed that the minutes written for each meeting have been helpful to catch up. I will also aim to contribute more to the programming side of things in this project if possible.

The main difference between this project and other groupwork previously is that we all have been communicating via video call on Zoom, rather than in person face to face. I believe this was difficult in the beginning, but has more recently been easier to adjust.