# EXPLORING OBJECT DETECTION AND SEMANTIC SEGMENTATION ON ROAD SCENE DATASET
<details>
This project provides a comparative study of two leading computer vision approaches, object detection and semantic segmentation, using YOLOv8 and U-Net on urban road scene images. The dataset is derived from the Waymo Open Dataset, with images extracted from parquet files and annotated using Roboflow for both pixel-wise segmentation masks and bounding box labels.

We train and evaluate both models on the same dataset and class definitions (person, sign board, traffic light, and vehicle) to analyze trade-offs in accuracy, speed, and scene detail.

Due to the size of the trained semantic segmnetation model, instead of adding it to the repo, it can be found in this drive link: https://drive.google.com/file/d/123k73Nk4xL33ZkLDiYGdR1RE-nE0wOWN/view?usp=sharing

The Image extraction file contains the code for downloading the images from the parquet files provided by Waymo's open source dataset.

The object detection best.pt file is the trained Yolov8s model
</details>


---

## Overview  
This project explores and compares two core computer vision techniques—**object detection** and **semantic segmentation**—in the context of autonomous driving and road scene understanding. Using the **YOLOv8** and **U-Net** models respectively, we evaluate trade-offs between detection speed, accuracy, and visual detail.

The models are trained on the same dataset (extracted from the Waymo Open Dataset) and use consistent class definitions to ensure a fair, side-by-side performance comparison.

---

## Key Highlights  
- Real-world urban road scenes from the **Waymo Open Dataset**  
- Custom annotations via **Roboflow** for both bounding boxes and segmentation masks  
- Evaluation of two vision tasks: object detection (YOLOv8) vs semantic segmentation (U-Net)  
- YOLOv8 model included; U-Net weights provided via Google Drive due to file size  

---

## Dataset  
- **Source**: Waymo Open Dataset (parquet format)  
- **Classes**:  
  - Person  
  - Sign Board  
  - Traffic Light  
  - Vehicle  
- **Preprocessing Steps**:
  - Images extracted from `.parquet` files using Python  
  - Annotated on Roboflow with both bounding boxes and segmentation masks  
  - Exported for use with both YOLOv8 and U-Net pipelines

---

## Future Work  
- Evaluate model performance in diverse weather and lighting conditions  
- Experiment with hybrid models that combine detection and segmentation  
- Optimize models for real-time deployment on embedded or edge devices  
- Expand the dataset to include nighttime, rainy, and foggy scenarios

---

## Acknowledgments  
- [Waymo Open Dataset](https://waymo.com/open) for providing high-quality driving scene data  
- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics) for the object detection framework  
- [Roboflow](https://roboflow.com) for annotation tools and dataset management  
