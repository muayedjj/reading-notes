# Linear Regressions

## Linear Regression In Python

- There are several ways in which you can do **linear regression**  in python; using _numpy_, _scipy_, _stats model_ and _sckit_ learn. [1]

- Scikit-learn is a powerful Python module for machine learning. It contains function for regression, classification, clustering, model selection and dimensionality reduction. [1]

## Steps for implementing linear regression in Python

1. The first step is to **import the required Python libraries** into Ipython Notebook.
    Those include _(Numpy, Pandas, SciPy, MatPlotLib.PyPlot & SKLearn)_

2. Import the data set you intend to use into Ipython notebook and store it in a variable.
    _Use `load_*()` method.

3. The object variable will be a dictionary, so you can explore the keys of this dictionary using the _VarName`.keys()`_ method.

4. Use other NumPy methods such as `.shape` and `DESC` to see the description of this data set to know more about it.

5. Convert the  _VarName`.data`_ into a pandas data frame using the _`pd.DataFrame(`VarName`.data)`_ command.

6. You can even replace the column names with the feature names of the dataset using data _frame_name`.columns` = data _frame_name`.feature_names`

## 7. Scikit Learn

WE IMPORT : `from sklearn.linear_model import LinearRegression`

### Fitting a Linear Model : `In [20]: lm.fit(X, bos.PRICE)`

## How to do train-test split:

### You have to divide your data sets randomly.

1. Input: print “Fit a model X_train, and calculate MSE with Y_train:”, np.mean((Y_train – lm.predict(X_train)) ** 2)
2. Output: Fit a model X_train, and calculate MSE with Y_train: 19.5467584735 Fit a model X_train, and calculate MSE with X_test, Y_test: 28.5413672756

### Residual Plots

Residual plots are a good way to visualize the errors in your data. If you have done a good job then your data should be randomly scattered around line zero. If you see structure in your data, that means your model is not capturing some thing.

## notes 
- We explore the boston data set and then rename its column names.
- We explore the boston data set using .DESCR, my goal was to make predictions using the given features.
- We use Scikit learn to fit linear regression to the entire data set and calculated the mean squared error.
- We make a train-test split and calculated the mean squared error for our training data and test data.
- We then plott the residuals for my training and test datasets.











 _For more on the subject of **Linear Regression In Python**, see this [**Article**](https://www.crayondata.com/how-to-run-linear-regression-in-python-scikit-learn/)  on crayondata_


## Things I want to know more about:
1. Linear regression in Python.
2. N-dimentional Matrices and Arrays.
3. NumPy different data types.
4. Python's Data Model.



[1]: https://www.crayondata.com/how-to-run-linear-regression-in-python-scikit-learn/
[2]: 