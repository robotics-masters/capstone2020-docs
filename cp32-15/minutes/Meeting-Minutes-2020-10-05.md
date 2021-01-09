# Meeting Minutes 2020-10-05 #

**Subject:** Client Meeting, Status & Scope Additions New F1 Tracks

**Prepared by:** Ben L

**Mode:** Zoom

**Date:** 2020-10-05  Monday October 5

**Time:** 6:45pm

**Attendees:** Ben L, Client Cian, Jarod R

**Absent:** Calum B, Manfred A, Will T, Zhaobo W


Meeting Notes & Client requests:

**Pay particular attention to stared * lines they mark client requests**

* IMPORTANT for this Thur 8th at 5pm our client Cian requests a Live Demo of what we have working.

* There is a new version of donkeycar 4, we are asked to install use that.

* New donkeycar version is compatible with Tensorflow 2, we are asked to install use that.

* for existing tensorflow models of previous version recommend recreate new models in latest tensorflow with same data.

here is a script to convert your existing data tubs to new format
https://github.com/autorope/donkeycar/blob/dev/scripts/convert_to_tub_v2.py

* Cian asked if we had reviewed the new specifications he sent us?		Yes

* In it it says we need to model 2 new real tracks and a real car as specified.

Cian asked some questions to see what we have done
have we got our code in donkeycar working with the simulator?	Yes
Which signs have we modelled?		4. Blue Left & Right, Green Park & Stop

* Cian Requests we model the 2 other park signs (White and Yellow).

Cian doesn't mind if we don't model traffic lights as other team has done that.

* Cian Requests we model the black left and right arrows.

Have we got donkeycar responding to all the signs?		No We have it responding to Stop

Ben notes that it doesn't stop as well as it should, it reverses slightly and doesn't stop for long enough

Cian advises that stop is hard for everybody for all his other teams.

Ben advises that donkeycars current velocity is not available and that that is something that would be very benefical.
I think I had talked about donkeycat velocity with Cian before.

Cian will ask donkeycar developers about the velocity in donkeycar.

For our reports when need to show communication please use tables not screenshots, Cian feedback to other team that he doesn't like all the screenshots of communication. makes the report hard to read.

However if Tutor requires screenshots them Ben suggests putting them after the tables or at the end of the report.

communication log table fields:
date, start, length, link to minutes, attended by

email communication log table fields:
date, time, from, to, subject, description detail

talked about modelling a new real car in the simulator.

* regarding the new car in the simulator specifically the camera, he doesn't want the camera to be visible hovering over the car, so make it invisible.

We can use any assets we like in the simulator but they must be free.

Ben asked Cian about best practice of adding new tracks to the simulator.

Cian suggests starting with 1 large flat image like we did for track 1.

Ben asked about where to get topography data for the tracks, Cian suggests an F1 fanatic site.
Ben looked on google map topography but didn't seem very useful.

The topography of the track can be added later.

Ben advised that Calum had some issues training a driver for the track, that the resulting model was broken or corrupted, raising that there seems to be a weird occasional issue with the training software.

Cian asks which Tensorflow version and GPU or CPU version.

* Cian asks that we split up the work.

Ben read his notes to check had recorded everything and asked if there was anything anyone wanted to add.

Ben thought about reordering but think the original order is sensible.

Please advise if any issues.
