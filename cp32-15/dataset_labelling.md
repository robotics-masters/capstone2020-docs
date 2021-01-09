# Labelled Dataset

Our model trains using a dataset of images that we have labelled ourselves with bounding boxes. The result is two directories: `images` and `labels`. The `images` directory contains the image files (e.g. jpg images from the simulator) and the `labels` directory contains .xml files which store the bounding box coordinates and the label of the object within the bounding box, as shown below.

```xml
<annotation>
	<folder>tub_cones</folder>
	<filename>cone_img_535.jpg</filename>
	<path>/home/jarod/COMP3888/personal/labelled_data/cones/tub_cones/cone_img_535.jpg</path>
	<source>
		<database>Unknown</database>
	</source>
	<size>
		<width>240</width>
		<height>240</height>
		<depth>3</depth>
	</size>
	<segmented>0</segmented>
	<object>
		<name>cone</name>
		<pose>Unspecified</pose>
		<truncated>0</truncated>
		<difficult>0</difficult>
		<bndbox>
			<xmin>65</xmin>
			<ymin>72</ymin>
			<xmax>94</xmax>
			<ymax>119</ymax>
		</bndbox>
	</object>
</annotation>
```
![Cone image](https://bytebucket.org/jarodreynolds/comp3888_t15a_group4/wiki/images/cone_img_535.jpg?token=7fab6b2b4ab0d07d0fa7fd6a093a1898f4fe60c6&rev=1945ab43b19f8835ca7a13781bc931c37a778b2a)


## Labelling Images for the Dataset
***Note:*** *Images from new tubs should be renamed from the default Donkey name (`x_cam_image_array.jpg`) to avoid name clashes when integrating with the existing dataset.*

We used [LabelImg](https://github.com/tzutalin/labelImg) to label all images for the dataset. This can be installed on Ubuntu by:

```
pip3 install labelImg
```

Begin by creating `classes.txt` containing all the labels required. Our classes.txt file contains the following.

```
left_black
right_black
stop
park_green
park_white
park_yellow
right_blue
left_blue
right_arrow_black
left_arrow_black
right_arrow_blue
left_arrow_blue
cone
traffic_light_off
traffic_light_red
traffic_light_yellow
traffic_light_green
```

Launch labelImg using the terminal, with arg1 being the path to one of the images needing labelling, and arg2 the path to the `classes.txt` file just created.

```
labelImg [IMAGE_PATH] [PRE-DEFINED CLASS FILE]
```

With the labelImg app open, select `Open Dir` and select the entire directory of images to be labelled. Then select `Change Save Dir` to select the `labels` directory to save all labels.

To create a label, use the `w` hotkey and drag the box to surround the object with minimal/no extraneous area around the border. Select the appropriate label.

Repeat for other objects if there are any others in the image, otherwise use the `d` hotkey to move on to the next image.

See [here](https://github.com/tzutalin/labelImg#hotkeys) for more hotkeys to speed up the process when labelling large sets.

If one object appears in multiple consecutive images, it can be convenient to use the `use default label` option to automatically apply a specific label after the bounding box has been drawn.

A brief video showing these steps is uploaded [here](https://youtu.be/ijGqyb4kbO0).

![LabelImg example](https://bytebucket.org/jarodreynolds/comp3888_t15a_group4/wiki/images/labelImg.png?token=ca0da020f706c6b0bd355db9e4b744182fabb382&rev=8a2d442e1a6a2b9a69a3455565b1fcfa12343c01)