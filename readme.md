# Oral Cancer Detection using Photographic Images

## Table of Contents
1. [Introduction](#introduction)
2. [Datasets](#datasets)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Data Preprocessing](#data-preprocessing)
6. [Data Augmentation](#data-augmentation)
7. [Google Drive Upload](#google-drive-upload)
8. [Model Training](#model-training)
9. [Results](#results)
10. [Contributing](#contributing)
11. [License](#license)
![output](https://github.com/mudasir21/oral-cancer-detection-in-photographic-images/assets/102840359/94639f44-0d1f-4fbf-8047-121162557b9f)

## Introduction
This project focuses on the analysis of oral cancer images. The aim is to download oral cancer image datasets from Kaggle and Mendeley, preprocess the data by removing duplicates and bounding boxes, and enhance the resolution of the images using a Single-Image Super-Resolution (SISR) model. The project also includes data augmentation, uploading augmented data to Google Drive, and running various models (CNN, VGG16, VGG19, DenseNet121) on Google Colab using transfer learning.

## Datasets
We utilize the following datasets for this project:
- **Kaggle Oral Cancer Dataset**: A comprehensive collection of oral cancer images available on [Kaggle](https://www.kaggle.com/datasets/zaidpy/oral-cancer-dataset).
- **Kaggle Tongue Lip Cancer Dataset**: A comprehensive collection of oral cancer images available on [Kaggle](https://www.kaggle.com/datasets/shivam17299/oral-cancer-lips-and-tongue-images.)
- **Mendeley Oral Cancer Dataset**: Another valuable resource for oral cancer images, accessible on [Mendeley](https://data.mendeley.com/datasets/mhjyrn35p4/2).

## Table of Contents
1. [Introduction](#introduction)
2. [Datasets](#datasets)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Data Preprocessing](#data-preprocessing)
6. [Data Augmentation](#data-augmentation)
7. [Google Drive Upload](#google-drive-upload)
8. [Model Training](#model-training)
9. [Results](#results)
10. [Contributing](#contributing)
11. [License](#license)

## Introduction
This project focuses on the detection of oral cancer from photographicimages. The aim is to download oral cancer image datasets from Kaggle and Mendeley, preprocess the data by removing duplicates and bounding boxes, and enhance the resolution of the images using a Single-Image Super-Resolution (SISR) model. The project also includes data augmentation, uploading augmented data to Google Drive, and running various models (CNN, VGG16, VGG19, DenseNet121) on Google Colab using transfer learning.

## Datasets
We utilize the following datasets for this project:
- **Kaggle Oral Cancer Dataset**: A comprehensive collection of oral cancer images available on [Kaggle](https://www.kaggle.com/datasets/zaidpy/oral-cancer-dataset).
- **Kaggle Yongue Lip Cancer Dataset**: A comprehensive collection of oral cancer images available on [Kaggle](https://www.kaggle.com/datasets/shivam17299/oral-cancer-lips-and-tongue-images.)
- **Mendeley Oral Cancer Dataset**: Another valuable resource for oral cancer images, accessible on [Mendeley Data](https://data.mendeley.com/datasets/mhjyrn35p4/2).

## Installation
To get started with this project, follow these steps:

1. **Create and activate a virtual environment**:
    ```sh
    python3 -m venv env
    source env/bin/activate
    ```

2. **Install the required packages**:
    ```sh
    pip install -r requirements.txt
    ```

## Usage
### Downloading Datasets
1. **Kaggle Dataset**:
    - Sign in to your Kaggle account.
    - Download the dataset using the Kaggle API:
      ```sh
      kaggle datasets download -d username/dataset-name
      ```
    - Unzip the downloaded dataset and place it in the `datasets/Oral_Cancer` directory.

2. **Kaggle Dataset**:
    - Sign in to your Kaggle account.
    - Download the dataset using the Kaggle API:
      ```sh
      kaggle datasets download -d username/dataset-name
      ```
    - Unzip the downloaded dataset and place it in the `datasets/Tongue_Lip` directory.

3. **Mendeley Dataset**:
    - Sign in to your Mendeley account.
    - Download the dataset manually and place it in the `datasets/Mendeley` directory.

## Data Analysis
The data analysis include:
1. **Class Distribution**: How are the images in differnet datasets distributed
2. **Visual Inspection**: To check for images deformations and irregularities 
3. **Image Stastics**: To get insights into how images resolution, height, width and pixels are distributed by computing mean, mode, minimum and maximum of each value.
4. **Further Analysis**: It include the distribution among various class of resoltion and height width<br>
For this run the below scripit
```sh
image_stastics.ipynb
``` 
## Data Preprocessing
The preprocessing steps include:
1. **Removing Duplicate Images**: We identify and remove any duplicate images to ensure unique entries in the dataset.
2. **Removing Bounding Boxes**: We manually remove bounding boxes from the images to focus on the entire image content.
3. **Increasing Image Resolution**: We use a Single-Image Super-Resolution (SISR) model to enhance the resolution of the images.

### Preprocessing Script
You can run the preprocessing notebooks individually:
1. **Merging Data**
```sh
moving_data.ipyb
```
2. **Duplicate Image Removing**
```sh
dup_image_remove_hash.ipynb
```
3. **Enhancing Image Resolution**<br>
For super resolution you have to download the models manually and put them in the sr_models folder
```sh
super_resolution.ipynb
```
4. **Manually Crop the boxes and remove images with water marks**
```sh
to_be_done_manually
```

## Data Augmentation
We augment the data using OpenCV to create a more diverse dataset and improve model performance. Augmentation techniques include:
- Rotation
- Flipping
- Shear
- Contrast 
- Brightness
- Grid Distort

### Augmentation Script
You can run the augmentation script with:
```sh
data_augmentation.ipynb
```

## Google Drive Upload
After augmentation, we upload the processed dataset to Google Drive for easy access during model training on Google Colab.


## Model Training
We use Google Colab to leverage its GPU capabilities for training our models. The models used in this project include:
- Convolutional Neural Network (CNN)
- VGG16
- VGG19
- DenseNet121

### Running Models on Google Colab
1. Open/Upload the `<notebook_name.ipynb`(As we have different notebooks which are in the notebooks folder) notebook in Google Colab.
2. Mount your Google Drive to access the dataset.
3. Follow the instructions in the notebook to run each model using transfer learning.

## Results
Results are contained with each notebook 

## Dependecies 
Most of the training notebooks on different architectures were run inside google collab. The preprocessing, analysis, resolution notebooks we run locally  
