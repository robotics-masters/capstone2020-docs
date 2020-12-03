# 3988 final individual

# Final Individual Report

## Individual Information

**Unikey:** hlan3540

**SID:** 480399375

**Group name:** COMP3988_T17B_Group1

**Client name:** Cian from Robotics Master

 

## Clear Statement of Work Done

- **Statement of XP roles and other responsibilities and contributions**

Evidence in this section can be found later in the report.

From week 6 to 13, we did not perform any role rotation in our group because according to the requirements, a group member has to undertake either manager or tracker at least once.

From week 1 to 5, I have undertaken customer contact point and tracker. Evidence can be found in my [first individual report](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/individual_report1_hao).

From week 6 to 13, I have undertaken the tracker, tester, customer contact point and programmer role.

1. **Tracker:** I am responsible for tracking the progress of the team. Notifying relevant deadlines and keep the progress of the development team on track. I noted down the progress, tasks, deliverables of the team each week on weekly status reports.

2. **Tester:** I am responsible for setting up automatic testing framework using a continuous integration/development tool on Bitbucket.

3. **Customer contact point:** I communicate with the client during group meeting as well as on Discord chat channel about my progress as a programmer, when developing random generator of training images.

4. **Programmer**: Following the requirement of the client and the incentive to develop a more efficient method to collect training images, I developed a generator of training images with random noise as background.

5. **Data classifier:** I have manually classified 30,000 images for training the sign detection model on the first two tracks.

6. **Git master:** I follow the convention and guide to actively asking our group member to develop in branches.
 I also integrate CI/CD tools into our repository.

- **Weekly plan**

Week 1 to 5 plans can be found in my [first individual report](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/individual_report1_hao).

| ****        | **Plan**                                                                                                                          | **Work done**                                                                                                                                                                                                                                                                                                                                             |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Week 6**  | 1. Submit reports and presentation 2. Read through Unity guide                                                                 | 1. Submit individual \ group reports. 2. Submit presentation video and scripts 3. Submit weekly status report 4. Read through Unity guide, prepare to help the Unity team                                                                                                                                                                        |
| **Week 7**  | 1. Prepare to transit to the Unity team                                                                                           | 1. Unity team does not need more members. Transit to the algorithm team instead. 2. Submit weekly status report. 3. Manually classify 30,000 images used for training the model.                                                                                                                                                                    |
| **Week 8**  | 1. Look for a method to efficiently collect/produce training images                                                               | 1. Submit a status report 2. Start building a prototype to generate image that has background with random noisy pixels.                                                                                                                                                                                                                                |
| **Week 9**  | 1. Get the image generator into production use                                                                                    | 1. Submit a status report 2. Successfully generate 1,000 images of stop and green parking signs with random backgrounds and submit them into the training database (Google Drive)                                                                                                                                                                      |
| **Week 10** | 1. Start looking for information on how to set up a continuous integration/development tool and integrate it into our repository. | 1. Submit a status report 2. Prepare to use Pipeline as our CI tool because the integration will be much easier than other tools.                                                                                                                                                                                                                      |
| **Week 11** | 1. Keep setting up and integrating Pipeline.                                                                                      | 1. Submit a status report 2. Pipeline is almost completed. Now just need to find a way to configure the running environment for our project on Pipeline.                                                                                                                                                                                               |
| **Week 12** | 1. Get the first automatic build running and keep improving Pipeline                                                              | 1. Submit a status report 2. Create a dependency requirement file to download dependency packages automatically 3. Running environment (dependency) will now be loaded automatically before each automatic test. Automatic build trigger when ever there is a push to the repository. Test cases written in PyTest are integrated into the project. |
| **Week 13** | 1. Clean up Wiki 2. Prepare for presentation and Q&A session.                                                                  | 1. Writing individual/group reports 2. Clean up Wiki 3. Complete presentation 4. Project wrap-up.                                                                                                                                                                                                                                                |

**A detailed list of work done can be found** [**on Wiki**](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Hao) **(including weekly summary video).**
 

## Extend of that work
**Work done as:**
**Tracker:**

A collection of all weekly status report has been submitted on Canvas as well as documented on Wiki, which can be found [here](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home), under the heading **Weekly Status Report**

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304022755_image.png)


(Weekly status report on Wiki)

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304030591_image.png)


