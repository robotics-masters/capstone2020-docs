USYD Capstone 2020

# CP31 & CP32 –

# Further Scope Information for Simulator

Updated: 2020- 10 - 04 23 : 40 PM

This document is to provide a detailed update on the ‘Simulator Improvements’ section of the
project requirement provided at the start of the semester.

This document affects all teams using the Donkey Car Simulator.

**Teams**

```
Project
ID
Project Name Team Name Team Short
Code
```
##### CP

```
Sign Detection using
Computer Vision
COMP3888_T13A_Group5 CP31-13A
```
##### CP

```
Sign Detection using
Computer Vision COMP3888_T17A_Group5^ CP31-17A^
```
```
CP32 Sign Detection with
TensorFlow
COMP3888_T15A_Group4 CP32-15A
```
##### CP

```
Sign Detection with
TensorFlow
```
##### COMP5615_GROUP2 CP32-17A

```
CP32 Sign Detection with
TensorFlow
COMP3988 T17B Group 1 CP32-17B
(CP32B)
```

## Contents

- USYD Capstone
- Scope & Requirements
   - High-Level Scope Summary
- Simulator Tracks
      - Team Track Allocations
      - Judgment Criteria
   - Track 1 - Nurburgring GP Circuit (F1)
   - Track 2 - Monaco GP Circuit (F1)
   - Track 3 - Marina Bay Street Circuit (F1)
   - Track 4 - Autodromo Algarve GP Circuit (F1)
   - Track 5 - Circuit of Americas GP Circuit (F1)
   - Track 6 - Circuit de Spa-Francorchamps (F1)
   - Track 7 - Baby Park (Mario Cart)
   - Track 8 - Sydney Motorsport Park Brabham Circuit
   - Track 9 - Albert Park GP Circuit (F1)
   - Track 10 - Shanghai GP Circuit (F1)
- Simulator Car Models
- Further Reference Material


USYD Capstone 2020

## Scope & Requirements

This project is broken into two challenge and problem components that are closely related.

**Challenge & Problem 1:** Simulator improvements.

**Challenge & Problem 2 :** Sign, Path & Object Detection

### High-Level Scope Summary

- **Milestone 1 – Simulator Additions (Week 3)**
    1. Add two new track layouts (outlined in email)
    2. Add objects to map
- **Milestone 2 – Simulator Enhancements (Week 9)**
    1. Improve and documented new fast way to import new track layouts
    2. Add up to two additional (four total) track layouts to simulator and document
       process
    3. Further improvements and documenting for placing objects (signs, traffic lights,
       objects)
- **Milestone 3 – Computer Vision minor sign detection (Week 6)**
    1. Improve existing solution (provided code)
    2. Research and Document improvements, show results
    3. Demo on sample data and in simulator (different environments)
    4. Add extra objects for detection not in original solution
- **Milestone 4 – Computer Vision major detection (Week 9)**
    1. All outlined signs detected and corresponding action response
    2. Demo on sample data and in simulator (different environments)
    3. _Advanced_ : Line following and Lane Detection, with response from object actions
    4. _Advanced_ : Lanes of different colours (white, yellow, etc) based on environment
    5. _Advanced_ : No Lanes solution / detection so vehicle still follows a path (e.g. a
       footpath)
- **Milestone 5 – Completed Solution with Demo and Documentation (Week 12)**
    1. Usage documentation (as per each Milestone)
    2. Demo of working solution in simulator
    3. Demo of working solution on real-world track (TBD)
    4. Deliverables as per ‘Hand-over deliverables’ section

The changes contained in this document are to account for adjustments to the ‘automatic track
creation’ which was not required to complete tasks. Instead, different tracks have been allocated to
each team to test track creation goals of the project.


USYD Capstone 2020

## Simulator Tracks

For the purposes of this unit, we are adding in extra tracks to the simulator. They are outlined and
described below. Each team will be required to implement two new track designs into the
simulator. These have been allocated in a table.

#### Team Track Allocations

