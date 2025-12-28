# **Electroencephalography Motor Movement/Imagery Classification Using Random Forest and Convolutional Neural Networks**

## **Problem Description**

The goal of this project is to classify electroencephalography (EEG) recordings corresponding to different motor conditions using machine learning techniques. Specifically, this project focuses on distinguishing between executed and imagined hand movements based on EEG data.

This is a supervised classification problem where EEG segments recorded during real motor execution and motor imagery are used as input. The project compares a classical machine learning approach (Random Forest) with a neural network model (Convolutional Neural Network) in their ability to classify patterns from EEG signals.

## **Data**

The project will use the **EEG Motor Movement/Imagery Dataset** from **PhysioNet**.

- **Link:** https://physionet.org/content/eegmmidb/1.0.0/
- **Description:** The dataset consists of over 1500 one- and two-minute 64-channel EEG recordings collected from 109 subjects during real and imagined motor tasks. EEG signals are sampled at 160 Hz and include event annotations indicating rest and motor activity. EEG segments corresponding to executed and imagined hand movements will be extracted and used as class labels.

## **Methodology**

Two modeling approaches will be implemented and compared:

- **Random Forest (RF):** implemented using **scikit-learn**. The model will be trained on minimally processed EEG features, such as fixed-length signal windows and simple statistical descriptors, to serve as a classical machine learning baseline.
- **Convolutional Neural Network (CNN):** 1D CNN implemented using **PyTorch**. The CNN will operate directly on multichannel EEG time-series data to learn temporal patterns relevant for motor imagery classification.

Model performance will be evaluated using classification accuracy and confusion matrices. Training and validation loss curves will be analyzed to assess convergence and overfitting.

### **Used stack:**

-  Python
-  NumPy
-  pandas
-  scikit-learn
-  PyTorch

# Plan of work

1. **Data Preparation:**
    
    Download the EEG dataset, segment recordings into fixed-length time windows, normalize signals, and select hand-related motor execution and imagery trials.
    
2. **Model Development:**
    
    Train a RF classifier on simple statistical features, and implement a 1D CNN in PyTorch using raw EEG windows.
    
3. **Evaluation and Analysis:**
    
    Evaluate both models using accuracy and confusion matrices, analyze training behavior, and compare model performance.
    
4. **Reporting:**
    
    Summarize methodology, results, and key observations in the final report.
