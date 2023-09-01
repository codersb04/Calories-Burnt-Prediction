# Calories-Burnt-Prediction
## Task
Build a Machine Learning model to predict the calories burnt.</br>
Comes under **Supervised Learning** as labelled data is used</br>
As continuos values have to be predicted, **XGBoost Regressor** Algorithm is used.</br>
Tool used: Jupyter Notebook, Python
## Dataset
Dataset is taken from Kaggle's. The dataset contains 2 files: Calories, Exercise. Total records are 15000.</br>
Feature for Calories Dataset : </br>
- User_ID
- Calories</br></br>
Features for Exercise Dataset : </br>
- User_ID
- Gender
- Age
- Height
- Weight
- Duration
- Heart Rate
- Body Temperature</br></br>

Source: https://www.kaggle.com/datasets/fmendes/fmendesdat263xdemos?select=exercise.csv

## Steps Involved
### Import Dependencies
The Libraries necessary for the task are:

- NumPy
- Pandas
- Matplotlib.pyplot
- Seaborn
- train_test_split from sklearn.model_selection
- XGBRegressor from xgboost
- Metrics from sklearn

### Data Collection and Analysis
- Load the data to Pandas DataFrame using read_csv function
- Concat the calories column of Calories dataset with exercise dataset using cancat function
- Use functions such as head, shape, info, isnull and describe to know more about the dataset.
### Data Visualization
- Create plots using Seaborn
- Build Countplot for Gender column
- Distribution plot for all the other column
- Construct a heat map to under stand the correlation between the features
### Data Preprocessing
- Convert the categorical column 'Gender' to numeric as 0 for Male and 1 for Female
- Sepearte the Feature and target Column where Target will only contain Calories column and Feature will contain rest of the columns except User_ID and Calories
### Model Building
- Separate the train and test data as 20% data for test and 80% data for training
- Used **XGBRegeressor** to create the model
- Model Evaluation: Evaluation is done on both trained and test data. Mean Absolute Error is calculated to evaluate the performance of the model.
  1. Mean Absolute error for trained data:  0.9656331550205747
  2. Mean Absolute error for test data:  1.4807048829992613
### Building a Predictive System
- Take a random data from the dataset
- Convert the categorical data to numeric
- Make it a Numpy array and reshape it to 2D array
- Feed the data to the build model
- Print the Predicted value</br></br></br>
Reference: Project 16. Calories Burnt Prediction using Machine Learning with Python | Machine Learning Projects, Siddhardhan, https://www.youtube.com/watch?v=ZD27QTvSbTY&list=PLfFghEzKVmjvuSA67LszN1dZ-Dd_pkus6&index=17
