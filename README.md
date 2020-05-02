# YOLO-deploy

The python implementation is pretty simple.
The problem which you may face might be when importing 'yolo.h5' model.
Most of the yolo.h5 models present for download or the pretrained weights which may used for creating the models will fail to execute stating that "AttributeError: module 'tensorflow' has no attribute 'space_to_depth'".
This is because while creating the yolo model, which is generally present online, tf.space_to_depth was used.
In the newer versions of tensorflow it has been changed to tf.nn.space_to_depth.
You can find the 'yolo.h5' model as well as the steps to creating your own pretrained model on darknet.

 
