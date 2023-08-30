# Gravitational Wave Detection using Machine Learning
![GW Workflow](https://github.com/RobinRosculete/Gravitational-Wave-Detection/blob/main/img/Screenshot%202023-08-29%20at%204.59.11%20PM.png)
## Introduction

This repository contains the implementation of a machine-learning approach to predict and detect gravitational wave signals from the collision of black holes. The inspiration for this work comes from Albert Einstein's prediction of gravitational waves in his general theory of relativity in 1916. Fast forward almost a century, on September 14, 2015, at 5:51 a.m., the first gravitational wave was detected using two LIGO interferometers located in Livingston, Louisiana, and Hanford, Washington [7].

## Problem Statement

The central challenge addressed in this project is predicting and detecting gravitational wave signals from black hole collisions. These signals are incredibly subtle ripples in the fabric of space-time. The main obstacle lies in the fact that the signals collected by gravitational wave detectors are obscured by the noise also collected by these detectors.

## Data Description

The dataset used for this project consists of a collection of time series data files. Each data file contains simulated gravitational wave measurements, acquired by three gravitational wave interferometers: LIGO Hanford, LIGO Livingston, and Virgo. Each time series within the data file represents either detector noise or a combination of detector noise and a simulated gravitational wave signal. Notably, each time series spans 2 seconds and is sampled at 2,048 Hz.

- Training Set: 560,000 .npy data files
- Test Set: Over 200,000 .npy data files

Due to the large size of the dataset and hardware limitations, the focus of this implementation is solely on the training set.<br>
Dataset used can be found here: [G2Net Gravitational Wave Detection Data](https://www.kaggle.com/competitions/g2net-gravitational-wave-detection/data)
## Data Preparation

The initial step involves loading the data files in batches into memory. The data files are then subjected to a noise reduction process to mitigate as much noise as possible. The resultant filtered data files are utilized to generate Constant Q-transform spectrograms. These spectrograms are the foundation for training our machine-learning models, enabling them to discern gravitational wave signals from the noise.



