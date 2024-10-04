# PCB-Defect-Detection-Instance-Segmentation
A segmentation-based defect detection model tailored specifically for printed circuit board (PCB) inspection, utilizing the capabilities of YOLOv7, and YOLOv8.

## Dataset Preparation
A dataset of 690 PCB images containing six classes of defects—missing hole, mouse bite, open circuit, short circuit, spur, and spurious copper—was collected from [this dataset](https://robotics.pkusz.edu.cn/resources/datasetENG/). Binary masks were created to highlight the defective areas on the PCB images, indicating the precise location and extent of defects. These masks were annotated using [Label Studio](https://labelstud.io/).

### Annotation Generation
#### Stage 1: Convert Binary Annotations to COCO JSON
This step involves converting the binary mask annotations into the COCO JSON format, commonly used for object detection and segmentation tasks.

#### Stage 2: Converting COCO JSON Annotations to YOLO Format
This step involves converting the COCO JSON annotations into YOLO format and creating a data.yaml configuration file for YOLO model training.

## Dataset Directory Structure
The dataset is organized into three main subsets: train, test, and valid. Inside each subset, there are two folders: images and labels.

The images folder contains the corresponding images for that subset.
The labels folder contains the YOLO format label annotations in .txt files. Each label file has the same name as the corresponding image file (except for the extension).
Additionally, the root of the dataset contains a data.yaml file, which defines the paths to the train, test, and valid subsets, along with the class names required for YOLO model training

[![DOI](https://zenodo.org/badge/864451430.svg)](https://doi.org/10.5281/zenodo.13871861)