(I also converted Microsoft word to Markdown file and upload them onto Wiki)

**Tester**

Set up a CI tool to automatically build and test the project when where is a commit pushed to the repository.
Link to the [Pipeline](https://bitbucket.org/RobertJia/comp3988_t17b_group1/addon/pipelines/home)

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304047522_image.png)


(The very first builds during my configuration of Pipeline)

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304056465_image.png)


(After many failed builds (try-and-error), Pipeline was setup successfully.
There is also [a script](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/bitbucket-pipelines.yml) that dictates what consists of an automatic build that I wrote.

**Customer contact point:**

Since our client prefers to use Discord where everyone is free to talk to the client, basically every one in the team can be considered as a “customer contact point”
Unfortunately, all communications is done during client meetings and there isn’t much evidence available.

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304066932_image.png)


(An earlier chat with the client when setting up the training environment)

**Programmer**:

This part is about the random background image generator. The purpose was to overcome the difficulty to collect training images that are highly distinct to each other.
A list of commits made during the development of this feature can be [found here](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/branch/random_background_image) under the branch random_background_image.

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304074260_image.png)


（The commits that are part of this feature）

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304081356_image.png)


(An original sign image and a sample result)

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304089967_image.png)


(The generator can create lots of random training images in a short time)
The sign in the image is resized randomly in each training image. The location of the sign is also randomized. The background consists of randomly generated pixels of different color (RGB values).

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304093644_image.png)


(Green parking signs and stop signs were uploaded and used as training data)

**Data classifier:**

Manually classify 30,000 training iamges.

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304103225_image.png)


(Images before classification)
Images are collected in the simulator using the on-board camera of the car model.

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304111863_image.png)


(Images are classified into 15 classes (there are two empty classes))

**Git master**

Part of this role is to configure the continuous integration tool. The other part is to ensure developers follow correct convention when using Git. For example, developments should be done on branches instead of the master branch.

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304119773_image.png)

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304126681_image.png)

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304130752_image.png)


(Group members developed their features on a branch and then merge into master)
 

## Quality of technical work done
- **A summary of the measures taken to ensure code and work quality in the context of individual's roles including technical development**

The coding part of my work is relatively limited in code size (more in reading documentations or browsing the Internet for possible solution, e.g. Understand how an image is represented in computer; how does the alpha channel of an image work; how to overlay one image over another).
I did simple testing and refactoring for my random image generator code. The following commits can be found [here](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/branch/random_background_image).

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304135369_image.png)


 
The file I am referring to can be found [here](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/5ef7d09ada7f4dcd763631f1d18e241c065be4e1#chg-random_background_image/random_background.py).
 
You can see from the commit messages, that initially I didn’t modularize my code; and the filename (arguments of the program) was input by changing it directly in the code. This is bad from the user’s perspective. So later, in order to make configuration of the program easier, I refactor the program so that it takes command line arguments as the input.

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304139483_image.png)


(As you can see, initially the argument was hardcoded into the program, now it is read from command line arguments)
 
Another refactoring I did was to modularize the program. Initially the program did not have a function. All logic is executed from the top of the file to the bottom. This is not good to collaborate with other (because other developers might need to import my function into their program). So I modularized the program and add a main function(which will not be executed if the module is being input) to it.

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304146146_image.png)

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304149716_image.png)


I also do testing on the resulted images. At the beginning I found that the images got blurrier as more of them are generated. I did some trail-and-error and found out that I incorrectly resizing the same images inside the loop. This caused the original image to lose quality and information as the loop goes on.
 
Version control (Git on Bitbucket) is used to ensure the quality of the code together with continuous integration (Pipeline).
In the earlier stage of our project, we wasted a lot of time developing on the inaccurate model because we didn’t do regression testing every time we modify our code. This caused us lots of time to fix it. So later test cases were written to test if the accuracy of the model is within acceptable range. By integrating a CI tool, we ensures that every commits we made to the repository does not break existing functionality (or downgrade the performance of existing model). This gives us confidence in keep getting more accurate and robust result.

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304153488_image.png)


(Pipeline itself was under continuous improvement as well. Initially there are some dependencies that are inaccessible on pipeline environment, so I manually tested them and delete those that are problematic).

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304156885_image.png)


