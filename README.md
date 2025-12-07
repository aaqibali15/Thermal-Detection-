# Thermal Object Detection Dataset (FLIR)

## 📌 Overview
This repository hosts the thermal imaging dataset used for training and evaluating object detection models (specifically YOLOv8). The dataset is derived from thermal sensor imagery, enabling detection in low-light, night-time, and adverse weather conditions where standard RGB cameras fail.

## 📊 Dataset Statistics
The dataset is based on the **Final FLIR DataSet** sourced from Roboflow. It has been processed and augmented to enhance model generalization.

* **Original Dataset Size:** 8,673 images
* **Total Size (after Augmentation):** 14,747 images
* **Format:** YOLOv8 (TXT annotations)

## 🗂️ Data Splits
The dataset has been meticulously split to ensure a robust training pipeline:

| Split | Percentage | Description |
| :--- | :--- | :--- |
| **Training** | **70%** | Used for model weight optimization. |
| **Validation** | **20%** | Used for hyperparameter tuning and preventing overfitting. |
| **Testing** | **10%** | Reserved for final performance evaluation on unseen data. |

## 🔗 Source & Acknowledgments
This dataset was obtained and adapted from Roboflow Universe.

* **Original Dataset:** [Final FLIR DataSet on Roboflow](https://universe.roboflow.com/flir-images/final-flir-dataset-hisfz)
* **Modifications:** Applied data augmentation to increase dataset size from ~8k to ~14k images to improve detection accuracy.

## 🚀 Usage with YOLOv8
To use this dataset for training, ensure your `data.yaml` configuration file points to the correct directories:

```yaml
train: ../train/images
val: ../valid/images
test: ../test/images

nc: <number_of_classes>
names: ['Person', 'Car', ...] # Update with your specific class names
