Aretefact workflow {.code-line data-line-start="0" data-line-end="1"}
==================

This file will explain the flow of the contents in the Artefacts. It
contains the datasets used for prediction and all codes developed to
build the models inorder to get their their accuracy. All code files are
in .R and .ipynb formats.

The *Recs2009\_public.csv* contains energy related data from almost
12083 households in 16 U.S. states with 940 variables. The
*recs2009\_public\_codebook.csv* file contains descriptive labels for
variables, descriptions of the response codes, and indicators for the
variables used in each end-use model.

### Preprocessing {.code-line data-line-start="5" data-line-end="6"}

The Recs2009\_public.csv is been preprocessed using python programming
language saved under preprocessing.ipynb\
 The steps followed are,

-   Replacing missing values using most frequently repeated values
-   Removing highly correlated features
-   Removing features with a single unique value
-   Removal of unwanted columns
-   Obtaining datasets that are equal classified as 3 class, 5 class and
    10 class classification with binning
-   Obtained datasets are stored in Preprocessing.csv,
    Preprocessing\_5cls.csv, Preprocessing\_10cls.csv

### Feature Selection {.code-line data-line-start="15" data-line-end="16"}

-   The datasets obtained are divided into 75% training set and 25%
    testing set.
-   The feature selection is done for the training data of all three
    datasets using R programming language.
-   Required libraries are installed and ReliefF, CFS and Mutual
    Information methods were used.
-   A maximum of 10 features were selected using them and csv files were
    generated based on the output for all classifications.

### Building the model {.code-line data-line-start="21" data-line-end="22"}

The models Gradient Boosting, KNN, MLP classifier, Random Forest and
Stacking were performed for all datasets with and without feature
selection using python programming language. All models were built
following the same pattern.

-   All categorial features are changed to numeric using the
    LabelEncoder.
-   The training and testing data are seperated as x\_train, y\_train,
    x\_test, y\_test.
-   x\_train and x\_test contains training and testing data predictor
    variables and y\_train and y\_test contains iheir response variable.
-   The classifiers are imported from the libraries with which the model
    is built.
-   The train data is fitted into the model for training the model.
-   Now the test set is predicted.
-   And the predicted values are compared with the actual values using
    confusion matrix and classification accuracy

##### Note: {.code-line data-line-start="32" data-line-end="33"}

The file path must be changed as required.
