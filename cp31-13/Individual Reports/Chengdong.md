# Individual Report

## Clear statement of work done and Extent the work each week
For this project, my role have been switched over each week, the main work i am assigned was all related about improving opencv code provided by client

Weekly plan and xp roles:

-	Week 1: installing the sourcetree and get familiar with the bitbucket stuffs.

-	Week 2: During this week, my XP role is manager, i am focus on installing the Donkeycar gym and simulator stuffs and get that work in my computer.

-	Week 3: During this week, my XP role is Programmer, I am focus on the turn sign code to see if there can be some improvement, I have tried to run the code by the video file provided by client and check how the detections is working for the output videos. The original code seems have many false detections and it mis-detect in many frame, I research on the color filtering stuffs and some image processing methods like dilate or erode to modify the code a bit and added the sign check helper functions by checking the color pixels value of the possible detected with the actual sign in reference folder, which is aim to decrease the false detections a bit.


-	Week 4: During this week, my XP role is Tester, I am still working on the turn sign code and I tried to extract every possible detected area into a folder and check that as a image flow into every functions one by one to find if there are some issues in certain functions, I found that the direction check function doesn’t always return the correct output all the time, here are some evidence:[link](https://youtu.be/-Yx0cLu5eyM)

-	Week 5: During this week, my XP role is Doomsayer, I have switched to work on the park sign code and similar to the turn sign one, it has some false detections, the aim is to decrease the false detections, I tried to transfer the similar progress from the turn sign code into that and do some research on the edge detection and houghline checking to see if there can be some improvement: [commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/3c87cbcb62420ed11952fa5a8bb477431939a081)

-	Week 6: During this week, my XP role is Tester, I am focus on writing the report and try to check if the edge detection is working in the park code, However, after testing by the frame flow extractions, I found it’s better to use other method called Harris detection instead and add some function related to that into the park code:[commit](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/commits/60dd22c98f92df9c03f4c5d8188f0bde22d5faa3)

## Quality of technical work done
Code review
I tried to run the code on the jupyter Notebook and reviewing that by extract out each function and test them by the frame flow and as mentioned above, this can be a great way to find the issues inside each function and improve that based on certain function.

Pair programming
In week 5, I tried the pair programming stuffs of park sign code with the team member Tamara through the zoom meeting sharing the screen, and we found that there are still many false detections when running the code, after the discussion I got some ideas about trying edge detection and shape checking in that code which might decrease some false detections. There are some evidences (only some chat, i forgot to take the screenshot of zoom meeting at that moment)

## Other contribution to group processes
working on the issues of assigned [#2](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/issues/6/refined-working-solution-of-provided-code)

Update the weekly summary stuffs inside the [WiKi](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/browse/Weekly%20update)

## Reflection
For the version control, I am working on the park sign code and there are only two commits now which both on the same branch called “opencvpark” , for future working I might try to update on that branch every time when there are some progressions on the park code, and I need to build other branch for the other style of park sign code progressions as well as the test branch, thus when I finish all of the stuffs I can merge these branches and get the final solution.


For the coding style, I am not good at this thing, as my code is quite massive and I might need to add more comments for explanations, I try to separate the code into many functions that each one have it’s unique use, which will be easier for testing but I still need to do some more research on PEP 8 style mentioned by osama in order to make the code much more clear.


For XP, the task are break down through the whole group, and I am keep working on the opencv related things during these weeks which will be the great way to learning the knowledges and improve the code skills.


For testing, I am lack of that as I haven’t added any unit test yet but it will be update soon, the only thing I use for testing is just run the image flow in each function and count the failure rate.


The major challenge is about the make sure the code will working in both simulator and real world as there might be some difference compare with the virtual ones and the real world ones so I need   to do more research on that and try to change the code a bit.