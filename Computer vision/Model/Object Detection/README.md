# YOLOv8 Model Training and Inference

This project demonstrates how to use the YOLOv8 model for object detection, focusing on training a custom dataset related to plant health classification. The project leverages Google Colab for cloud-based training and includes detailed steps for training, validation, and inference using the YOLOv8 framework.

## Project Structure

- **`YOLO_model.ipynb`**: A Jupyter notebook that contains the entire workflow for training and evaluating a YOLOv8 model. It includes steps for dataset loading, model training, validation, and inference.
- **Dataset**: The dataset is stored training, validation, and test sets.

## Dataset

The dataset is structured into three main directories:

- **Training Data**: `/train` your path
- **Validation Data**: `/val` your path
- **Test Data**: `/test` your path

The dataset consists of 7 classes: (your class)
- class1
- class2
- class3
- class4
- class5
- class6
- class7

## Dependencies

To run the notebook, the following dependencies are required:

- **YOLOv8 by Ultralytics**: You can install it by running the command below in a Jupyter cell:
  
  ```bash
  !pip install ultralytics==8.0.196
  ```

- **Supervision library**: Used for visualization. Install using:

  ```bash
  !pip install supervision
  ```

## Instructions for Use

### Step 1: Set up the YOLOv8 Environment

Install YOLOv8 and its dependencies:

```python
!pip install -q ultralytics==8.0.196
!pip install -q supervision
```

### Step 2: Model Training

1. **Initialize the YOLOv8 model**:
   ```python
   from ultralytics import YOLO
   model = YOLO('yolov8n.pt')  # Use the YOLOv8 nano model
   ```

2. **Train the model**:
   Define the dataset and start training the model:
   ```python
   model.train(data='/content/drive/MyDrive/YangBOT/Dataset/dataset.yaml', epochs=50)
   ```

   - **`data`**: Path to the `.yaml` file containing dataset paths and class names.
   - **`epochs`**: Number of training epochs.

### Step 3: Model Validation

After training, you can validate the model using the validation dataset:

```python
model.val(data='/content/drive/MyDrive/YangBOT/Dataset/dataset.yaml')
```

This will output metrics like accuracy, mAP (mean Average Precision), and loss.

### Step 4: Inference

To use the trained model for inference on new images, run the following code:

```python
results = model('/path/to/image.jpg')
results.show()  # Display the prediction on the image
```

This will show bounding boxes and class predictions on the image.


## Acknowledgements

- This project uses the [YOLOv8 framework](https://github.com/ultralytics/ultralytics) for object detection.
- The dataset and annotations are manually created for plant health classification.
- This notebook was developed in Google Colab, leveraging its GPU capabilities for faster training.