(Now when my team mate pushes to the repository, they can be confident what they just submitted is indeed an improvement and does not break existing code)

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304164022_image.png)


(There were times when the model pushed to the repository does not satisfy the requirements of tests. E.g. lower than acceptable accuracy. These failed builds will trigger an email notifying all developers that their builds have just failed)

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304168668_image.png)


(Email notification was set up to notify developers)
 
By employing CI and regression testing, we eliminates the possibility of pushing incorrect commits (which is a headache to find them) to the repository, resulting in code with higher quality.

- **A summary of the use and application of discipline knowledge**

This part is not so relevant to our project (especially not to my work) because our project is not a software project. I will list a few points that might be relevant to my work:
I develop my work following software development principle. For example, modularization of code components for better reusability and portability (mentioned in previous subsection).
The usability of my code is ensured by making the code configuration without having to look at the code itself (encapsulation, the user does not have to know any implementation details).
Other than that. my work (including pipeline setup, manual image classification) is mostly done on a graphical user interface. There isn’t much other than clicking, dragging and searching on the Internet.

- **Summary of challenges and complex problems in individual's work and how you addressed/solved it with evidences (links, screenshots. other)**

The biggest challenges I faced was on the random image generator.
There was a problem on blurry images but that was mentioned in first subsection of this section.
The other challenge is the effectiveness of these images. These images were develop to train the TensorFlow model. However, towards the end of our project, our direction shifts from TensorFlow to OpenCV (developed by other teams working on similar project). To emphasize on the collaboration between teams, we took another approach using the bounding box (which was not my work). These images became not so relevant any more. Although we and the client both had very high expectation in these randomly generated images; but as the context shifted, they are no longer irrelevant.
The challenge was to modify the program so the images generated can work with the new OpenCV model (also in other group’s simulator). But that was hard to accommodate because the background used in other group’s simulator was not as complex as ours (i.e. much less noises). And the intended modification did not went well and I gave up on the generator.
There was not any evidence related to this. It is just decided in Zoom group meeting that we would abandon this approach.

## Other contribution to group processes
- **All group activities**
    - I completed all works assigned to me by the client, the tutor, or our teams.
    - I followed the group contract and attend every group and client meetings on time.
![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304177798_image.png)


(I really don’t know how to provide evidence of meeting)

- I contributed to team process as the tracker. I was responsible for all weekly status report throughout the semester.
![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304183115_image.png)

