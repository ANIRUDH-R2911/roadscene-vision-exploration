# Roadscene-Vision-Comparison
This project provides a comparative study of two leading computer vision approaches, object detection and semantic segmentation, using YOLOv8 and U-Net on urban road scene images. The dataset is derived from the Waymo Open Dataset, with images extracted from parquet files and annotated using Roboflow for both pixel-wise segmentation masks and bounding box labels.

We train and evaluate both models on the same dataset and class definitions (person, sign board, traffic light, and vehicle) to analyze trade-offs in accuracy, speed, and scene detail.

Due to the size of the trained semantic segmnetation model, instead of adding it to the repo, it can be found in this drive link: https://drive.google.com/file/d/123k73Nk4xL33ZkLDiYGdR1RE-nE0wOWN/view?usp=sharing

The Image extraction file contains the code for downloading the images from the parquet files provided by Waymo's open source dataset.
