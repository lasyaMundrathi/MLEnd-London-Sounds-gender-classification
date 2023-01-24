# Machine-Learning-audio-gender-classification
![image](https://user-images.githubusercontent.com/98383338/213646780-a5f20c53-e840-4f3b-9aa8-015dc41cbba8.png)

## Classification of gender based on audio signals

Problem-statement: The problem here is to classify the gender of the participitant based on the audio input. We will be using Supervised Machine Learning Models by using features from the librosa python package to retrive information.

Note: All the participants are labelled manually as female or male since the demographic data is not given

*2) What's Intresting about it*

This project helps to classify the gender based on this we can intrepet many others charecterstics based on the gender for further analysis.This project gives an insight to work with different audio features to classify its environment.

Additionally this project gives an inference of machine learning model that best suits this application. Furthermore, We will explore different methods to choose best hyperparameteters and compare the effectiveness of supervised models for this application.Moreover, this project can be extended to classify age by extracting more additional features.

## Machine Learning pipeline

### Input
The csv file consists of name of the audio files along with the Area Spot, environment, Participant Number recorded in different filiming locations of London and 2498 audios in mp3 format which have been imported from the google drive

Data Preprocessing There are totally 176 participants, 6 areas and 36 spots in our data. Since the demographic data is not provided I manually identifying the gender of 176 participants in a separate csv file and merged this into audio dataset for further processing.

### Feature Extraction

In this stage we are loading a collection of audio files along with the dataframe where name of the audio file is given as index. Here we are extracting spectral features using librosa library using different functions. It returns and array(X) of these features and a binary boolean label (y) which is True for Male and False for female.

### Feature Analysis

In this stage data having high skewness is transformed into low skewness using logorithmic, square, cube root math functions. We are reducing the skewness so that the data has smoothned curve.If the skewness of the data lies between -1 to 1 it is normally distributed. Data is inconsistent so the data is standardised by using sklearn library where the transformed data has mean as zero and varience as 1.

### Training and Tuning the model

The processed data is given as input to the models after spliting into 70% Training and 30% Testing data. Followed by the Supervised Machine Learning Models to predict labels as female and male participitants. Each model is accesed for evaluation using accuracy metric, precision, recall, f1-score. Using RandomizedSearchCV best hyperparameters are selected that best suits the model.

### Model Evaluation

In this stage we will further select the best model using accuracy obtained for each model on the validation dataset(30%). The final model is selected based on accuracy, confusion matrix, classification report so that the suitable model is not biased towards any predictors.

### Output 
Output of each model will be the predictions based on gender of each model
## Results
