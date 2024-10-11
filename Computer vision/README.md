
# Computer Vision Project

This project focuses on computer vision tasks with tools for managing files and models for image classification and object detection.

## Folder Structure

The project is organized as follows:

```bash
Computer Vision/
│
├── FileManagement/
│   ├── check_move_duplicate.ipynb
│   ├── copy_split.ipynb
│   ├── count file in folder.ipynb
│   ├── count_multi_instances.ipynb
│   ├── forquicktest.ipynb
│   └── rename.ipynb
│
├── Models/
│   ├── Classification/
│   │   ├── Tool/
│   │   │   ├── confusion_matrix.ipynb
│   │   │   └── dataset_preparation
│   │   └── Resnet-50.ipynb
│   │     
│   └── Object Detection/
│       ├── Tool/
│       │   └── display.ipynb
│       │    
│       ├── dataset.yaml
│       └── YOLO_model.ipynb
│ 
└── README.md
```

### 1. **FileManagement Folder**
   This folder contains utilities and tools that assist in file management and processing tasks. These tools streamline operations like organizing datasets, pre-processing images, and managing output results. The tools include:

   - **check_move_duplicate.ipynb**: A tool to check, move, and handle duplicate files.
   - **copy_split.ipynb**: Script for copying and splitting datasets into training, validation, and test sets.
   - **count file in folder.ipynb**: Script to count the number of files in a folder.
   - **count_multi_instances.ipynb**: A tool for counting multiple instances in a dataset.
   - **forquicktest.ipynb**: A script for quick tests and file checks.
   - **rename.ipynb**: A bulk file renaming tool.

### 2. **Models Folder**
   This folder contains all models related to image classification and object detection. It is divided into two main subfolders:

   - **Classification:**
     This subfolder contains models, scripts, and configurations related to image classification tasks. These models categorize images into predefined classes. Includes:
     - **Tool/confusion_matrix.ipynb**: Notebook for generating confusion matrices to evaluate classification performance.
     - **Tool/dataset_preparation**: Scripts for preparing datasets for training and testing.
     - **Resnet-50.ipynb**: Notebook for training and evaluating a ResNet-50 model for image classification.
   
   - **Object Detection:**
     This subfolder holds models, scripts, and configurations for object detection tasks. These models are used to detect and localize objects within images. Includes:
     - **Tool/display.ipynb**: Notebook for visualizing detection results.
     - **dataset.yaml**: Configuration file for the object detection dataset.
     - **YOLO_model.ipynb**: Notebook for training and evaluating the YOLO model for object detection.

## Installation

To set up and run the project, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/teamseankukps/code.git
   ```

2. **Navigate to the project directory:**
   ```bash
   cd computer-vision
   ```






