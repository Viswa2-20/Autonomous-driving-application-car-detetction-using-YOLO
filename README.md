# Autonomous Driving Application: Car Detection

This project implements real-time car detection for autonomous driving applications using the YOLO (You Only Look Once) model. YOLO is known for its fast and accurate performance in object detection tasks, which makes it well-suited for real-time applications like autonomous driving.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Model](#model)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview

The goal of this project is to detect cars in images, which is a crucial task for autonomous vehicles. The YOLO model is used to identify objects (in this case, cars) in images and draw bounding boxes around them.

This project uses pre-trained weights for the YOLO model, and the code demonstrates how to load the model, process input images, and output the detection results.

## Dataset

The project works with sample images for car detection, but it can be extended to any dataset containing images of cars and other objects.

- **Input:** Images of roads and cars, stored in the `images` directory.
- **Output:** Detected bounding boxes drawn on the input images.

## Model

This project uses the YOLO model, which is capable of detecting multiple objects in an image by predicting both their bounding boxes and their class labels.

- **YOLO:** A convolutional neural network that divides the image into grids and, for each grid, predicts bounding boxes and corresponding class probabilities.

## Installation

To run the code in this project, follow these steps:

1. Clone the repository:

    ```bash
    git clone https://github.com/your-repo/autonomous-driving-car-detection.git
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Download the pre-trained YOLO model weights and place them in the appropriate folder.

## Usage

1. Place the images for car detection in the `images/` directory.
2. Run the notebook or the Python script to perform detection on the images.
3. The results (images with bounding boxes) will be saved in the `out/` directory.

### Example

To run detection on an image named `test.jpg`, use the following code:

```python
out_scores, out_boxes, out_classes = predict("test.jpg")

