# Individual Report - Jarod Reynolds

### XP roles and non-technical Contributions

I have been nominated as Bitbucket Expert, so I was responsible for creating the Bitbucket repository and I am still the repository administrator. I'm responsible for managing user access privileges and maintaining the structure and content of the repository.

I've also taken on the manager role during week 3 of the role rotations at the start of the project. During this time I was responsible for organising meetings and ensuring the correct process was followed at these meetings. I've since been responsible for keeping minutes and updating the wiki on several occasions. These minutes can be found [here](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/browse/minutes).

### Weekly Tasks
#### Week 2/3

Intended:

* Set up Bitbucket repo and add client
* Set up donkeycar simulator and unity
* Implement a Tensorflow model to detect a sign

In weeks 2 and 3 I created the [Bitbucket repository](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/src/master/) and added all team members and the client. I successfully installed the Unity hub and editor and completed the Karting Micrograme tutorial to introduce myself to some basic functionality of the Unity editor. I also worked with Calum to train a model using the Image Classification tutorial (listed in the Tutorials section of the [Tensorflow](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/Tensorflow) page of the wiki). Watch the [Video](https://youtu.be/FTm_QzsqFL0).


#### Week 4

Intended:

* Get donkey car simulator up and running with a trained driving model
* Get "parts" working in the simulator
* Run TensorFlow sign detection model in the siulator (gathering more data)

In week 4 I gathered training data for the driving model by spending some time driving the donkey car in the simulator. The data gathered was stored in "tubs" which I then used to train the autonomous driving model. The car was able to drive around the track without collision or leaving the bounds of the road for up to 10 minutes before I closed the simulation. See the video [here](https://youtu.be/gby9SQ68U1Y).

I also found and aided in the implementation of an object detection model on the TensorFlow Hub. The Object Detection tutorial (linked on the [Tensorflow](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/Tensorflow) wiki page). We used an "out-of-the-box" model to detect various objects in the frames captured by the car in the simulator. The model was trained using the COCO dataset, which contains 80 object labels including stop signs and traffic lights, and integrated with the donkeycar sign detector part. The model was able to identify other objects in the frame of one of the pre-loaded tracks in the simulator such as chairs, people and other cars. The frames with detected objects were initially saved to the local drive with bounding boxes and labels. See a video from Calum of the detector working on his machine [here](https://youtu.be/bTRXHhLhcH4).

#### Week 5

Intended:

* Integrate Tensorflow sign classifier as a donkeycar "part"
* Make the car perform an action in response to a turn / stop sign

In week 5 I assisted with adding a full-frame classifier inference into the simulator as a donkeycar part with mild success. The was able to correctly identify some signs, but has a very low accuracy when the signs appeared very small in the frame.

#### Week 6

Intended:

* Group report
* Group presentation
* Individual report

In week 6 the client instructed us to focus on the report and presentations. This week I took responsibility for the [minutes](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/browse/minutes) at each client/tutor meeting, as well as the additional meeting where we divided the report and presentation workload and assigned parts to everyone.

Asside from completing my allocated parts in the group tasks, and completing my own individual report, I am also responsible for the final formatting and submission of the group report. Additionally, I collected the team's individual pre-recorded videos and edited them together to form the group presentation.

### Code Quality

While this project largely focuses on technical aspects other than programming/written code, any code that has been completed has been written in pairs during a Zoom video call to ensure quality. This allows for live discussion regarding best approach, resource sharing and code review while the code is written.

Our models have also been tested externally to the simulator to ensure the models work as expected and are able to identify/classify images and objects before they are integrated into donkeycar parts within the simulation environment and tested again.

### Other contribution to group progress

I have attended every group meeting since the project began. These include weekly tutorials/check-in with the tutor, two client meetings every week as well as the post-client-meeting team debriefs. I have engaged with both the client and the tutor and discussed issues or asked questions where necessary.

I've also tried to remain responsive at all times on our main communication platform (Slack) to answer questions and participate in discussions/decision making.

### Reflections

#### Version Control

We are using git and Bitbucket for version control for both code files and for all the resources/notes in the wiki. We have all had some experience using git before, so we were able to quickly adjust to the Bitbucket environment. One slight challenge we are experiencing at the moment stems from the fact we are making changes and additions to multiple different repositories; donkeycar, gym-donkeycar and sdsandbox. In the recent weeks, we have been making changes to files from various subdirectories within all of these repositiories, but the client had initially advised us not to make our own fork, but rather add the artifacts we have modified from each repository to our own repo when we are committing to share with the team for now. This is enforcing a bottleneck on the merge process, as we need to manually replace the outdated files on our local machines after each new pull from the repo, however the client has recently advised that he is in the process of arranging a more suitable method for us.


#### Challenges

The project has not been without it's challenges thus far. Personally, I've had frequent issues with installing various libraries required for the machine learning models to run. I also needed to format and repartition my laptop's internal hard drive to allow more storage space for my dual-booted Ubuntu system. I was originally working in a small environment with lightweight tools for writing and compiling code, however the Unity editor and the simulator environment, as well as the predicted large machine learning datasets, required more space than was available.

The current global pandemic has also added challenges to the project, primarily related to group communication and XP practices such as pair programming. The inability to meet in person, especially when the majority of the group had never met, made initial introductions and getting to know the team challenging. Over time, we have become more accustomed to the online environment and are still engaging in pair programming and code reviews on video calls and group calls using the Zoom platform.

Processing power has started to become a challenge in the most recent week or two, as we are tryig to implement more complex machine learning models and neural nets. The high number of computations required to train these models is increasing and therefore so is the time required for training. Even with the GPUs configured on some of our machines (some unfortunately don't even have compatible GPUs at all), our limited processing power will be a significant bottleneck to our progress in the coming weeks. Fortunately, our client has advised that he is working on getting a server set up that we can access remotely to run these models, eliminating this problem.

#### Role as a software engineer

Due to the nature of this project, being that we are making alterations and additions to an already existing suite of software packages, both we as a group and I individually have not written as much code as many other projects would require. I have, however, spent a lot of time reading through the existing code from the various repositories to understand how modules integrate and how the system works as a whole, so I can identify specifically where our additions should be included.

In saying this, I have started developing my skills using the Tensorflow library and learning about AI in general, and have made contributions to the machine learning models that have been implemented so far in the project.


#### Moving forward

So far I think our team has worked well together. There's been open and constant communication whenever questions or problems have arisen, and we have supported each other when any issues, bugs or errors arise.

Moving forward, I think the entire team (myself included) should make better use of the wiki by making more frequent updates with any resources we find or progress we make, and in more detail. I wasn't completely aware of the importance of the wiki until reflection during the preparation for the first report and presentation, so in future I will aim to make better use of the wiki.

I will also use my initiative to actively make more first-hand contributions to the code for the detection models, rather than aiding as a secondary (code reviewer).