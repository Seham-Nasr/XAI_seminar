# XAI_seminar
This repository contains Tutorial notebooks for "Explainable AI for Affective Speech Recognition".

# Setup
### Virtual Environment (optional)
Setup a new conda environment and install all the required libraries

`conda create --name your-env-name`
`pip install -r requirements.txt`

# Datasets
For simplicity, we perform experiments on one dataset. 
Ravdess: contains 1440 audio recordings from 24 individuals.
 
Links: 

1- [Paper](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0196391)

2- Download link: [Kaggle](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio)

Extract the dataset into the newly created folder named `data`.
The final path of the dataset should look like '/data/Ravdess/audio_speech_actors_01-24/'

If the dataset is downloaded and extracted in a different directory, please ensure the paths defined in _notebooks_ match their location and names.

The proceed data and extracted features are available in CSV file formats _'XAI_seminar/emoRav_data.csv'_, and _'XAI_seminar/speech_features.csv'_ respectively. Therefore you can skip the notebook called _data_processing.ipynb_.

# Network architecture and trained models
The Sequential CNN trained model on Ravdess data is available in the directory _'/XAI_seminar/trained_model/Speech_CNN.h5'_.

# Usage
I recommend starting with the notebook called _data_processing.ipynb_ to build some knowledge about the dataset, which is just a straightforward implementation for processing and visualizing the speech data.

The next step is available with two options, either start with training the model from scratch and test the model with the available metrics then save the model for the next step of _'post-hoc'_ explanation. **OR** Start directly by using the saved model mentioned above in  _'/XAI_seminar/trained_model/Speech_CNN.h5'_.

**The last step is generating SHAP explanations**
Follow the code structured in the notebook called _'/XAI_seminar/trained_model/SHAP_XAI4SER.ipynb'_. Just so you know, generating SHAP Values for all datasets of 1440 instances might cost much computation time. Thus, for learning purposes, you can sample a small number of instances from the data and proceed with feature importance generation as in C13.








