# Computer Vision Cookie Inspection System

## Project Overview
This project simulates an automated visual inspection system for a food production line. In modern Industrie 4.0 environments, manual quality control is a bottleneck. This system automates the inspection process by utilizing image processing techniques to identify product classes and calculate ingredient distribution ratios.

The objective is to ensure that every unit on the production line meets predefined Quality Assurance (QA) control limits, reducing scrap rates and ensuring consistent product quality.

## Methodology
The system follows a modular engineering pipeline designed for robust feature extraction:

1 **Image Pre-processing:** Utilizes Gaussian blurring and adaptive color space conversion (RGB to HSV) to minimize lighting noise and isolate the product from the manufacturing environment.

2 **Segmentation:** Implements Otsu’s thresholding and Canny edge detection to create a precise binary mask of the product.

3 **Feature Engineering:**

* **Texture Analysis:** Computes Gray-Level Co-occurrence Matrix (GLCM) properties, specifically Contrast and Homogeneity, to classify product types.

* **Information Complexity:** Uses Entropy calculation to quantify surface detail density.

4 **Quality Control:** Performs pixel-intensity segmentation on the product's saturation channel to identify and quantify ingredient ratios (e.g., chocolate chip distribution), triggering an automatic "Accept/Reject" assessment based on density thresholds.

## Technical Implementation
The pipeline is built with modularity and scalability in mind:

* **Language:** Python

* **Computer Vision:** OpenCV, scikit-image

* **Numerical Analysis:** NumPy, SciPy

* **Visualization:** Matplotlib

## Project Architecture
* **identify_cookie():** The core processing function that encapsulates the full CV pipeline.

* **data/:** Directory for input batch processing.

* **analysis_results:** Generates visual reports including intensity histograms and segmented masks for verification.

## Getting Started
### Prerequisites
Ensure you have the required libraries installed:

Bash
pip install numpy opencv-python scikit-image scipy matplotlib


### Usage
1 Place your production line images in the ./data/ directory.

2 Run the main script to process the batch.

3 The system will output processed masks, feature metrics (Contrast, Entropy, Ingredient Ratio), and a visual audit report.

## Engineering Application
This project demonstrates the ability to translate physical production requirements into digital data workflows. It highlights core competencies in:

* **Process Automation:** Transforming manual visual inspection into an automated, data-driven task.

* **Root Cause Analysis:** Using texture and intensity data to diagnose process deviations.

* **Quality Management:** Establishing quantifiable metrics (ingredient ratios) to enforce production standards.