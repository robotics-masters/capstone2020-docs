# Individual Contribution Yuanda

## Week 3

* Communicate with course co-coordinator, tutor and clients to change our project from CP4 to CP32
* Established communication with new client
* Updated the format of Wiki page 
* Attended group meeting with client to discuss the project scope

## Week 4 

* Set up Tensorflow, Donkey car and Donkey car simulator environment on my PC. 
* Using the simulator, I trained a self-driving Donkey car model. See the video here https://youtu.be/d9mRQXM1_dc 
* Learned about how to use Tensorflow to train a neural network that classifies images. 
* Using the [tutorial!](https://www.tensorflow.org/tutorials/images/classification), i built a classifier that is able to classify stop/non-stop signs.
* Looked into how to run model training on Colab.
* See my weekly summary video here: https://youtu.be/1o-RmwG3IqA

## Week 5 

* Trained a neural network using the same model from last week, to classify [dataset](https://discordapp.com/channels/750412538637975633/753894317138903120/757404530915803177), and observed low accuracy measures ~ 20%. 

* Written documentation on [training neural network using Colab](https://bitbucket.org/RobertJia/comp3988_t17b_group1/wiki/Training%20neural%20network%20using%20google%20colab)

* Looked into and experimented with setting up servers for running donkey car races. Managed to get it working in LAN, but unable to host it on WAN due to ISP issues. 
* Implemented the code to classify a given directory of images, and write the class label on the image. Also, was able to produce a video from the labelled images.
* Modified rmracerlib so that the image detection code would work in the simulator, and printing out the class labels in real-time.  
* See my weekly update video here: https://www.youtube.com/watch?v=-Ea1S9x55oQ&feature=youtu.be

## Week 6 

* Collected more image data by manually driving in our custom map. 
* Trained an self-driving model using donkey car framework for our custom map. 
* Experimented and improved on the sign detection models for our custom map which has (stop, left, right, park, other) signs. 

* Continued to modify rmracerlib so that the donkey car reacts to the sign detected, involving stop, turn left, turn right behaviour. 
* See my weekly update video here: https://www.youtube.com/watch?v=hWSs6zBgu_s&feature=youtu.be

## Week 7 (Initial Client Deployment)

* Updated to Donkey car 4.0 module, and fixed some related bugs with simulator 
* Attended Venture Cafe event online with Mouyi Xu 
* Created another [bitbucket repository](https://bitbucket.org/Yuanda4228/comp3988-client-deployment/src/master/) for client deployment 
* Discussed with my team and we made decision to make another 2 maps with signs of different colours (to overcome the issue with having too many signs on one map)
* Collected training data from the new maps for both autonomous driving and sign detection module 
* Trained an autonomous driving model for new maps 
* Worked with Yiran to improve the sign classification model, I mainly do testing in the simulator
* Wrote deployment documentation for client 
* Moved everything for client deployment from google drive, Bitbucket site, to the dedicated repo for client deployment 
* Wrote the client deployment presentation slides with Hao Lan. 
* Attended the client deployment, and presented the introduction section before we start the actual Demo. 
* Demoed the sign detection + self-driving in simulator. 

## Week 8 

* Attended a inter-group meeting with the other CP32 teams, to exchange results, and set up server for data sharing 

* Tested sign detection model without ‘other’ class, and concluded it’s better to have ‘other’ class for full-frame detection. 
* Tested sign detection model without sub-classing, and concluded it’s better to not bother with sub-classing for full-frame detection. 
* Discussed with the client and CP31, to decide the next feature (to be implemented) for sign detection. We decided to adapt existing openCV code to extract the full-frame images, and do classifications on the extracted images. 
* Assigned work between Yiran and myself to implement this feature. In summary, Yiran will be working on building the image classification model; I’ll use that model and make it work in the simulator. 
* Discussed with client, @Wilson, Yiran on how to adapt the openCV code. 
* Looked at an alternative approach (other than openCV), which uses tensorflow only + Unity perception packages to generate synthetic data at scale. However, decided our team don’t have enough time to do this from scratch. 

## Week 9 

* Continue discussion with client, Yiran on how to adapt the openCV code. 
* Yiran built a prototype model for sign detection(using openCV), and i used the model, and made it work in the simulator.
* Attempted to draw real-time bounding boxes for signs in the simulator camera, but had some issues (to be discussed next week with the client)
* Manually classified 20000 images for Shenzhen track with Robert. Shenzhen track images will be used as the main test for our sign detection model.

## Week 10 

* Had a coding meeting with the client to try fix the bounding box issues, however it was not resolved, but the issue is posted to Donkey Car Discord. 
* Fixed the bounding box issue with the suggestion from @MaximeEllerbach
* Added pytest for model accuracy that will be used later on in testing pipeline. The test involves checking the diagonal/off-diagonal entries of the confusion matrix and precision, recall and f1-scores of the models’ performance on different test data.  

## Week 11

* Gave help to give to @CP32-aradhikaguha  and @CP32 - Thomas with their TensorFlow work
* Collaborate with @Yiran, we found a method (using colour picker) to change the upper/lower bound of OpenCV color filters,to overfit to given signs, and produce very good OpenCV extraction. 
* Using the new filters, We were able to get great sign detection results on F1 tracks, which shows the generalisation capabilities of our approach. 

## Week 12 (+ Final Client Deployment)

* Together with @Yiran, @LanHao, we created the demo for testing section of our project. Also I compiled everyone’s video together to produce the final demo video. https://youtu.be/U5xmpcQhekQ
* Created Github Repository dedicated for the final client deployment, and added final rmracerlib to the repo https://github.com/Yuanda-Dong/Client-Final-Deployment
* Together with @Yiran, we created a showWeel for the sign detection part of our project https://drive.google.com/drive/folders/18mV71fDfvLSkojq61_i8B7IqWVVNC85p?usp=sharing
* Present the project introduction and sign detection in simulator part of the client deployment. https://www.youtube.com/watch?v=6H6geVCDLH8
* Wrote the testing section of the group report, as well as doing some additional testing of sign detection.  https://docs.google.com/document/d/1pPQTqB6OSCoV3mSsRMsvVmgs9b68zqMQP2TM0W_YBM4/edit#













