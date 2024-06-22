# Pix2Pix-Diffusion-for-Brain-Tumor-Segmentation

This repository contains a Jupyter notebook for training a Pix2Pix model using diffusion techniques to segment brain tumors from MRI scans. The dataset used is from the Medical Segmentation Decathlon (MSD) Task 01: Brain Tumor.

## Objective

The primary objective of this project is to develop a machine learning model capable of accurately segmenting brain tumors from MRI images. Brain tumor segmentation is a critical task in medical imaging as it assists in diagnosis, treatment planning, and monitoring the progression of the disease. By leveraging advanced machine learning techniques like Pix2Pix with diffusion, this project aims to achieve high-quality segmentation results that can support medical professionals in their work.

## Data

The dataset used in this project is from the Medical Segmentation Decathlon (MSD) Task 01: Brain Tumor. The dataset includes MRI scans with corresponding labeled masks that indicate the location and boundaries of brain tumors. The data is provided in a tar file and contains two main directories after extraction:

imagesTr: Contains the training MRI images.

labelsTr: Contains the corresponding labeled masks for the training images.

Each MRI scan and its corresponding label are in NIfTI format, a common format for medical imaging data. The notebook includes steps to extract, preprocess, and visualize these images to prepare them for model training.

## Model
### Pix2Pix Model

The Pix2Pix model is a type of conditional Generative Adversarial Network (cGAN) designed for image-to-image translation tasks. In this project, the Pix2Pix model is used to translate MRI images (input) into segmented tumor masks (output). The model consists of two main components:

Generator: The generator creates synthetic images (segmented masks) from input images (MRI scans). It tries to produce outputs that are indistinguishable from the real segmented masks.

Discriminator: The discriminator evaluates the authenticity of the generated images by distinguishing between real segmented masks and those produced by the generator. It helps the generator improve its outputs through adversarial training.

## Diffusion Techniques

Incorporating diffusion techniques into the Pix2Pix framework helps in refining the generated images, making the segmentation boundaries more accurate and smooth. Diffusion models work by iteratively refining the image through a series of noise reduction steps, enhancing the quality of the output.

## Training and Evaluation

The notebook includes steps to train the Pix2Pix model with diffusion techniques:

Data Preparation: Extracting and preprocessing the data, including normalizing the images and splitting them into training and validation sets.

Model Training: Setting up the Pix2Pix model with diffusion and training it on the prepared data. This involves defining the generator and discriminator architectures, setting up loss functions, and optimizing the model parameters through iterative training.

Evaluation: After training, the model's performance is evaluated on a test set. The notebook includes code to visualize the segmented outputs and compare them with the ground truth labels, providing metrics to assess the model's accuracy and effectiveness.

## Usage

Open the Jupyter notebook:

bash

Copy code

jupyter notebook pix2pix_diffusion.ipynb

Follow the steps in the notebook to:

Import necessary libraries.

Extract the dataset.

List and verify the extracted files.

Preprocess the data.

Train the Pix2Pix model.

Evaluate the model's performance.
