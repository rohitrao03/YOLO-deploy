# YOLO-deploy

The python implementation is pretty simple.
The problem which you may face might be when importing 'yolo.h5' model.
Most of the yolo.h5 models present for download or the pretrained weights which may used for creating the models will fail to execute stating that "AttributeError: module 'tensorflow' has no attribute 'space_to_depth'".
This is because while creating the yolo model, which is generally present online, tf.space_to_depth was used.
In the newer versions of tensorflow it has been changed to tf.nn.space_to_depth.
You can find the 'yolo.h5' model as well as the steps to creating your own pretrained model.
Step 1:
Linux:
wget http://pjreddie.com/media/files/yolo.weights
Windows:
http://pjreddie.com/media/files/yolo.weights

Step2:(download the config file)
http://pjreddie.com/media/files/yolo.weights

Step3:
https://github.com/allanzelener/YAD2K
download the zip or clone/download
Of course you can download it using the git command.

Step4:
Copy or cutyolo.weightswithyolo.cfgas well asyad2k.pyThree files, as well as the folders yad2k and model_data....all these should in in your working directory.
Step5:
In (..yad2k\models) you'll find a file keras_yolo.py.
search for tf.space_to_depth and replace it with tf.nn.space_to_depth

Step6:
Open annaconda prompt and run the following command
C:\Users\user_new>python yad2k.py yolo.cfg yolo.weights model_data/yolo.h5

 
