# Meeting Minutes 29/10/2020

**Subject:** Tutorial

**Prepared by:** Jarod R

**Mode:** Zoom

**Date:** 5:00pm Monday October 29

**Attendees:** Jarod R, Ben L, Will T,  Calum B, Zhaobo W

**Absent:** Manfred Ai


Notes:

* Brut Server
    * Now has 4 GPUs for training
    * Let other teams know when we're using the server to train
* Tensorflow
    * Will reduced the lagging issues by properly configuring the GPUs, still using Resnet
* Jetson Nano
    * Cian to set up a Jetson Nano to deploy the current setup and test that our current system will run on the limited hardware. Testing to most likely take place on Saturday afternoon.
* Testing (see Cian's email)
    * Json file for each of the 100 images.
    * Does not need to be completely automated.
    * Filenames could contain the expected result, can then use this to confirm whether the detection was successful.
    * CP32B has an existing testing framework similar to what Cian wants. They have a script that can check whether the model successfully detected the sign or not.
* Timeline from email
    * Extend the "10 day" timeline 7 days, so the final completed work should be ready by the end of week 11.
* Track Altitude
    * Waiting for Joseph's response on Discord to advise on how to do this based on an asset.