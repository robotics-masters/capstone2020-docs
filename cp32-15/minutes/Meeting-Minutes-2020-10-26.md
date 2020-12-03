# Meeting Minutes 26/10/2020

**Subject:** Client Meeting

**Prepared by:** Jarod R

**Mode:** Zoom

**Date:** 6:45pm Monday October 26

**Attendees:** Jarod R, Ben L, Calum B, Zhaobo W

**Absent:** Will T, Manfred Ai


Notes:

* Tensorflow:
    * New model trained to work with very high accuracy on left/right blue turn signs, left/right black/blue rectangular signs, white/yellow park signs.
    * Previous model need worked on stop, black left/right turn and park sign. Once model is trained using the merged dataset, it should be able to detect everything listed here.
* Detection Lag:
    * Temporary "solution": Reduce donkey loop from 20Hz to 5Hz.
    * Problem assumed to be because the model (Resnet) is notoriously slow. We will focus on trying to implement a Yolo or Yolo Tiny model to remove the lag.
* Resolution:
    * Fix coming (pull requested) to change frame resolution from a config file rather than changing the unity settings and rebuilding.
* CodeCombat:
    * See Ben's discord [message](https://discord.com/channels/750412538637975633/750412538637975636/770149347177922580)
    * Three maps to test.
    * Google docs link has instructions.
    * Feedback form at the bottom.
    * Each person on our team should test one map.