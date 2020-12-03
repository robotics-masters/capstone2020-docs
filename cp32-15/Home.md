# Implement Sign Detection using TensorFlow

## Project Description

Autonomous Vehicle Tech involves many different aspects of Software, Computer Vision, AI, Hardware, Electrical, VR, AR, IoT, and embedded computing.
The goal of this project is to develop a serious understanding of Artificial Intelligence (AI) technologies associated with autonomous vehicles, so they can develop and apply them to real-world roles post university.
We will implement both a real world and simulated world traffic sign detection algorithms using TensorFlow 2.

## Documentation

* [Installation Full](Installation_Full.md)
* [COCO loader](coco_model.md)
* [Sign Classifier](sign_classifier.md)
* [Unity](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/Unity)
* [Simulator](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/Simulator.md) (contains: New Tracks, Improved Track importation, SpineMesh, Splines, Paths, Real F1 Tracks, Terrain, Spawning on Path or Spline, Random Cone Generation)
* [Getting started with Tensorflow](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/Tensorflow)
* [Some useful datasets](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/Datasets)
* [Jupyter Notebook](Jupyter.md)
* [User Stories](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/User%20Stories)
* [Minutes](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/browse/minutes)
* [XP Notes](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/XP%20Notes)
* [Dataset Labeling](https://bitbucket.org/jarodreynolds/comp3888_t15a_group4/wiki/dataset_labelling)

## Generating automatic documentation

```text
$ pip install pdoc3
$ pdoc donkeycar/donkeycar/parts/object_detector/coco_model.py > wiki/coco_model.md
$ pdoc donkeycar/donkeycar/parts/object_detector/sign_classifier.py > wiki/sign_classifier.md
```