The Mission Script is manually tested with different input files by the following test cases, and their expected and actual outcome is compared against each other through manual inspection of the drone's flight in the simulator.

## Square Mission ##

A simple test case where the waypoints form a square pattern 

* Expected outcome: Drone traverses all waypoints correctly and in order, landing at each waypoint. Returns to starting location after.
* Actual outcome: same as expected 

## Trangle Mission ##

Similar to the Square mission, but with one less waypoint

* Expected outcome: Drone traverses all waypoints correctly and in order, landing at each waypoint. Returns to starting location after.
* Actual outcome: same as expected

## One Waypoint ##

The file only contains one waypoint.

* Expected outcome: Drone will takeoff, go to the single waypoint and land. Returns to starting location after.
* Actual outcome: Drone takes off, goes to the single waypoint but does not land. Returns to starting location after.

## Many Waypoints ##

Test case with 40 waypoints created.

* Expected outcome: Drone traverses all waypoints correctly and in order, landing at each waypoint. Returns to starting location after.
* Actual outcome: same as expected

## Duplicate Waypoints ##

Test case with multiple of the same waypoint coordinates, both consecutively and non-consecutively

* Expected outcome: Drone traverses all waypoints correctly and in order. When there are consecutive waypoints where the coordinates are the same, the drone will takeoff and land again at the same spot. Returns to starting location after.
* Actual outcome: same as expected

# Integration Testing
## Variable Drone Spawning Locations
The Drone is also able to start in different locations. The same test cases are also run to ensure that the drone will traverse the way points correctly.

E.g. If the first way point is at [5, 5] and the drone starts at [-5. -5], the drone should go to [5, 5] (relative to the map) instead of going to [0, 0] (relative to its own location).

## Multi-Drone Spawning
Multiple drones are also able to be spawned, each at different locations. The same test cases are again used to ensure that the drones each process the way points as absolute coordinates (relative to the map), such that they all fly cohesively.