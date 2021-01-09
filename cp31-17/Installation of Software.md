# Installation Instructions

We followed these videos for the installation of the DonkeyCar platform and gym-donkeycar:

Linux: https://youtu.be/J6Ll5Obtuxk

Windows: https://youtu.be/wqQMmHVT8qw

Further links:  
https://docs.donkeycar.com/guide/install_software/#step-2-install-software-on-donkeycar  
https://docs.donkeycar.com/guide/simulator/

## Contents

[TOC]

## Prerequisites
These instructions assume you have git, miniconda and Unity installed on your computer already.  
Miniconda: https://docs.conda.io/en/latest/miniconda.html  
Unity: https://store.unity.com/download

## Step 1: Download our repository

Open the miniconda prompt window, go to the directory where all your files will be and run the commands:

```
mkdir projects
cd projects
git clone https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5.git
cd comp3888_t17a_group5
```

## Step 2: Installing donkeycar

If you have previously installed donkey, you will need to first delete it. Use the commands:
```
conda update -n base -c defaults conda
conda env remove -n donkey
```

This part will depend on your operating system.

For **Windows** run the commands:
```
cd donkeycar
conda env create -f install\envs\sagemaker.yml
conda activate donkey
pip install -e .[pc]
```

for **Linux**:
```
cd donkeycar
conda env create -f install/envs/ubuntu.yml
conda activate donkey
pip install -e .[pc]
```

for **Mac**:
```
cd donkeycar
conda env create -f install/envs/mac.yml
conda activate donkey
pip install -e .[pc]
```

## Step 3: Building the simulator

Open Unity. Load the sdsim folder from our repo in it. Click File > Build and Run. Place the build within the 'projects' folder the repo was cloned into.

## Step 4: Installing gym-donkeycar and creating simulator files
Continuing from where the previous instructions left off, run the commands:
```
cd ..
cd gym-donkeycar
pip install -e .[gym-donkeycar]
donkey createcar --path ~/mysim --template simulator
```
Your new simulator will now be located in the folder called "mysim" in your root directory. Alternatively "~/mysim" can be replaced with the desired location for your simulation.

In order to use the implemented sign detection features you will need to train your own autopilot. To do so, read and follow the instructions [here](https://docs.donkeycar.com/guide/train_autopilot/).

Now in your mysim folder, edit **'myconfig.py'**, uncomment these three lines located at line 230-232 and edit them to be:
```
DONKEY_GYM = True
DONKEY_SIM_PATH = "/home/<user-name>/projects/DonkeySimLinux/donkey_sim.x86_64"
DONKEY_GYM_ENV_NAME = "donkey-track1-v0"
```
**Note:** The 'DONKEY_SIM_PATH' is where you built the simulator from step 3.  
**Note 2:** How DONKEY_SIM_PATH ends will differ with operating systems. The above example is for **Linux** as "DonkeySimLinux/donkey_sim.x86_64". For **Windows** it is "DonkeySimWin/donkey_sim.exe", and finally, for **Mac** "DonkeySimMac/donkey_sim.app/Contents/MacOS/donkey_sim".  
**Note 3:** For Windows, the path may require double slashes instead of the singular i.e. replace all '/' with '//'.  


You now should be able to run the simulator using step 6. Continue with step 5 if you wish to install sign detection, otherwise continue to step 6.

## Step 5: Installing RMRacer
This step can be skipped if you do not wish to have self driving features. To install RMRacer, use the following commands in your conda donkey environment:

```
cd ..
cd RMRacerlib
pip install -e .
```

In your **'myconfig.py'**  file in your mysim folder, replace line 273 with the line below:
```python3
STOP_SIGN_DETECTOR = True
```

## Step 6: Running the simulator

To run the simulation, use the following commands in the terminal assuming your mysim folder is in the same place as the instructions:

```
cd ~/mysim
conda activate donkey
python manage.py drive

```
Sign detection is compatible only with autopilot. If you wish to use a trained autopilot that you created in step 5, run:

```
cd ~/mysim
conda activate donkey
python manage.py drive --model "insert model path"/"model_name".h5
```
Enjoy!


# Editing the Simulator
If you wish to change/add maps and signs to the simulator you should head over to this tutorial to be able to do this: [Link](https://bitbucket.org/comp3888-t17a/comp3888_t17a_group5/wiki/Map%20implementation)