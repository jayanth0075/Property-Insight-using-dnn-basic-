HOUSE PREDICTION DATASET - EDA AND MODEL TRAINING 
Dataset was taken from the kaggle ( Competition )

##  Exploratory Data Analysis (EDA)

###  Understanding the Data

We begin by understanding what the dataset contains — how many rows and columns, and what each column represents.
We check if the columns are numerical or categorical and understand the overall structure of the data.



### Checking for Missing Values

Next, we check if there are any missing values in the dataset.
If some values are missing, we decide whether to fill them with averages or remove those rows or columns.



###  Removing Duplicates

Sometimes, the same record appears more than once.
We remove duplicate rows to ensure the dataset only has unique data for accurate training.

---

### Outlier Detection

We look for very high or low values that are far away from the normal range.
Outliers can affect model performance, so we decide whether to keep, adjust, or remove them.



### Summary Statistics

We calculate simple measures like mean, median, minimum, maximum, and standard deviation.
This helps us understand how each feature is distributed and if any feature needs transformation.



### Univariate Analysis

Each feature is analyzed individually:

* For numerical columns, we check how the values are spread (normal or skewed).
* For categorical columns, we observe which categories occur most often.



###  Bivariate Analysis

We compare different features with each other and with the target variable.
This helps us understand which features have a stronger relationship with the output.



###  Correlation Analysis

We check correlations between numerical features.
Highly correlated features are identified to avoid redundancy during model training.



###  Feature Importance

We find which features contribute most to the prediction.
This helps us keep only the useful features and remove less important ones.



###  Final Data Preparation

After cleaning, handling missing values, and removing outliers, the dataset is now ready for model building.



##  Model Training and Evaluation

### Splitting the Data

The cleaned dataset is divided into **training** and **testing** parts.
The training data is used to teach the model, while the testing data checks how well it performs.



### Data Normalization

All numerical features are scaled to a similar range so that the model treats them equally.
This makes the learning process smoother and faster.



### Building the Model

A **Deep Neural Network (DNN)** is created with input, hidden, and output layers.
Each layer learns different levels of patterns from the data using activation functions.



###  Compiling the Model

We select a **loss function** (like Mean Squared Error) to measure prediction error,
an **optimizer** (like Adam) to adjust the weights,
and a **metric** (like Mean Absolute Error) to evaluate performance.


###  Training the Model

The model is trained over several **epochs** — each epoch improves the model slightly.
The **loss** and **error** values decrease as the model learns from the data.



###  Validation

During training, we also use a portion of the data for validation.
This helps to check if the model is learning correctly or overfitting.



###  Early Stopping ( Depends on patience level )

If the model’s performance stops improving on validation data, training is stopped early.
This prevents overfitting and saves training time.


###  Visualizing Results

We plot graphs of **Loss vs Epochs** and **MAE vs Epochs** to see how well the model has learned.




### Model Evaluation

After training, we test the model on unseen data.
We use metrics like **R²**, **MSE**, and **MAE** to measure accuracy and reliability.
The R^2 score is - 0.89
The MSE score is - 820447218
The Rmse score is - 28643