![](https://paper-attachments.dropbox.com/s_590CDFE308CFFA114421F6A84443D07B36533F47169B963AEBE7EBBDBB7CFE2E_1606304187526_image.png)


(Two examples; all submission history of weekly status report can be found here on [Wiki](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home) or on Canvas (The tutor should have full access to it))

- I have participated in group presentation and demonstration.

The Google Doc that contains my part of the presentation can be found [here](https://docs.google.com/presentation/d/1D2ldYPLLpUOHR_xMz1kFZU-CrPrlHsQyow-lb2i1E0Y/edit?usp=sharing)

- I took part in writing user stories that were included in the final report (final report can be found [here](https://docs.google.com/document/d/1pPQTqB6OSCoV3mSsRMsvVmgs9b68zqMQP2TM0W_YBM4/edit?usp=sharing))
- **Evidence of collaboration and teamwork**

This part is irrelevant to me. The random generator task was assigned to me and me solely. It did not involve any collaboration or teamwork.
 
Manual classification of training images was my collaboration with my team. That can be found in the “Extend of that work” section of this report.
 
Setting up the pipeline so that the team can work collaboratively and more effectively using continuous integration (That can be found in the “Extend of that work” section of this report).
 

- **“Issues” created and progress with evidences (links, screenshots. other)**

This part is irrelevant to me. My work was mostly individual work and I did not use our team’s issues board (Trello or Jira) to record any issues since they are only relevant to me and the other group members have no knowledge of them.

## Reflection
- **Reflections on version control, coding styles, XP; challenges met in the project, how these were tackled.**

**Version control:**
Our team used both [Bitbucket](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/bitbucket-pipelines.yml) for our sign detection algorithm and [GitHub](https://github.sydney.edu.au/moxu7046/COMP3988_simulator) for our simulator improvement. At later stage, we also integrated continuous integration tools into the repo. This eliminates the possibility of problematic code being pushed to the repository and breaking existing code. Version control system is also used for release. Several releases were made on important check point (e.gl. client deployment).
 
**Coding styles:**
Our team writes descriptive code with comments and documentations. This helps the collaborations among team members.
 
**XP:**
Our team followed agile software development principles.
 
**Weekly meeting among development teams**: We have meeting on the tutorial of every week to discuss challenges and issues faced by the team. We also discuss the progress of each team member.
 
**Weekly demonstration and meeting with the client:** we closely work with the client to understand their new requirements as well as scope changes. We aim to develop and demonstrate working new features to the client every week. If required by the client, the project manager will demonstrate new features to the client. The client is actively involved in the software development process to achieve the best result.
 ****
**Communication:** team members actively involved in team communications. We responded to messages promptly both to fellow members and the clients. We also keep in touch with the client closely to understand their needs and their changes of requirements.
 
**Feedback and improvement:** In every week’s group meeting, the team had discussion on their improvements since last week as well as challenges faced by the team. We discuss possible solutions to these challenges and aim to overcome them in the week to come.
 
**Challenges:**

**Time pressure:** towards the end of the semester, some members of our group are preparing for their job interviews; the other are preparing for assignments and final exams. Our progress slows down but the deadline is approaching. We had to re-distribute work among members so that members with light work load take more than they usually will. This helps us survive the last few weeks of the semester while also delivering the final project.

**Environment setup:** Since our projects requires the latest version of many dependencies, there are bugs introduced by these instable versions and solutions are hard to find (developers usually use stable versions). This causes us many problem and to me. The GPU running environment I tried to set up failed because the version did not match. The solution we had for this kinds of issues is to always use the most robust software (CPU instead of GPU, etc.).

**Client keeps adding more requirements:** the client keeps adding more elements to the existing scope of the project. This often leaves behind unfinished or unsatisfactory features. It also takes up a large portion of our times (from other units of study). This problem was not tackled properly; but luckily, at the end the client realizes that we are approaching the end of the semester and stopped asking for more features added to the project.

****

- **Your role in the group and as a software engineer/computer scientist**
    - As previously mentioned, I developed a random image generator.
    - As previously mentioned, I set up an integrated continuous integration tools in the repository.
    - I collaborate with fellow engineers to understand their needs and requirements and help them when necessary.
    - I write detailed weekly report to reflect my work done and let others view them.
    - I collect and classify data used for the project.
    - I attend weekly group meeting to express my concern of the project and report my progress.
    - I take part in presenting our work to the supervisor and the client
- **How the final project delivered as expected and how the team have worked together to finish the project, how could you improve**

We have not completed the scope of the project. We have not done the detection code for all traffic signs. The accuracy of the model is not robust, especially in complicated environments where there are lots of noises and distraction. Nevertheless, the model works perfectly in a simulated environment with limited interference. Our team tried to improve the model from multiple approaches such as TensorFlow, OpenCV, bounding boxes, etc. A combination of different techniques is complementary to each other, to improve to overall quality of the model.
The simulator improvement has been done well. Multiple tracks and a car model have been developed. It is effectively to collect training data for the model in the simulator.
 
The algorithm team is @Yiran and @Yuanda. One of them improve the model while the other test it in the track; the simulator team are mainly @Mouyi and @Ziyin, they build 3D models of tracks, cars, and signs in the simulator. @Sipei and I mainly do the miscellaneous stuff, we involve whenever a team needs us.
 
Based on the feedback from the tutor, I developed a continuous integration tool and integrated it into our repository. If we had done this earlier in the semester, our final model would surely be much more accurate and effectively since we would not have gone down the wrong path (This does not have any evidence; it was mentioned by the tutor during weekly tutorial in Zoom meeting).
Based on the feedback from tutor on the individual report, I provide more evidence in the form of hyperlink in this report. I also add captions to pictures or diagrams.
I think the team had spent too much time on the simulator. The focus of the project should be on the detection algorithm. We assigned 3 persons to each part of the project while we should have assigned 4 to the algorithm group.
 

## Writing and wiki use quality
- **Accounts for feedback provided during presentation from the tutor and client.**

The client expected us to present more “results” rather than “process“ last time. So in the final presentation, we leave out all the process leading us to achieve the final result, which was the focus of the demonstration.
[Link to the Wiki](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home)