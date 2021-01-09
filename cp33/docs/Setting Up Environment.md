# Setting Up Environment #

**Warning**: Only Ubuntu 18.04LTS is tested and working.

## 0. Terminology ##

 - profile file: the profile file of your preferred shell. (`.bashrc` for bash, `.zshrc` for zsh, etc..)
 - source your profile file: reload your profile file. execute (`source ~/.bashrc` for bash, `source ~/.zshrc` for zsh)
 - source tree: This project's source tree.

## 1. Prerequisites ##

A working [Ubuntu 18.04 LTS](http://releases.ubuntu.com/18.04/) machines with following packages installed.

Required:

 - git
 - cmake
 - ninja-build
 - gcc
 - python3
 - python3-pip
 - python3-venv

Optional:

 - ccache

If you have ccache install, put the following line at the end of you profile file and source it.

```{bash}
export PATH=/usr/lib/ccache:$PATH
```

## 2. Gazebo ##

```{bash}
sudo sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable `lsb_release -cs` main" > /etc/apt/sources.list.d/gazebo-stable.list'

wget http://packages.osrfoundation.org/gazebo.key -O - | sudo apt-key add -

sudo apt update

sudo apt install gazebo9 libgazebo9-dev
```

Add the following line into your profile file and source it.

```{bash}
source /usr/share/gazebo/setup.sh
```

## 3. PX4 ##

This will install PX4 at `~/src/Firmware`, You can change it to somewhere else as well.

```{bash}

cd ~
mkdir src
cd src
git clone https://github.com/PX4/Firmware
cd Firmware
git submodule update --init --recursive
./Tools/setup/ubuntu.sh

# required by the video streaming plugin
sudo apt install libgstreamer1.0-dev gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly

make

# test it
make px4_sitl gazebo_typhoon_h480
```
## 4. [TensorFlow GPU Support](tensorflow_GPU_setup.md) ##

## 5. Setup the Source Tree ##

```{bash}
# Firstly, clone our repository by
git clone https://zson5784@bitbucket.org/zson5784/comp3988_t17b_group_5.git

# enter the source tree
cd comp3988_t17b_group_5
```

### 5.1 Setup Python Virtual Enviornment ###

```{bash}
# in the source tree

python3 -m venv venv
source ./venv/bin/activate
sudo apt install libgirepository1.0-dev gcc libcairo2-dev pkg-config python3-dev gir1.2-gtk-3.0
pip3 install -r requirements.txt
```

#### **Tips and Trick**: How to use virtual environment ####

In your preferred shell:

```{bash}
# entering venv
source ./venv/bin/activate

# do stuff ...

# exit venv
deactivate
```

### 5.2 Build the Traffic Light Controller Plugin ###

```{bash}
# Assume your are now in the root of source tree.
cd plugin
mkdir build
cd build
cmake ..
make
```

For detail of this plugin please refer to [Traffic Light Control Plugin](Traffic Light Control Plugin.md)

### 6 Build MAVSDK ###

As the official build lacks some functionality we need.
We need to build the MAVSDK with a patch.

```{bash}
#in the root of repo

#enter virtual environment first
source ./venv/bin/activate

## for MAVSDK
## Make sure you are in thirdparty/mavsdk
## and on distance_sensor_2 branch

git submodule update --init --recursive
cd thirdparty/mavsdk
#changes for mavsdk are on distance_sensor_2 branch
git checkout distance_sensor_2
git submodule update --init --recursive

cmake -DCMAKE_BUILD_TYPE=Release -DBUILD_BACKEND=ON -DBUILD_SHARED_LIBS=OFF -Bbuild -H.
cmake --build build -- -j8

## for MAVSDK-Python
## make sure you are in thirdparty/mavsdk-python
## and on distance-sensor branch

cd ../mavsdk-python
#changes for mavsdk-python are on distance-sensor branch
git checkout distance-sensor
git pull --tags

#in your virtual environment
pip3 install -e .

#copy the built mavsdk_server
cp ../mavsdk/build/src/backend/src/mavsdk_server mavsdk/bin

```