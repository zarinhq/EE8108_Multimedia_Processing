# EE8108_Multimedia_Processing

## Introduction

Human Stress management has become an important factor in the present days as it causes various chronic diseases such as depression, cancer, and various cardiovascular diseases. Classifying the stress signals using electrocardiogram (ECG) signals are more popular because of the signal acquisition method. When a person is in stressful situation, a displacement occurs in the ECG signals, hence it is possible to detect the stress signals by experimenting with the ECG signals. In this study, two convolution neural network models have been proposed to accurately analyse the stress signals from the ECG signals and both the models has got an accuracy around 96% with a slight difference. To maximize the performance of the model, the data was preprocessed by removing the noise from the ECG signals as well as to prevent the underfitting of the model, the two classes of the dataset was balanced by generating synthetic data by implementing SMOTE technique. As the performance evaluation benchmarks of this stress classification model, confusion matrix and receiver operating curve were applied. 

## Dependencies
1.	Tensorflow – 2.4.0 -rc0
2.	Keras – 2.4.3
3.	Scikit learn
4.	Pandas
5.	Numpy
6.	Imbalanced Learn

## Getting Started
### Downloading Dataset
In this project, two datasets of MIT-BIH is used. One of them is **Arrythmia** dataset and another is **ST Change** dataset. These datasets can be downloaded from the following link,
- [Arrythmia dataset](https://physionet.org/static/published-projects/mitdb/mit-bih-arrhythmia-database-1.0.0.zip)
- [ST Change Dataset](https://physionet.org/static/published-projects/stdb/mit-bih-st-change-database-1.0.0.zip)

**Note:** This is an optional step and already part of **Preprocessing dataset** step code.

### Preprocessing dataset
The datasets were preprocessed using **Low pass** filter to reduce the noise from the signal. In order to balance the datapoints **SMOTE** has been applied to generate synthetic data and later converted into spectrogram. The code for preprocessing all the data of both datasets is available in [**Preprocessing_ECG_Data.ipynb**](https://github.com/zarinhq/EE8108_Multimedia_Processing/blob/main/Preprocessing_ECG_Data_.ipynb) notebook.  

However, by running the [**Preprocessing_ECG_Data.ipynb**](https://github.com/zarinhq/EE8108_Multimedia_Processing/blob/main/Preprocessing_ECG_Data_.ipynb) notebook, the datasets can be downloaded and preprocessed. So, there will be no need to download the dataset separately.

**Note:** Data preprocessing is a time-consuming process and requires high amount of RAM usage, hence preprocessed datasets are also uploaded in this [**Download link**](https://drive.google.com/file/d/1BMWkYjPMo_hcPK3WQ9_DyJwxGMVyafzC/view?usp=sharing). So you can just download the preprocessed datasets and move to **Model Train** step.

### Model Train
To train the model, the **data_ecg** folder need to be uploaded in the working directory. **data_ecg** folder can be get after preprocessing the data, or directly downloading the folder from the above link.

Later, [**Version_1_Stress_classification_CNN.ipynb**](https://github.com/zarinhq/EE8108_Multimedia_Processing/blob/main/Version_1_Stress_classification_CNN.ipynb) and [**Version_2_Stress_classification_CNN.ipynb**](https://github.com/zarinhq/EE8108_Multimedia_Processing/blob/main/Version_2_Stress_classification_CNN.ipynb) need to be executed to train and evaluate the models. 

The trained models are also uploaded in the repository as [**CNN_version_1.h5**](https://github.com/zarinhq/EE8108_Multimedia_Processing/blob/main/CNN_version_1.h5) and [**CNN_version_2.h5**](https://github.com/zarinhq/EE8108_Multimedia_Processing/blob/main/CNN_version_2.h5)
