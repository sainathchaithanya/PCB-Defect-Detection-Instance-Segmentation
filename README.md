# PCB-Defect-Detection-Instance-Segmentation
A segmentation-based defect detection model tailored specifically for printed circuit board (PCB) inspection, utilizing the capabilities of YOLOv7, and YOLOv8.

## Dataset Preparation
A dataset of 690 PCB images containing six classes of defects—missing hole, mouse bite, open circuit, short circuit, spur, and spurious copper—can be collected from either [Robotics Dataset](https://robotics.pkusz.edu.cn/resources/datasetENG/) or the [Kaggle PCB Defects Dataset](https://www.kaggle.com/datasets/akhatova/pcb-defects).
Binary masks were created to highlight the defective areas on the PCB images, indicating the precise location and extent of defects. These masks were annotated using [Label Studio](https://labelstud.io/).

### Annotation Generation
#### Stage 1: Convert Binary Annotations to COCO JSON
This step involves converting the binary mask annotations into the COCO JSON format, commonly used for object detection and segmentation tasks.

#### Stage 2: Converting COCO JSON Annotations to YOLO Format
This step involves converting the COCO JSON annotations into YOLO format and creating a data.yaml configuration file for YOLO model training.

## Dataset Directory Structure
The dataset is organized into three main subsets: train, test, and valid. Each subset includes two folders: one for images and another for labels.

The images folder contains the corresponding images for that subset.
The labels folder contains the YOLO format label annotations in .txt files. Each label file has the same name as the corresponding image file (except for the extension).
Additionally, the root of the dataset contains a data.yaml file, which defines the paths to the train, test, and valid subsets, along with the class names required for YOLO model training

## Model Implementation 
I utilized Roboflow for dataset management and model training, leveraging its foundational code while implementing key modifications. This included customizing the code, streamlining the Jupyter Notebook, adjusting directory paths, fine-tuning hyperparameters, employing data augmentation techniques, integrating visualization tools, and enhancing evaluation metrics. These changes allowed me to tailor the model specifically for detecting and segmenting PCB defects precisely.

The code and dataset for this project can be accessed via the following Google Drive links:

- **Code**: [YOLOv7 code](https://drive.google.com/file/d/1FaI8jHIVW8sbYMUBxPYFMsoYr3PA6gjZ/view?usp=sharing) and [YOLOv8 code](https://colab.research.google.com/drive/1g-bNS03-VRLsyNBGKC1bauDhqvYOlRF3?usp=sharing).
- **Dataset**: [Google Drive link for dataset](https://drive.google.com/drive/folders/1qnaA9MANMiZgmB3Xbo3cP4NlRIeXYhvT?usp=sharing).


### Acknowledgments
I would like to acknowledge the following resources referred to for this project:
- Bhattiprolu, S. (2023). *All about image annotations* from the *python_for_microscopists* repository on GitHub. Available [here](https://github.com/bnsreenu/python_for_microscopists/tree/master/332%20-%20All%20about%20image%20annotations%E2%80%8B).
- Skalski, P. (2022). *Training YOLOv7 Instance Segmentation on Custom Data* from the Roboflow Blog. Read more [here](https://blog.roboflow.com/train-yolov7-instance-segmentation-on-custom-data/).
- Ariuntuya, A. (2023). *Training YOLOv8 Instance Segmentation* from the Roboflow Blog. Learn more [here](https://blog.roboflow.com/how-to-train-yolov8-instance-segmentation/).
