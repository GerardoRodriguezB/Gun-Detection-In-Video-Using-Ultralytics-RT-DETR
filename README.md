# Gun-Detection-In-Video-Using-Ultralytics-RT-DETR

In this repository [Ultralytics RT-DETR](https://docs.ultralytics.com/es/models/rtdetr/) is trained to detect guns. Then, the custom detector is used to detect guns in video.
This a more challengin problem than the plate license detection implemented in another [repository](https://github.com/GerardoRodriguezB/License-Plate-Detector-Using-YOLOv8.git) since in this case the object of interest has a huge variety of models and colors, also the angles in which it can appear in a video vary su much, and also has oclusion since tipically a person has the gun in his hand, or hidden in his clothes. 

The [dataset](https://drive.google.com/drive/folders/1gp4zzNTbTmkgv5mpvzgdXIDXsZJInSzk) used in this project is open and was reported in this [paper](https://ieeexplore.ieee.org/document/9659207). It consists of +50,000 images from movies, survillance cameras, academic footages, with high quality annotations in format `PASCAL VOC`.



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














