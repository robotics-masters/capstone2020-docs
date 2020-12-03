# Unity #

## Installation ##
Following the installation procedure [here](https://store.unity.com/academic/unity-student).

1. Authorise Unity with Github using the button on the unity-student page. I logged into Unity with Facebook.
2. Download Unity by clicking the Download Unity link after getting past the linking with Github stage (choose "Start Here"). On Linux, this downloads a "UnityHub.AppImage", which you can move to any applications folder you want.
3. Make the app image executable with `chmod +x UnityHub.AppImage` and then launch it.
4. Log in (top right).
5. Activate new licence -> Pro/Professional License then copy paste the license number from email. Had no issues with this, although was confused by the lack of student option.
6. Exit preferences and go to projects -> New.
(7. When I downloaded the Karting Minigame, I had to install Unity 2019.4. Originally I only selected Linux, but later wanted WebGL for the Karting tutorial - it was easy to Add Module from the Installation page on the UnityHub)

## Tutorial/Learning The Ropes ##
I downloaded the Karting Minigame, and started following the tutorial [here](https://learn.unity.com/tutorial/join-your-first-game-jam-1?uv=2019.3&projectId=5c82b27cedbc2a0e8db0c728#5e82f478edbc2a00200bcaee). Once the project is loaded up, there are about 6 tutorials I did to understand Unity basics (Tutorials -> Show Tutorials). More tutorials [here](https://learn.unity.com/project/karting-template).

## Concepts ##
* **GameObject** - object primitive, consists of components and child GameObjects (as many of each as you want)
* **Component** - like a "property", e.g. mesh, transform, physics, camera, audio, lighting, scripts, etc.
* **Prefab** - a template object you can add into a scene. For example a car (a GameObject possibly with many child GameObjects and physics, transform and script components) might be made a Prefab.
* **Scene** - place where objects exist

## Asset Creation ##
### Making four signs (William Talbot) ###
To create the left sign:

1. I created an empty GameObject, then gave it two child GameObjects. I named the child objects Post and Head. 
2. In the inspector menu for Post, I clicked "Add Component" and added a Mesh Filter. I then chose Cylinder as the primitive type. It wasn't visible yet.
3. I then added a Mesh Rendered component to make the mesh visible, and modified the position and scale in the Transform component. 
4. I created a new dark-grey Material object in my Assets folder, and then set the element of the Mesh Renderer of the Post to be this material.
5. In the Head child object, I make it a cylinder and transformed it to be thin and correctly oriented above the post.
6. After adding the png of the sign head to a folder in Assets, I dragged it onto face of the Head. This creates it as a new material in the Assets folder.
7. Dragged the game object into a folder in Assets to make it a Prefab.

The right sign was created identically.

To create the parking sign, the head was a cube instead of a cylinder (although a Quad object may have been more appropriate).

To create the stop sign, I had to create an octagonal mesh first. To do this I used Blender (`sudo apt install blender`). This was quite difficult and involved the following tricks:

* Creating an octagonal prism from a cube in blender. To do this, I subdivided vertices, and used edit mode to drag around edges/faces. This took while to get a handle on.
* Had to create the UV map on the top face of the octagonal prism to match (figured out a trick to project from 3D view by watching [this video](https://www.youtube.com/watch?v=n6t3tehdsHU) between 4 and 5 minutes.
* I think I had to recalculate normals to point outside but not 100% sure if this affected anything.
* The blend file could easily be put into Unity with no issues, and in fact can be opened from Unity with no issues, however can only be read by others if they have Unity installed. To make the meshes portable, I exported them to fbx files, being careful to turn on "Experimental Translation" during the export step so that the scale was corrected in the final object.