```
Team Track 1 Track 2
CP31-17A5 Nurburgring GP Circuit (F1) Monaco Circuit (F1)
CP31-13A5 Marina Bay Circuit (night time – F1) Autodromo Algarve GP Circuit (F1)
CP32-15A4 Circuit of Americas GP Circuit (F1) Circuit de Spa-Francorchamps (F1)
CP32-17A2 Baby Circuit (Mario Cart) Sydney Motorsport Park Brabham Circuit
CP32B Albert Park GP Circuit (F1) Shanghai GP Circuit (F1)
```
All GP F1 Circuits will be 1:10 scale compared to their real-world sizes. If the scale of the Donkey Car
already in the simulator is different, please use the scale of the Donkey Car assuming it is 1:10 scale
real-world.

#### Judgment Criteria

The completed product will be judged on the below characteristics:

- **Accuracy** – How does the track best represent the real-world equivalent (if applicable). This
    will be judged on layout (turns in correct places), altitude changes/hills, and scale.
- **Environment** – Teams are expected to use basic static environment objects based on their
    allocated location. For example: Melbourne’s Alberto Park Circuit has a lake in the middle
    of it – teams should attempt to render in a lake-colour texture. Example: All GP F1 Circuits
    have crash barriers that are placed around the track with signage.
- **Creativity** – Teams can be as can be as creative as they like for any elements outside the
    track such as grand-stands and buildings. This includes spectators.
- **Special Effects** – Any team who wishes to implement a traffic light starting sequence the
    same as F1, will be looked upon favourably (including sound effects). Other lighting effects
    as well.
- **Pit Lane Detail** – If teams can achieve all the above, teams should add in a Pit Lane based on
    their allocated track.

All tracks are to be lined with a barricade with a scaled height of 1.5 metres and 3 - metre-long
sections. Teams should also render a fence that is 3 metres higher than the barricade (4.5 metre
total height). Some samples will be provided to teams on Discord #downloads.

All track edges should be thick white lines. Use discretion based on conditions. Road should all be
the a slightly lighter grey colour as the track 1 from the first specification document. Turns can have
the striped red and white as per normal F1.

Below are the tracks. Please consult the above table for which track(s) your team is implementing –
you are implementing the two tracks assigned to your team.


USYD Capstone 2020

### Track 1 - Nurburgring GP Circuit (F1)

```
Track Name Nürburgring GP Circuit (F1) 2019
City / Country Germany
Simulator ID
Simulator Name/ Code f1-gp-germany
Length 4 .574 km
Number of Turns 16
Wikipedia Article https://en.wikipedia.org/wiki/German_Grand_Prix
Other Sources https://www.nuerburgring.de/en/fans-info/race-
tracks/grand-prix-track.html#prettyPhoto
```
**Other Information:**

- Use any information relating to the 2019 circuit.
- This track is not flat and will require terrain data being added at the correct points.
- Circuit contains a pit lane
- There is no requirement to add in the ‘utility’ lanes.
- Circuit contains large sand and grass safety areas.
- Track width varies. Please research thoroughly.


USYD Capstone 2020

### Track 2 - Monaco GP Circuit (F1)

```
Track Name Circuit de Monaco (F1) 2019
City / Country Monte Carlo
Simulator ID
Simulator Name/ Code f1-gp-monaco
Length 3.337 km
Number of Turns 19
Wikipedia Article https://en.wikipedia.org/wiki/Circuit_de_Monaco
Other Sources https://www.formula1.com/en/information.monaco-
circuit-de-monaco-monte-
carlo.2ZWRtIcSI6ZzVGX1uGRpkJ.html
```
**Other Information:**

- Use any information relating to the 2019 circuit.
- This track is not flat and will require terrain data being added at the correct points.
- Circuit contains a complex pit lane. Render in if time permits (at the end).
- There is no requirement to add in the ‘utility’ lanes.
- Circuit contains fences all around the track. Turn 10 is open.
- Track width varies but is mainly narrow. Please research thoroughly.
- Ignore road markings, only render the edge and centre lines.


