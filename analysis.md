# Deep Learning Project: Charity Funding Predictor
CU-VIRT-DATA-PT-12-2023-U-LOLC MODULE 21 ASSIGNMENT Repository

## Background

The non-profit foundation Alphabet Soup wants to create an algorithm to predict whether or not applicants for funding will be successful. With my knowledge of machine learning and neural networks, I used the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, I have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

* **EIN** and **NAME**—Identification columns
* **APPLICATION_TYPE**—Alphabet Soup application type
* **AFFILIATION**—Affiliated sector of industry
* **CLASSIFICATION**—Government organization classification
* **USE_CASE**—Use case for funding
* **ORGANIZATION**—Organization type
* **STATUS**—Active status
* **INCOME_AMT**—Income classification
* **SPECIAL_CONSIDERATIONS**—Special consideration for application
* **ASK_AMT**—Funding amount requested
* **IS_SUCCESSFUL**—Was the money used effectively

## Instructions

### Step 1: Preprocess the data

Using my knowledge of Pandas and scikit-learn’s StandardScaler(), I preprocessed the dataset in preperation for the next step where I compile, train, and evaluate the neural network model.
Preprocessing steps taken:

1. Read in the charity_data.csv to a Pandas DataFrame, and be sure to identify the following in your dataset:
  * What variable(s) are considered the target(s) for your model?
  * What variable(s) are considered the feature(s) for your model?
2. Drop the `EIN` and `NAME` columns.
3. Determine the number of unique values for each column.
4. For those columns that have more than 10 unique values, determine the number of data points for each unique value.
6. Use the number of data points for each unique value to pick a cutoff point to bin "rare" categorical variables together in a new value, `Other`, and then check if the binning was successful.
7. Use `pd.get_dummies()` to encode categorical variables

### Step 2: Compile, Train, and Evaluate the Model

Using my knowledge of TensorFlow, I designed a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup-funded organization will be successful based on the features in the dataset. 


1. Continue using the jupter notebook where you’ve already performed the preprocessing steps from Step 1.
2. Create a neural network model by assigning the number of input features and nodes for each layer using Tensorflow Keras.
3. Create the first hidden layer and choose an appropriate activation function.
4. If necessary, add a second hidden layer with an appropriate activation function.
5. Create an output layer with an appropriate activation function.
6. Check the structure of the model.
7. Compile and train the model.
8. Create a callback that saves the model's weights every 5 epochs.
9. Evaluate the model using the test data to determine the loss and accuracy.
10. Save and export your results to an HDF5 file, and name it `AlphabetSoupCharity.h5`.

### Step 3: Optimize the Model

Using my knowledge of TensorFlow, I optimized my model to achieve a target predictive accuracy higher than 75%.

The following were methods considered for completion of this step:
* Adjusting the input data to ensure that there are no variables or outliers that are causing confusion in the model, such as:
  * Dropped more or fewer columns.
  * Created more bins for rare occurrences in columns.
  * Increased or decreasing the number of values for each bin.
* Added more neurons to a hidden layer.
* Added more hidden layers.
* Used different activation functions for the hidden layers.
* Added or reducing the number of epochs to the training regimen.

1. Created a new Jupyter Notebook file and name it `AlphabetSoupCharity_Optimzation.ipynb`.
2. Imported dependencies, and read in the `charity_data.csv` to a Pandas DataFrame.
3. Preprocess the dataset like Step 1, taking into account any modifications to optimize the model.
4. Design a neural network model, taking into account any modifications that will optimize the model to achieve higher than 75% accuracy.
5. Saved and exported your results to an HDF5 file, and name it `AlphabetSoupCharity_Optimization.h5`.

### Step 4: Write a Report on the Neural Network Model

Wrote a report on the performance of the deep learning model I created for AlphabetSoup.

The report contains the following:

1. **Overview** of the analysis: Explain the purpose of this analysis.

2. **Results**: Using bulleted lists and images to support my answers, address the following questions.

  * Data Preprocessing
    * What variable(s) are considered the target(s) for my model?
    * What variable(s) are considered to be the features for my model?
    * What variable(s) are neither targets nor features, and should be removed from the input data?
  * Compiling, Training, and Evaluating the Model
    * How many neurons, layers, and activation functions I selected for your neural network model, and why?
    * Were I able to achieve the target model performance?
    * What steps did I take to try and increase model performance?

3. **Summary**: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain my recommendations.
