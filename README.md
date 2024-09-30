# PCB-Defect-Detection-Instance-Segmentation

## Dataset Preparation
A set of 690 PCB images containing six classes of defects—missing hole, mouse bite, open circuit, short circuit, spur, and spurious copper—was collected from [this dataset](https://robotics.pkusz.edu.cn/resources/datasetENG/). Binary masks were created to highlight the defective areas on the PCB images, indicating the precise location and extent of defects. These masks were annotated using [Label Studio] (https://labelstud.io/).

## YOLO Annotation Generation
### Part 1: Convert Binary Annotations to COCO JSON
This part involves converting binary masks into COCO JSON format.

### Part 2: Converting COCO JSON Annotations to YOLO Format
This part includes creating a YAML configuration file for use in training YOLO models.

## Dataset Directory Structure
The dataset directory contains images and labels divided into three parts: training, testing, and validation subsets, along with a `data.yaml` file in the dataset root directory. I used Roboflow, which offers free API usage for certain functions like training my model.

## Label File Structure
Each label file is in `.txt` format and has the same name (except for the extension) as the corresponding image.
## Acknowledgments
I would like to acknowledge the following resources used in this project:

- Bhattiprolu, S. (2023). *python_for_microscopists - 332: All about image annotations*. GitHub. Available at: [https://github.com/bnsreenu/python_for_microscopists/tree/master/332%20-%20All%20about%20image%20annotations%E2%80%8B](https://github.com/bnsreenu/python_for_microscopists/tree/master/332%20-%20All%20about%20image%20annotations%E2%80%8B)
- Skalski, P. (2022). *Train YOLOv7 Instance Segmentation on Custom Data*. Roboflow Blog. Available at: [https://blog.roboflow.com/train-yolov7-instance-segmentation-on-custom-data/](https://blog.roboflow.com/train-yolov7-instance-segmentation-on-custom-data/)
- Ariuntuya, A. (2023). *How to Train YOLOv8 Instance Segmentation*. Roboflow Blog. Available at: [https://blog.roboflow.com/how-to-train-yolov8-instance-segmentation/](https://blog.roboflow.com/how-to-train-yolov8-instance-segmentation/)









