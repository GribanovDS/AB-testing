# A/B tests
This repository contains the results of A/B tests.

The tests were conducted on data taken from an application that combines a news feed and a messenger. There were 4 groups involved in the test, with 1 group not being changed, and for 2 groups, a new post recommendation algorithm was used, in which similar posts were shown based on what they had liked. Group 0 was not changed, and for group 4, a new post recommendation algorithm was used in which similar posts were shown based on what similar users had liked.

## AA test
The file *ab_task1.ipynb* contains the results of an AA test conducted from 2022-01-24 to 2023-01-30. The test consisted of 10000 iterations, each of which formed subsamples of 500 users from 2 and 3 experimental groups. A comparison of these subsamples was made using t-tests and Mann-Whitney tests. As a result, it was concluded that there were no statistically significant differences between the groups after hashing, so it can be concluded that the AA test works correctly.

## AB test
The file *ab_task2.ipynb* contains the results of an AB test conducted from 2023-01-31 to 2023-02-06. Changes in CTR, number of likes, and number of views were analyzed. As a result, it was found that the new recommendation algorithm led to a decrease in CTR and the number of likes. Statistical tests showed that there were no statistically significant differences in views between groups 1 and 2, but there was a statistically significant difference in likes. Conclusion: the new recommendation algorithm did not lead to positive changes in CTR and likes, possibly because users do not like seeing similar posts that they have already liked.

## AB test - linearized likes method
In the file *ab_task3.ipynb*, I analyzed the test between groups 0 and 3 and between groups 1 and 2 using the metric of linearized likes. I concluded that the linearized likes method increased the sensitivity of the t-test by several times: the p-value really decreased, however, the sensitivity of the Mann-Whitney test was decreased

## Getting Started

To get started with this notebook, you will need to clone or download the repository containing the notebook onto your local machine. You will also need to have Jupyter Notebook installed on your machine, along with the following Python packages:

numpy
pandas
scipy
matplotlib
To install these packages, you can use the following command:

```
pip install numpy pandas scipy matplotlib
```
Once you have cloned or downloaded the repository and installed the required packages, you can open the notebook using Jupyter Notebook.

## Usage

The notebook contains step-by-step instructions for conducting an A/B test on two samples and calculating relevant metrics using Python. The notebook includes explanations of the functions used and provides examples using sample data.

To run the code in the notebook, you can simply click on the cells containing the code and press the "Run" button in the toolbar. Alternatively, you can use the keyboard shortcut "Shift + Enter" to run the cells.

The notebook also includes visualizations of the sample data and the results of the A/B test, which can be viewed directly in the notebook.
