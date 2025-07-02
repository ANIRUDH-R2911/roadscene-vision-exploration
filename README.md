# EXPLORING OBJECT DETECTION AND SEMANTIC SEGMENTATION ON ROAD SCENE DATASET
<details>
Due to the size of the trained semantic segmnetation model, instead of adding it to the repo, it can be found in this drive link: https://drive.google.com/file/d/123k73Nk4xL33ZkLDiYGdR1RE-nE0wOWN/view?usp=sharing

The Image extraction file contains the code for downloading the images from the parquet files provided by Waymo's open source dataset.

The object detection best.pt file is the trained Yolov8s model
</details>


## Overview  
This project explores two foundational deep learning approaches in computer vision, **object detection (YOLOv8)** and **semantic segmentation (U-Net)**, for understanding urban road scenes in the context of autonomous vehicles. Using a common dataset extracted from the **Waymo Open Dataset**, both models were trained and evaluated on identical image samples and class definitions: `Person`, `Vehicle`, `Traffic Light`, and `Sign Board`.

Our goal is to highlight each model’s capabilities and limitations through quantitative metrics and visual analysis, enabling informed decisions for real-world intelligent transportation applications.


## Key Highlights  
- **Unified dataset**: 8600 images prepared and annotated via Roboflow for bounding boxes and segmentation masks.  
- **Object detection** with YOLOv8: optimized for real-time bounding box predictions.  
- **Semantic segmentation** with U-Net: provides detailed pixel-wise classification.  
- **Evaluation metrics** include:
  - **YOLOv8**: `mAP@0.5`, `mAP@0.5:0.95`
  - **U-Net**: `Mean IoU`, `Foreground Mean IoU`
- **Class-wise performance** analysis reveals object-specific strengths and weaknesses.
- **Visualizations** demonstrate how both models handle cluttered urban scenes, occlusions, and varying object sizes.


## Dataset  
- **Source**: [Waymo Open Dataset](https://waymo.com/open)  
- **Image Extraction**: Custom Python scripts to convert `.parquet` files to RGB frames  
- **Annotations**: Pixel-wise segmentation + bounding boxes using [Roboflow](https://roboflow.com)  
- **Classes**:
  - Person
  - Vehicle
  - Traffic Light
  - Sign Board
- **Preprocessing**:
  - Standardized resolution to 640×640
  - Normalization & augmentation (flipping, brightness, rotation)
  - Converted masks to integer-encoded format for training
- **Final dataset size**: ~8600 images split into train/val/test sets


## Future Work  
- **Larger and more diverse datasets**: Expanding beyond 3000 raw frames could improve robustness and generalization.  
- **Unified architectures**: Combining object detection and segmentation into a single multi-task model could offer both speed and detail.  
- **Class imbalance solutions**: Techniques like weighted loss functions and synthetic augmentation can enhance performance on rare objects (e.g., traffic lights, sign boards).  
- **Model optimization**: Exploring lightweight variants and hybrid designs for real-time deployment on embedded systems.


## Acknowledgments  
- **Waymo Open Dataset** for real-world autonomous vehicle imagery  
- **Ultralytics YOLOv8** framework for object detection  
- **Roboflow** for annotation, dataset export, and augmentation 
- **Purdue University** – CE 56201: Vehicular Cyber-Physical Systems course  
