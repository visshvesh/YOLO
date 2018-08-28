# YOLO
Object Detection

what is YOLO v2 (aka YOLO 9000)
YOLO9000 is a high speed, real time detection algorithm that can detect on OVER 9000! (object categories)

you can read more about it here (https://arxiv.org/pdf/1612.08242.pdf)
watch a talk on it here (https://www.youtube.com/watch?v=NM6lrxy0bxs)
and another talk here (https://www.youtube.com/watch?v=4eIBisqx9_g)

Step1 - Requirements
Python 3.5 or 3.6. Anaconda (install tutorial https://www.youtube.com/watch?v=T8wK5loXkXg)
Tensorflow (tutorial GPU verions https://www.youtube.com/watch?v=RplXYjxgZbw&t=91s)
openCV (https://www.lfd.uci.edu/~gohlke/pythonlibs/)

Step2 - Download the Darkflow repo
https://github.com/thtrieu/darkflow
extract the files somewhere locally

Step3 - Build the library
open an cmd window and type
python setup.py build_ext --inplace
OR
pip install -e .

Step 4 - Download a weights file
Download the YOLOv2 608x608 weights file here (https://pjreddie.com/darknet/yolov2/)
NOTE: there are other weights files you can try if you like
create a bin folder within the darkflow-master folder
put the weights file in the bin folder
Processing a video file
move the video file into the ``darkflow-master```
from there, open a cmd window
use the command
python flow --model cfg/yolo.cfg --load bin/yolov2.weights --demo videofile.mp4 --gpu 1.0 --saveVideo
videofile.mp4 is the name of your video.

NOTE: if you do not have the GPU version of tensorflow, leave off the --gpu 1.0

--saveVideo indicates to save a name video file, which has the boxes around objects
