# Client Handover Document #

## CP-33 Object Detection for Simulated Drones ##

**Project Team**: COMP3988 T17B

## Project Description

Autonomous Vehicle Tech involves many different aspects of Software, Computer Vision, AI,
Hardware, Electrical, VR, AR, IoT, and embedded computing.
If you are interested in being prepared for industry jobs the best place to learn the methods is to get
involved and start experimenting with the technologies by seeking out where the most community
support and development is happening.
The goal of this project is for students to walk away with a serious understanding of Artificial
Intelligence (AI) technologies associated with autonomous vehicles, so they can develop and apply
them to real-world roles post university.
For this project we will be asking students to implement in a simulated world algorithms to detect
different objects.

---
## Showcase Video

[Showcase Video](https://youtu.be/8uX_xw7voME)


## Documents

- [Proposal Document](https://github.com/wallarug/capstone2020/blob/master/proposals/CP33%20-%20Project%20Proposal.pdf)
- [Requirements Document](https://github.com/wallarug/capstone2020/blob/master/requirements/CP33%20-%20Scope%20and%20Requirements%20Document%20September%202020.pdf)

## Code & Respository

- [Main repository](https://bitbucket.org/zson5784/comp3988_t17b_group_5/src)

- [Trainned model](https://drive.google.com/file/d/1DfsALY0DRb2BmYIAi34JECGLuODiurw8/view)

    * Unzip and place it in `objdetection/drone_controller`

The Following two repositories are submodules of the main repository

- [Mavsdk-Python with distance sensor](https://bitbucket.org/zson5784/mavsdk-python/src/master/)

    * distance-sensor: the branch with the distance sensor patch

- [Mavsdk with distance sensor](https://bitbucket.org/zson5784/mavsdk/src/master/)

    * distance_sensor_2: the branch with the distance sensor patch


---
## Team Members & Tasks

| Name           | Primary Email                                                   | Core Role(s) Tasks      |
|----------------|-----------------------------------------------------------------|-------------------------|
| Zhiyi Song     | [zson5784@uni.sydney.edu.au](mailto:zson5784@uni.sydney.edu.au) | Simulator, OpenCV, misc |
| Yexin Mao      | [ymao5456@uni.sydney.edu.au](mailto:ymao5456@uni.sydney.edu.au) |                         |
| Martin Chai    | [mcha3431@uni.sydney.edu.au](mailto:mcha3431@uni.sydney.edu.au) |                         |
| Boswell Lin    | [blin5895@uni.sydney.edu.au](mailto:blin5895@uni.sydney.edu.au) |                         |
| Steven Condell | [scon5713@uni.sydney.edu.au](mailto:scon5713@uni.sydney.edu.au) |                         |
| Gio Picones    | [gpic4558@uni.sydney.edu.au](mailto:gpic4558@uni.sydney.edu.au) |                         |

## Video Summaries

### Weekly Updates

| Week | Yexin Mao                               | Gio Picones                             | Zhiyi Song                              | Martin Chai                             | Boswell Lin                             | Steven Condell                          |
|------|-----------------------------------------|-----------------------------------------|-----------------------------------------|-----------------------------------------|-----------------------------------------|-----------------------------------------|
| 5    | [Youtube](https://youtu.be/9LmkGtMvqp4) | [Youtube](https://youtu.be/ZnC8gs_pmeo) | [Youtube](https://youtu.be/LvALBdcM4KA) | [Youtube](https://youtu.be/gUlybUtf4dc) | [Youtube](https://youtu.be/aJe-ol0gW8E) | [Youtube](https://youtu.be/VXcbDvt-E1E) |
| 6    | [Youtube](https://youtu.be/GfQQ_KQWgpc) | [Youtube](https://youtu.be/3u_x2S2db4g) | [Youtube](https://youtu.be/Ds3Da5b4x38) | [Youtube](https://youtu.be/7mbz_fBpZtE) | [Youtube](https://youtu.be/KRAACpgwimk) | [Youtube](https://youtu.be/0_dovm9ZXhs) |
| 7    | [Youtube](https://youtu.be/YWK3NEBWJIU) |                                         | [Youtube](https://youtu.be/G4K7YC4-7TI) | [Youtube](https://youtu.be/F0a8vUpRoJA) | [Youtube](https://youtu.be/rrdWy0aTnt8) | [Youtube](https://youtu.be/VwWV_oVrATk) |
| B    |                                         |                                         |                                         |                                         |                                         |                                         |
| 8    | [Youtube](https://youtu.be/2ZQExqvSmr4) |                                         | [Youtube](https://youtu.be/-aRFTL9uBds) | [Youtube](https://youtu.be/9Q_2LSw11GY) | [Youtube](https://youtu.be/rrdWy0aTnt8) | [Youtube](https://youtu.be/VwWV_oVrATk) |
| 9    | [Youtube](https://youtu.be/oPDPv9TJZ2g) |                                         |                                         |                                         |                                         |                                         |
| 10   |                                         |                                         |                                         |                                         |                                         |                                         |
| 11   |                                         |                                         | [Youtube](https://youtu.be/MTeDqtkY4a0) |                                         |                                         |                                         |
| 12   |                                         |                                         |                                         |                                         |                                         |                                         |

### Major Milestones

`feel free to add any additional videos into this table.  Include tutorials, workshops, demos, tips & trick`

| Description                 | Video                                                                                          |
|-----------------------------|------------------------------------------------------------------------------------------------|
| Client Deployment (Week 7)  | [YouTube](https://youtu.be/u9_upOwucOA)                                                        |
| Client Deployment (Week 12) | [YouTube Part 1](https://youtu.be/dDbUKxR0kYY), [YouTube Part 2](https://youtu.be/yrX_DVjtC0A) |

---

## Documentation

### For User ###
 - **Setup**: [Setting Up Environment](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/Setting%20Up%20Environment)
 - **Run**: [Start Simulation](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/Start%20Simulation)

### For Developer ###
 - [Setting up TensorFlow GPU](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/tensorflow_GPU_setup)
 - [Traffic Light Control Plugin](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/Traffic%20Light%20Control%20Plugin)
 - [Map of Traffic Signs/Lights for Simulator World](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/Map%20of%20Traffic%20Signs%20in%20World)
 - [Add Model](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/Add%20Models)
 - [Manual control](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/docs/Manual%20control)

### [The doc folder](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/browse/docs) ###

## Goal & Deliverables

- Simulated city built
- All traffic signs and traffic lights modelled in simulator
- Trees/plants and buildings modelled in simulator
- Customisable object placement possible
- Drone controllable with scripts, including rotation and turning
- Drone capable of capturing frames/video feed
- Sign detection functional on still images  for all traffic signs
- Sign detection functional on live feed from drone camera for all traffic signs


## Testing Results

`TODO @wallarug: insert table of testing for each project with link to data.`

[Training data in Google drive](https://drive.google.com/file/d/1ML9VLytO6mKn2PD4MrMmbY9HU3pJHhrL/view)

![v2_confmat.jpg](https://bitbucket.org/repo/jkq4oxG/images/3295969896-v2_confmat.jpg)

Class Dictionary

| Int Label | Label           |
|-----------|-----------------|
| 0         | noise           |
| 1         | parking-green   |
| 2         | speed-limit-10  |
| 3         | speed-limit-25  |
| 4         | speed-limit-40  |
| 5         | speed-limit-5   |
| 6         | speed-limit-50  |
| 7         | stop            |
| 8         | turn-left-blue  |
| 9         | turn-right-blue |



|           | noise | parking-green | speed-10 | speed-25 | speed-40 | speed-5 | speed-50 | stop  | turn-left-blue | turn-right-blue |
|-----------|-------|---------------|----------|----------|----------|---------|----------|-------|----------------|-----------------|
| Precision | 0.741 | 0.562         | 0.923    | 1.0      | 0.977    | 0.979   | 0.721    | 0.485 | 0.01           | 0.085           |
| Recall    | 0.298 | 1.0           | 0.619    | 0.976    | 0.972    | 0.404   | 0.982    | 0.408 | 0.02           | 0.086           |
| F1 Score  | 0.425 | 0.72          | 0.741    | 0.988    | 0.975    | 0.571   | 0.831    | 0.443 | 0.014          | 0.086           |
