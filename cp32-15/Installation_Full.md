# Installation Instructions

Instructions to setup development environments

1. Install python3.7

        sudo apt install python3.7

2. Install and start virtual environment

        python3.7 -m venv env
        source env/bin/activate

3. Get latest donkeycar

        git clone https://github.com/autorope/donkeycar
        cd donkeycar
        git checkout dev
        pip install -e .[pc]
        cd ..

4. Get gym-donkeycar

        git clone https://github.com/tawnkramer/gym-donkeycar
        cd gym-donkeycar
        pip install -e .
        cd ..

5. Object detection

        git clone https://github.com/tensorflow/models
        sudo apt install -y protobuf-compiler
        cd models/research/
        protoc object_detection/protos/*.proto --python_out=.
        cp object_detection/packages/tf2/setup.py .
        python -m pip install .
        cd ../..
  This may produce some warning (non fatal) messages.
  If you encounter other errors please see wiki/Tensorflow.md

6. OPTIONAL: Install Tensorflow GPU

        conda install tensorflow-gpu==2.2.0

7. Install [Unity 3D Editor](https://store.unity.com/academic/unity-student)

8. Get the latest sdsandbox simulator:

        git clone https://github.com/tawnkramer/sdsandbox.git

9. Install our project and copy sdsandbox and gym-donkeycar assets across

        git clone https://bitbucket.org/jarodreynolds/comp3888_t15a_group4.git
        cd comp3888_t15a_group4
        pip install -e .
        cp gym-donkeycar/* ../gym-donkeycar -r 
        cp sdsandbox/* ../sdsandbox -r 

10. using `tar xvzf <filename>.tar.gz` to decompress the following files:

    1. extract <https://drive.google.com/file/d/1Lwv0ByZy5_5ni5CViw32jTh_kkVKnJUQ/view?usp=sharing> into `comp3888_t15a_group4/mysim`
    2. extract <https://drive.google.com/file/d/1dnNhLaMdED9MfgSrkZXWNSbVt_U0XwkW/view?usp=sharing> into `comp3888_t15a_group4/mysim/models`
    3. extract <https://drive.google.com/file/d/1-uhPaU1kJiiVw9TFCdbnwtpJfzB7xNw6/view?usp=sharing> into `comp3888_t15a_group4/tf_sign_detector/models`

11. edit `comp3888_t15a_group4/mysim/myconfig.py` to suit your needs

11. From inside `comp3888_t15a_group4/mysim` you can now run the program.

        python manage.py --model models/test3

## Resources

- <http://docs.donkeycar.com/guide/host_pc/setup_ubuntu/>
- <http://docs.donkeycar.com/guide/simulator/>
- wiki/[Simulator.md](Simulator.md)
- wiki/[Tensorflow.md](Tensorflow.md)
- wiki/[Unity.md](Unity.md)
- slack posts

## Building the simulator fresh

1. Open Unity hub
2. Open Unity project ~/projects/sdsandbox/sdsim
3. Once the project is open in Unity
    Go to `File > Build Settings` and then click build. save the executable in `comp3888_t15a_group4/mysim/` and ensure `DONKEY_SIM_PATH` in `comp3888_t15a_group4/mysim/myconfig.py` is pointing to the right simulator.
