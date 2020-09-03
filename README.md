# Comparative-Analysis-of-NB-and-ID3

## Introduction
As credit card becomes the most general mode of payment (both online and regular purchase), fraud rate tends to accelerate. In later years, credit card fraud has grown to a serious and threatening financial crime. This crime involves counterfeit or hijack of one or several legitimate attributes of the user, by means of identity theft, physical theft of cards, hacking of online user credentials etc, and using such illegitimate information for own advantages. Data mining is one of the effective methods of controlling credit card fraud. Detecting fraudulent transactions using traditional methods of manual detection are time consuming and inaccurate, thus the advent of machne learning had made these manual methods more impractical

## Objective
The main objective of this project is to give in detail comparison based on certain performance metrics between Naive Bayes and ID3 algorithms.
Other objectives include:
- To study a better Supervised learning algorithm
- To extract relevant features
- To hyper-tune the model eventually, helping in better predictions

## Naive Bayes
Naïve Bayes is a statistical approach based on Bayesian Theory, which chooses the decision based on highest probability. Bayesian probability estimates unknown probabilities from known values. It also allows prior knowledge and logic to be applied to uncertain statements. This technique has an assumption of conditional independence among features in the data. The Naïve Bayes classifier is based on the conditional probabilities.
<div align=center><img src=https://github.com/ghatoleyash/Comparative-Analysis-of-NB-and-ID3/blob/master/Conditional_probability.png></div>
where n represents maximum number of features (30), P(ci | fk) is probability of feature value fk being in class ci, P(fk | ci) is probability of generating feature value fk given class ci, P(ci) and P(fk) are probability of occurrence of class ci and probability of feature value fk occurring respectively. The classifier performs the binary classification based on Bayesian classification rule.
<div align=center><img src=https://github.com/ghatoleyash/Comparative-Analysis-of-NB-and-ID3/blob/master/class_probability.png></div>
Ci is the target class for classification where C1 is the negative class (non fraud cases) and C2 is the positive class (fraud cases).


## Decision Tree
Decision tree learning is a supervised machine learning technique for inducing a decision tree from training data. A decision tree is a predictive model which is a mapping from observations about an item to conclusions about its target value. In the tree structures, leaves represent classifications, nonleaf nodes are features, and branches represent conjunctions of features that lead to the classifications. 
Iterative Dichotomiser 3 is the implementation based on the concept of Decision tree. As the name suggests he algorithm iteratively performs analysis on the features/ attributes and divides (dichotomizes) into two or more group. It performs the greedy approach by creating tree using the top-down approach. ID3 does this so by aplying the concept of entropy and information gain which can be described as:
- Entropy: It measures the amount of uncertainity in the dataset and can be calculated using the formula,
<div align=center><img src=https://github.com/ghatoleyash/Comparative-Analysis-of-NB-and-ID3/blob/master/entropy_formula.png></div>
Where, S is the current dataset changes with every iteration to the subset of previous data, c is the set of classes is S, Pi is the probability of being class c with total classes present in S
- Information gain: It measures that which attribute in a given set of training feature vectors is useful to discriminate between two classes that needed to be learned which can be calculated by, 
<div align=center><img src=https://github.com/ghatoleyash/Comparative-Analysis-of-NB-and-ID3/blob/master/information_gain_formula.png></div>
Where, H(S) is the entropy of Set S, D is the subset created by spltting Set from attribute D, |V| is the number of elements of a particular class belonging to the attribute D, and |S| is the total number of elements in set S, H(V) is the entropy of subset V  



## Data Preprocessing & Feature Selection
The data preprocessing can often have a significant impact on generalization performance of a supervised ML algorithm. The elimination of noise instances is one of the most difficult problems in inductive ML. The symbolic, logical learning algorithms are able to process symbolic, categorical data only. However, real-world problems involve both symbolic and numerical features. Therefore, there is an important issue to discretize numerical (continuous) features. Grouping of values of symbolic features is also a useful process. It is a known problem that features with too many values are overestimated in the process of selecting the most informative features, both for inducing decision trees and for deriving decision rules. Moreover, in real-world data, the representation of data often uses too many features, but only a few of them may be related to the target concept. There may be redundancy, where certain features are correlated so that is not necessary to include all of them in modeling; and interdependence, where two or more features between them convey important information that is obscure if any of them is included on its own.
#### Dataset
The dataset used for training the algorithm is german credit fraud dataset which contains total 20 attributes. Attributes such as credit amount, debtors/guarantors, installment plans are included in the data, there are 13 categorical variable and remaining are continuous variables. No missing values are existing in the data hence, the algorithms take only categorical variable as inputs we have processed the continuous columns into categorical by dividing them into the range of values.
#### Pre-processing
Columns such as credit amount has been converted into the nominal variable by using the statistical inference. Finding out the distribution of credit amount and since it came out to be positively skewed log transformation has applied to make it more alike normal distribution. Lastly, the variable is segregated into three types low, medium and high by defining credit amount less than (mean-stdev) as low, with amount between 1 standard deviation as medium, and credit amount being greater than 1 standard deviation as high.
Moreover, the labelencoding is performed to receive the integer forms of categorical variable which can be given as an input to both the algorithms. 
#### Feature Selection
Selecting the relevant categorical features can be done using the chi-square test of independence. The test is performed on dependent (class) and independent (attribute) variable, wherein the contingency table is drawn using both of the variables, which includes total count of instances involved in subsequent categories. The reference contingency table can be show below:
<div align=center><img src=https://github.com/ghatoleyash/Comparative-Analysis-of-NB-and-ID3/blob/master/contingency_table.png></div>
Where, map category corresponds to categories in independent variable, and reference category is the dependent variable
Using the table, chi-square value is calculated with the help of observed and expected outcome and can be given as:
<div align=center><img src=https://github.com/ghatoleyash/Comparative-Analysis-of-NB-and-ID3/blob/master/chi_square_formula.jpg></div>
Where, Oi is the observed outcome and Ei is the expected value, i is the segment for each of the cell in contingency table
The chi-square value obtained and using the degree of freedom, p-value is received which further can be compared with the significance value. If the p-value is greater than significance level then there exist no relation between dependent and independent variable, where the variable can be removed else, we have to keep the variable.  


## Experimental Results
In this section, we analyze the results obtained through the experiment performed on test set.
<div align=center><img src=https://github.com/ghatoleyash/Comparative-Analysis-of-NB-and-ID3/blob/master/roc.png></div>
- area under curve for Naive Bayes is 76.5%
- area under curve for ID3 is 76.5%

confusion_matrix for both 
~ | Non-fraud | Fraud
------|-------|-----
 Non-fraud | 118 | 0
 Fraud | 64 | 7616

- accuracy of Naive Bayes and ID3 is 
- True negative rate for Naive Bayes and ID3 is 


