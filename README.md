# ARI3129 Group Project Repository

This repository contains all the practical work for the ARI3129 Group Project. This README describes the structure of the repository and its contents.

---

## Repository Structure

### 1. Dataset
The **`Dataset/`** directory is structured as follows:

* **`images/`**: Contains the complete set of captured raw images used for training and evaluation.
* **Member Subfolders**: Contain exported COCO/JSON annotation files, YOLO `.yaml` configurations and specific training run outputs.
    * `IanCaruana/`
    * `MatthewBorgBarthet/`
    * `TiffaneyPsaila/`
    * `NikolinaFilipovPajic/`

### 2. Data Visualization
* **`1_data_visualisation.ipynb`**: A notebook implemented to visualise class and sign attribute distributions.

### 3. Object Detection Notebooks (Task 2a)
Each memebr implemented a different architecture to evaluate performance across different model families:

| Model | Notebook |
| :--- | :--- |
| **RF-DETR** | `2a_RFDETR_TiffaneyPsaila.ipynb` |
| **YOLOv12** | `2a_YOLOv12_MatthewBorgBarthet.ipynb` |
| **YOLOv11** | `2a_object_detector_YOLOv11_ian_caruana.ipynb` |
| **YOLOv8** | `2a_YOLOv8_NikolinaFilipovPajic.ipynb` |

### 4. Sign Attribute Detection (Task 2b)
Similarly, the following notebooks were used to train detectors to identify specific attributes:

* **Condition**: `2b_Condition_MatthewBorgBarthet.ipynb`
* **Mounting Type**: `2b_mounting_type_ian_caruana.ipynb`
* **Sign Shape (Faster R-CNN)**: `2b_sign_shape_FasterRCNN_TiffaneyPsaila.ipynb`
* **View Angle (Faster R-CNN)**: `2b_view_angle_FasterRCNN_NikolinaFilipovPajic.ipynb`

### 5. Results Comparison
* **`2c_results_comparison.ipynb`**: A centralised notebook to compare the results and metrics for all models used in this project.

---

## Setup & Dependencies

To run these notebooks, using Google Colab or a local Jupyter environment is recommended. Most core libraries are pre-installed in Colab. However, certain model frameworks and evaluation tools require manual installation.

### Core Frameworks
* **Object Detection:** `ultralytics` (YOLOv8, v11, v12) and `torchvision` (Faster R-CNN, RetinaNet)
* **Deep Learning & Logging:** `torch`, `tensorboard`
* **Evaluation & Augmentation:** `torchmetrics`, `pycocotools`, `albumentations`
* **Data Handling:** `pandas`, `numpy`, `pyyaml`, `scipy`
* **Visualization:** `matplotlib`, `seaborn`, `Pillow`, `opencv-python`

### Quick Installation
If you are running the project in a local environment, you can install all required external dependencies with the following command:

```bash
pip install ultralytics torch torchvision torchmetrics pycocotools albumentations opencv-python pandas seaborn pyyaml tensorboard scipy
```
---

## Contributors

* **Ian Caruana**
* **Matthew Borg Barthet**
* **Tiffaney Psaila**
* **Nikolina Filipov Pajic**
