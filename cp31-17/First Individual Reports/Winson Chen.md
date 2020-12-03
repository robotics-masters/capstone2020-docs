# Individual Report for Winson (wche5722)

## Roles

### Slack Expert
As the Slack expert, I was responsible for the creation and management of the Slack channel. As a part of my responsiblities I have added all members and created appropriate channels for topics. I have also added automations within the platform which notifys when new tasks on Trello are created and reminders of any upcoming meetings and paperwork.

### Tracker Week 2
My week as a tracker involved asking everyone personally of their progress and plans. As it was the first week that we had interactions with the client, many of us had been settling into our roles unaware of the amount of work we are required to do. [This check-in](https://imgur.com/a/T3lcKFl) contributed to the pace of work increase to a satisfactory level to meet the deadlines.

### Tester
I contributed to the testing role by creation of the unit testing tool which included the [refactoring of the code and several basic test cases](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/337f1e0c7a80d1506b8b9d0556a46ee4bbdd7a53).

## Contribution

### Technical
My technical contributions have focused around OpenCV. This contribution included refinement of the [stop sign](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/3d31c468556f42479fcc377e7e2606bbc1d0d7ab), [turn sign](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/ecc0dbe596f3553776d849db577f2db78d1bdf97) and [traffic sign](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/b3f84f1354c03c5b815f316bcb97d5789aa4699d) detection. I have also attempted to implement some novel methods (Houghlines and circles, and feature matching). I played an important role in the smooth integration of OpenCV in DonkeyCar with ensuring compatibility with the modified code base ([1](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/403187ad2b510e20f6b0d3aad0d77249cf954281),[2](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/commits/f63c66a7b915c63230d6f3d7b4160082594c3dc8)). As mentioned earlier, I adapted and created the unit testing platform

### Non technical
My non-technical contributions involve [research into potential literature for OpenCV](https://docs.google.com/document/d/1EPbtukk1guyyKxdIKQGCnnN5zTgFnq5bZEXALv65Mww/edit?usp=sharing) and [extreme programming](https://docs.google.com/document/d/16ML1vLP75vRKrA2i71_quMwSnnURlKUIVyNWXhii2zs/edit?usp=sharing). I have contributed to several meeting minutes (Week 2 Tutorial, Week 4 Tutorial, Week 5 Client) and weekly updates (Week 2 and Week 4). I also added some quality of life changes such as the creation of a template for the meeting minutes and weekly updates, as well as landing pages for both of those and wiki homepage. I have been consistent with attending and contributing to team and tutorial meetings, and client meetings once a week (see meeting minutes for more, for client meetings I attend the second client meeting). In addition, I consistently and frequently check for new messages by other group members and try my best to assist solve problems that come up.

## Reflection

### Version control
Version control has been generally good with the use of Bitbucket and commits notes. It was important to keep track with the version in regards to the frequent major simulator updates, but less so for the minor changes towards the sign detection (but it was important for the OpenCV integration portion of sign detection changes). Although we could use some improvement, including more frequent merges among branches and markers of version.

### Coding style
Coding style hasn't been a problem so far. This is likely due to the lack of big changes in the codebase and most changes have only been one or two lines and experimental in nature. Consistent reference to the config file for quick and universal changes has been an agreed-upon convention as well as frequent comments.

### Extreme Programming
We have attempted to implement the XP guidelines. This includes the roles (as mentioned earlier), planning, frequent meeting with the client, simplest task first, low overtime, refactoring, collective code ownership and having coding standards. Some guidelines, however, have been impractical to implement such pair programming (due to most of the sign detection involving tweaking of numbers and low number of lines of code added) and passing all tests before adding more features (due to limitations of sign detection and avoidance of stalling/overfitting). One improvement I aim to implement is more work in and stricter roles.

### Challenges and resolution
We met some communication challenges in terms of missing/late to meetings and ensuring group work submitted. These are resolved by increasing the amount of necessary communication and assigning someone responsible for submitting.

### Project and team
I am enjoying the project as it has given me new perspectives on big scale code production, computer vision and group work. The teamwork has been pleasant with most members having a solid work ethic and frequent, transparent communication. I  expected work that was less experimental/research-like and more creation of code.

### Improvements
As previously mentioned, some further improvements can be made in stricter roles. We also require much more work on the OpenCV side of things, more frequent merges with the main branch. There is also room for improvement with transparency and frequency of communication with the work.