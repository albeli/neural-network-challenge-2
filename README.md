# Employee Attrition & Department Classification Model

## Overview
This project builds a neural network model to predict employee attrition and the most suitable department for each employee in a company using TensorFlow and Keras. The model uses a branched architecture to simultaneously predict binary attrition status and multi-class department affiliation.

## Data
The dataset used (`attrition.csv`) includes various employee characteristics such as age, job satisfaction, education, and more. The dataset consists of 1470 samples with 27 features.

## Preprocessing
The preprocessing steps include:
- Encoding categorical variables ('Attrition', 'OverTime', 'Department') using `OneHotEncoder`.
- Scaling numerical features with `StandardScaler` to normalize the data.
- Splitting data into training and testing sets.

## Model Architecture
The model features:
- An input layer that takes in the scaled features.
- Two shared dense layers.
- Two branches:
  - **Attrition Branch**: Predicts employee attrition with a softmax output layer.
  - **Department Branch**: Predicts department classification with a softmax output layer.

## Compilation and Training
- The model is compiled with the `adam` optimizer and `categorical_crossentropy` loss for both outputs.
- It is trained for 50 epochs with a batch size of 32.

## Evaluation
- Model performance is evaluated on the test set with accuracy as the metric for both outputs.

## Usage
To run this model, you will need Python 3 and the following libraries:
- `pandas`
- `numpy`
- `tensorflow`
- `sklearn`

## Example Results
- Attrition prediction accuracy: 81.79%
- Department classification accuracy: 51.90%

## Possible Improvements
- Implementing cross-validation to assess model stability.
- Adding dropout layers to prevent overfitting.
- Tuning hyperparameters like learning rate and number of neurons.

## Conclusion
This neural network model serves as a robust tool for predicting employee attrition and department suitability, aiding HR decisions in corporate environments.

