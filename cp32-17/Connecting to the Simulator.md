To connect to the simulator:

1. Check out the repository, and checkout branch `driving`.
2. Run the simulator executable on whatever machine you wish to. Note the IP address of the machine on which you are running the simulator.
3. Using your freshly checked out code, install all the dependencies that are required to use DonkeyCar, preferably in an Anaconda environment.
4. Edit mysim/myconfig.py, setting the variable `SIM_HOST` to match the IP address of the simulator machine.
5. Use the following command to run the Python client:
```
./mysim/manage.py drive --model mysim/models/track1.h5
```