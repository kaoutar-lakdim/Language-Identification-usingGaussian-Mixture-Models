# Language-Identification-and speaker identification
## Language-Identification-usingGaussian-Mixture-Models
## Introduction
This project aims to develop a language identification system using Gaussian Mixture Models (GMMs). It enables automatic detection and classification of different languages based on the given text data. This README provides an overview of the project, its objectives, the data used, the preprocessing steps, the model construction, evaluation metrics, and a conclusion.

<p align="center">
  <img src="https://github.com/kaoutar-lakdim/Language-Identification-usingGaussian-Mixture-Models/assets/74473164/8ef52fea-7ad0-45ba-8edb-aaf514dd2865" alt="schema">
</p>


## Table of Contents
- [Introduction](#introduction)
  - [Objective of the Project](#objective-of-the-project)
  - [Description of the Data Used](#description-of-the-data-used)
  - [Descriptive Schema](#descriptive-schema)
- [Prétraitement des données](#prétraitement-des-données)
- [Construction du modèle](#construction-du-modèle)
- [Évaluation du modèle](#évaluation-du-modèle)
- [Speaker Identification](#speaker-identification)
- [Conclusion](#conclusion)


### Objective of the Project

In my project, I focus on language identification from an audio file. The goal is to detect the language used in the audio. I have worked with various languages such as English, Arabic, French, and Spanish.

In this project, I describe the steps I followed to build my language identification model. Firstly, I present the description of the database I used to train and test my model. Then, I discuss the preprocessing steps, including silence removal and feature extraction. After that, I explain the construction of the language identification model using Gaussian Mixture Models (GMMs) and the training process. Finally, I evaluate the performance of the model using appropriate metrics and discuss the results


### Description of the Data Used
For the description of my database, I collaborated with my classmates in collecting the data. Each of us gathered two audio files (one male and one female) in the languages we selected for our project.

Each audio file has a duration of at least one minute, and we stored all the audio files in a shared folder on Google Drive. This collaborative approach allowed us to gather a diverse set of audio data for our language identification project.

The dataset is stored in a shared folder on Google Drive, which can be accessed through the following link https://drive.google.com/drive/folders/1OezDyIRWZDsjmb6x7YXuEObjDk8G_XlL?usp=sharing
<p align="center">
  <img src="https://github.com/kaoutar-lakdim/Language-Identification-usingGaussian-Mixture-Models/assets/74473164/03b17762-82ba-4908-9102-31d128c5230f" alt="schema">
</p>

### Descriptive Schema
A descriptive schema is developed to organize and represent the language identification system's structure, components, and processes. It provides an overview of the system's architecture, data flow, and the interaction between different modules.
<p align="center">
  <img src="https://github.com/kaoutar-lakdim/Language-Identification-usingGaussian-Mixture-Models/assets/74473164/54ca9914-f5b7-4fd9-9e52-55a9563b317c"
 alt="schema">
</p>


<p align="center">
  <img src="https://github.com/kaoutar-lakdim/Language-Identification-usingGaussian-Mixture-Models/assets/74473164/5cf22015-e01f-4034-98b9-46bf739b3139"
 alt="schema">
</p>

## Prétraitement des données
The preprocessing stage involves two main steps:
1. **Élimination de silence**: Elimination des parties silencieuses du texte.
   <p align="center">
  <img src="https://github.com/kaoutar-lakdim/Language-Identification-usingGaussian-Mixture-Models/assets/74473164/60131c27-ae89-4009-b86b-11bdc93ee168"
 alt="schema">
</p>

Upon comparison, it is observed that the duration decreases after removing the silence or noise from the audio.

3. **Extraction de caractéristiques (MFCC)**: Extraction des caractéristiques du texte en utilisant les coefficients MFCC (Mel Frequency Cepstral Coefficients).

## Construction du modèle
The model construction phase includes the following steps:
1. **Train/Test Split**:
   
In this project, we have collected audio samples for both male and female speakers in each language of interest. The dataset includes recordings of individuals speaking in languages such as English, Arabic, French, and Spanish. To ensure a balanced representation, we have split the audio samples into separate training and testing sets. This division allows us to train our language identification model on a diverse range of speakers and evaluate its performance accurately on unseen data.
3. **Gaussian Mixture Model**:
 ###  Model Training
   Construction du modèle de Mélange Gaussien pour chaque langue à l'aide des caractéristiques extraites.
 ### Saving the Model
  <p align="center">
  <img src="https://github.com/kaoutar-lakdim/Language-Identification-usingGaussian-Mixture-Models/assets/74473164/46a6e4d1-2ad9-473f-bc0a-55bdcf625e7f"
 alt="schema">
</p>

## Évaluation du modèle
I performed model evaluation using the Receiver Operating Characteristic (ROC) curve, which is a commonly used method for assessing the performance of a binary classification model. The ROC curve illustrates the relationship between the True Positive Rate (TPR) and the False Positive Rate (FPR) for various classification threshold values.

By plotting the ROC curve, we can visualize and analyze the model's ability to discriminate between positive and negative classes. The TPR represents the proportion of actual positive instances correctly identified as positive, while the FPR represents the proportion of actual negative instances incorrectly classified as positive.

The ROC curve provides valuable insights into the model's classification performance across different thresholds. The area under the ROC curve (AUC-ROC) is often used as a summary metric to quantify the overall discriminatory power of the model. A higher AUC-ROC value indicates better model performance in distinguishing between positive and negative classes

This code utilizes the true labels "y_true" and the predicted scores "scores" to calculate and plot the Receiver Operating Characteristic (ROC) curves for three different datasets
<p align="center">
  <img src="https://github.com/kaoutar-lakdim/Language-Identification-usingGaussian-Mixture-Models/assets/74473164/e5baefa5-263d-484e-8e0b-cf48b435f8dc"
 alt="schema">
</p

### Remarks
Upon analysis, we observe that the recordings lasting 15 seconds yield the best results, followed by the recordings of 10 seconds, and then the recordings of 5 seconds. This suggests that the duration of audio recordings has an influence on the performance of the prediction model.

Additionally, it is worth noting that the recordings of 15 seconds converge more rapidly in terms of model performance compared to the other recording durations. This indicates that longer recordings provide more comprehensive and informative data for the model to make accurate predictions.

These observations emphasize the importance of considering the duration of audio recordings when developing and evaluating prediction models, as it can significantly impact their performance and convergence rate

## Model Evaluation with Different GMMs
<p align="center">
  <img src="https://github.com/kaoutar-lakdim/Language-Identification-usingGaussian-Mixture-Models/assets/74473164/c71b871e-688f-4ea3-876c-e46f03961c47"
 alt="schema">
</p


I have obtained a comparison curve between different GMM models, and I have observed that the GMM with 32 components achieved the best result. It was followed by the GMM with 128 components, then the GMM with 64 components, and finally, the GMM with 16 components, which yielded the lowest result.

This comparison provides valuable insights into the performance of the different GMM models in language identification. It indicates that increasing the number of components generally improves the model's accuracy and effectiveness. However, there may be a diminishing return as the number of components increases, as evidenced by the lower performance of the GMM with 128 components compared to the GMM with 32 components

<p align="center">
  <img src="https://github.com/kaoutar-lakdim/Language-Identification-usingGaussian-Mixture-Models/assets/74473164/c61a8c50-988e-408a-a279-54f5e189e5f1"
 alt="schema">
</p


### Feature Extraction

The speaker identification feature aims to determine the identity of the speaker in an audio sample. This functionality can be useful in various applications such as forensic analysis, voice-based user authentication, or personalized services.

### Feature Extraction

To perform speaker identification, the first step is to extract relevant features from the audio samples. Commonly used features include Mel-Frequency Cepstral Coefficients (MFCCs), pitch contour, spectral features, or prosodic features. These features capture unique characteristics of an individual's voice.

### Model Training

Once the features are extracted, a machine learning model is trained to recognize different speakers. Popular techniques for speaker identification include Gaussian Mixture Models (GMMs), Hidden Markov Models (HMMs), Support Vector Machines (SVMs), or deep learning-based models such as Convolutional Neural Networks (CNNs) or Recurrent Neural Networks (RNNs).

Training the speaker identification model involves providing labeled audio samples from different speakers and optimizing the model's parameters to minimize identification errors. Cross-validation or train-test splits can be employed to assess the model's performance.

### Speaker Identification Inference

After the model is trained, it can be used for speaker identification inference on new audio samples. During inference, the model takes the extracted features from the input audio and predicts the identity of the speaker. The model outputs the most likely speaker label or provides a probability distribution over potential speakers.

### Integration with User Interface

In this project, the speaker identification functionality is integrated into the existing user interface alongside the language identification feature. Users can upload an audio sample and choose whether they want to identify the language or the speaker. The system processes the input accordingly and presents the results on the user interface.

It's important to note that the performance of the speaker identification model depends on the quality and diversity of the training data, as well as the effectiveness of the chosen feature extraction techniques and machine learning algorithms.




****
## Conclusion
Cette projet démontre la faisabilité de l'identification de langues à l'aide de modèles de Mélange Gaussien. Les résultats obtenus montrent une précision satisfaisante et une classification précise des différentes langues.
