# Guide to Setting up Object Detection

As posted in slack on 2020-09-24

You have to do this in the terminal

And inside your conda donkey environment

remember conda activate donkey

Warning I estimate this uses around 500MB of download

Later it downloads the model and its 800MB

I suggest your current directory be projects

that's where I did this

Your current directory is important

The last step is long. Warning the last step installs tensorflow 2.3.0

If you have a GPU I'm not sure if it will change your tesorflow-gpu

suggest check your version after

with conda list

git clone --depth 1 https://github.com/tensorflow/models

sudo apt install protobuf-compilercd models/research/

protoc object_detection/protos/*.proto --python_out=.cp object_detection/packages/tf2/setup.py .python3 -m pip install .

(changed python to python3 above)

Does it say? Successfully installed ....... object-detection ....…

Pull OUR repository and merge folders with other repos

in stop_sign_detector.pyin did this with --- replaced,

\# dir_path = os.path.dirname(os.path.realpath(\__file\__))

PATH_TO_LABELS = '---/COMP3888/projects/models/research/object_detection/data/mscoco_label_map.pbtxt'

in myconfig.py

STOP_SIGN_DETECTOR = True-- your choice

DONKEY_GYM_ENV_NAME = "donkey-roboracingleague_1-track-v0"

Suggest caching the model below

suggest https://www.tensorflow.org/hub/caching

not sure if should do this 1st or not read on

then python3 manage.py -driveit will download the model (800MB) it says, don't stop it.

INFO:absl:Downloading https://tfhub.dev/tensorflow/centernet/hourglass_512x512_kpts/1:

by default it is cached in /tmp/tfhub_modules/ for next time you drive it

But will probably be cleared if you restart or turn off

Unless you set a cache folder suggested above.

Suggest you back it up.

then I think you should be able to drive and images of objects detected will be saved in /tmp/

--------------------

If you have use CPU for tensorflow and its lagging increase the number below.If you have a GPU and tensorflow-gpu installed

then note this line in stop_sign_detector.py

if img_arr is None or image_count % 100 != 0:

its only analysing every 100th image because CPU is slow

see how low you can reduce 100 to before it starts lagging

try 50 or 20then increase it to make sure it doesn't lag.

in the real world every 100th image is probably not safe or good enough.

in real life we need it to identify fast maybe even 10.
