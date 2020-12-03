# Individual Report

## Clear statement of work done
the work done including the technical work and non-technical ones which are all listed below.

### Technical work
- Add some helper functions (Harris detection for determine the signs shape and color ratio check for determine the green background in parking sign) to improve the simulator detections of green parking sign codes. [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/4cde801aef24b300d23382df13c34d89ae2bcb09)
- update the color filter of green parking code to fit with the new resolutions in simulator. [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/0c7805a0c08e737c3d890235844397e863dc3a40)
-	add the detection code for yellow park sign in simulator. [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/41bbefa661fb33ed08183d8b0e75f3e7b02229b5)
-	update the different variables between the real world and simulator cases and add the functions that can roughly estimate the running environments (SIM or REAL) which will be useful in the further working on my detection code. [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/d1f25092cef5e170669952035e177a908ddc4027)
-	add more white color ratio check in the interesting area which can estimate the letter ‘P’ inside the parking sign, and it improves the green park code accuracy a lot in real world data. (in previous code, data1, data2 real world accuracy: 0.53 and 0.65, now: 0.84 and 0.87). [result](https://drive.google.com/file/d/1Jdaa1LzptfyHHvg0CerkIoNv6aULIycI/view?usp=sharing), [issue #17](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues/17/find-a-solution-for-detecting-park-signs), [Pull request](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/28), [video sim](https://youtu.be/0jxJcv1f2yI), [video real](https://youtu.be/P3REYoA8GQc).
-	Fixing some false detections of yellow park sign, build approximately 175 frames video for testing that (success 161 frames). [issue #23](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues/23/add-detection-code-for-yellow-park),[Pull request](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/37), [video sim](https://youtu.be/p3WurbsrMDk)
-	Adjust the color filter of traffic cone, add some helper functions to check the trigonal shape and color ratio of traffic cone. [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/46ca1174df9c79b9220884346c4e26e6a6544605)
-	Add the detection code for traffic cone in simulator, [issue #33](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues/33/add-detection-code-for-traffic-cones-in), [Pull request](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/37), [video sim](https://youtu.be/G_H5xE59flE)
-	Reviewed other members pull request. [Evidence](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/?state=MERGED)

### Quality of technical work done and Challenges

The work I have done during week 7-13 is mainly for writing the detection codes and debugging them. to convince myself in debugging section, there are multiple helper functions which each one will have its unique operation. Thus, when some issues occur, I can test them individually and get ideas about how to fix that. The pull requests are reviewed by other group members before merging. [Evidence](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/pull-requests/28), and from the result of testing framework, [result](https://drive.google.com/file/d/1Jdaa1LzptfyHHvg0CerkIoNv6aULIycI/view?usp=sharing), the code have made some improvements in detection accuracies. 

Considering the algorisms, in the helper functions(bgr_check, ratio_check, harris_check), I try to iterate though certain regions of the image instead of the whole images which will reduce a bit space complexity, also, there are some NumPy slicing works made in order to reduce little operation time. Here are the related commit and evidence: [Commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/b901b288fdf5f448db829f29b8977bfbe9423585), [Evidence](https://stackoverflow.com/questions/993984/what-are-the-advantages-of-numpy-over-regular-python-lists#:~:text=NumPy%27s%20arrays%20are%20more%20compact%20than%20Python%20lists,and%20writing%20items%20is%20also%20faster%20with%20NumPy.)

For the technical challenges, at the start, I’m unfamiliar with the donkey simulator works and it cost me a lot of time to install it and I have issues when running my detection code in that, after getting some helps from Keenan, the issues are fixed and I got more and more familiar with the simulator operations on the detection. [Evidence 1](https://drive.google.com/file/d/18mPMS7uGYj_mWILx9Kmz6eTWdGXChMmw/view?usp=sharing), [Evidence 2](https://drive.google.com/file/d/1ukSpWw9VWvrrvIpGQxInZnV2lG8Ai-mC/view?usp=sharing). 

Another challenge I met was the different version of my OpenCV library with the simulator code and different operating system I use compare with the other group members, it may lead some grammar difference in the code, I tried some research onto that and edit my code to fit with the different versions thus there won’t be any conflictions occurs. [Evidence](https://stackoverflow.com/questions/48291581/how-to-use-cv2-findcontours-in-different-opencv-versions)

### Non-technical work and group contributions
-	Do some research studies on OpenCV stuffs including Harris detection, NumPy slicing and Contour properties. [Reference 1](https://docs.opencv.org/3.0-beta/doc/py_tutorials/py_feature2d/py_features_harris/py_features_harris.html?highlight=harris), [Reference 2](https://numpy.org/devdocs/user/quickstart.html), [Reference 3](https://docs.opencv.org/3.0-beta/doc/py_tutorials/py_imgproc/py_contours/py_contour_properties/py_contour_properties.html?highlight=mask)
-	Reading the user stories carefully and create the related issue for achieving the certain user stories. [User story #5, #6, #12](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/User stories), [issue #6](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues/6/refined-working-solution-of-provided-code), [issue #17](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues/17/find-a-solution-for-detecting-park-signs)
-	Reading the instructions of donkey car simulator stuffs and make that running in my personal computer. [simulator](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/docs/Running the software)

## Extent the work each week
The detailed evidence can be found above

**Week 7:**

- download and run the latest simulator on my computer with Keenan's help
- improve the park code for the simulator work. (changes color filter a bit, fix some mistakes i've made in color check functions)

**Week 8:**

- improving the park code for the new light
- put the code into simulator work

**week 9:**

- add yellow park code in simulator
- add two more ratio check for letter 'P' in green park code

**Week 10:**

- add the function that roughly guess the running environment (in simulator or real)
- improve the greenpark detection for real word data

**Week 11:**

- fix some false detections in yellow park code
- add traffic cone detection in simulator

**week 12-13:**

- bug fixing on parking codes

## Reflection
**Version control:** as the major stuffs I have done during week 7-13 are adding the detections codes. There are only two branches from my side, the Greenpark_sim and new_park_fix, where the Greenpark_sim I update the detection code of greenpark and yellowpar, and the new_park_fix are used for debugging and add traffic cone detection code. These branches are keep updating with the master, I deleted some old branches and transferring their stuffs into the current branches because it seems much easier for keep following the master in the current branches. And that also convenient myself for reviewing the codes.

**Coding style:** all of my codes are functions based, which was easy for testing and find the issues, also, there are some comments inside to explain the aim of certain operations. During the review sections, it may convenient team members for testing.

**Extreme programming:** during the first 6 weeks, my XP roles keep rotating, I have the chance to experience the different roles through the team, and try some stuffs related, which seems pretty interesting. During the week 7-12, my XP roles is the tester, I find out some issues in my functions and add some debugging stuffs into that. 

### role in the group and as a software engineer/computer scientist
as a software engineer, I mainly focus on OpenCV stuffs of writing the detection codes for the green-parking signs. I tried some image methods to reduce the false detections and build that into the simulator functions which will improve the accuracy of parking detections a bit in simulator. And in order to reducing some time complexity of running green park code in simulator there are some algorisms mentioned in Quality of technical work done and Challenges above designed. 

### Project work
The tasks for this project mainly divided into the categories: OpenCv detection code and Simulation Improvements/Implementation. During the W1-W6, the 4 group members are focus on the building the tracks and signs models, and 2 are working on the OpenCV code. The tasks all take great progress. But it seems that the OpenCV stuffs need more people to work on. So, during W7-W13, the group are mainly focus on the OpenCV codes, it helps a lot on coding progress as we share the ideas within the group and can deal with some problems together by discussion, pair programming or code reviewing parts. [Evidence](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/browse/)