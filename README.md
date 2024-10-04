# PCB-Defect-Detection-Instance-Segmentation
A segmentation-based defect detection model tailored specifically for printed circuit board (PCB) inspection, utilizing the capabilities of YOLOv7, and YOLOv8.

## Dataset Preparation
A set of 690 PCB images containing six classes of defects—missing hole, mouse bite, open circuit, short circuit, spur, and spurious copper—was collected from [this dataset](https://robotics.pkusz.edu.cn/resources/datasetENG/). Binary masks were created to highlight the defective areas on the PCB images, indicating the precise location and extent of defects. These masks were annotated using [Label Studio](https://labelstud.io/).

## Annotation Generation
### Stage 1: Convert Binary Annotations to COCO JSON
This part involves converting binary masks into COCO JSON format.

### Stage 2: Converting COCO JSON Annotations to YOLO Format
This part includes creating a YAML configuration file for use in training YOLO models.

## Dataset Directory Structure
The dataset directory contains images and labels divided into three parts: training, testing, and validation subsets, along with a `data.yaml` file in the dataset root directory. Each label file is in `.txt` format and has the same name (except for the extension) as the corresponding image.

[![DOI](https://zenodo.org/badge/864451430.svg)](https://doi.org/10.5281/zenodo.13871861)
