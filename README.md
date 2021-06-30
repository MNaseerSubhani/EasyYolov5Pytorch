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
![set parameters](tmp/1.PNG)

## Create dataset.yaml 
![generate dataset.yaml](tmp/2.PNG)

## download pretrained model
![download pretrained model](tmp/3.PNG)


## Upload the dataset to instance's name folder
After initilization the parameters of yolo, gather the dataset and label them according to yolo's label formating, and put the "data" folder in instance's name folder.
The data structure should like this:
  
    ├── data
    ├────── train
    ├──────────── images
    ├──────────────── --.jpg
    ├──────────── labels
    ├──────────────── --.txt
    ├───────test
    
    