USYD Capstone 2020

### Track 3 - Marina Bay Street Circuit (F1)

```
Track Name Marina Bay Street Circuit (F1) 2018
City / Country Singapore
Simulator ID
Simulator Name/ Code f1-gp-singapore
Length 5.063 km
Number of Turns 23
Wikipedia Article https://en.wikipedia.org/wiki/Marina_Bay_Street_Circuit
Other Sources
```
**Other Information:**

- Night-time Circuit – must render in streetlights as the source of light
- Use any information relating to the 2018 circuit.
- This track is flat and will not require terrain data being added at the correct points.
- Circuit contains a pit lane.
- Circuit contains fences all around the track.
- Track width varies. Please research thoroughly.


USYD Capstone 2020

### Track 4 - Autodromo Algarve GP Circuit (F1)

```
Track Name Autodromo Algarve GP Circuit (F1) 2020
City / Country Portugal
Simulator ID
Simulator Name/ Code f1-gp-portugal
Length 4.6 53 km
Number of Turns 15
Wikipedia Article https://en.wikipedia.org/wiki/Algarve_International_Circuit
Other Sources https://www.formula1.com/en/racing/2020/Portugal/Circuit.html
```
**Other Information:**

- Use any information relating to the 2020 circuit.
- This track is not flat and will require terrain data being added at the correct points.
- Circuit contains a pit lane
- There is no requirement to add in the ‘utility’ lanes.
- Circuit contains large sand and grass safety areas.
- Track width varies. Please research thoroughly.


USYD Capstone 2020

### Track 5 - Circuit of Americas GP Circuit (F1)

```
Track Name Circuit of Americas GP (F1) 2019
City / Country United States of America
Simulator ID
Simulator Name/ Code f1-gp-usa
Length 5.513 km
Number of Turns 20
Wikipedia Article https://en.wikipedia.org/wiki/Circuit_of_the_Americas
Other Sources
```
**Other Information:**

- Use any information relating to the 2019 circuit.
- This track is not flat and will require terrain data being added at the correct points.
- Circuit contains a pit lane
- There is no requirement to add in the ‘utility’ lanes.
- Circuit contains large sand and grass safety areas.
- Track width varies. Please research thoroughly.


USYD Capstone 2020

### Track 6 - Circuit de Spa-Francorchamps (F1)

```
Track Name Circuit de Spa-Francorchamps (F1) 2019
City / Country Belgium
Simulator ID
Simulator Name/ Code f1-gp-belgium
Length 7.004 km
Number of Turns 19
Wikipedia Article https://en.wikipedia.org/wiki/Circuit_de_Spa-
Francorchamps
Other Sources
```
**Other Information:**

- Use any information relating to the 2019 circuit.
- This track is not flat and will require terrain data being added at the correct points.
- Circuit contains a complex pit lane.
- There is no requirement to add in the ‘utility’ lanes.
- Circuit contains large sand and grass safety areas.
- Track width varies. Please research thoroughly.


USYD Capstone 2020

### Track 7 - Baby Park (Mario Cart)

```
Track Name Baby Park (Mario Cart 8 or DS)
City / Country NA
Simulator ID
Simulator Name/ Code mario-babypark
Length
Number of Turns
Wikipedia Article https://www.mariowiki.com/Baby_Park
Other Sources https://mariokart.fandom.com/wiki/Baby_Park
```
**Other Information:**

- Track should include the colours as per the above picture (half red, half blue)
- For the length, use your own judgement and research. Each lap should be approximately 10
    seconds.
- Render in some scenery including, grass and walls.
- It does not need to be floating, but if you want, you can make it float.


USYD Capstone 2020

### Track 8 - Sydney Motorsport Park Brabham Circuit

```
Track Name Sydney Motorsport Park (Brabham Extended)
City / Country Sydney
Simulator ID
Simulator Name/ Code f1-gp-sydney
Length 4.5 km
Number of Turns 18
Wikipedia Article https://en.wikipedia.org/wiki/Sydney_Motorsport_Park
Other Sources https://www.racingcircuits.info/australasia/australia/sydney-
motorsport-park.html#.X3m0xmgzaJM
```
**Other Information:**

