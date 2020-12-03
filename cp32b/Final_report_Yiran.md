# Yiran Jing
This is the individual report for @YiranJing for the Final Report due Sun 20 November 2020. 

[Yiran‘s Report 1 on wiki](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Final_report_Yiran)

- **Unikey:** yjin5856
- **SID:** 460244129
- **Group name:** COMP3988_T17B_Group1
- **Client name:** Cian from Robotics Master

# Work done
## XP Roles

**Programmer (week 4-13)**

I have been involved in implementing the sign detection algorithm using a hybrid of OpenCV and Tensorflow, Collaborating with @Yuanda, we used OpenCV (colour based) to extract region of interest (ROI), then manually filtered the signs out. Then using this data, we have tuned a neural network that classify different traffic signs in the simulator environment.

I took the main responsibility for programming sign detection algorithm using Tenserflow and openCV, my main coding results: 

1. **CNN model** on both [unity map](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_Unity.ipynb) and [shenzhen track](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/ShenzhenImages_Classification.ipynb)
2. **OpenCV** implementation for object detection on both [unity map](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Object_Detection_Unity.py) and [shenzhen track](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Object_Detection_shenzhen.py)

**Tester (week 4-13)** 

We have continuously tests on multiple parts of sign detection, my testing work involves:

1. **OpenCV testing for image pre-processing (success rate of detect correct ROI):** 
To ensure our openCV function can abstract the ROI, we define the function `test_iamges` and every time when we run image preprocessing using [Object_Detection_Unity.py](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Object_Detection_Unity.py), it can calculate and automatically print the success detection rate of each class (folder). By doing so, we easily monitor our openCV functions’ performance under different cases (controlled by the input folder).

2. **Accuracy and confusion matrix of the sign detection model**, and improved our model based on that.
3. Collaborating with @Yuanda and @Lanhao, we build test pipeline on Bitbuckect. I provide [python script for model testing purpose](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/tests/). 
4. To improve real-time prediction performance based on the testing result, I have frequent discussion via Zoom and Discord with @Yuanda and also Client. 

**Data collector and engineering (week 4-13)**

