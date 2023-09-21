# Fundamentals Of Machine Learning
This assignment was part of the "Fundamentals of Machine Learning" module offered to masters students at Brunel University London. The module consisted of weekly lectures and labs in order to build up an intuitive understanding behind machine learning models, specifically the mathematics  of their construction. This assignment was completed using python, jupyter notebooks and the write up was done in  $LaTeX$. It was composed of three parts:

## TASK 1 - Completion Overview

1. A $k$-NN binary classifier was created. 

2. A subset of feature data was provided from $569$ breast cancer test results. This subset was generated, and personalized values of $k$ and $p$ (for the $p$-norm) for the $k$-NN method were used, as provided by the *untouchable* code. No changes were made to this code.

3. In this notebook:
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
