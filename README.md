# EasyYolov5Pytorch

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/18dcCM1js2QSAB-GcPFOLg25vYUi2sB6B?usp=sharing)

This repo contains a simple notebook **TheEasyYolo.ipynb** to train multiple instance of YoloV3 and YoloV4 with their tiny versions. You can train yolo with initilization of  different parameters like number of classes, channels, width and height. 

The directory structure:
    
    ├── TheEasyYolo
    ├────── Instance-1
    ├─────────── data
    ├─────────────── train
    ├─────────────── test
    ├────── Instance-2
    .
    .
    ├────── Instance-N
    ├────── darknet
    ├────── TheEasyYolo.ipynb
    ├────── README.md
    

# Instructions
## Setup on Google Drive
Link notebook with your google drive for saving checkpoint,

![link to gdrive](temp/gdrive.PNG)

## Clone this repo
Clone this repository to your gdrive

## Setup the parameters and yolo settings
Setting up the yolo with different instance name as your project required, change the parameters according to custom training, 

![Setup yolo parameters](temp/settings.PNG)



## Upload the dataset to instance's name folder
After initilization the parameters of yolo, gather the dataset and label them according to yolo's label formating, and put the "data" folder in instance's name folder.
The data structure should like this:
  
    ├── data
    ├────── train
    ├──────── --.jpg
    ├──────── --.txt
    ├───────test
    
    


## Generate train.names file and add all classes names

![create train.names file](temp/names_png.PNG)

