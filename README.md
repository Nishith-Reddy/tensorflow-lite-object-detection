# tensorflow-lite-object-detection

## Steps to set up object detection using Tensorflow lite:

### step1: clone the tensorflow-lite-object-detectetion repository

`git clone https://github.com/Nishithw3b/tensorflow-lite-object-detection`
### step2: Install TensorFlow Lite dependencies and OpenCV
installing OpenCv 

`pip install opencv`

For installing tensorflow lite first you need to install tesorflow

`pip install tensorflow`

After, installing tensorflow head to https://www.tensorflow.org/lite/guide/python and pip install the required tensorflow lite interpreter depending on your computer os.

`(In my case I am using mac os and Python version I am using is 3.7)`

`pip install https://dl.google.com/coral/python/tflite_runtime-2.1.0.post1-cp37-cp37m-macosx_10_14_x86_64.whl`

### step3: Downloading Google's sample TFLite model
Google provides a sample quantized SSDLite-MobileNet-v2 object detection model which is trained off the MSCOCO dataset and converted to run on TensorFlow Lite. It can detect and identify 80 different common objects.

To download the sample model just run the following command,

`wget https://storage.googleapis.com/download.tensorflow.org/models/tflite/coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip`

Unzip it to a folder called "Sample_TFLite_model" by issuing:

`unzip coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip -d Sample_TFLite_model`

Now, you are good to go.

##  Running the TensorFlow Lite model!
Here I am focusing much on object detection in real-time(webcam), To do that run the following command in tensorflow-lite-object-detection directory.

`python3 TFLite_detection_webcam.py --modeldir=Sample_TFLite_model`

Here, we are using **"Sample_TFLite_model"**. You can also use any other model or your custom model by changeing `--modeldir=Name-of-Your-Model` in the above command.

## Creating Custom trained model and using USB accelerator will be updated soon.
