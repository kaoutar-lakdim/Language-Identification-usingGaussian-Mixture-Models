# Language-Identification-usingGaussian-Mixture-Models

## Introduction
This project aims to develop a language identification system using Gaussian Mixture Models (GMMs). It enables automatic detection and classification of different languages based on the given text data. This README provides an overview of the project, its objectives, the data used, the preprocessing steps, the model construction, evaluation metrics, and a conclusion.

<p align="center">
  <img src="https://github.com/kaoutar-lakdim/Language-Identification-usingGaussian-Mixture-Models/assets/74473164/8ef52fea-7ad0-45ba-8edb-aaf514dd2865" alt="schema">
</p>

## Table of Contents
## Table of Contents
- [Introduction](#introduction)
  - [Objective of the Project](#objective-of-the-project)
  - [Description of the Data Used](#description-of-the-data-used)
  - [Descriptive Schema](#descriptive-schema)
- [Prétraitement des données](#prétraitement-des-données)
- [Construction du modèle](#construction-du-modèle)
- [Évaluation du modèle](#évaluation-du-modèle)
- [Conclusion](#conclusion)
- [Problèmes](#problèmes)

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



## Prétraitement des données
The preprocessing stage involves two main steps:
1. **Élimination de silence**: Elimination des parties silencieuses du texte.
2. **Extraction de caractéristiques (MFCC)**: Extraction des caractéristiques du texte en utilisant les coefficients MFCC (Mel Frequency Cepstral Coefficients).

## Construction du modèle
The model construction phase includes the following steps:
1. **Train/Test Split**: Répartition des données en ensembles d'entraînement et de test.
2. **Gaussian Mixture Model**: Construction du modèle de Mélange Gaussien pour chaque langue à l'aide des caractéristiques extraites.

## Évaluation du modèle
L'évaluation du modèle de langue comprend les mesures de performance suivantes:
- **Mesures de performance**: Utilisation de la méthode `sample.score` pour évaluer les performances du modèle sur les données de test.

## Conclusion
Cette projet démontre la faisabilité de l'identification de langues à l'aide de modèles de Mélange Gaussien. Les résultats obtenus montrent une précision satisfaisante et une classification précise des différentes langues.

## Problèmes
Dans cette section, les problèmes rencontrés durant le projet seront décrits en détail, ainsi que les solutions ou les pistes de résolution envisagées.

Feel free to modify and expand this README file according to your project's specific details and requirements. Include installation instructions, usage examples, and any additional information that would be helpful for users who want to utilize or contribute to your language identification project.
