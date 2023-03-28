# deep-learning-challenge
## Module 21 Challenge
For this challenge I received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. I was tasked with building a tool that can help it select the applicants for funding with the best chance of success in their ventures. With my knowledge of machine learning and neural networks, I used the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

## Preprocessing the Data
First I read the charity_data.csv to a Pandas DataFrame, and identified what variable is the target for the model and what variables are the features for the model. I dropped the EIN and NAME columns, determine the number of unique values for each column, used the number of data points for each unique value to pick a cutoff point to bin "rare" categorical variables together in a new value, Other, and then check if the binning was successful. 

Using pd.get_dummies() I encoded categorical variables, then split the preprocessed data into a features array, X, and a target array, y. Using these arrays and the train_test_split function I split the data into training and testing datasets.

## Compile, Train, and Evaluate the Model
I used my knowledge of TensorFlow and designed a neural network to create a binary classification model that can predict if an Alphabet Soup-funded organization will be successful based on the features in the dataset.

Here is my first attempt:

![first attempt model structure](Images/first_attempt_model_structure.png)
![first attempt model eval](Images/first_attempt_model_eval.png)

You can view the first attempt starter code [here](Starter_Code.ipynb)

## Optimize the Model
Using much of the same steps as the process before, I used my knowledge of TensorFlow to optimize the model to achieve a target predictive accuracy higher than 75%.

    In order to optimize the model I:

    * Dropped fewer columbs by including the 'NAME' column to the database
    * Created more bins for rare occurrences by binning the 'NAME' column
    * Added more neurons to the hidden layers

Below are the results of my second attempt:

![second attempt model structure](Images/second_attempt_model_structure.png)
![second attempt model eval](Images/second_attempt_model_eval.png)

You can view the second attempt code [here](AlphabetSoupCharity_Optimization.ipynb)

## Write a Report on the Neural Network Model
For this part of the assignment, I was tasked to write a report on the performance of the deep learning model I created for Alphabet Soup. The report can be viewed [here](Neural_Network_Model_Report.pdf).


## References
IRS. Tax Exempt Organization Search Bulk Data [Downloads](https://www.irs.gov/charities-non-profits/tax-exempt-organization-search-bulk-data-downloads).