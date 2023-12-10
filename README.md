# Nuclei-Segmentation-using-U-NET

# Overview
This project aims to automate the detection of cell nuclei in microscopic images using the U-Net++ architecture. The task is part of the 2018 Data Science Bowl, where the goal is to accelerate research for various diseases by expediting nucleus detection.

# Motivation
Identifying cell nuclei is a crucial step in understanding biological processes and expediting drug development. By automating nucleus detection, this project aims to contribute to the acceleration of medical research and the development of cures for various diseases.

# Dataset
The dataset used in this project is from the 2018 Data Science Bowl, consisting of microscopic images for training (stage1_train) and testing (stage1_test). The images contain information about the location and characteristics of cell nuclei.

# Model Architecture: U-Net++
Overview:
U-Net++ is an enhanced version of the U-Net model for semantic segmentation. It introduces skip connections and deep supervision to improve segmentation accuracy.


Key Features:
Encoder-Decoder Structure: Hierarchical feature extraction through an encoder-decoder architecture.
Skip Connections: Connections between encoder and decoder blocks for leveraging low and high-level features.
Deep Supervision: Intermediate predictions at various decoder stages to address information loss.


Building Process:
Input Layer: Takes (96, 96, 3) images as input.
Encoder Blocks: Convolutional blocks and max-pooling form the encoder.
Skip Connections: Concatenation of encoder and decoder blocks for feature fusion.
Decoder Blocks: Upsampled feature maps refined by skip connections.
Deep Supervision Output: Intermediate predictions for improved training.
Output Layer: Final segmentation map obtained from the last decoder block.


Benefits:
Multi-Level Feature Fusion: Improved feature capturing at different scales.
Information Retention: Mitigation of information loss during downsampling.


Usage:
Build and train the model using the UNetPlusPlus class. Compile and summarize the model with the CompileAndSummarizeModel method.