- Use any information relating to the Brabham Extended circuit.
- This track is not flat and will require terrain data being added at the correct points.
- Circuit contains no pit lane.
- There is no requirement to add in the ‘utility’ lanes.
- Circuit contains large sand and grass safety areas.
- Track width varies. Please research thoroughly.


USYD Capstone 2020

### Track 9 - Albert Park GP Circuit (F1)

```
Track Name Albert Park GP Circuit (F1) 2019
City / Country Melbourne
Simulator ID
Simulator Name/ Code f1-gp-melbourne
Length 5.303 km
Number of Turns 16
Wikipedia Article https://en.wikipedia.org/wiki/Sydney_Motorsport_Park
Other Sources https://www.racingcircuits.info/australasia/australia/sydney-
motorsport-park.html#.X3m0xmgzaJM
```
**Other Information:**

- Use any information relating to the 2019 circuit.
- This track is flat and not will require terrain data being added at the correct points.
- Circuit contains a complex pit lane.
- There is no requirement to add in the ‘utility’ lanes.
- Circuit contains large sand and grass safety areas. Also a lake in the middle.
- Track width varies. Please research thoroughly.


USYD Capstone 2020

### Track 10 - Shanghai GP Circuit (F1)

```
Track Name Shanghai GP Circuit (F1) 2019
City / Country Shanghai, China
Simulator ID
Simulator Name/ Code f1-gp-shanghai
Length 5.451 km
Number of Turns 16
Wikipedia Article https://en.wikipedia.org/wiki/Shanghai_International_Circuit
Other Sources
```
**Other Information:**

- Use any information relating to the 2019 circuit.
- This track is not flat and will require terrain data being added at the correct points.
- Circuit contains a complex pit lane.
- There is no requirement to add in the ‘utility’ lanes.
- Circuit contains large sand and grass safety areas.
- Track width varies. Please research thoroughly.


USYD Capstone 2020

## Simulator Car Models

As part of the original specification document, it stated to implement a new car model in the
simulator. Details of these cars are below. Two cars model per CP31 team and one car per CP
team are allocated below.

```
Team Car Model 1 Car Model 2
CP31-17A5 Telsa Truck RM Racer DC
CP31-13A5 Red Bull Racing RB16 Robo Car Store DC
CP32-15A4 Mercedes W11 (2020) NA
CP32-17A2 McLaren MP4/4 NA
CP32B Ferrari SF1000 (2020) NA
```
1. All cars should be modelled 1:10 scale. If the scale of the Donkey Car already in the
    simulator is different, please use the scale of the Donkey Car assuming it is 1:10 scale real-
    world.
2. Use the existing car model and physics for all cars to speed up development time.
3. Please render the camera at the same height on a pole above each car (like the other models
    already in the simulator).
4. All the information for the RM Racer DC and Robo Car Store DC can be found on the
    #downloads channel of discord.
5. All car models should be selectable in the myconfig.py file.

```
Simulator Name Associated Link
Red Bull Racing RB
(2020)
```
```
f1-redbull-rb16 https://en.wikipedia.org/wiki/Red_Bull_Racing_RB
```
```
McLaren MP4/4 f1-mclaren-mp44 https://en.wikipedia.org/wiki/McLaren_MP4/
Ferrari SF
(2020)
```
```
f1-ferrari-sf1000 https://en.wikipedia.org/wiki/Ferrari_SF
```
```
Mercedes W
(2020)
```
```
f1-mercedes-w11 https://en.wikipedia.org/wiki/Mercedes-
AMG_F1_W11_EQ_Performance
RM Racer DC custom-rmracer #downloads on Discord
Robo Car Store DC custom-
robocarstore
```
```
#downloads on Discord
```

USYD Capstone 2020

## Further Reference Material

All reference materials will be provided by the client to teams via Discord or email.

End of Document