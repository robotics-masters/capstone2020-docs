# Inidviudal work Yiran


### Week3 Fri - Week4 Mon

1. Communicate with the client and tutor to get a new project and Join discord̨
2. set up Simulator and Tensorflow
3. Reading materials to understand our project

### Week4 Tue- Fri

- [video link](https://youtu.be/XmacjpMjD_I)

1. Join group meeting and separate tasks
2. Sort out Wiki (Home and other wiki page setup based on the template given by tutor)
3. **Practice on TensorFlow image classification**
    -  Run model with the provided left and right sign data  based on the  tutorial Image Classification
    - [Model in jupyter notebook](https://github.com/YiranJing/Sign-Detection/blob/master/Yiran/history_code/TurnSign_Classification_17Sep.ipynb)https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/history_code/TurnSign_Classification_17Sep.ipynb
4. **Train Donkey Car model** using standard track
    - colllect raw data (around 3000 iamges) by driving car manually
    - Train model and the plot the accuracy result

### Week4 Sat - Week5 Mon

- **Model: Jupyter notebook Notebook link**: [Turn_and_Stop_Sign_Classification_21Sep](https://github.com/YiranJing/Sign-Detection/blob/master/Yiran/Turn_and_Stop_Sign_Classification_21Sep.ipynb)
https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/history_code/Turn_and_Stop_Sign_Classification_21Sep.ipynb
- [Video link](https://youtu.be/NJyp6R7ZGR0)


1. **Train model with four classes (right turn, left turn, stop, other.)** in larger dataset, using 260 colored images collected from both donkey car and online recoruses.
2. **Add classification report, and confusion matrix to evaluate individual class' performance**.  (the detail and discuession of the model can be found in the juputer notebook)
3.  Do some research on image classification model and also asked my stat3888 lecturer over weekend. Confirm that NN is the most successful model for image classification. 
4. CNN self-online learning (basic concepts)  (*havenot finish*)


### Week5 Tue - Week6 Mon

- [Video link](https://youtu.be/Pdbp4nOL8Lk)

#### **Finished tasks**:
1. Improve wiki pages based on tutor's feedback 
    - Convert scope statement into markdown, and link to home pages
    - Link all important docs on Wiki home page
    - Update week4 and 5 wiki page
2. Help team members improve signed map: Run donkey car on the newly signed map (with resolution = 240*240), then manually separate collected data into 3 classes "stop", "left" and "other". Based on the collect data, given feedback to team members to improve the map further.
3. **Train model on the new map with sign**: Run image classification model based on the sample data collected on the new map with the sign
    - Based on 270 images, including clear and unclear images
    - the model still get accuracy = 1. 
    - The Conclusion currently, is although the input images are not clear, but it is enough for the model to identify the sign. 
    - See [Model in Jupyter Notebook](https://github.com/YiranJing/Sign-Detection/blob/master/Yiran/Turn_and_Stop_Sign_Classification_28Sep-Based_on_new_signed_map.ipynb)https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/history_code/Turn_and_Stop_Sign_Classification_28Sep-Based_on_new_signed_map.ipynb
4. Get more familiar with myconfig.py, but fail to correct with others as hosting server.

#### Unfinished tasks (challenges):
5. Install [RM Racer lib](https://cdn.discordapp.com/attachments/756113778831261777/756113862675267595/week4-rmracerlib.zip.), and add `STOP_SIGN_DETECTOR = True`，but fail to drive car, meeting error *RuntimeError: No Edge TPU device detected*! Tried to install Edge TPU on my mac through docker, based on https://github.com/google-coral/edgetpu this website, still fails after 3 hours (terminal continually install and fail ). I seek help on Channel #donkey-platform. Will try to resolve it later on.
6. Leaderboard implementation 
    - The contents need to be recorded on Leaderboard: 
    - How many laps completed, the fastest time, if the car is still racing on the track (some users may join the server and disconnect. I want the leaderboard to be persistent), The name of the model/user who submitted the model.


### Week6 Tue - Week6 Sun
- [Model in jupyter notebook](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_2Oct.ipynb)
- [Video Link](https://youtu.be/6CO-E7Vt03I)
- [Video Link - CNN model demo](https://youtu.be/NEpj-uTg3Hk)

1. **Improve CNN model performance** based on the better evaluation rule: low misclassification cost: That is, If the model cannot detect the sign, then classified to “other”(i.e. no action). 
2. Collect and classify donkey data to fit model evaluation rule better.
3. **Test CNN model performance**: 
      - No overfitting
      - Achieve high accuracy overall (more than 90%) over 6700 trained images.
      - Achieve high correct prediction rate in individual classes. 
      - Low misclassification cost
4. Write wiki document about how to evalulate CNN model performance
      - [CNN_model_Evaluation](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/CNN_model_Evaluation)
5. Generate [python documentation for CNN model code](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/doc/model_train.html)
6. Contribution on the wiki and repo structure
      - Improve the scope statement on wiki page 
      - Reset historical data and current used data folder to another public link
      - Write technical documentation on wiki page
      - Update wiki video page and week6 wiki page
7. Writing the individual project report
8. Write the evaluation part of group project report with Yuanda
9. Take video for the demo



### Mid-Break - Week7 Mon
- [Model in jupyter notebook](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_11Oct.ipynb)
- [Video Link](https://youtu.be/3xD5ec7F6L8)

**Tasks done**:

1. Collect images based on the new map, and classify into 13 classes: 
       - "other", "stop", "right_blue", "right_black", "right_purple", "left_blue", 
          "left_black", "left_purple", "park_yellow", 'park_green', 
          'park_blue', "park_white", "speed_50_white"
1. Train new model into 13 classes
1. Update the new version of TF and donkeycar

**Questions need to seek help from client during the Monday Meeting**:

1. **The solution for the density of signs on the map**: The current map size is too small to put all kinds of signs in: 
       - can we have a new map with much larger size ?
       - or can we separate different signs into 2-3 maps? 
1. The sign's color is not clear to see: e.g. green park, yellow park, shall we adjust them?
1. **Shall we classify the model into main-classes, or subclasses?** 
       - i.e. should the model trade `green park` and `yellow park` as different classes or the same class. 
1. **Confirm the support documents, code, dataset need to give to client for the live meeting**. 
1. How to use the GPU you provide to us.


### Week7 Tues - Week8 Mon
- [Model in jupyter notebook](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_15Oct.ipynb)
- [Video Link](https://youtu.be/lp8B9a6NXHw)

1. Collect new images from 3 new created maps for model training 
1. **Train new model with 11 classes on TF**, and corporate with Yuanda to improve simulator accuracy based on the car's reaction.
1. Analysis issues within the model, then discuss with team members and client for the possible solutions to try in the following weeks.
1. **Try improving model based on client's suggestion**: Reduce and combine the number of classes and re-train the model.
1. Demo sign detection model on the first client deployment
1. Participate Q&A and demo sign detection model to tutor 

### Week8 Tues - Week9 Mon
- [re-train CNN Model combining real-world images](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_mainClass_24Oct.ipynb)
- [Test openCV from cp31-17a5 to label signs](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_testOpenCV_25Oct.ipynb)
- [Video Link](https://youtu.be/nntQoA_ZGRM)

1. Join the group meeting with the other two CP 33 groups, discussing model questions, and then share the dataset with them.
2. **Combine real-world images into the training model dataset** (To test if this method useful)
3. **Try the openCV algo from cp31-17a5 to label signs** (looks useful). 
4. Corporate with Yuanda and a group member from cp31-17a5 to improve openCV algo to fit better in our model and map.

### Week9 Tues - Week10 Mon
- [Video Link](https://youtu.be/ZBgl6bLZNFs)

1. Classify 5000+ images from new map, for CNN model training and testing
2. Adjust the different range of blue-color sign to fit better openCV result
3. Manually clean dataset after openCV, to train CNN mode better
4. Modify function given by cp31, **write `Object_Detection.py`, combine all different color sign detection**
5. **Build a new CNN model based on the processed images from openCV, also removed `other` class for more robust result**
6. Test model on different unity maps with Yuanda, and discuss other possible issues and solution with yuanda and client.
7. **Build local pytest (unity test) `evaluate_predictions.py` based on different situations**.


### Week10 Tues - Week11 Mon
- [Video Link](https://youtu.be/AdHaU4O7G_g)
- [openCV function for shenzhen images](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Shenzhen_OpenCV_5Nov.ipynb)
- [openCV + CNN model for shenzhen images](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/ShenzhenImages_Classification_6Nov.ipynb)
- [TFmodel.py](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/TFmodel.py)

1. Build function [TFmodel.py](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/TFmodel.py) for unit testing
2. Prepare the testing dataset for shenzhen images: manually filter thousands of Shenzhen images before and after openCV filter.
3. **Write new openCV function for the object detection of Shenzhen images**.
4. **Build new data pipeline using openCV and CNN model for shenzhen image classification**
5. Test the true success rate of the Shenzhen images, and discuss issues and possible solutions with client on discord, for further improvement. 


### Week11 Tues - Week12 Mon
- [Video Link](https://youtu.be/zU0vtKoXRBM)
- [new openCV function for unity map](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/unityModel/Object_Detection_Unity.py)
- [new CNN model, which is good for both Robotics Masters Challenge Track and F1 Track prediction](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/unityModel/sign_16Nov_4Classes.h5)

1. **With the help of yuanda, improve the openCV function for the object detection on unity map and F1 track**
2. collect, classify and clean more unity map images for model training.
3. Add black-turning sign for CNN model classification, and improve the model accuracy of the blue-turning sign.
4. **Corporate with Yuanda, get good real-time predictions on the F1 track**.
5. Corporate with yuanda to improve the testing pipeline built on bitbucket.


### Week12 Tues - Week13 Mon
- [video](https://youtu.be/Qvmi7Z04hxA)

1. Clean data and code, push to the repo for [Final release and documentation for Client](https://github.com/Yuanda-Dong/Client-Final-Deployment)
1. Took video for the [Final project report & presentation](https://www.youtube.com/watch?v=eCw6QChhvj4&feature=youtu.be)
1. Took video for the [Showreel](https://www.youtube.com/watch?v=VxKC9a5ixNI&feature=youtu.be)
1. Write parts of the final group report
1. Clean the Wiki page for the final submission. 
2. Corporate with Yuanda for the Client deployment and join client's Q&A part. 

****
****