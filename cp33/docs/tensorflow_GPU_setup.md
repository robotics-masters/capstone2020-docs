# TensorFlow GPU Acceleration setup #

This is the setup instructions for TensorFlow using a GPU. This was tested on Ubuntu 18.04.

Note that this requires an NVIDIA GPU with CUDA architectures 3.5, 3.7, 5.2, 6.0, 6.1, 7.0 and higher than 7.0. You can check if your card is compatible [here](https://developer.nvidia.com/cuda-gpus).

We need to set up NVIDIA drivers, CUDA toolkit, and NVIDIA cuDNN, before finally setting up TensorFlow on Linux.

## NVIDIA drivers ##

The easiest way in Ubuntu 18.04 is through the Software Updater GUI. Go to 'Software and Updates', then 'Additional Drivers'.

You can also do this via the command line.

```{bash}
# Add NVIDIA package repositories
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-repo-ubuntu1804_10.1.243-1_amd64.deb

sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub

sudo dpkg -i cuda-repo-ubuntu1804_10.1.243-1_amd64.deb

sudo apt-get update

wget http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64/nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb

sudo apt install ./nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb

sudo apt-get update

# Install NVIDIA driver
sudo apt-get install --no-install-recommends nvidia-driver-450

# Reboot to load the driver
reboot

# Check GPU is visible
nvidia-smi
```

Manually choosing a driver can also be done via command line with the following.

```{bash}
sudo apt-get update
sudo apt-get upgrade

sudo ubuntu-drivers devices
sudo ubuntu-drivers autoinstall
```

The third command will list available drivers. The fourth will auto-install the recommended driver. You can also manually install a driver version with the following.

```{bash}
sudo apt install nvidia-driver-version-number
```

## CUDA Toolkit  ##

Next we install the CUDA Toolkit. Visit this [link](https://developer.nvidia.com/cuda-toolkit-archive) for details on what the toolkit is, or if you want to install manually. Use the latest version (CUDA 11).

Run the following code (Will work for Linux, x86_64, Ubuntu 18.04. If running a different setup, follow the link above).

```{bash}
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-ubuntu1804.pin

sudo mv cuda-ubuntu1804.pin /etc/apt/preferences.d/cuda-repository-pin-600

wget https://developer.download.nvidia.com/compute/cuda/11.0.3/local_installers/cuda-repo-ubuntu1804-11-0-local_11.0.3-450.51.06-1_amd64.deb

sudo dpkg -i cuda-repo-ubuntu1804-11-0-local_11.0.3-450.51.06-1_amd64.deb

sudo apt-key add /var/cuda-repo-ubuntu1804-11-0-local/7fa2af80.pub

sudo apt-get update

sudo apt-get -y install cuda
```

## NVIDIA cuDNN  ##

This can be installed via the command line.

```{bash}
# Install development and runtime libraries (~4GB)
sudo apt-get install --no-install-recommends \
    cuda-10-1 \
    libcudnn7=7.6.5.32-1+cuda10.1  \
    libcudnn7-dev=7.6.5.32-1+cuda10.1
```

If you run into issues, you can manually install as described below, or even download a different version as you wish.

Visit the following [link](https://developer.nvidia.com/cudnn) and download cuDNN Developer Library for Ubuntu18.04 x86_64 (Deb). Remember to select the right version for your CUDA install (different versions of cuDNN exist for CUDA 10 and 11)

Unfortunately this will involve making an NVIDIA account before you can download the file, but it is a quick process.

Afterwards, assuming the downloaded file is in your Downloads folder, run the following.

```{bash}
cd Downloads
sudo apt install ./package_name.deb
```


## Linux Setup  ##

Now that the dependencies are fulfilled, we move on to the Linux setup.

First, update pip.

```{bash}
pip3 install --upgrade pip
```

Then run the following.

```{bash}
# Install TensorRT. Requires that libcudnn7 is installed above.
sudo apt-get install -y --no-install-recommends libnvinfer6=6.0.1-1+cuda10.1 \
    libnvinfer-dev=6.0.1-1+cuda10.1 \
    libnvinfer-plugin6=6.0.1-1+cuda10.1
```

We also install the tf-nightly package, which is just the nightly release of TensorFlow, because some functions exist only in tf-nightly and not in the major release.

```{bash}
sudo pip3 install tf-nightly
```


Guides used

[Setting up TensorFlow GPU](https://www.tensorflow.org/install/gpu)
