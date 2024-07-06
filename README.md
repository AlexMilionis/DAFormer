# Description
Overview\n
This project aims to reproduce the results presented in the paper "DAFormer: Improving Network Architectures and Training Strategies for Domain-Adaptive Semantic Segmentation" by Lukas Hoyer, Dengxin Dai, and Luc Van Gool. The paper introduces a novel unsupervised domain adaptation (UDA) method for semantic segmentation using a Transformer-based network architecture named DAFormer.

Paper Details
Title: DAFormer: Improving Network Architectures and Training Strategies for Domain-Adaptive Semantic Segmentation
Authors: Lukas Hoyer, Dengxin Dai, Luc Van Gool
Published by: ETH Zurich, MPI for Informatics, KU Leuven
Publication Date: March 2022
Link to Paper: DAFormer Paper

Objectives
The primary goal of this project is to implement the DAFormer architecture and its training strategies as described in the paper and to verify the performance results on the specified datasets.

Methodology
DAFormer Architecture
DAFormer consists of a Transformer encoder and a multi-level context-aware feature fusion decoder. The key components include:

Transformer Encoder: Based on Mix Transformers (MiT), tailored for semantic segmentation.
Context-Aware Feature Fusion Decoder: Uses multi-level features with depthwise separable convolutions and multiple dilation rates for robust segmentation.
Training Strategies
Rare Class Sampling (RCS): Improves the quality of pseudo-labels by sampling images with rare classes more frequently.
Thing-Class ImageNet Feature Distance (FD): Regularizes the network using feature distances between the ImageNet pre-trained model and the DAFormer model.
Learning Rate Warmup: Gradually increases the learning rate at the start of training to stabilize and enhance feature transfer from ImageNet pre-training.
Datasets
Source Domain: GTA dataset (24,966 synthetic images)
Target Domain: Cityscapes dataset (2,975 training images, 500 validation images)
Implementation
Dependencies
Python 3.8+
PyTorch
mmsegmentation
CUDA-enabled GPU
