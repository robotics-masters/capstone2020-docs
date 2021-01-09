# Simulator #

[TOC]

## Getting Started ##

There are are a few moving parts, so here is a synopsis of the various software components:

* [autorope/donkeycar](https://github.com/autorope/donkeycar) - This is the python autonomous driving car toolbox for donkeycar.
* [tawnkramer/gym-donkeycar](https://github.com/tawnkramer/gym-donkeycar) - This is AI toolbox for donkeycar, which allows you to run the simulation with "parts" added to the donkeycar. It is through this that the neural net steering can be trained and run, the web interface can be enabled, and it is where our Tensorflow sign detection will go.
* [DonkeySimLinux](https://github.com/tawnkramer/gym-donkeycar/releases) (or Mac/Windows equivalent). This is the full simulator, and can be downloaded to run the pipeline out of the box. This is not necessary if you build the Unity simulator yourself from `sdsandbox`.
* ([tawnkramer/sdsandbox](https://github.com/tawnkramer/sdsandbox)). This is simulator repository. You can open `sdsim` in Unity and start editing scenes, assets, menus, etc. Once you are done, you can build the simulator into an executable (using `File>Build`).

Installation instructions:

* [Simulator Installation Guide](https://docs.donkeycar.com/guide/simulator/) which has the following steps:
    1. Download DonkeySimLinux (or equivalent) simulator release.
    2. Installation of `autorope/donkeycar`
    3. Installation of `tawnkramer/gym-donkeycar`
    4. Creation of your car

## Running the Simulator ##

* Ensure that the DONKEY_GYM, DONKEY_SIM_PATH and DONKEY_GYM_ENV_NAME are set correctly in `myconfig.py`. For example:
```
DONKEY_GYM = True
DONKEY_SIM_PATH = "/home/<user-name>/projects/DonkeySimLinux/donkey_sim.x86_64"
DONKEY_GYM_ENV_NAME = "donkey-generated-track-v0"
```
* To drive (make sure `donkey` is activated with `conda activate donkey`):
```
python manage.py drive
```
* For Mac OS, there might be an error "OMP: Error #15: Initializing libiomp5.dylib, but found libiomp5.dylib already initialized". To resolve this, a line should be added to manage.py.
```
os.environ["KMP_DUPLICATE_LIB_OK"]="TRUE"
```
* Open the web interface at [http://localhost:8887/drive](http://localhost:8887/drive)
* Use the joystick pad to drive around. Data will be recorded to a "tub" in the data folder.
* To train an autonomous driving neural network on your recorded data:
```
python manage.py train --tub <tub-directories> --model models/<model_name>.h5
```
* To drive with the trained model:
```
python manage.py drive --model models/<model_name>.h5
```

## Editing the Simulator ##

To open the simulator in Unity (see [Unity Page](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/Unity)):

1. Launch UnityHub
2. Open `sdsandbox/sdsim` as a Unity project (Add button). It may complain that it is built with an older Unity version. This means that it will go through an update the first time you open it.

To build and run our group's simulator:

1. Clone this repository if you haven't already.
2. Copy `sdsandbox` files to the simulator. For example from our repository's working path (paths may vary) `cp -r sdsandbox/sdsim ../sdsandbox`.
3. Copy `gym-donkeycar` files across as well. E.g. `cp -r gym-donkeycar/gym-donkeycar ../gym-donkeycar` (paths may vary).
4. Open `sdsandbox/sdsim` in Unity as described above.
5. Go to `File > Build Settings` and then click build. Put the saved files somewhere sensible.
6. In your car's `myconfig.py` script, edit the DONKEY_SIM_PATH variable to the path of the build executable, and you may wish to change DONKEY_GYM_ENV_NAME also. Note that the simulator can be run on its own, or through the `python manage.py drive` interface.

### Creating New Tracks ###

#### Adding a track ####
requires a new scene in Unity,
copy the existing track 1 scene and rename it
because donkey requires many objects and this is easier than starting from scratch.

#### What is a Scene? ####
A scene is mainly a unity scene (.unity) file but also may depend on other object files
each file has a associated meta file which contain a unique id for that file which is vital for unity to reference its needed files
these should not be changed but a new id can be created if the meta file is deleted or if a conflicting id already exists. but the scene will not be able to load the files it needs and you will have to fix the scene to use the files you want. A scene can also override some parts or values from its dependent files.

#### How to copy a scene? ####
Because of the above the best way to copy a scene is to duplicate it inside unity editor.
Open Unity, open the scene. in the hierarchy view select the scene (the top root)
in the project view select the scene
in the Edit menu select duplicate
a duplicate scene file will be created in the project view it will have a slightly different name.
rename the scene as you like.
It will be using all the files that the original scene uses, and have all the same overrides.

#### Edit the scene ####
put new track image into material into the ground, resize the ground, reposition the ground so the car starts where you want. Place other objects in the scene.
Save the scene.

Build a track by building a spline on a reference image (see SplineMesh below)

Adding a desired driving path is a fun manual process presently.

#### What is a path? ####
A path is a script that says things like go forward, turn 30 degrees right over 10 units, etc
Or a path can be a series of 3D points in sequence.
A path does not have to be a cycle, ie ending at its beginning, but it can.
Paths are in the resources folder eg racePi2.txt, roboracingleague_1.txt
However it should be very possible to duplicate and modify exiting code that uses a path to use a spline. (see SplineMesh below)
existing code uses paths to generate a road and to advise how far off the desired driving path the car is used by the builtin auto drive the PIDController.cs
some known existing scripts are PathManager.cs, TrackScript.cs, CarPath.cs, RoadBuilder.cs
adding a spline as a desired driving path should be easy (see SplineMesh below) if the track is built using a spline then its done, use that spline.

#### Is a Path required? Yes ####
DonkeyCar requires a path for each track, if a path isn't provided a NULL runtime exception will occur since it requests the 1st node of the path.

Add the scene to your Unity Build Settings under file menu.
	add open scenes button.

#### Adding a button to the menu ####
The menu is a scene, open it.
copy the existing track 1 button rename it, position it in the canvas in the scene, and edit it, change its image and caption and its action function.
for the button to work the scene needs to added to your build settings
and you need a new function in the buttons script to load the scene by its id

Moving a button on canvas is not as easy as moving in 3D. Doing that can cause a glitch. noticeable when the window showing the canvas is resized.

#### How was Track1 created? ####
It was created by duplicating the existing road_generator scene.
disabling the random rod generation.
then editing it as above.

#### How was Track2 created? ####
was created by duplicating Track1 and changing the track image.

Later we wanted signed and unsigned versions, theses were made by duplicating Track1 & Track2

Later some changes were made to the signed versions that were quickly applied to the unsigned versions by deleting the original Track1 & Track2 version, duplicating the signed version renaming and hiding the signs in the new unsigned versions.

### SplineMesh ###
see next 2 main sections & their subsections

### Improved and document way to import new track layouts ###
the following section shows a very fast and efficient method of creating new tracks no matter what shape using SplineMesh we feel this satisfies the request to make importing new tracks faster.
SplineMesh is a free asset from the online store that allows you to create splines that have many applications.

Before SplineMesh was discovered, Created a tool NavPoints.cs the purpose of this is to speed up the process of writing a driving path for a new track. It exports a set of navigation points, the positions of placed or a tagged set of objects from unity that with some very basic and quick filtering and formatting can be saved and used as a path. once you have a path you can build on it, interpolate more points and smooth the curves.

### Creating F1 tracks ###
Created 2 new F1 tracks in the simulator
Circuit of the Americas - Track 3
Circuit de Spa-Francorchamps - Track 4

Measured the track size on Google Earth, Measured length of the furthest corners
in Blender imported a track reference image onto a plane, scaled a cube to the measured length as a ruler, positioned and rotated it, then scaled the plane to match the ruler.
(optional could scale ruler to a scale size instead of full size)
exported the plane as an fbx file
in Unity imported the plane from the fbx file, and rendered the reference image on it.
Used SplineMesh
Using the reference image build a spline on the plane
Place a node at the start, centre, and end of every corner, in the middle of each straight,
at each inflexion point, at each slight bend, at each known height point, set all heights to 0, and
adjust the tangents of each node so the spline follows the track.
Perhaps use 4 times the number of nodes for the number of corners. Initially only move nodes and tangents on the X Z ground plane.

#### Generate road from Spline using Spline Extruder ####
Generated road from Spline, using Spline Extruder.
Before the workshop we had built a spline but didn't know how to turn it into a road, now we do and we can do it slightly simpler (see straight line).
The road needs a material and an image and the image needed to be rotated 90 degrees from the existing road texture images.
Was able to extrude the road using only 3 points [(-5,0),(0,0),(5,0)] (are on a straight line). instead of the 6 that was advised in the workshop. These points define the cross-section of the 3D shape you want the spline to make. you can choose any points you like.
The workshop didn't explain what U coordinates are, now know what they are and what they mean, (U is like the x value of the image).
Need to set the U coordinates to the [0, 0.5 , 1] (left, centre and right) of the image for those 3 points.
Note that [0, 0.5, 1] is not a 3D point or vector its a sequence of 3 values. using different U cords will use different parts of the image. you can choose not to use the whole image.
In our implementation during implementation experimentation we set the tiling of the material used to 0.5. So we used U cords of [0, 1, 2] instead. (if its not broken don't touch it).

You can extrude fences along the spine as workshop demonstrated.

To contain the car to the road thought about extruding a half pipe (or more) curve along the spline, like an open water slide, the car could climb up the side the road or pipe then slide then slide back down to the middle. the pipe could be as wide as the road or potentially much wider. This would require many more points, think is very possible to implement but not experimented due to time constraints.

Or thought about extruding a wider plane giving you ground either side to drive on. You could change the material image used to have ground texture like grass either side of the road. This would not require any additional points, they could just be moved further apart. This was experimented but without changing the material image, just making the road very wide (20 times wider).

Or thought about extruding a gentle and wide hill shape along the road giving you sloped ground either side of the road to drive on.  This would require many points, think is very possible to implement but not experimented due to time constraints. If was implemented this may help smoothing the terrain with the road.

Added a green, rigid, ground plane, and hid the reference image.

Note that due to the road generated from the spline and its size, the size of the scene files for Track3 & 4 are approx 20MB compared with < 100kb for other scene files.


#### Comparison of Track from Spline vs Track from Path ####
If you compare a road built with a spline to one built with a path eg the mountain track you will see that the spline track is much smoother, in the mountain track you can see sharp joins of the track texture along the corners.

#### adjust width of road ####
you can adjust the width of the track at any node by setting its scale of X or Z or both as desired.

#### adjust height of track ####
once happy with the flat track, if desired and as was requested you can adjust the height of any node along the y axis and can adjust the tangent along the y axis so the road smoothly changes height.
we got the height of each curve of the track from google Earth.


#### Adjust Terrain ####
once happy with the track you can add paint terrain into the scene (adjusting the height of the terrain to match the track) using unity's terrain toolbox.


### Adding a track to the simulator ###
For adding a track to the simulator so its loadable from the terminal with an environment variable

requires editing multiple files, in multiple (2) repos, to see which files and lines do the following, and also look at nearby lines, this is code related to the roboracing scene, for an overview see below

use existing code as a template for coding the new track.

in OUR repo folder

```
grep -inr "roboracing" *
```

note there are more files listed here than there are in the other team’s youtube video

```
grep -inr "roboracing" *
```

gym_donkeycar/__init__.py
gym_donkeycar/envs/donkey_env.py
Scripts/SceneLoader.cs
Scripts/tcp/TcpMenuHandler.cs
ProjectSettings/EditorBuildSettings.asset


the existing design of it is very complicated
donkey uses a registry class
an environment variable value is registered with an entry point with a coded class.
it calls its superclass with its coded level

Later
it indexes an array by the level
it uses the scene_name of the array item to call a function of a class
the function calls a scene to be loaded by its id defined in unity build settings.

Presently there are more scenes than there are environment variables
eg the main menu scene
so level <> id. just be aware.

also some names are mismatching there is a scene called small_looping_course, but its enviro class is GeneratedTrackEnv
very similar to GeneratedRoadsEnv

so a scene is referenced by an environment variable value, a class, a level, a scene_name, an array index (=level), a function name and its id in unity.
:)

Update a change was made to gym-donkeycar project by developer MaximeEllerbach#2439 to simplify this so that a level is a name not a number or index.

### Adding Assets to Tracks ###

See the [Unity Page](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/Unity) for details on how to create new assets. To add them into the simulator, simply drag the prefab you want to an approximate place on the map. Use `F` to go to the object, and translate/rotate as desired. You may want to add it using a scene top view, and you may want to ground the object by setting its y position to 0.

### Creating New Cars ###

#### Car Model Creation ####

We used the AutoDesk 3D Max to build the Model for new Cars. The [car modeling tutorial](https://www.youtube.com/watch?v=sBxH-f4ERK4) is a good example of how to model the curved surface of a car. Therefore, we can use the basic tools of 3D Max to model a similar F1 car. As for the wheels, we can directly import the model of donkey car and reuse it.

#### Importing the Car ####

To import the car into our simulator, we can first make a copy of "donkey car" prefab and delete every physical part except the wheel, because wheels are already bonded with the control script. Then we can import our model and adjust the position of the wheels to match the model. Therefore, we can create a new drivable prefab with the new model.

#### Change the Car for Testing ####

In the car spawner parts of the track, we can change the car prefab to our new prefab.



### Spawning on Path or Spline ###

Use ConesRandom to spawn on a Path (was implemented 1st)

Or Use SpawnOnSpline to spawn on a Spline.

can be used to spawn on or near the path or spline uniformly or randomly.

you use 1 of these scripts by adding it as component to a game object in Unity editor

you will see and be able to set the public fields (variables) in the inspector.

the public fields are defined in the next section

can be used to spawn any object not just cones. you drag a prefab or object into the prefab field in the inspector.

If you want to spawn cones I suggest you use the ConesScale prefab. it is based on the existing cone prefab but has been improved with physics, a rigid body, with a cylindrical and 2 capsule colliders so that the cones can be pushed away or knocked over and roll when on their side. The original prefab could be collided with but would not move the cylindrical collider was necessary at the base so that they stand upright and don't fall over immediately as they would without it. the colliders closely match the shape of the cone. it is possible to drive over just the base of the cone without touching the rest and so without knocking it over just like a real cone. The cones are scaled as the client desired.

mindiif and maxdiff are variables that control how close to and far away from each other 2 objects should spawn, the difference is the number of spawn points between, not distance in units.

if mindiff and maxdiff are equal then it will spawn uniformly along the path instead of randomly.

If you set offsetmax to 0 then there is no offset from the path and it will spawn along the path, it is distance in units.


#### ConesRandom.cs fields (variables) ####

PathManager manager: is a reference to the PathManager that has the path.

GameObject conePrefab: is a reference to the cone prefab or other object to spawn.

int offsetmax: default 5 is the maximum number of units to offset by the radius of a circle (on the X Z plane).

int mindiff: default 10, is the minimum difference (not distance) between chosen spawn points.

int maxdiff: default 30, is the maximum difference (not distance) between chosen spawn points.


#### SpawnOnSpline.cs fields (variables) ####

Spline spline: is a reference to the Spline to use.

GameObject Prefab: is a reference to the cone prefab or other object to spawn.

float NumPerNode: default 5, the number of virtual possible spawn points to consider per node of the spline, the rate of how many spawn depends on other variables too. value 0 is not supported.

int offsetmax: default 5, is the maximum number of units to offset by the radius of a circle (on the X Z plane).

int mindiff: default 10, is the minimum difference (not distance) between chosen spawn points.

int maxdiff: default 90, is the maximum difference (not distance) between chosen spawn points.

bool randomise: default true, if true then will spawn randomly instead of uniformly.

The uniform increment rate is calculated by 1 over NumPerNode, eg the default of 5 would give increment of 0.2 so it considers 5 spawn points per node.


### Random Cone Generation ###
The initial idea was to randomly choose points in a path (a set of points) and then randomly offset from that path.
to implement random offest a virtual grid was considered, but then the random 3D vector function Random.onUnitSphere multiplied by offsetmax was discovered and used with y set to 0. this gives a flat random 2D XZ vector within a circle of radius offset max, eg (2.83, -4.71) or (3, 3) note X value mostly different Z value (it is possible for them to be equal but they are probably not equal)
The existing tracks already have a path defined.
To implement randomly choosing points. used more efficient method: randomly choosing an initial value then incrementing by a random value, skipping many points, many times (a different random value increment each time) until at end of path.
The range of the random value increment is bounded by mindiff and maxdiff.
once SplineMesh was understood was able to use random postion along a spline and then randomly offeset similarly from there.
use ConesRandom Or SpawnOnSpline with the ConesScale prefab

Spawning random cones is helpful for building a dataset for training and testing TensorFlow neural networks. and most importantly for testing our collision avoidance algorithms with cones in different random positions each time.

See previous Spawning on Path or Spline section above

This has been demonstrated in images in final presentation and videos posted to slack and shown final showcase video to client posted on youtube.
