# Voice-classification-using-ML
TEAM MANIACS
## Project Overview
Through all the available senses humans can actually sense the emotional state of their communication partner. The emotional detection is natural for humans but it is very difficult task for computers; although they can easily understand content based information, accessing the depth behind content is difficult and that’s what speech emotion recognition (SER) sets out to do. It is a system through which various audio speech files are classified into different emotions such as happy, sad, anger and neutral by computer. SER can be used in areas such as the medical field or customer call centers. With this project I hope to look into applying this model into an app that individuals with ASD can use when speaking to others to help guide conversation and create/maintain healthy relationships with others who have deficits in understanding others emotions.
## Dataset
The Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS) Dataset from Kaggle contains 1440 audio files from 24 Actors vocalizing two lexically-matched statements. Emotions include angry, happy, sad, fearful, calm, neutral, disgust, and surprised.
https://www.kaggle.com/uwrfkaggler/ravdess-emotional-speech-audio
## Process
1. See Data_Preprocessing_&_Initial_Model.ipynb: Loaded audio files, created visualizations, conducted feature extraction (log-mel spectrograms) resulting into dataframe (see audio.csv) and built inital 1D CNN Model. Obtained an accuracy score of 38% with the model having difficulty classifying calm, surprised, angry, and digust.
2. See Data_Augmentation.ipynb: Implemented data augmentation methods including adding noise, speed and pitch, and stretch to all audio files and used feature extraction methods to turn audio files into images to feed into 1D CNN Model. Obtained an accuracy score of 80%, but overfitting the data.
## Conclusion
Using feature extraction methods by itself did not achieve a high accuracy score within my CNN model, but using data augmentation methods did improve the accuracy score to 53% however it was overfitting the data. This model needs to be improved upon before being applied towards making an app to detect emotion in real time. Fine tuning the VGG-16 architecture with image augmentation improved the overall model accuracy to 81%
## Limitations
Limitations include not using feature selection to reduce the dimensionality of my augmented CNN which may have improved learning performance. Another limitation included using minimal data, the RAVDESS Dataset has only 1,440 files which may be why there was overfitting of the data. Additional datasets could have been utilized.
