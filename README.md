# HW13-Neural-Networks
Venture Funding with Deep Learning

# Instructions:
The steps for this challenge are broken out into the following sections:

# Prepare the data for use on a neural network model.

Compile and evaluate a binary classification model using a neural network.

Optimize the neural network model.

Prepare the Data for Use on a Neural Network Model
Using your knowledge of Pandas and scikit-learn’s StandardScaler(), preprocess the dataset so that you can use it to compile and evaluate the neural network model later.

Open the starter code file, and complete the following data preparation steps:

Read the applicants_data.csv file into a Pandas DataFrame. Review the DataFrame, looking for categorical variables that will need to be encoded, as well as columns that could eventually define your features and target variables.

Drop the “EIN” (Employer Identification Number) and “NAME” columns from the DataFrame, because they are not relevant to the binary classification model.

Encode the dataset’s categorical variables using OneHotEncoder, and then place the encoded variables into a new DataFrame.

Add the original DataFrame’s numerical variables to the DataFrame containing the encoded variables.

Note To complete this step, you will employ the Pandas concat() function that was introduced earlier in this course.

Using the preprocessed data, create the features (X) and target (y) datasets. The target dataset should be defined by the preprocessed DataFrame column “IS_SUCCESSFUL”. The remaining columns should define the features dataset.

Split the features and target sets into training and testing datasets.

Use scikit-learn's StandardScaler to scale the features data.

# Compile and Evaluate a Binary Classification Model Using a Neural Network
Use your knowledge of TensorFlow to design a binary classification deep neural network model. This model should use the dataset’s features to predict whether an Alphabet Soup–funded startup will be successful based on the features in the dataset. Consider the number of inputs before determining the number of layers that your model will contain or the number of neurons on each layer. Then, compile and fit your model. Finally, evaluate your binary classification model to calculate the model’s loss and accuracy.

To do so, complete the following steps:

Create a deep neural network by assigning the number of input features, the number of layers, and the number of neurons on each layer using Tensorflow’s Keras.
Hint You can start with a two-layer deep neural network model that uses the relu activation function for both layers.

Compile and fit the model using the binary_crossentropy loss function, the adam optimizer, and the accuracy evaluation metric.
Hint When fitting the model, start with a small number of epochs, such as 20, 50, or 100.

Evaluate the model using the test data to determine the model’s loss and accuracy.

Save and export your model to an HDF5 file, and name the file AlphabetSoup.h5.

# Optimize the Neural Network Model
Using your knowledge of TensorFlow and Keras, optimize your model to improve the model's accuracy. Even if you do not successfully achieve a better accuracy, you'll need to demonstrate at least two attempts to optimize the model. You can include these attempts in your existing notebook. Or, you can make copies of the starter notebook in the same folder, rename them, and code each model optimization in a new notebook.

Note You will not lose points if your model does not achieve a high accuracy, as long as you make at least two attempts to optimize the model.

To do so, complete the following steps:

Define at least three new deep neural network models (the original plus 2 optimization attempts). With each, try to improve on your first model’s predictive accuracy.
Rewind Recall that perfect accuracy has a value of 1, so accuracy improves as its value moves closer to 1. To optimize your model for a predictive accuracy as close to 1 as possible, you can use any or all of the following techniques:

Adjust the input data by dropping different features columns to ensure that no variables or outliers confuse the model.

Add more neurons (nodes) to a hidden layer.

Add more hidden layers.

Use different activation functions for the hidden layers.

Add to or reduce the number of epochs in the training regimen.

After finishing your models, display the accuracy scores achieved by each model, and compare the results.

Save each of your models as an HDF5 file.
