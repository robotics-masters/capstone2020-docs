For training self-driving donkey car using the donkey framework, follow instructions [here](https://colab.research.google.com/github/robocarstore/donkey-car-training-on-google-colab/blob/master/Donkey_Car_Training_using_Google_Colab.ipynb)

For training neural network with custom script using tensorflow, follow instructions below 


```
# Insert Following code on top of your exisiting nodebook in Colab 
# Install python modules if necessary
# !pip install tf-nightly ;
## Make a zip file of your dataset and name it blob, and upload to google drive yourself 
## This assumes you have good internet connection, if not you can download the dataset using wget to /model yourself
from google.colab import drive
drive.mount('/content/drive')
!mkdir /model
%cd /model 
%cp /content/drive/My\ Drive/blob.zip . 
!unzip blob.zip
# Run your code as usual 
```
There is a way to 
[save to model](https://www.tensorflow.org/guide/keras/save_and_serialize) . Then you can use 
from google.colab import files
files.download('example.txt')  to download your model !