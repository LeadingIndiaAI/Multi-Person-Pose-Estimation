# Realtime Multi-Person Pose Estimation
This is a keras version of [Realtime Multi-Person Pose Estimation](https://github.com/ZheC/Realtime_Multi-Person_Pose_Estimation) project  

## Introduction
Code repo for reproducing [2017 CVPR](https://arxiv.org/abs/1611.08050) paper using keras.  

## Requirements
Linux/Ubuntu system
 if not, try on Google Colab. Works like charm.!


## Contents
0. [intro to GoogleColab]
1.[Training](#training-steps)
2.[Testing](#testing-steps)

## Google Colab
- Go to google colab and create new ipynb file.
- !git clone {this repository clone}
- go to dataset folder
- `!wget http://images.cocodataset.org/zips/test2017.zip`
- `!wget http://images.cocodataset.org/zips/val2017.zip`
- `!wget http://images.cocodataset.org/zips/train2017.zip`
- enter these commands one by one. then unzip each of them using !unzip {filename}
- create annotations folder and upload these files from the given link https://drive.google.com/open?id=1Oa4FKj4xwOz_44Psi059Y3-on4Ebz0uv
- DONE! YOUR DATASET IS READY


## Training steps
- Go to the "training" folder `cd ../../../training`.
- Optionally, you can set the number of processes used to generate samples in parallel
  `dataset.py` -> find the line `df = PrefetchDataZMQ(df, nr_proc=4)`
- Run the command in terminal `python train_pose.py`
	 You can change no.of epochs in `train_pose.py` file
- This will take some time depending upon your pc/ no.of epochs

## Testing steps
- Convert caffe model to keras model or download already converted keras model https://www.dropbox.com/s/llpxd14is7gyj0z/model.h5
- Run the notebook `demo.ipynb`.
- `python demo_image.py --image sample_images/ski.jpg` to run the picture demo. Result will be stored in the file result.png. You can use
any image file as an input.



## Related repository
- CVPR'16, [Convolutional Pose Machines](https://github.com/shihenw/convolutional-pose-machines-release).
- CVPR'17, [Realtime Multi-Person Pose Estimation](https://github.com/ZheC/Realtime_Multi-Person_Pose_Estimation).


## Thanks to our mentor Dr. Tapas Badal for continuos encouragement.
