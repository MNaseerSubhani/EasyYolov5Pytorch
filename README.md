# EasyYolov5Pytorch

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/18dcCM1js2QSAB-GcPFOLg25vYUi2sB6B?usp=sharing)

This repo contains a simple notebook **EasyYolov5Pytorch.ipynb** to train multiple instance of YoloV5  with pytorch. 

The directory structure:
    
    ├── EasyYolov5Pytorch
    ├────── Instance-1
    ├─────────── data
    ├─────────────── train
    ├──────────────────── images
    ├──────────────────── labels
    ├─────────────── test
    ├────── Instance-2
    .
    .
    ├────── Instance-N
    ├────── yolov5
    ├────── EasyYolov5Pytorch.ipynb
    ├────── README.md
    

# Instructions
## Setup on Google Drive
Link notebook with your google drive for saving checkpoint,

## Clone this repo
Clone this repository to your gdrive

## Setup the parameters and yolo settings
Setting up the yolo with different instance name as your project required, change the parameters according to custom training,

```python
from google.colab import drive
drive.mount('/content/drive')
```

## Create dataset.yaml 
Add each class name in "names" list variable, 

```python
%cd {instance_name}
with open("dataset.yaml", "w") as f:   
    f.write(f"""path: ../{instance_name}/data  # dataset root dir
train: train/images  # train images (relative to 'path') 128 images
val: test/images  # val images (relative to 'path') 128 images
test:  # test images (optional)\n\n
nc: {num_of_classes}  # number of classes\n\n
names: [ 'class1', 'class2', 'classN' ]""")
%cd ..
```

## download pretrained model
```sh
!wget https://github.com/ultralytics/yolov5/releases/download/v5.0/{model}.pt
```


## Upload the dataset to instance's name folder
After initilization the parameters of yolo, gather the dataset and label them according to yolo's label formating, and put the "data" folder in instance's name folder.
The data structure should be like this:
  
    ├── data
    ├────── train
    ├──────────── images
    ├──────────────── --.jpg
    ├──────────── labels
    ├──────────────── --.txt
    ├───────test
    
    



