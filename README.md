![Brain Tumor Detection CNN](Brain_Tumor_Detection_CNN.png)
<br>
![Python](https://img.shields.io/badge/python-v3.11-blue.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
<a target="_blank" href="https://www.linkedin.com/in/tkacz-milosz-data-science/"><img height="20" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
<br>
## Overview

This repository contains the code and resources for a Convolutional Neural Network (CNN) designed to detect brain tumors in MRI scans. The model is trained and evaluated on a dataset consisting of labeled brain MRI images, sourced from two Kaggle datasets ([Dataset 1](https://www.kaggle.com/datasets/ahmedhamada0/brain-tumor-detection) and [Dataset 2](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)).

## Installation

To use the model, follow these steps:

1. Ensure that you have Python 3.11.2 installed.
2. Install the required dependencies by running:
    ```
    pip install matplotlib==3.7.1 tensorflow==2.12.0
    ```
3. Put all the project files into a single folder.
4. Download the datasets from the provided links and rename the zip files to "3000_dataset" and "first_dataset".
5. Unpack the zip files into two separate folders for each dataset.
6. Delete unnecessary folders inside the dataset folders, leaving only "yes" and "no" folders.
7. Unpack the "Model 9867 Accuracy.zip" into a folder with the same name.
8. Run all cells in the provided .ipynb file.

## Folder Structure

Ensure your project folder is structured as follows:

```
- Project Folder
    - 3000_dataset
        - yes
        - no
    - first_dataset
        - yes
        - no
    - Model 9867 Accuracy
        - (Contents of the model)
    - Your.ipynb (The provided notebook file)
```

## Training the Model

The model was trained on 2400 samples and tested on 853 samples, using grayscale images scaled to 64x64 pixels. The final settings achieved a high accuracy of 98%. The training process faced challenges such as finding the optimal model complexity and learning rate. Experimentation led to the removal of Dense Layers and a learning rate between 0.00007 and 0.00008 for optimal results.

## Final Results

The model achieved the following results on the main dataset:
- Accuracy: 98%
- AUC: 0.99
- Precision: 98%
- Recall: 99%

Results on the additional dataset from another source were comparable, demonstrating the versatility of the model. Despite its high accuracy, the model has limitations:
1. Limited to analyzing brain scans from a single perspective.
2. Unable to distinguish between different types of cancer.
3. May struggle with very small cancerous tissue volumes due to heavy downscaling of resolution (64x64 pixels).

## Versions

- matplotlib: 3.7.1
- tensorflow: 2.12.0

Feel free to explore the notebook for more details on the model architecture, training process, and evaluation metrics. For any questions or issues, please open an [issue](link_to_issues) in this repository.