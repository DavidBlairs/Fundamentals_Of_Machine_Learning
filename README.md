# Fundamentals Of Machine Learning
This assignment was part of the "Fundamentals of Machine Learning" module offered to masters students at Brunel University London. The module consisted of weekly lectures and labs in order to build up an intuitive understanding behind machine learning models, specifically the mathematics  of their construction. This assignment was completed using python, jupyter notebooks and the write up was done in  $LaTeX$. It was composed of three parts:

## TASK 1 - Completion Overview

1. A $k$-NN binary classifier was created. 

2. A subset of feature data was provided from $569$ breast cancer test results. This subset was generated, and personalized values of $k$ and $p$ (for the $p$-norm) for the $k$-NN method were used, as provided by the *untouchable* code given at the beginning of the notebook. 

3. In the notebook:
    - The data was extracted, and any invalid entries were checked and handled.
    - An appropriate train/test split fraction was chosen, and the sizes of the resulting data sets were documented.
    - The `sklearn` library's $k$-Nearest Neighbours method was employed to classify breast cancer test results as either *benign* or *malignant*.
    - A confusion matrix was plotted to visualize the classifier's performance.
    - The accuracy score of the classifier was determined.
    - The probability that a test result was positive (malignant) given that the classifier predicted it as negative (benign), denoted as $\mathrm{Prob}(P\mid-)$, was estimated.

4. In the report for Task 1:
    - A concise overview of the $k$-NN method was provided, elaborating on its primary features and hyperparameters.
    - The chosen **train/test** split was explained.
    - The methodology for calculating $\mathrm{Prob}(P\mid-)$ was detailed.

## TASK 2 - Completion Overview

In this task, the following steps were executed as a continuation of Task 1 with a focus on PCA (*Principal Component Analysis*):

1. The data subset and personalized values from Task 1 were utilized. After executing the *untouchable* code, a personalized value of `nc` was obtained which represented the number of principal components used.

2. In this notebook:
    - PCA was used to analyze the variance in the training data. `sklearn` was used for this.
    - The total number of principal components was identified.
    - A visual representation (in the form of a bar graph) of the explained variance percentages for all components was produced.
    - PCA was performed to compress the training data using `nc` components. This was achieved with the aid of `sklearn`.
    - A visualization (plot or bar graph) of the explained variance percentages for the `nc` component(s) was generated.
    - The $k$-NN method was re-executed, this time using the data compression resulting from the selection of just `nc` principal components.
    - The accuracy score and a confusion matrix were obtained.
    - The same training and test data from Task 1 were used.
    - The principle that the test data is regarded as unseen was strictly adhered to.

3. In the report for Task 2:
    - A concise overview of PCA was provided. Main concepts and formulas were included, but proofs or derivations were omitted.
    - The amount of variance captured by the given value of `nc` was explained.
    - The obtained results, specifically in terms of accuracies and confusion matrices, were discussed. A comparison was made to determine if they were similar. Recommendations were given on whether using just `nc` principal components for the model was beneficial. Probabilistic arguments were utilized to explain the advantages and disadvantages.
    - Care was taken to spell *principal* correctly and not as *principle* as physical violence was threatened by the professor in the event of the latter.
  
## TASK 3 - Completion Overview

In this task, the following procedures were undertaken:

1. **Data Setup and Cleaning**:
    - The untouchable code was executed, producing two dataframes: `dfth` (containing historical data for the TESLA share price) and `dftu` (containing a more recent set of data).
    - The data was checked for cleanliness. Any issues found were rectified.

2. **Data Visualization and Analysis**:
    - Using *seaborn*, a pair plot for `dfth` was generated with the `sns.pairplot` function.
    - A combined scatter plot showcasing *Volume* vertically against *Open* horizontally for both data sets (distinguished by color) was produced.
    
3. **Singular Value Decomposition (SVD)**:
    - Training data, `X_train`, was selected from `dfth`, excluding the columns *Date* and *Adj Close*.
    - An SVD of `X_train` was performed, revealing the rank of the dataset.
    - A logarithmic scree plot was created from the singular values.
    - `Xc_train`, an SVD-compressed version of `X_train` was generated by retaining the first `c` dominant singular components.
    - The error in the SVD approximation of `X_train` by `Xc_train` was calculated using `linalg.norm(X_train - Xc_train)` from `numpy` and subsequently visualized in a plot or bar chart against all suitable values of \(c\).
    - Using \(c=1\), `X_train` was SVD-transformed to `Kc`, a compressed training set.
    - Scatter plots contrasting *Open* against *Volume* for `X_train` and `X_test` were crafted on the same axis, but with differing colors. Two subsequent scatter plots with `Kc` and `X_test`, and then `Kc` and `Qc` were also produced.
    - The entire scatter plot creation procedure was repeated for \(c=2\).

4. **Report Details**:
    - A concise overview of the *Singular Value Decomposition* (SVD) was provided.
    - The pairplot's features were discussed, and predictions regarding the number of dominant independent components in the data were made.
    - The dataset's rank was stated.
    - Mathematical details outlining the SVD transformation of `X_train` to `Kc` were provided.
    - Mathematical details and the rationale behind the transformation of `X_test` to `Qc` were detailed.
    - Observations about the differences and similarities between the scatter plots for \(c=1\) and \(c=2\) were discussed and interpreted.



