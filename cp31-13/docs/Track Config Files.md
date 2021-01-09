# Track Config Files
These config files allow us to edit properties in a scene without having to rebuild the entire Unity project. As of right now, only the robotics masters tracks 1 and 2 have objects which can be edited via their respective config files. The only objects which can be affect by the config files are the traffic lights currently.

Config files can be found / are placed in the `donkey_sim_Data/Resources` folder and are named according to their respective tracks:

* `track_1.json` for the track with the intersection in the middle
* `track_2.json` for the circuit track

Currently, track 1 has two traffic lights with IDs `LH44` and `VB77` that can be edited

## Traffic Lights
Traffic lights have 2 properties which can be edited:

* `states`: determines which lights are on and the order they loop in
* `timers`: determines how long to stay on each state from the `states` list (in seconds)

`states` and `timers` must be the same length for the config to be valid.
`states` are base 10 unsigned integers from 0 to 7 (inclusive). The binary representation of this number determines which light is on; so for example

* 1 = green on
* 2 = amber on
* 4 = red on

Multiple lights can be on at the same time.

Sample config file for `track_1` can be found here https://bitbucket.org/Osamaaa/comp3888_t13a_group5/src/master/sdsandbox/sdsim/Assets/Resources/track_1.json which sets the traffic light with ID `LH44` to cycle from red -> green -> amber, staying in each state for 5 seconds and `VB77` to go crazy