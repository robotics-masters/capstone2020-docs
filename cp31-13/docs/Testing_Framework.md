Our testing framework can be found in the 'accuracy_tester.py' file found [here](!https://bitbucket.org/Osamaaa/comp3888_t13a_group5/src/master/donkey%20gym/mycar/accuracy_tester.py).

# To use the testing framework #

- use the command 'conda activate donkey'

- run the command 'python accuracy_tester.py'. The program will then run the tests, and output the results to terminal and to 'results.csv'.

# To create your own tests #

Collect the images you want to use for testing. Make sure they're in the format where they have a number as the first character of the image name.Partition the data into 3 groups. For the 1st group of images, you should not expect the detectioncode to detect anything, for the 2nd group you should expect the detection code to detect something, and for the third group, you should not expect the detection code to detect something.

Make it so that the numbers that start the name of each image starts from 0 and is in ascending order.
Once you have your data correctly labelled, place it in a folder, calling it whatever you want.
Place this folder in the "Images" folder located in this directory.

Make sure that the detection algorithm you want to use is imported in the accuracy_tester.py file
To add your data as a test, go to the 'main' function of accuracy_tester.py and call writer.writerow(testing_framework(group_list, name_of_folder_with_data, detection_function)),
where group_list is an int array of length 3, where index 0 specifies the index of the last image
in the first partition you created previously, index 1 specifies the index of the 2nd partition you created previously.