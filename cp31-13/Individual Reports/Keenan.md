# Individual Report

## Clear statement of Work Done and Extent of that work
For this project, my major XP role was customer, where I oversaw communication between the client and our group. This included sending emails and asking questions via Discord regarding ideas or issues we had with the project. Below I have included some screenshots as evidence of this communication.
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/4203853562-image.PNG)
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/290507616-image.PNG)
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/3826165346-image.PNG)
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/4122606391-image.PNG)


For my major technical contributions to the project, I largely worked on the Unity Simulator. In particular, I focused on implementing track 1 into the simulator, training an AI model and integrating the OpenCv code into the Unity simulator. For the function that controls how the car reacts to signs in the simulator, I have also created the following [unit tests](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/56fbdeb80607c335690b7eedfbb581eac54ed29d).

For evidence of these tasks, I will include the relevant issues or demos I conducted:

- [Track 1](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues/1/new-tracks-modelled-into-simulator)

- [Training an AI](https://youtu.be/q-kHvkxQNug)

- [Integration of OpenCv](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues/13/integrating-everything-into-the-simulator)

I will now give a breakdown of how I assigned my weeks to completing these tasks as well as some of the minor tasks I completed.


Weekly plan:

-	Week 1: N/A (hadn’t met with client yet)

-	Week 2: During this week, my major focus was on installing the donkey car simulator and then implementing track 1 into the simulator per client specifications. I achieved this through implementing a 3D GameObject in the Unity simulator and applying the track 1 texture onto it.

-	Week 3: During this week, my major focus was on understanding ‘env_id’s’ within the unity simulator and attempting to get Unity to recognise track 1 as a level so that we can select the track from the Donkey Car menu. I was able to get about 75% of the way through this task, where I could set up the simulator to load track 1 upon launch, but had help from Johnny in getting track 1 onto the menu screen.

-	Week 4: During this week, my major focus was on training an AI to drive around track 1 and 2 that we had created, tweaking the lighting of the scenes as well as implementing the ‘RMRACERLIB’ package provided by the client without any errors. By following the documentation I was able to successfully train the AI to drive around the track, and with help from the client I was able to properly configure the RMRACERLIB package. I implemented an ambient lighting solution for the tracks.

-	Week 5: During this week, my major focus was on integrating the OpenCv code into the simulator so that signs could be detected, as well as ensuring that the Donkey Car did the appropriate action depending on what sign it saw. This is where I had the most difficulty, but with help from the client I was able to debug a lot of the errors I was getting and eventually have the detection code working with the simulator.

-	Week 6: During this week, our major focus was on writing up our report and preparing our presentation.

## Quality of technical work done
The main methods I took to ensure quality were:

-	Pair programming

-	Testing

-	Code review

For pair programming, I would work with other members to either ensure that my work was functioning correctly and efficiently, or vice versa for my members. Typically, we achieved this using Discord by entering a call and sharing screens as we worked. Because I was working on the simulator along with Johnny, the majority of my pair programming sessions were done with him. He would help me debug certain errors I was having with my work, as well as provide with my tips and advice for how to implement certain features into the simulator.  In particular, through our pair programming session he helped me figure out how to implement our new tracks on the simulator main menu screen.

During the latter weeks of the project, I also did pair programming sessions with Osama. This is because we were attempting to integrate our work together (his work being the OpenCv code and mine being the simulator), so we had to work together to ensure our integrated work was functioning correctly without any bugs. The pair programming sessions were invaluable for me in understanding the functionality and algorithm of the OpenCv code, as well as figuring out how it would fit into the overarching system of the simulator. I also did a pair programming session with Oscar to help him [train an AI model](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/Pair%20Programming%20Evidence/Oscar-Keenan-03-10-2020).

For evidence of these sessions, I will include screenshots of the messages between each other when coordinating joining a call together. For reference, on Discord my name is given by “CP31-Keenan” or “SkeletonOfTheMexicanWalkingFish”. Johnny’s name is “Jyoni” on Discord.

![image.PNG](https://bitbucket.org/repo/oo8byMk/images/868001657-image.PNG)

Above is a message between Johnny and I where we join a discord call for a pair programming session. This was for integrating OpenCv into the simulator.
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/2197087982-image.PNG)
Above is another pair programming session I did with Johnny that lasted 29 minutes. This was for adding track 1 onto the simulation menu.
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/466561210-image.PNG)
Pair programming session with Osama and Johnny on 28/09/2020. This was for integrating OpenCv into the simulator.

