# This guide is for setting up the environment so that the new track can be used in your simulator.  #
## In this part, it will just be adding code to pre-existing python files.  ##

1. “gym_test.py” (gym-donkeycar\examples) and search for ‘env_list’. It should be an array where you add whatever name you want environment to be called. 
![Picture 1.png](https://bitbucket.org/repo/G6xBMXK/images/908236147-Picture%201.png)
Note: I added “donkey-pinky-track-v0”. Before that you should only see the first 5 environment names. Add your track after.

2. Do this same step from above with these files: “test_cam_config.py” (gym-donkeycar\examples), “simple_gen_driver.py” (gym-donkeycar\examples\genetic_alg), “ddqn.py” (gym- donkeycar\examples\reinforcement_learning), “ppo_train.py” (gym- donkeycar\examples\reinforcement_learning).

3. Now go to the “donkey_env.py” (gym-donkeycar\gum_donkeycar\envs) and scroll down to the very end of the python file. You should see classes here for other environment from here you want to add a class for your environment using the same formatting as the other tracks environment but change the level to be the number that the scene is associated with i.e.  
![Picture 1.png](https://bitbucket.org/repo/G6xBMXK/images/2097604304-Picture%201.png)
Note: The associated number is just +1 from the last level in your last class listed. For example, I add Pinky, its level is 4+1 = 5. Since the last class before I added is MountainTrackEnv, and level = 4.

4. There is one last thing we need to do before we can actually run the environment and that is to register the actual environment. To do this go into “__init__.py” (gym-donkeycar/gym_donkeycar) and register your environment with the names you used before. i.e. “donkey-track2-v0” and pretty much just copy the layout of the previous.
![Picture 1.png](https://bitbucket.org/repo/G6xBMXK/images/1703422143-Picture%201.png)

5. Now all you have to do is change DONKEY_GYM_ENV_NAME in “myconfig” (gym-donkeycar\mysim) to equal to your new environment name and now you can drive around in your new map.