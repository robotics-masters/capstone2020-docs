# Yiran Jing
This is the individual report for @YiranJing for the First Report due Sun 3rd October 2020.

# Work done
## XP Roles

Main XP roles undertaken are listed as:

- **Programmer** (since week 4): As a programmer, I implement the sign detection algorithm [CNN model code on repo](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/) 
- **Tester** (since week 4): Test the image classification model performance, and provide feedback

       - [The explanation of model evaluation on wiki](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/CNN_model_Evaluation)
       - [The CNN model test data and code on repo](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/test/Test-CNN/)
       - Provide the feedback of model testing result ([issue 21](https://yuanda-dong.atlassian.net/browse/CP-21), [11](https://yuanda-dong.atlassian.net/browse/CP-11?atlOrigin=eyJpIjoiNzhkNmMyYTAwMWJmNDBiOWIxZGZjMTAwMzc3ZjVjNDIiLCJwIjoiaiJ9), [12](https://yuanda-dong.atlassian.net/browse/CP-12?atlOrigin=eyJpIjoiZTM3Njk4ZTY1OTI2NGYxMDhhOTdiMGM4MTI3YTlkMDIiLCJwIjoiaiJ9))

- **Wiki maintainer** (since week 3): I take the response of organising our [wiki pages](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home), update weekly report on wiki. 
- **Data collector and engineering** (since week 4): I collect and classify thousands of donkey data to train mode better, and keep track all historical data [here](https://drive.google.com/drive/folders/1jGSZPrPlZ2ET9jY1pk_Af7OcWhweIO3J?usp=sharing).

These are the main roles I undertook and work I completed each week, and I was also **Tracker** in week3 and **Doomsdayer** in week 2. 

## Weekly Plan

The changes in project topic (from CP4 *Object Oriented Architecture design for bioreactor user interface and control software system* to CP32 *Implement Sign Detection using TensorFlow) occurred at the end of week 3.* So my weekly plan started from Friday week 3 as well.

[**The detail of my weekly process on my individual wiki page**](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Yiran). 

| **Week**              | **Work done**                                                                                                                                                                                                                                                                                                   | **Video for work demo**                                                                                        | **Code for work demo**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | C**hallenges**                                                                                                                                                                                           |
| --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Week3 Fri - Week4 Mon | 1. Communicate with the client and tutor to get new project and Join discord̨ 2. set up Simulator and Tensorflow 3. Reading materials to understand our project                                                                                                                                           | No, since the project just start.                                                                              | No, mainly setup Simulator and Tensorflow, no code writing needed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 1. Understanding CNN model algorithm                                                                                                                                                                     |
| Week4 Tue- Week4 Fri  | 1. Sort out Wiki (Home and other wiki page setup based on the template given by tutor) 2. Practice on TensorFlow image classification. 3. Train Donkey Car model using standard track                                                                                                                     | [video link](https://youtu.be/XmacjpMjD_I)                                                                     | [Model in jupyter notebook](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/history_code/TurnSign_Classification_17Sep.ipynb)                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1. Try image classifiction on more kinds of signs                                                                                                                                                        |
| Week4 Sat - Week5 Mon | 1. Train model with four classes (right turn, left turn, stop, other.) in larger dataset 2. Add classification report, and confusion matrix to evaluate individual class' performance 3. CNN self-online learning                                                                                         | [video link](https://youtu.be/NJyp6R7ZGR0)                                                                     | [Model in jupyter notebook](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/history_code/Turn_and_Stop_Sign_Classification_21Sep.ipynb)                                                                                                                                                                                                                                                                                                                                                                                                                                                          | No                                                                                                                                                                                                       |
| Week5 Tue - Week6 Mon | 1. Improve wiki pages based on tutor's feedback 2. Update week 4 &5 wiki page 3. Help team members improve signed map and collect new data to train the model 4. Train model on the new map with signs.                                                                                                | [video link](https://youtu.be/Pdbp4nOL8Lk)                                                                     | [Model in jupyter notebook](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/history_code/Turn_and_Stop_Sign_Classification_28Sep-Based_on_new_signed_map.ipynb)                                                                                                                                                                                                                                                                                                                                                                                                                                  | 1. For the task of Virtual race League, failed to correct with others as hosting server. 2. Unsolved issues on Leaderboard implementation([issue 13](https://yuanda-dong.atlassian.net/browse/CP-13)) |
| Week6 Tue - Week6 Fri | 1. Improve CNN model performance based on the better evaluation rule 2. Collect and classify donkey data to fit model evaluation rule better 3. Test CNN model performance and write up documents 4. Write technical documentation on wiki page 5. Generate python documentation for CNN model code | - [video link](https://youtu.be/6CO-E7Vt03I) - [video link of CNN model demo](https://youtu.be/NEpj-uTg3Hk) | - [Model in jupyter notebook](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_2Oct.ipynb) - The explanation of model evaluation [on wiki page](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/CNN_model_Evaluation) - The CNN model test data and code [on repo](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/test/Test-CNN/) - [Data drive](http://more than 10 thousand data) - Python documentation [repo link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/doc/model_train.html) | No                                                                                                                                                                                                       |



# Contributions
## Technical development 

Since my main task is training the image classification model, the code quality includes not only the correctness and good style, but the evaluation on the model performance.

To ensure the correctness and good style of the model function, I did **Pee Code review and pair programming** via Zoom and Discord with @Yuanda. See [my repo folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/) and [yuanda’s folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yuanda/) of CNN model, we are following a consistent style and well-documented, and there are lots of improvements based on peer’s feedback. 

I evaluate model performance mainly based on the stability and accuracy. Firstly, we test the model has no overfitting, which means that the test accuracy using new images (test data) is close to the evaluation accuracy achieved during model training. Secondly, we test our model structure can achieve the highest test accuracy and based on the hyper-parameter turning result. Thirdly, we test our model has low misclassification cost. That is, If the model cannot detect the sign, then classified to “other”(i.e. no action). Fourthly, I evaluate model performance based on the confusion matrix and the classification report. 

- [The detail of image classification model evaluation on wiki page](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/CNN_model_Evaluation)
- [Jupyter notebook link for the CNN model testing](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_2Oct.ipynb)
- Evidence of my repo commits are in [appendix-A](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Untitled-2.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=211687109571398423698865&h2=Appendix-A) 
- Feedback of model testing result ([issue 21](https://yuanda-dong.atlassian.net/browse/CP-21), [11](https://yuanda-dong.atlassian.net/browse/CP-11?atlOrigin=eyJpIjoiNzhkNmMyYTAwMWJmNDBiOWIxZGZjMTAwMzc3ZjVjNDIiLCJwIjoiaiJ9), [12](https://yuanda-dong.atlassian.net/browse/CP-12?atlOrigin=eyJpIjoiZTM3Njk4ZTY1OTI2NGYxMDhhOTdiMGM4MTI3YTlkMDIiLCJwIjoiaiJ9))


## Non-technical contribution to group processes

I have played a key role in organising our [wiki page](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home) as **Wiki maintainer**, also keep tracking weekly wiki page (weekly wiki report on [week 5](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Week5), [week 4](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Week4), [week 3](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Week3)) and video summaries, and I wrote status report in week 3 ([issue 9](https://yuanda-dong.atlassian.net/browse/CP-9)). Additionally, I helped my team member to improve signed map (evidence in [appendix-B](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Untitled-2.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=823391866695829362624726&h2=Appendix-B---discussions-and-c)). Moreover, I am keeping discussion with client on discord frequently (evidence in [appendix-C](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Untitled-2.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=172311170714606631255752&h2=Appendix-C---discussion-with-c)).

# Reflections

**Programming, Version Control, Coding styles**
From week 3 to week 6, my code is written in jupyter notebook and Colab for CNN model training and testing. And I are also working on the code of donkey car simulator libraries. I use Version Control to keep tracking multiple version of model tests and resolve the conflicts among team members. We use jupyter notebbok for CNN model training, since it can deploy model on a remote server using GPU, and allows us to present our models results among ourselves.

However, the size of our repository has grown almost at its limit of 2 GB, because the dataset we used for training was quite large. And thus, we have moved our dataset to the google drive storage.

**Extreme Programming** 
The team has been using the principles of XP throughout the current lifespan of the project. We collaborate efficiently under the monitor of tracker and manager. We also documented all of the acceptance testing while adhering to the principles of XP programming. [All processes are documented on wiki page](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home). Therefore, our teams works successfully in identifying key elements to helped us track project, and improve the results.


## Challenges

There are main challenges our group meet and trying to resolve in the following weeks

**Challenge 1: Limitations of the CNN model (**[**issue 11**](https://yuanda-dong.atlassian.net/browse/CP-11)**)**

1. No data cleaning and feature engineering in the image pre-processing, Will try to add them to improve mode performance further.
2. Dataset limitation: The current dataset is collected based on one map. We will add more kinds of maps' data in the next few weeks.
3. Should consider better hyper-parameter turning tech: The CNN hyper-parameter turning currently just focus on the number of layers, the number of epochs, will try more advanced techniques in the next few weeks.

**Challenge 2: Leaderboard implementation (**[**issue 13**](https://yuanda-dong.atlassian.net/browse/CP-13)**,** [**issue 26**](https://yuanda-dong.atlassian.net/browse/CP-26)**)**
We need to implement a dashboard for the Virtual race League like the one shown in the simulator except as a web-based interface. We found difficulties to implement it in week 5, and asked client relevant questions ([appendix-D](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Untitled-2.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=875658405578901077430498&h2=Appendix-D---discussing-with-t)). After confirming with client, this challenge will be resolved in week 7-8.

**Challenge 3: Detect more signs in the following weeks (**[**issue 24**](https://yuanda-dong.atlassian.net/browse/CP-24)**)**
After confirming with client, also mentioned in [issue 11](https://yuanda-dong.atlassian.net/browse/CP-11) and [issue 17](https://yuanda-dong.atlassian.net/browse/CP-17), we will add more signs and build new tracks. Then train the new model based on more kinds of maps' data in the next few weeks.


## Role As A Software Developer
- As mentioned above, my role as a software engineer involve [coding](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/) (TensorFlow image classification), and [testing](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/test/) model performance on Colab. Also generated [Python Documentation](http://v).
- Collaborating and helping my team members to build better map (evidence in [appendix-B](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Untitled-2.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=823391866695829362624726&h2=Appendix-B---discussions-and-c))
- Discussing with the client about the leaderboard implementation for the Virtual race League. The evidence can be found in [appendix-D](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Untitled-2.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=875658405578901077430498&h2=Appendix-D---discussing-with-t). 


## Further Improvements

Our project has been quite successful considering very short time frame (started at the end of week 3). Our team has good group communication, and the team dynamics for our group also has improved a lot in this short-term, specifically we have practised XP as a group with diverse range of skill sets and learnt how to combine everyone’s contribution to a unified product. In the future, we will try to meet the clients’ requirement better, and collaborate more efficiently.

# Appendix
## Appendix A - repo commits

[Link to repo commits](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/)

![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1601735870877_Screen+Shot+2020-10-04+at+12.37.44+am.png)

## Appendix B - discussions and collaborations with my team members 

[Discord channel](https://discord.gg/fVUS2wA)

![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1601736280684_Screen+Shot+2020-10-04+at+12.44.35+am.png)



## Appendix C - discussion with client

[Discord channel](https://discord.gg/fVUS2wA)

![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1601736513462_Screen+Shot+2020-10-04+at+12.48.28+am.png)

## Appendix D - discussing with the client about the leaderboard implementation

[Discord channel](https://discord.gg/fVUS2wA)

![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1601776367076_Screen+Shot+2020-10-04+at+12.52.42+pm.png)