# Gun-Detection-In-Video-Using-Ultralytics-RT-DETR

In this repository [Ultralytics RT-DETR](https://docs.ultralytics.com/es/models/rtdetr/) is trained to detect guns. Then, the custom detector is used to detect guns in video.
This a more challengin problem than the plate license detection implemented in another [repository](https://github.com/GerardoRodriguezB/License-Plate-Detector-Using-YOLOv8.git) since in this case the object of interest has a huge variety of models and colors, also the angles in which it can appear in a video vary su much, and also has oclusion since tipically a person has the gun in his hand, or hidden in his clothes. 

The [dataset](https://drive.google.com/drive/folders/1gp4zzNTbTmkgv5mpvzgdXIDXsZJInSzk) used in this project is open and was reported in this [paper](https://ieeexplore.ieee.org/document/9659207). It consists of +50,000 images from movies, survillance cameras, academic footages, with high quality annotations in format `PASCAL VOC`. The original dataset contains images of guns, machineguns, shutguns, long guns. For this project we restricted to guns, then we made a python script to randomly select 3,000 images and their annotations, and then manually I selected 400 images for training and 100 for validation, I did this way to select variety of images, and combined with data aumentation of ULTRALYTICS the detector is robust. See image below.
- Bright and dark scenes
- Different angles
- Guns alone in white and custom background
- People near and far
- Guns of different models and color
- Different types of oclussions



Creeate an Anaconda environment using `python=3.10`. If you have a GPU compatible with CUDA install

```bash
pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1 --index-url https://download.pytorch.org/whl/cu118
```

otherwise install the versions for CPU

```bash
pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1
```

Move to the root folder of the project and install requirements

```bash
pip install -r requirements.txt
```

In `video` folder it's included a video o me with a toy gun, and the scene was processed achieving good results (in the repository is included the video already processed).In this repository is included the datasets (images and labels) used in this projects for training the model.












