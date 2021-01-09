# __Individual Report – Gio Picones__ #

This is the Final Project Report (Individual) for Gio Picones, due Sunday 29th October 2020.  

### XP Roles ###

Note that on the request of the tutor, manager and customer roles were fixed. For the second half of the semester, I had the role of Customer.

- Customer -- This role involved leading team meetings with the client, updating the client on work done and work to be done, and ensuring that the team was clear with what the client expects, with these being translated to user stories.

In the second half of the semester as the team settled into routine, we became very efficient during team client meetings, where we were able to quickly provide updates, report on progress and obstacles, and estimate what we want to achieve by the next meeting. As the Customer role, I would lead these meetings and provide an overall update of the progress made by each team member.

Due to this, we were able to perform effectively with almost all correspondance happening through the scheduled client meetings.

[Role
rotations](https://bitbucket.org/zson5784/comp3988_t17b_group_5/wiki/Role%20Rotation.md) 


## Contribution ##

### Technical ###

The project has two main components - building a simulated world in Gazebo with traffic signs and a simulated drone with a camera, and building/training a neural network in TensorFlow which would make predictions based on the drone's camera feed, with the video feed input first being processed through OpenCV for the extraction of regions of interest. 

I played a key role in the TensorFlow component, as well as the integration between the drone camera feed, OpenCV and TensorFlow.


### Week 7 + Midsem Break: First Integration Milestone and Better Data Collection ###

- First major milestone of integration! Achieved neural network integration with the drone camera. The model was trained to detect fountains. The drone camera would feed frames into the neural network, which would predict whether or not a fountain was in the frame. [Commit](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/55fbefb4ae9ac2820d20a1d8570bb1ae8c5bba71). [Demo video](https://youtu.be/P-4iJHQQJsM)

- First attempt at function to make the neural network asynchronous, refactored a few existing files.. [Commit](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/6ced0d56d36fbad92f508c129ce21e9ae494a7f8)

- Data collection of data from within Gazebo (prior to this we were training on images from online datasets). Here, I manually placed signs in front of the drone and took photographs with the drone camera. The dataset was not stored on git due to space constraints (max 2GB before the repo is frozen).

- New model on the "better" sign data as captured above. The binaries of the weights of the new model are in this [commit](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/e51c19ee2b4b040ffd739212fd98c7ad3d43b1ec). Note that due to the huge size of trained models, we decided as a group that moving forward, we would store any model weight binaries locally, sharing through other means when needed.

- Note: Work done this week exceeded what was intended, in order to mitigate the busy weeks ahead.

- Work done this week is related to this [user story](https://trello.com/c/V2fLbYZs/12-as-a-client-i-need-100-object-detection-rate-so-i-can-clearly-know-whether-the-drone-should-be-obeying-traffic-directions).

- Milestone this week resolves this [issue](https://bitbucket.org/zson5784/comp3988_t17b_group_5/issues/5/sign-detection-integration).



### Week 8: General Housekeeping ###

- General cleanup of the repo, specifically the model weight binaries. Some team members had accidentally committed and pushed the binaries of their experimental trained models, which froze the repo temporarily. [Commit](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/f8e936aeade548b4438f964918b00950543e0f11)

- Note: This week was a week busy with other commitments, so no additional progress was planned.



### Week 9: Neural Network Data Experimentation ###

- This week and the following week was dedicated to furthering domain knowledge of neural networks and experimentation, which frankly none of the team are experts in. Our current model seems to have decent validation performance when the model is trained and tested standalone, however in practice, when the drone is flying around and the realtime predictions are made, the accuracy is quite bad.

- The current model was trained on a combined dataset of real-life images of signs, images from a previous OpenCV project given by our client, and our self-collected images from within Gazebo. I suspected that perhaps the bad accuracy was due to the dataset containing images from real life, whereas the final product was expected to predict on images from within a simulator. 

- I experimented with training a model on two sets of data, one was the whole set, and another contained only images taken from inside Gazebo. For the space-constraint reason explained above, I did not commit the two models' weight binaries. As evidence, here are google drive links for the binaries of [model 1](https://drive.google.com/drive/folders/11xijhQXDehNns3DiexL4LuTfiv_nOR3Q?usp=sharing) and [model 2](https://drive.google.com/drive/folders/1huKYAsw9c4AcRyt1qm7fqLx8QcRJ4sI4?usp=sharing). In addition, here are images of the two models' accuracy and loss.

![9_1.png](https://bitbucket.org/repo/jkq4oxG/images/2813863344-9_1.png)

![9_2.png](https://bitbucket.org/repo/jkq4oxG/images/3745726550-9_2.png)

- As can be seen above, both models have high standalone accuracy, with the only difference being the amount of loss. However, both models still performed poorly in practice.

- Note: Work done this week was what was intended to be done.

- Work done this week is related to this [user story](https://trello.com/c/V2fLbYZs/12-as-a-client-i-need-100-object-detection-rate-so-i-can-clearly-know-whether-the-drone-should-be-obeying-traffic-direction://trello.com/c/5lNadSI6/2-user-able-to-define-which-dataset-to-train-from-and-define-how-many-classes-there-are-when-choosing-to-build-a-neural-network-fr).



### Week 10: Neural Network Architecture Experimentation ###

- This week I tried a different approach to experimentation. I did research on neural networks, and learned about the theory behind convolutional neural networks. I read up on existing architectures for the specific problem of image detection, for example [LeNet](https://towardsdatascience.com/understanding-and-implementing-lenet-5-cnn-architecture-deep-learning-a2d531ebc342) and [AlexNet](https://towardsdatascience.com/alexnet-the-architecture-that-challenged-cnns-e406d5297951). I also read up on uthe effects of tweaking the hyperparameters of neural networks, for example the filter/kernel sizes, pooling layers, the number of nodes in hidden layers, and the activation functions you can use for each layer.

- Similar to week 9, I designed and trained my own architecture based loosely on LeNet, tweaking the number of convolutional and hidden layers, kernel sizes and number of nodes in each layer, as well as different activation functions.

- The test results for my best attempt is shown here, alongside the current model.

- Google drive [link](https://drive.google.com/drive/folders/15igGHxYyoEj1gAAJAFfHCqGeJ6jhj7G1?usp=sharing) to my model weight binaries.

- The first image is the current model, the second is my attempt.

![9_2.png](https://bitbucket.org/repo/jkq4oxG/images/3239995100-9_2.png)

![10_1.png](https://bitbucket.org/repo/jkq4oxG/images/2657829225-10_1.png)

- As seen above, clearly I'm not an expert at neural network architecture design. Despite the much worse standalone performance, both models performed comparably in practice with the input from the drone camera.

- Note: Work done this week was what was intended to be done, however we needed to find some other method to improve performance in practice. In the following weeks we would attempt a 2-layer approach, with OpenCV filtering out regions of interest for input into the neural network, as opposed to feeding in the whole frame, which we were currently doing.


- Work done this week is related to this [user story](https://trello.com/c/5lNadSI6/2-user-able-to-define-which-dataset-to-train-from-and-define-how-many-classes-there-are-when-choosing-to-build-a-neural-network-fr).


### Week 11: Integration Attempt ###

- This week, other teammates (Zhi Yi and Ye Xin) had managed to get OpenCV working. My work this week involved attempting to find a way to integrate OpenCV into Tensorflow, to no avail.

- Note: Not much more was achieved this week due to other university commitments.



### Week 12: Integration Milestone and Statistical Testing ###

- This week, I retrained the model on a dataset containing images of regions of interest, where before we were training on images of full frames from Gazebo. We suspected that the predictions were being dominated by the background of the frame, especially when the sign in an image would take up very little space (small) relative to the size of the whole image.

- Second major milestone of integration! I was able to integrate the neural net code with Zhi Yi's OpenCV code, and we achieved object detection with good accuracy in practice! The system now takes full frames from the drone camera, extracts regions of interest from the frames with OpenCV, and feeds these regions as input to the neural network. Input images are now no longer dominated by the background, and include only signs and noise. Noise is just another class the model can predict on, so it is not a problem. [commit](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/12632cd3cd7030df32f5c853ce79280c29e4c08c) and [commit](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/12632cd3cd7030df32f5c853ce79280c29e4c08c)
 
- I also fixed an issue with Tensorflow where cuda would sometimes fail to initialise due to the vram being completely filled up. This was done by limiting the memory usage. [Commit](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/0648c85f915b2eb7b54b456dc87736f6117336da)

- Small refactor changes, eg converted the neural net prediction code to be a function instead of a for-loop against a generator. [Commit](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/4d70ea97567cc2efc9ac4dae7ba65c6043a9f7b3)

- Implemented statistical testing. This was after I learned the theory behind it from another unit of study. Before we had been measuring performance based only on validation and testing accuracy/loss. I implemented a script that would measure the F1 score, precision and recall, both for each class, and an overall unweighted mean. The script would also generate a confusion matrix, so we would be able to see specifically which classes were being predicted as which other classes. [Commit](https://bitbucket.org/zson5784/comp3988_t17b_group_5/commits/45d3141a3dda8abaffc15016fb3e880947f5d743)

- Below are the confusion matrix and test results

![confmat.png](https://bitbucket.org/repo/jkq4oxG/images/3960439943-confmat.png)

![test_result.png](https://bitbucket.org/repo/jkq4oxG/images/2074065036-test_result.png)

- I ran part of the technical demo part of the university deployment, showing manual drone control and live prediction. [Video](https://www.youtube.com/watch?v=yrX_DVjtC0A&feature=youtu.be)

- Note: Work done this week was what was intended to be done.

- Work done this week is related to this [user story](https://trello.com/c/5lNadSI6/2-user-able-to-define-which-dataset-to-train-from-and-define-how-many-classes-there-are-when-choosing-to-build-a-neural-network-fr).

- Milestone fixes this [issue](https://bitbucket.org/zson5784/comp3988_t17b_group_5/issues/8/integration-tensorflow-with-opencv#resolve).

- Statistical tests fixes this [issue](https://bitbucket.org/zson5784/comp3988_t17b_group_5/issues/9/need-better-way-to-test).


### Week 13: Client Demo ###

- I ran the technical demo part of the client deployment, explaining how Tensorflow and OpenCV worked together, showing the bounding boxes of the regions of interest captured by OpenCV, and also demonstrated manual flight and live image detection. [Video 1](https://drive.google.com/file/d/1amBgJFSAYQBfKab-WHLyONQ-3nE-iAqx/view?usp=sharing) [Video 2](https://drive.google.com/file/d/1hya5Zj90pIC9ylXfeCN8Dsqkqoz9z6A0/view?usp=sharing) 

- Note: Work done this week was what was intended to be done.



### Non-technical ###

- Running the technical demo part of the first university deployment. [Video](https://www.youtube.com/watch?v=u9_upOwucOA&feature=youtu.be)

- Running the technical demo part of the second university deployment. [Video](https://www.youtube.com/watch?v=yrX_DVjtC0A&feature=youtu.be)

- Running the technical demo part of the final client deployment. [Video 1](https://drive.google.com/file/d/1amBgJFSAYQBfKab-WHLyONQ-3nE-iAqx/view?usp=sharing) [Video 2](https://drive.google.com/file/d/1hya5Zj90pIC9ylXfeCN8Dsqkqoz9z6A0/view?usp=sharing) 

- [Wrote some of the User Stories](https://trello.com/b/Y8qWmnWG/user-story)

- Leading the agenda of all team meetings



## Quality of technical work done ##


### Code Quality ###

To ensure code quality, we made sure to make a pull request and ask a team member to do a code review before merging branches into master. Here's an [example](https://bitbucket.org/zson5784/comp3988_t17b_group_5/pull-requests/12) where a team member made a pull request to merge the realtime prediction branch to the master branch. I did a quick code review with him to ensure that everything was good to go before the merge was completed.

There were also cases where we did a bit of pair programming. For example, Zhi Yi wrote a lot of the OpenCV code, which I was not familiar with. I had to find a way to integrate my neural network code into his code - we did pair programming over a Zoom call, where I shared screen, and he coached me through how his code worked and possible insertion points for my code. I wrote the integration while he watched and pointed out possible flaws and improvements. In the end the code was functional, and we achieved realtime obejct detection. 

![pair_2.png](https://bitbucket.org/repo/jkq4oxG/images/3725887309-pair_2.png)

### Discipline Knowledge ###

#### Neural Network Architecture & Convolution  ####

As explained in the week-by-week breakdown of progress, in week 7, I was able to get the neural network model and the drone camera feed integrated. At that point, we hadn't yet decided to start using OpenCV (the original scope was a pure Tensorflow implementation of object detection), and so the next milestone was to simply improve the object detection performance.

This required knowledge of neural networks and how they work, before you can effectively design an architecture for your specific problem. We started off with a simple architecture from an online [tutorial](https://www.tensorflow.org/hub/tutorials/tf2_image_retraining), and used it as a placeholder until we got all the moving parts integrated, after which it was time to optimise the model.

I studied the [theory](https://towardsdatascience.com/a-comprehensive-guide-to-convolutional-neural-networks-the-eli5-way-3bd2b1164a53) behind convolutional neural networks, and applied the knowledge to the design of a new architecture. Now I will give a brief overview of the knowledge I have gained, and how we applied it to this project.

A neural network is a network of neurons. The structure includes an input layer with an equivalent number of neurons as the length of the input array, and an output layer with an equivalent number of neurons as the number of classes. There can be any number of ‘hidden layers’ between the input and output layers, each with any number of neurons. Each neuron carries a weight, which multiplied and summed with output from the previous layer (depending on the activation function), will be part of the input for the neurons in the next layer. This weight will change via backpropagation as the algorithm trains, which is how the neural network ‘learns’.

Convolution is an extra step in the process, which is typically used to reduce the size of the image while retaining important features. In other words, convolution is used to capture the spatial and temporal dependencies in an image through the application of filters. 

A filter, or kernel, is defined as a matrix of numerical values. This kernel moves across the image (which can be thought of as a 2D array of numerical values), from left to right, going down the rows, until the whole image is traversed. At each step, a single value is computed based on the values in the kernel and the ‘window’ of the original image. These values are then put together into a convoluted image, which is then fed forward to the next layer in the neural network.

With this knowledge, it is easy to see why CNNs are the right class of neural networks to use for this project, where the image detection portion is essentially an image classification task, if you define 'noise' as just another class to be predicted.

The first reason is because the convolution step is an effective way of reducing the dimensionality of the data while retaining important features.

The second reason is because neural networks, due to the hidden layers, are able to learn non-linear functions, and are able to solve problems where the data is not linearly separable, such as the data used in this study.

The third reason is due to ease of prototyping - in practical terms, tweaking the architecture of a neural network is relatively easy, as a lot of the functionality is implemented in Tensorflow as functions, for example, defining a hidden layer with a number of nodes and activation function is as easy as calling a function with the right parameters. The hard part is designing it. For this project, a lot of time went into rapidly prototyping new architectures and training/testing them.

All this knowledge went into designing the neural network model, where we defined the number of convolutional layers and the size of their filters, the hidden layers and their activation functions and number of nodes. In the end, it would take a combination of the neural network model and an OpenCV layer to get the object detection to perform decently well.

Evidence of prototyping multiple architectures and training on different datasets with different charactertistics can be seen in the Week 9 and Week 10 subsections above.


#### Statistical Testing ####

Another example of the use and application of discipline knowledge would be the use of statistical methods of evaluating model performance, ie testing. Before, we had just relied on measuring validation loss and accuracy. 

I learned about other measures of performance from another unit of study. Specifically I learned about the confusion matrix, and the F1 score, precision and recall. Using these methods would give us insight into where exactly our model is performing badly (eg: stop signs being classified as turning signs), as opposed to summarising the performance into a single number like accuracy.

Once I had learned of this methodology, I implemented a testing script that would import a pre-trained model, and then predict on a set of test data. It would generate an array of predictions, one for each image, and compare it against the array of the 'true' labels of these images. These two arrays would allow me to generate the confusion matrix, and compute the other measures of performance stated above.

This allowed us to tweak the model in a more granular way. For example, as can be seen in the confusion matrix in the subsection Week 12: Integration Milestone and Statistical Testing above, we can see that the turn signs (class 8 and 9) are frequently being classified as noise (class 0). We could then inspect the data, and check if there were any instances of noise images that looked too similar to turn signs, and if so, consider removing them from the training set. 


### Challenges ###

#### Bad In-Practice Performance ####

Perhaps the biggest challenge which took us the longest to solve was the bad in-practice performance of the object detection, regardless if the neural network performed well on its own. After not being able to improve the performance by much with a pure Tensorflow implementation despite a lot of time and effort in trying different ways to improve it, we suspected that the problem could be the data itself; training and predicting on the full frame from the drone camera might make the model be dominated by the background of an image, as opposed to the sign that is in an image.

I attempted to address this problem by tuning the convolution layers of my model. Convolution layers, as explained above, are essentially how a neural network can select features. I thought that perhaps, with enough tuning, the model could accurately feature-select the signs, and downplay the effect of the background detail and noise. Evidence of my efforts can be seen in the screenshots in the subsection 'Week 10: Neural Network Architecture Experimentation' above.

In the end, the most effective way to solve the problem was to add an OpenCV layer to do the feature selection for us; that way the neural net could be trained on and predict on images with much less background detail, which ensures that it would 'learn' the details of the signs, and not the inconsequential background noise of full frame images.



## Other contributions to group processes ##

Our team makes use of [issues](https://bitbucket.org/zson5784/comp3988_t17b_group_5/issues) to keep track of bugs to be fixed or features to implement. As shown in the above section, most of my work in each week goes towards solving some issue or implementing some user story feature, which are all detailed in each week.

As stated above, we also made a habit of [pull requests and code reviews](https://bitbucket.org/zson5784/comp3988_t17b_group_5/pull-requests/12) before we merge a branch in which we have successfully implemented a feature. 

We also keep each other updated on our progress and help each other where needed. Since some members are working on the drone simulation part, and others are working on the object detection part, there needs to be communication between the two subgroups to be able to make integration work. Obviously there also needs to be communication between members of the same subgroup.

[evidence_collab_1.jpg](https://bitbucket.org/repo/jkq4oxG/images/2534320007-photo_2020-11-28_20-42-36.jpg)

[evidence_collab_2.jpg](https://bitbucket.org/repo/jkq4oxG/images/2809818595-photo_2020-11-28_20-42-33.jpg)




## Reflection ##

### Version Control ###

We used Bitbucket for version control. All members have experience with git, with some members being skilled enough to help the rest fix any issues, so using version control the way it was intended (merging branches, fixing conflicts, pull requests) was smooth sailing.


### XP ###

To be honest, the nature of our project doesn't lend itself very well to XP methodology, for example in the start, where the first few weeks was spent figuring out how to set up all the different software layers required for this project (and thus the Tester and Programmer wouldn't have had much to do). However we did stick them as much as possible, for example with the Manager and Customer roles still playing their part. For most of it though, we split the work and we were all Programmers every week.

For the second half of the project, it became a bit easier to implement XP practices, as we had gotten all the moving parts set up and we were doing more actual programming. There are still limitations like continuous integration not really being a good fit as our project relies on a simulator and not text output on a terminal. Some examples of XP practices we were able to implement are detailed below.

- I implemented the statistical Testing, which was then used on every new model trained after that. New models would then be evaluated partly based on how well they improved on the flaws of the old model, for example in terms of how well it predicts on a particular sign that the previous model would often get wrong.

- Pair Programming with the integration as detailed above.

- Refactoring, for example turning the standalone neural network code into a realtime prediction script hooked up to the drone camera, and then further into a combined script with OpenCV and the drone camera.


### Challenges ###

One challenge we faced was the number of moving parts in the project, in terms of software. We needed Gazebo for the simulator, PX4 for the simulated drone and camera feed, MAVSDK to control the drone with code, and TensorFlow and OpenCV for the neural network and object detection. We had to figure out which software to use to begin with, how they would all communicate, and finally which Operating System supported them all, which was a lot of work.

We tackled this by splitting the team into 2 subgroups, with Zhi Yi and Boswell leading the simulator component, and myself leading the object detection component with Martin and Steven, with Ye Xin working on integration. Zhi Yi figured out and wrote an excellent guide on setting up the simulator components, while I figured out and wrote a guide on how to set up the neural network component. This saved time compared to if everyone had to figure out how to set up every component on their own.

We also decided to all install Ubuntu 18.04 to ensure software compatibility, which itself took a bit of time.

Another challenge was the suboptimal in-practice performance of the object detection with a pure Tensorflow implementation. This challenge is explained in more detail in the section above; essentially we fixed this by using an additional OpenCV layer.

Another challenge was the lack of ability to sit in one room to work on the project together, which in my experience really helps to get things going. We tried our best to emulate this by working together during Zoom and Discord calls.



### Role in The Group ###

My role in the group is essentially the neural net/object detection programmer/lead - I figured out how to set up TensorFlow with GPU acceleration and wrote a guide for it on the wiki for others to follow, I wrote the initial model trained on Cian's data, and I wrote the code that would extract frames from the drone camera and build a training dataset from it. I also wrote the code that would load a pre-trained model and then use that model with input from the drone camera to detect objects in realtime.

In addition, I experimented with different neural network architectures, different types of data to train on, and finally I set up the integration between the neural network and OpenCV together with Zhi Yi. I also implemented the statistical testing.

I also did a good half of the technical demos, running the code on my machine and showcasing the manual drone flight and object detection. The other half of the technical demos were usually handled by Zhi Yi.


### Project Teamwork ###

In my opinion, the team has worked excellently together. This project was a hard one, and none of us really had any prior expertise in the fields required. We had to do a lot of learning, a lot of experimenting, and a lot of failing. We did our best with what we had, and ultimately, I am proud of what we have achieved.

We could have improved in terms of delegating work rapidly and moving on to the next thing, there were times were I felt like we lingered too long one one thing. For example, spending so much time trying to make the system work by tuning the neural network, when in fact a simple model combined with an OpenCV layer would be more effective. 

We also could have improved a little bit on coordination, but to be honest that's also just part of living in a world with covid, where we're all still getting used to the new normal. I still maintain that we did our best given the circumstances.

Some feedback from the tutor and client included focusing on getting the integration working before tuning/perfecting the model, which we acted on. The first integration milestone was achieved in week 7, with neural network tuning coming after.

Here are some of our planning documents. 

- [Final presentation planning doc](https://docs.google.com/document/d/1cBeF0sAXi-yJZoH-BQ7Sdf1ySybLcoVW4jrsocOmsSs/edit)
- [Final client demo planning doc](https://docs.google.com/document/d/17Ewe5qMCrgm3ndw__NWB2umMc0f4KWkz1NbUm_SIBFc/edit#heading=h.dj3mo9ry6uib)
- [Final report and handover doc task allocation](https://docs.google.com/document/d/1gMMOLYx4DYODtbyyi7Bw8Wz08PEu2aGY/edit)