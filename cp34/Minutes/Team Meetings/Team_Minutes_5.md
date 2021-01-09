# Meeting Minutes

**Subject:** Team Minutes 5

**Project Name:** CP34 - Optimal Path for Drone Delivery

**Facilitator:** Nicholas

**Prepared by:** Dylan

**Date:** Sunday 26 September 2020

**Time:** 9:30 PM - 12:30 AM

**Location:** Zoom Online Meeting

**Attendees:**

* Dylan Duplessis (Team Member)
* William Wu (Team Member)
* Nicholas Hui (Team Member)
* Justin Lee (Team Member)
* Yufan XU (Ivan) (Team Member)

**Absent:**

* Derong Liu (Jimmy) (Team Member)

## Agenda

Meeting open at: 9:30 PM

| Agenda Item | Description | Action | Who? |
| -- | -- | -- | -- |
| Able to spawn charging stations in the world | Spawning of charging stations in the world | Editing sdf files for objects | Ivan, Dylan, Nicholas |
| Coding in an object into the world file | It is possible to do so, and thus it can be automated using python | Create python function to add in objects to selected world file | Dylan |
| Implement battery in PX4 | To find a way to have the drone in PX4 to utilise battery and have battery drain | Do research on gazebo px4 battery | Nicholas, Justin |
| Implement battery failsafe | Drone land/stop when the battery is low/dead | Add plugin on drone | Nicholas, Justin, Ivan |
| Object collision decisions | What options are there for the drone to get around an object? How can we pre-compute this to ensure we have a value to give to the algorithm beforehand | Generate a sphere shape around the object in question using the maximum radius enclosing the object and use it’s circumference to add distance to the weight of the graph that the algorithm will use | William |
| Drone’s remaining battery life for flying | How does the parameters such as speed, weather, altitude affect the battery life of the drone | Draft a formula to take all relevant factors into account and return the remaining distance that the drone could fly | Ivan, Nicholas |

Meeting closed at:  12:30 AM