![image.PNG](https://bitbucket.org/repo/oo8byMk/images/38197961-image.PNG)
Above is evidence of pair programming sessions with Osama. This was for resolving some issues with integrating OpenCv into the simulator.

For testing, I did acceptance testing with the client and unit testing. For the acceptance testing, I would typically run the simulator and ensure that it was behaving the way the client specified. After completing a key piece of the project, I would also send him an image/video to ensure he was happy with it.

![image.PNG](https://bitbucket.org/repo/oo8byMk/images/2267988736-image.PNG)
Above is evidence of verification of track 1.

![image.PNG](https://bitbucket.org/repo/oo8byMk/images/3893897150-image.PNG)

Above is evidence of improvements to lighting.


For unit testing, I found it more difficult to apply this methodology to what I was working on in the project. This is because I rarely worked with code; rather, I worked with the Unity editor and the Donkey Car packages. Within the Unity editor, I wasn’t required to write any scripts so there weren’t any functions for me to test using [Unity’s testing framework](https://docs.unity3d.com/Manual/testing-editortestsrunner.html). The output of my Unity Editor work was an executable program which contained the 3D objects I had created, so the majority of my testing was visual. For the Donkey Car packages, I was largely downloading code provided by the client and integrating it into the Donkey Car system by placing the necessary libraries in the correct folders, correcting return values of existing functions etc. However, I did apply some unit tests for the code which determined how the car reacted to traffic signs when detected, because I knew that this is code that I would have to modify in the future and so establishing a good test base of expected behaviour was crucial. The tests can be found [here](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/56fbdeb80607c335690b7eedfbb581eac54ed29d?at=Simulator-testing).

For code reviews, since the new code I wrote was limited, I did most of my review by showing the client the models and tracks I had implemented and getting verification from him. During pair programming sessions with team members, we would also do code reviews, where as we went through the code together we would give our thoughts on what needed improvement.

## Other contribution to group processes
I invited the client to our Bitbucket and Slack repositories with evidence here.
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/2503129955-image.PNG)

I also helped with writing sections of the Group Report.

During the initial weeks of the project when we were still determining XP roles, I would occasionally upload Meeting Minutes to the BitBucket Wiki as well setting up Google Drive so that we can collaborate on files together. I also uploaded our weekly status reports to Canvas.

For evidence of teamwork and collaboration, regretfully I don’t have many good ways of displaying this. This is because we did most of our communication over Facebook and Discord, with us slightly neglecting Slack. Towards the end weeks of the project, I made an initiative to try and communicate over Slack more but the evidence there is still limited. In the future, I will take a greater effort to use Slack for more of my communications. Instead, I have included some messages with Johnny which show us collaborating together. 
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/1949153554-image.PNG)
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/3849982830-image.PNG)
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/298398786-image.PNG)
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/1018742451-image.PNG)

There are also some messages between me and other group members on the [Slack channel](https://app.slack.com/client/T01AJMAGTMW/C019US118KC).

## Reflection
This was the first major project I have worked on where I had to work with a group to produce specified software for a client. As such, a lot of common software development practices were new to me and I have identified a lot of key areas I need to improve on.

For example, when using BitBucket and working on the project, I would often wait weeks before I pushed my completed work onto the repository, when I should have been pushing new changes as soon as they were complete. This resulted in version conflicts later on in the project, where because I hadn’t pushed my newest changes onto the branch, group members would work with older versions of the project and we would have to combine the two versions together manually. For the remainder of the project, this is a major area that I need to work on and I will be aiming to push any changes I make onto the remote server immediately.

Regarding coding styles, this is not something I can discuss in too much depth due to the lack of coding I’ve had to complete so far. As the project progresses and I get to write new code, I am aiming to write well commented code that clearly documents the expected behaviour of functions, their inputs and their expected output so that it’s easier to maintain for future developers and my teammates.

For XP, my use of pair programming was lacking. Although I would occasionally do a pair programming session with members, I would not do this on a consistent weekly basis. In the future, it would be more beneficial for me to try and aim for a weekly pair programming session with a member so that I can obtain the benefits to code quality and consistency that pair programming provides.

Regarding testing, this is something that I was also lacking. I again found it hard to set up rigorous testing procedures due to working with the Unity simulator, as discussed previously in the report. The testing I did was largely in the form of acceptance testing; that is running the software and ensuring that it met what the client expected. However, I typically created these tests after implementing the feature rather than before, which conflicts with the XP methodology of writing tests and then implementing the code/software. In the future, I should aim to design test cases before I begin working with the software.

The major challenge that I’ve experienced in the project was with understanding the Donkey Car simulator. When initially working with the simulator, I found that there was no documentation when it came to understanding the various files, classes, functions and data types of the simulator. As a result, I spent a large majority of my initial research time reading through the code of the simulator and trying to understand how everything worked. What made this harder for me was that my experience with Unity was limited, with my only major experience being on projects in high school. This added to the confusion of trying to understand how the simulator worked and how to use it.

To remedy this, I made efforts to ask questions where possible. For example, I joined the Donkey Car discord where I was able to ask the developer Tawn Kramer any questions I had. Evidence:
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/2357993398-image.PNG)

Similarly, I would ask the client questions if I was really stuck, where we would occasionally join a call to discuss the problem.
Evidence: 
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/741136444-image.PNG)
![image.PNG](https://bitbucket.org/repo/oo8byMk/images/100648322-image.PNG)

Reflecting on my role in the group as the client point of contact, initially during the project I felt useful. This was because we had yet to establish alternative lines of communication other than email so I had a clear purpose of summarising any questions we had and sending them to the client. However, as the project progressed and we established other ways of communicating with the client such as Discord and Slack, my role felt less purposeful. This is because it was easier for a member to just send their question directly to the client.

In terms of work and as a team, I think we’ve done a good job of keeping on top of the work and meeting the requirements of the client. However, I think something that I could improve in the future would be providing more updates to team members on my allocated tasks, and doing a better job of explaining to members what I had done and how they can use what I made. This will make it easier for members to understand my work and will improve collaboration.