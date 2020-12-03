# Instructions

- Follow the documentation [here](https://docs.donkeycar.com/guide/simulator/) to install Donkey, Donkey Car and Donkey Gym. Make sure you download and install Anaconda too.

- Go to our [repository](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/src) and sure that you've pulled the latest version of our master branch.

- In our wiki, go to the [Donkey car simulator build page](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/wiki/Donkey%20car%20simulator%20builds) and download the one for your operating system (we may still be updating these before Sunday so double check you have the latest one before Sunday)

- Extract the files from the .zip

- From the master branch you pulled, ensure that you have access to a folder called "donkey gym". This folder contains three subdirectories: "donkeycar", "gym-donkeycar" and "mycar". The folder mycar contains our manage.py file as well as the modifications we made to the RMRacerLib part, so it's essential that when you run the donkey car simulator, you run it from this manage.py file.

- For the gym-donkeycar folder described above, copy this folder and use it to replace the gym-donkeycar directory that you created during these steps in the documentation below:

![gym-donkeycar.PNG](https://bitbucket.org/repo/oo8byMk/images/4164592242-gym-donkeycar.PNG)

This step is essential as we have modified certain files to make the brake system work.

- Similarly, for the donkeycar folder described above, copy the folder and use it to replace the donkeycar directory that you created during these steps in the documentation below:

![donkoeycar.PNG](https://bitbucket.org/repo/oo8byMk/images/4168257221-donkoeycar.PNG)

- In our master branch repository, open the file myconfig.py found [here](https://bitbucket.org/Osamaaa/comp3888_t13a_group5/src/master/donkey%20gym/mycar/myconfig.py)
. Go to line 244 and change the variable `DONKEY_SIM_PATH` to equal the path directory of the `donkey_sim` executable that was contained in the simulator build you downloaded previously from the wiki and extracted. For example, on Windows, you would set it to the following: `C:\\Users\\User\\Desktop\\OpenCV_build\\donkey_sim.exe` as this is the folder where the executable is located (assuming that 'OpenCv_build' is the name of the folder containing the extracted files'.

- Open Anaconda and input the command `conda activate donkey`

- In the Anaconda terminal, navigate to the `Donkey Gym/mycar` directory from the master branch files that you cloned/pulled earlier. To ensure that you're in the right directory, make sure that it contains a `manage.py` file.

- Run the command `python manage.py drive --model ./models/dumbai.h5`. This should run the simulator now. After a few minutes, you'll be able to navigate to the site `http://localhost:8887`. Please check your terminal / command line for the exact URL.

- Once on this page, go to the `Mode and Pilot` dropdown and select `Local Pilot`. The car should now drive by itself.