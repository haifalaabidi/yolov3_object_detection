# YOLO Object Detection and Document Part Extraction
## Introduction
This project focuses on using the YOLO (You Only Look Once) algorithm for object detection and extracting specific parts from documents, particularly resumes. The key components include data extraction, dataset preparation, custom YOLO model training, and object detection with model inference.
## Data Extraction and Labeling
-- The extract_blocks_and_crop.py script extracts labeled blocks from images using a JSON file with annotations. It normalizes coordinates, crops and saves regions, creating an organized dataset for model training.
## Dataset Preparation
The extracted blocks are organized into a custom dataset, and train.txt and test.txt files are generated to facilitate model training.
## Custom YOLO Model Training
The Darknet framework is used for training the custom YOLO model. The training command includes the custom dataset, customed configuration file (yolov3_custom.cfg), and pre-trained weights (darknet53.conv.74).
## Object Detection and Model Inference
The script for object detection reads the pre-trained YOLO model and configuration files, loads an image, performs inference, and displays bounding boxes with labels and confidence scores.
## Usage
Data Preparation:
1. Place image files in the specified folder.
Annotate images and generate JSON files for labeling.

2. Run Data Extraction Script:
Execute extract_blocks_and_crop.py to create a labeled dataset.

3.Prepare Dataset:
Run trainNtestFilesCreater to generate train.txt and test.txt files.

4.Train Custom YOLO Model:
Use the Darknet framework to train the YOLO model.

5.Object Detection:
Run the object detection script on an image for inference.

## Files and Directories
/path/to/annotations.json: JSON files with block annotations.
/path/to/images: Folder containing input images.
/path/to/output: Output folder for cropped blocks.
/content/drive/MyDrive/yolo-data-extraction/custom_dataset: Custom dataset containing images and annotations.
/content/drive/MyDrive/yolo-data-extraction/darknet: Darknet framework for YOLO

## Additional Notes
Ensure GPU availability for accelerated training (!nvidia-smi).
Mount Google Drive for file access (drive.mount('/content/drive')).
Customize the scripts based on specific project requirements.
Review and adjust confidence thresholds and parameters for optimal results.


