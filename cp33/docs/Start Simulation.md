# Start Simulation #

**Note**: all `python` command in this section should be invoked inside python's virtual environment.
If you did not setup the virtual environment yet please refer to [Setting Up Environment](Setting Up Environment.md)

## 1. [Setting Up Environment](Setting Up Environment.md) ##

## 2. start Simulation ##

We provide a start script to automate this process. The start script will read a configuration file, then
start gazebo follow by px4.

### 2.1 Before start ###

Please make sure:

 - you have at least run `make px4_sitl_default gazebo_typhoon_h480` in the PX4 source tree once.

### 2.2 Configuration file for this script ###

The startup script will read a configuration file in the current working directory named `start_sitl.ini` (Typically, the root of project source tree `~/comp3988_t17b_group_5`).
There is a example configuration file supplied.
The file can be found at `objdetection/example-start_sitl.ini` in the source tree.
You will need to copy it to your current directory and edit it as needed.
The detailed for the configuration file can be found in the example.

### 2.3 Start simulation ###

For a full list of operation supported by the startup script, use

```{bash}
./startup.py --help
```

To run the startup script without any argument is to start the default mission script, which is not implemented yet.

The implemented mission scripts:
 
 - Manual controller `./startup.py -m`
 - basic integration test `./startup.py --test`


When first time run this script, use

```{bash}
./startup.py --first-run
```

It will take 5-10 minutes for gazebo to fetch missing models from internet.
If the running time for first run is beyond 10 minutes, that might due to some issues.
Please stop the script with `Crtl-C` and run

```{bash}
gazebo --verbose worlds/small_city.world
```

To let gazebo alone fetch missing models.

If there is any issue when using this script, run the script again with `./startup.py --debug` and report issue with its full log.
typically, most of issues are caused by configuration, double check your `start_sitl.ini` file.

** Note **: If the script crashed, there might be some orphaned process needs to be manually killed.
Please find and kill any orphaned `mavsdk_server` or `px4_simulator` process, if you found the startup script frozed at some stage.


# See also #

 - [Manual Control](./Manual Control.md)