1. Row data collection: I collect and classify thousands of donkey data to train mode better, and keep track all historical data, and maintain the data folder, also keep tracking the historical images (evidence in [appendix-E](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=229706166648464803623123&h2=Appendix-E---Data-folder-maint)).
2. Row image classification and manually filter data for further usage (evidence in [appendix-F](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=199987425769357942149450&h2=Appendix-F---Classifiy-and-Fil))
3. Provide data for [testing pipeline on bitbucket](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/tests/). 
4. Made the final dataset used for client deployment is [here](https://drive.google.com/drive/folders/1jGSZPrPlZ2ET9jY1pk_Af7OcWhweIO3J?usp=sharing)

**Wiki maintainer (since week 3-13)**

I take the response of organising our [wiki pages](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home), update weekly report, video on wiki. 

**Discord expert**

Instead of using Slack, our group has decided to use just one main communication platform with the client, Discord, which is also client’s preference. I have been using Discord to actively communicate with our client about our weekly progresses, and technical difficulties regarding to the project. (evidence in [appendix-C](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=172311170714606631255752&h2=Appendix-C---discussion-with-c))

**Doomsayer**

I took the responsibility for the object detection part, and raised any potential blockers, discuss during teem meeting (mainly with @Yuanda and Client)


## Weekly Plan  **(Week 7 - 13)**

[**The detail of my weekly process on my individual wiki page**](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/IndividualWork-Yiran).

**Week 7** 

- [Video link of mid-break work summary](https://www.youtube.com/watch?v=3xD5ec7F6L8&feature=youtu.be)
- [Video link of week 7 work summary](https://www.youtube.com/watch?v=3xD5ec7F6L8&feature=youtu.be)

| Task                                                                                                                                                                                                                                                   | Status | **Support Evidence**                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Collect images based on the new map, and classify into 13 classes                                                                                                                                                                                      | DONE   | [historical data in google drive](https://drive.google.com/file/d/1GrbPXBP3bVVn_8OMS3szBh3qRlKlYK0Z/view?usp=sharing)                                                                                                                                                                                                                                                                                                                                                |
| Analysis issues within the model, then discuss with team members and client for the possible solutions to try in the following weeks.                                                                                                                  | DONE   | [appendix-B](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=823391866695829362624726&h2=Appendix-B---discussions-and-c)                                                                                                                                                                                                                                                                             |
| **Try improving model based on client's suggestion**: Reduce and combine the number of classes and re-train the model: **Train new model with 11 classes on TF**, and corporate with Yuanda to improve simulator accuracy based on the car's reaction. | DONE   | [commit](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/101ce73bce8e7783e34c2e7c8b435022ff7c34ab#chg-sign_detection_code/Yiran/Sign_Classification_mainClass_24Oct.ipynb)[**101ce73**](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/101ce73bce8e7783e34c2e7c8b435022ff7c34ab#chg-sign_detection_code/Yiran/Sign_Classification_mainClass_24Oct.ipynb)<br>[pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/improve.png) |
| Participate Q&A and demo sign detection model to tutor                                                                                                                                                                                                 | DONE   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Demo sign detection model in the first client deployment                                                                                                                                                                                               | DONE   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Participate the preparetion of the first client document                                                                                                                                                                                               | DONE   | [first client deployment repo](https://bitbucket.org/Yuanda4228/comp3988-client-deployment/src/master/)                                                                                                                                                                                                                                                                                                                                                              |


**Week 8**

- [Video link of this week’s work summary](https://www.youtube.com/watch?v=nntQoA_ZGRM&feature=youtu.be)

| Task                                                                                                                                                | Status | **Support Evidence**                                                                                                                                                                                                                                                     |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Join the group meeting with the other two CP 33 groups, discussing model questions, and then share the dataset with them                            | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/inter.png)                                                                                                                                                                                              |
| Corporate with @Yuanda and @Wilson (a group member from cp31-17a5 )to improve openCV algo to fit better in our model and map.                       | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/wilson.png)<br>[Appendix-D](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=875658405578901077430498&h2=Appendix-D---discussing-and-co) |
| Combine real-world images into the training model dataset (To test if this method useful), and retrain the new model                                | DONE   |                                                                                                                                                                                                                                                                          |
| Corporate with @Yuanda, tested sign detection model without ‘other’ class, and concluded it’s better to have ‘other’ class for full-frame detection | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/other.png)                                                                                                                                                                                              |
| Test openCV from cp31-17a5 to label signs                                                                                                           | DONE   | [commitfee4180](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/fee4180167c39f34ad1193c697885a624c89c25d)                                                                                                                                                   |


**Week 9**

- [Video link of this week’s work summary](https://www.youtube.com/watch?v=ZBgl6bLZNFs&feature=youtu.be)

| Task                                                                                                                   | Status | **Support Evidence**                                                                                                                                                                                                                                                                                                                       |
| ---------------------------------------------------------------------------------------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Classify 5000+ images from new map, for CNN model training and testing                                                 | DONE   |                                                                                                                                                                                                                                                                                                                                            |
| Adjust the different range of blue-color sign to fit better openCV result                                              | DONE   | [pic](https://raw.githubusercontent.com/Yuanda-Dong/COMP3988-Evidence/main/continue2.png) [pic2](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/continue4.png)                                                                                                                                                                 |
| Manually clean dataset after openCV, to train CNN mode better                                                          | DONE   | [Appendix-G](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=661413142576807883212977&h2=Appendix-G---Work-on-OpenCV%2C-a)                                                                                                                                                 |
| Modify function given by cp31, write `Object_Detection.py`, combine all different color sign detection                 | DONE   | [committed 9919d98](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/9919d9882876cdbe5dfe90df88d06f746c9a9a12)                                                                                                                                                                                                                 |
| Build a new CNN model based on the processed images from openCV, also removed `other` class for more robust result     | DONE   | [committed f0b05ed](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/f0b05edde83067f365101210d5b55e975296bfb0)                                                                                                                                                                                                                 |
| Test model on different unity maps with Yuanda, and discuss other possible issues and solution with yuanda and client. | DONE   | [committed 1f9028e](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/1f9028eaa5edfc986248ee551c9f34a57da11813)<br>[committed ebcd60b](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/ebcd60b91cd0e303db11859a792fc5c8d523aac2)<br>[pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/continue.png) |
| Build local pytest (unity test) `evaluate_predictions.py` based on different situations.                               | DONE   |                                                                                                                                                                                                                                                                                                                                            |
| Retrain CNN model using the new dataset                                                                                | DONE   | [committed 78b0439](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/78b0439112e47da825d50e317ae77586b67666c5)                                                                                                                                                                                                                 |



**Week 10**

- [Video link of this week’s work summary](https://www.youtube.com/watch?v=AdHaU4O7G_g&feature=youtu.be)

| Task                                                                                                                                          | Status | **Support Evidence**                                                                                                                                                                                                                                     |
| --------------------------------------------------------------------------------------------------------------------------------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Build function TFmodel.py for unit testing                                                                                                    | DONE   | [committed de7bff8](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/de7bff848d01de2b5cc1611e80b2c41784453ec5)                                                                                                                               |
| Prepare the testing dataset for shenzhen images: manually filter thousands of Shenzhen images before and after openCV filter.                 | DONE   |                                                                                                                                                                                                                                                          |
| Build new data pipeline using openCV and CNN model for shenzhen image classification                                                          | DONE   | [committed 553e5be](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/553e5be447928c913b5fbba1cd84d8c08adf4c80)                                                                                                                               |
| Test the true success rate of the Shenzhen images, and discuss issues and possible solutions with client on discord, for further improvement. | DONE   | [Appendix-H](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=025114871459945044502868&h2=Appendix-H---Discussion-Shenzh)                                                                 |
| Create and give requirements.txt to @Hao for test pipeline building                                                                           | DONE   | [committed d64b274](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/d64b274a47ce72038f6d70b2b28db0e7d1411d5e)<br>[committed 553e5be](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/553e5be447928c913b5fbba1cd84d8c08adf4c80) |


**Week 11**

- [Video link of this week’s work summary](https://www.youtube.com/watch?v=zU0vtKoXRBM&feature=youtu.be)

| Task                                                                                                         | Status | **Support Evidence**                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------ | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| With the help of yuanda, improve the openCV function for the object detection on unity map and F1 track      | DONE   | [pic](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/help.png)                                                                                                              |
| collect, classify and clean more unity map images for model training, also discuss the process with client   | DONE   | [Appendix-I](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=668942379372643317784113&h2=Appendix-I---week-11-evidence) |
| Add black-turning sign for CNN model classification, and improve the model accuracy of the blue-turning sign | DONE   | [committed c6fd9bc](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/c6fd9bcb9b5f9c3692e3937a8423f79cb2cb9422)                                                              |
| Corporate with Yuanda, get good real-time predictions on the F1 track                                        | DONE   | [committed 519983f](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/519983f835a28f720e7d89d4432e6cff48974454)                                                              |
| Corporate with yuanda to improve the testing pipeline built on bitbucket                                     | DONE   |                                                                                                                                                                                         |
| Update shenzhen model using the new method                                                                   | DONE   | [committed c827d27](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/c827d270ce28be23b06a41b43e36f7b77fab127f)                                                              |


**Week 12** 

- [Video link of this week’s work summary](https://www.youtube.com/watch?v=Qvmi7Z04hxA&feature=youtu.be)

| Task                                                                                                                                                 | Status | **Support Evidence**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Took video for the [Final project report & presentation](https://www.youtube.com/watch?v=eCw6QChhvj4&feature=youtu.be) (model and code explaination) | DONE   | [video](https://www.youtube.com/watch?v=eCw6QChhvj4&feature=youtu.be)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Clean data and code, push to the repo for [Final release and documentation for Client](https://github.com/Yuanda-Dong/Client-Final-Deployment)       | DONE   | [Github](https://github.com/Yuanda-Dong/Client-Final-Deployment)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Prepare new document for testing purpose                                                                                                             | DONE   | [committed f597e41](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/f597e419fb6f1341e1798230dafecb73b66bbc5b)<br>[ab0b631](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/ab0b63148296bce127f43fe18c888a59e3959ce3)<br>[f98e8c9](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/f98e8c98aba1aa89d3ba230d11ead6b5d51ce307)<br>[ab0b631](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/ab0b63148296bce127f43fe18c888a59e3959ce3)<br>[4d22210](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/4d222108857fb2748881308323ceeaee2199d6aa) |
| Debug model, and ensure the lastest version will be submit                                                                                           | DONE   | [f78d485](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/f78d485d63d58133ce975d9f7fdcc9cde909602e)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Participate the preparetion of the final client document                                                                                             | DONE   | [a7a62cb](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/a7a62cbfd3baf42ed651bea4828e53e6bc0a9e73)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |


**Week 13**

| Task                                                                                    | Status | **Support Evidence**                                                                         |
| --------------------------------------------------------------------------------------- | ------ | -------------------------------------------------------------------------------------------- |
| Together with @Yuanda, we created a showWeel for the sign detection part of our project | DONE   | [video](https://www.youtube.com/watch?v=VxKC9a5ixNI&feature=youtu.be) (1.20 - 1.40)          |
| Clean the Wiki page for the final submission                                            | DONE   |                                                                                              |
| Participate the technical deployment with Client (Monday)                               | DONE   |                                                                                              |
| Corporate with @Yuanda for the Client deployment and join client's Q&A part (Thursday)  | DONE   |                                                                                              |
| Corporate with @Yuanda, wrote the testing section of the group report                   | DONE   | [link](https://docs.google.com/document/d/1pPQTqB6OSCoV3mSsRMsvVmgs9b68zqMQP2TM0W_YBM4/edit) |
| Move and format the final group report on wiki page                                     | DONE   | [link](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/FinalGroupProject)          |

**Evidence in links of the above statement**
All the links are entered in the weekly plan table so that it’s easy to find. Here, i provide more links for completeness.

1. Code repository: [https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/)
2. Commit history: [https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/)
3. Discord channel: [https://discord.gg/fVUS2wA](https://discord.gg/fVUS2wA)
4. Wiki homepage: [https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home)
5. Final client deployment codebase:[https://github.com/Yuanda-Dong/Client-Final-Deployment](https://github.com/Yuanda-Dong/Client-Final-Deployment)
# Quality of technical work done
## Pair Programming 

To ensure the correctness and good style of the model function, I did **Peer Code review and pair programming** via Zoom and Discord with @Yuanda. See [my repo folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/) and [yuanda’s folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yuanda/) of CNN model, we are following a consistent style and well-documented, and there are lots of improvements based on peer’s feedback. 

For example, in week 11, @Yuanda found some mistake of my code, and helped me fixed them. After that, our model performance improved a lot. (see evidence in [Appendix-J](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=091673303013742089880129&h2=Appendix-J---Evidence-or-pair-) )


## Bitbucket Testing pipeline

As I mentioned in the weekly plan, coorporate with @Hao and @Yuanda, we build test pipeline on bitbucket. I provide coding script and testing data, and requirement.txt for the testing purpose.


## Quality of Work Done as Programmer and Tester

As I have mentioned the detail in [XP role part](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=454977565008390470950279&h2=XP-Roles).
Also, in the client demo ([video here](https://www.youtube.com/watch?v=6H6geVCDLH8)), our client expressed very high satisfaction with the project result in video 1.22.00 after I answered his question.


## Software Engineering principles and CI/CD pipeline 

To ensure the coding correctness and continuous deployment with other team members (mainly @Yuanda and client).


1. Continuous integration code buildings (version control) with other team members through bitbucket (evidence in [appendix-A](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=211687109571398423698865&h2=Appendix-A---repo-commits))
2. Test openCV: To ensure our openCV function can abstract the ROI, I define the function `test_iamges` and every time when we run image preprocessing using [Object_Detection_Unity.py](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Object_Detection_Unity.py), it can calculate and automatically print the success detection rate of each class (folder). By doing so, we easily monitor our openCV functions’ performance under different cases (controlled by the input folder).
3. Test CNN model before deployment: Consider model has no overfitting, also evaluation accuracy using test dataset through normalised confusion matrix and classification report (consider F1, recall as well). (evidence in [Sign_Classification_Unity.ipynb](https://github.com/Yuanda-Dong/Client-Final-Deployment/blob/main/SourceCode/Sign_Classification_Unity.ipynb))
4. Integrated testing on openCV + CNN model: I test the misclassification ratio on the raw images, combining the openCV pre-processing and confidence level using function `*test_missclassification_images*` in [TFmodel_helper_function.py](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/TFmodel_helper_function.py). I also write testing function to visualize the misclassification images using `*draw_misclassification_images*`*.* 
5. Measure efficiency (running-time) of our algorithm: To ensure our new hybrid method can give the real-time prediction in the simulator without latency, I monitor the image preprocessing time for the whole dataset, and calculate the average running time, to ensure the algorithm can process more than 10 thousand images within 1 min. 
6. Continuous automated [testing pipeline](https://bitbucket.org/RobertJia/comp3988_t17b_group1/addon/pipelines/home) on bitbucket. As I mentioned above, I provide [python script for model testing purpose](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/tests/). 
7. Real-time testing through donkey car simulator. @Yuanda modified [rmracerlib](https://github.com/Yuanda-Dong/Client-Final-Deployment/tree/main/rmracerlib) library based on the CNN model (.h5) I provide to him. To debugging and improve donkey car performance, I have multiple meeting with Yuanda via zoom and discord channel.  


## Challenge

**OpenCV filter challenge**

Since week 7 we decide to use openCV for preprocessing. But it is hard for us to start this new tool, so I start with learning other team’s code, see evidence in [appendix-D](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=875658405578901077430498&h2=Appendix-D---discussing-and-co). Later on, our team found the code provided by other team doesn't fit well in our case, so I start to try to write our own openCV code script in week 9 [committed 9919d98](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/9919d9882876cdbe5dfe90df88d06f746c9a9a12). We had many meetings with the client to discuss the code before we can fully use it for our purposes. (See evidence in [appendix-k](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=516404843045708754288067&h2=Appendix-K---Challenge-1:-open)).  Finally, I get good openCV result with the help of client and @Yuanda.  As I memtioned above, pair coding with @Yuanda helps me find the mistake in my openCV functions.

**Shenzhen Track challenge**

I met lots of challenges on the shenzhen track testing. I seek help from team member, also ask suggestions from client (see evidence in [appendix-L](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=352787246650939459501200&h2=Appendix-L---Challenge-2:-shen)). Then I tried to build new data pipeline using openCV and CNN model for shenzhen image classification ([committed 553e5be](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/553e5be447928c913b5fbba1cd84d8c08adf4c80)).  Finally, I report the shenzhen track result in the Q&A part of client demo, our client expressed very high satisfaction with the project result in [video 1.22.00](https://www.youtube.com/watch?v=6H6geVCDLH8) after I answered his question.

**Data cleaning and labelling**

We had to manually label the class label (stop, left, right, park, other) for each new map, and I also have to filter images, maintain the good quality of training data,  which requires a lot of time and patience devoted.

**Other challenges**

- **late start**: We changed from *Object Oriented Architecture design for bioreactor user interface and control software system* to CP32 at the end of week 3. This has caused some challenges in schedule, we had to work hard to deliver the user stories for each sprint on a timely manner.
- **Software environment**: To actually start experimenting and developing models for donkey car self-driving and sign detection, we need to install the required environment including TensorFlow, Donkey car, Gym Donkey, Donkey car simulator, Unity and Blender(for building tracks). Now, this has posed some significant challenges for us early on in the project, because the documentation on donkey car was not accurate and due to different computer platform Windows, Linux, Macos that we have in the team.


# Contributions
## Technical development 

Since my main task is training the image classification model using tensorflow and openCV, the code quality includes not only the correctness and good style, but the evaluation on the model and openCV performance.

To ensure the correctness and good style of the model function, I did **Peer Code review and pair programming** via Zoom and Discord with @Yuanda. See [my repo folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/) and [yuanda’s folder](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yuanda/) of CNN model, we are following a consistent style and well-documented, and there are lots of improvements based on peer’s feedback. 

[The quality of coding and testing has been mentioned above.](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=590784533111143308400329&h2=Quality-of-Work-Done-as-Progra) 


## Non-technical contribution to group processes

**Wiki maintainer**
I have played a key role in organising our [wiki page](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home) as Wiki maintainer, also keep tracking weekly wiki page, move and format the final group report on wiki page ect. The evidence has been attached in the weekly plan.

**Video demo**
As mentioned in the weekly plan table (week 12-13), I join the video creation of showWeel, Final project report & presentation. 

**Client demo and Q&A**
I participate the client demo on Thurday week 13,  and join Q&A part, evidence in [video 1.20](https://www.youtube.com/watch?v=6H6geVCDLH8)

**Client communication**
There are lost of evidence of my communication with client on discord (see evidence in [appendix-C](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=172311170714606631255752&h2=Appendix-C---discussion-with-c), F, J, H, I, J, K, L)

**Final report contribution**
I took responsibility of work and quality part of our final group report.

**Evidence of collaboration and teamwork**

The weekly meeting minutes and status report on [wiki page](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home) can show our team collaboration. Also, there are evidence of [collaboration with other team](https://github.com/Yuanda-Dong/COMP3988-Evidence/blob/main/inter.png) as well.  Also, have mentioned above, I did **Peer Code review and pair programming** via Zoom and Discord with @Yuanda. There are lots of collaboration evidence in the weekly plan table.


# Reflections 

**Version Control, Coding styles**
In week 7 - 13, my code is written in jupyter notebook for CNN model training and testing. I use Version Control to keep tracking multiple version of model tests and resolve the conflicts among team members. We use jupyter notebbok for CNN model training, since it can deploy model on a remote server using GPU, and allows us to present our models results among ourselves.

**Extreme Programming** 
The team has been using the principles of XP throughout the current lifespan of the project. We collaborate efficiently under the monitor of tracker and manager. We also documented all of the acceptance testing while adhering to the principles of XP programming. [All processes are documented on wiki page](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Home). Therefore, our teams works successfully in identifying key elements to helped us track project, and improve the results.

- Scope planning: Even if client update scope and add more task in week 7 and week 10, but we did well, and finish all the tasks he required.
- Close interaction with client: each week, we have two group meetings with the client. Frequently the meeting holds more than 15 mins,  as not only update our work, but also discuss key issues and try to find some solution together during the meeting. Also, we communicate with the client on Discord on a daily basis.
- Pair programming and code review: I did **Peer Code review and pair programming** via Zoom and Discord with @Yuanda. This has been really helpful in improving our models’ accuracy, and understanding how our code are going to interact with each other, specifically, the OpenCV + TensorFlow sign detection model drives the behaviour of the donkey car in the simulator.

**Collaboration with client is critical to make the project successful**
There are lost of unaware challenges and issues in the project, also it is important to maintain the scope, meet the client’s requirement all the time. Thus, corporate and communicate with client is key to make the project successful.

Also, during week 10-12, I seek help from client for the openCV algorithm building, and he turly gave me useful hints.

**Improve team work based on feedback from Tutor**
We have also received feedback on testing methodologies from our Tutor. Before that, we didn't realised that how important to build automatic test pipeline. However, after we build test pipeline on bitbucket, we benefit a lot, since it can monitor coding correctness and quality efficiently. 


## Challenges

I have mentioned in [Quality of work done](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=030727707645300289997800&h2=Challenge)


## Role As a Software Developer

My main role as a software engineer involve [coding](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/) (TensorFlow image classification), and test model through multiple ways. Also generated [Python Documentation](http://v).

As I mentioned in section [SE and CI/CD pipeline](https://www.dropbox.com/scl/fi/4rfzgmlse86rlmew4koga/Yiran-Jing.paper?dl=0&rlkey=qt8uorxq0evy3zr3uaia5n102#:uid=938147347269754617543169&h2=Software-Engineering-principle), my work also involves Continuous integration code buildings (version control), unit tests, Integrated tests, measure efficiency (running-time) of our algorithm


## How the final project delivered as expected

Our client expressed very high satisfaction with the project result in the final client demo(see [video 1.22.00](https://www.youtube.com/watch?v=6H6geVCDLH8)).


## Further Improvements

Our project has been quite successful considering very short time frame (started at the end of week 3). Our team has good group communication, and the team dynamics for our group also has improved a lot in this short-term, specifically we have practised XP as a group with diverse range of skill sets and learnt how to combine everyone’s contribution to a unified product.  In terms of technical improvement of sign detection model, I think the model should focus more on the image pre-processing (ensure and improve data quantity and quality). 


# Appendix
## Appendix A - repo commits

[Link to repo commits](https://bitbucket.org/RobertJia/comp3988_t17b_group1/commits/)

![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606434321801_Screen+Shot+2020-11-27+at+10.45.10+am.png)

![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606434340720_Screen+Shot+2020-11-27+at+10.45.35+am.png)

## Appendix B - discussions and collaborations with my team members 

[Discord channel](https://discord.gg/fVUS2wA)

![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606427572251_Screen+Shot+2020-11-26+at+11.28.10+pm.png)



## Appendix C - discussion with client  

[Discord channel](https://discord.gg/fVUS2wA)

![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606390241275_Screen+Shot+2020-11-26+at+10.30.37+pm.png)

## Appendix D - discussing and collaborating with other team

[Discord channel](https://discord.gg/fVUS2wA)

![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606390969940_Screen+Shot+2020-11-26+at+10.42.37+pm.png)



## Appendix E - Data folder maintainer
![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606388390350_Screen+Shot+2020-11-26+at+9.59.46+pm.png)



## Appendix F - Classifiy and Filter data for further model process
![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606388734128_Screen+Shot+2020-11-26+at+10.05.31+pm.png)

## Appendix G - Work on OpenCV, and discuss with Client and yuanda
![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606444890348_Screen+Shot+2020-11-27+at+1.41.23+pm.png)

## Appendix H - Discussion Shenzhen-track with Client
![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606501139587_Screen+Shot+2020-11-28+at+5.18.55+am.png)

## Appendix I - week 11 evidence
![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606501516543_Screen+Shot+2020-11-28+at+5.25.05+am.png)

## Appendix J - Evidence or pair coding
![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606390012683_Screen+Shot+2020-11-26+at+10.26.49+pm.png)

## Appendix K - Challenge 1: openCV 
![](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606444994967_Screen+Shot+2020-11-27+at+1.42.58+pm.png)

## Appendix L - Challenge 2: shenzhen track
![User-uploaded image: Screen+Shot+2020-11-26+at+10.07.24+pm.png](https://paper-attachments.dropbox.com/s_D4F6065FC9DADD6902AF0D166E852522C984549F567651E94FC9CECF4FDA8AAE_1606388881889_Screen+Shot+2020-11-26+at+10.07.24+pm.png)