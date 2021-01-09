# Client Handover Document 
## Project Title: Implement sign detection using TensorFlow
**COMP5615 Group 2**

## Project Description

Our main task is to make a car drive autonomously in a simulator, specifically taking action upon detection of traffic signs or lights. The car will drive on its own and turn when it detects right/left turn signs, stop when it detects stop sign and act accordingly to other signs and traffic lights.

---

## Prerequisites to run TensorFlow code in Jupyter notebook

1. pip install keras
2. pip install livelossplot
3. pip install tensorflow==2.3.0
4. pip install efficientnet

## Documents

- [Initial Requirement](https://bitbucket.org/aradhikaguha/comp5615-group-2/downloads/CP32_-_Scope_and_Requirements_Document_September_2020.pdf)
- [Updated Requirements](https://bitbucket.org/aradhikaguha/comp5615-group-2/wiki/Requirements)
- [Simulator Further Requirement](https://bitbucket.org/aradhikaguha/comp5615-group-2/downloads/CP31_and_CP32_-_Further_Scope_Information_for_Simulator.pdf)


## Code & Respository
[BitBucket Repository Link](https://bitbucket.org/aradhikaguha/comp5615-group-2)

```
Branch outline  
simulator, this contains all the file related to unity, it can be set as project in unity
aradhika_new, this contains all the tensorflow code.
driving_joko, this contains all the file related to the python donkeycar, this also contain code to train the TensorFlow (i.e. aradhika and aradhika2 folder, train_binary.py and train_multiple.py, it already contains the data and folder structure for training)
```

---
## Team Members & Tasks

| Name | Primary Email | Core Role(s) Tasks |
|--|--|--|
| Joko Wijaya | jwij4042@uni.sydney.edu.au | Unity (Tracks, Car, Menu), Python donkeycar|
| Aradhika Guha | aguh5894@uni.sydney.edu.au | TensorFlow (Model, Data, Training, Testing)|
| Thomas Porcaro | tpor9095@uni.sydney.edu.au | Unity (General), Python donkeycar, TensorFlow (Python Script)|

## Video Summaries

### Weekly Updates
| Week | Joko | Aradhika | Thomas | 
|--|--|--|--|
| 4 | [YouTube](https://youtu.be/xGHSXvVktTk) | [YouTube](https://youtu.be/3fcn_Df-oqY) | [YouTube](https://youtu.be/hoGmuo-ZAJU) | 
| 5 | [YouTube](https://youtu.be/UkV4nGqSdpg) | [YouTube](https://youtu.be/a7EtxPSWPDg) | [YouTube](https://www.youtube.com/watch?v=ZADoUJ_QepU) | 
| 6 | [YouTube](https://youtu.be/kFlkRNg6rCw) | [YouTube](https://youtu.be/ohnd6sSqa8M) | [YouTube](https://youtu.be/IxYLI0l24PM)| 
| 7 | [YouTube](https://youtu.be/Gxy0pJX7dnE) | [YouTube](https://youtu.be/k60nzDyjlH4) | |  
| 8 | [YouTube](https://youtu.be/jhOGZpQ26y8) | [YouTube](https://youtu.be/9pKCM1M3gdk) | | 
| 9 | [YouTube](https://youtu.be/eQQ-kmLiuoM) | [YouTube](https://youtu.be/PS6giYmYpkM) | [YouTube](https://youtu.be/1S4dJs9LVFU) | 
| 10 | [YouTube](https://youtu.be/PFzGlrbEJXA) | [YouTube](https://youtu.be/Q3BXgYGMq2M) | | 

### Major Milestones

| Description | Video |
|--|--|
| Client Deployment (Week 7) | [YouTube](https://www.youtube.com/watch?v=PSn722ziqSE)
| Unity Workshop (Week 10)| [YouTube](https://www.youtube.com/watch?v=dI-CaKepWIA)|


---
## Documentation

* [How to compile the simulator](https://bitbucket.org/aradhikaguha/comp5615-group-2/wiki/How%20to%20compile%20simulator)
* [How to connect to the simulator](https://bitbucket.org/aradhikaguha/comp5615-group-2/wiki/Connecting%20to%20the%20Simulator)
* [How to add track](https://bitbucket.org/aradhikaguha/comp5615-group-2/wiki/Documentation%20on%20how%20to%20add%20track)
* [How to add asset](https://bitbucket.org/aradhikaguha/comp5615-group-2/wiki/Documentation%20on%20how%20to%20add%20asset)
* [Image classification Using Tensorflow](https://bitbucket.org/aradhikaguha/comp5615-group-2/wiki/Image%20Classification%20Using%20Tensorflow)
* [Avoiding overfitting in multiclass tensorflow code](https://bitbucket.org/aradhikaguha/comp5615-group-2/wiki/Avoiding%20overfitting%20and%20increasing%20accuracy) 
 
 
## Goal & Deliverables

* Only 4 new circuits will be implemented.
* 1 model of car (F1 car) will be created.
* Only 6 traffic signs will be modelled.
* Actions that need to be done are turning left, right, stop and park.
* Tensorflow model needs to be able to successfully detect left , right , stop , speed and park signs ( total = 6 signs with different color)


## Testing Results

Overall accuracy of TensorFlow model is above 90%. Hence , it is able to detect traffic sign images correctly into their respective classes with an accuracy as high as 90%.