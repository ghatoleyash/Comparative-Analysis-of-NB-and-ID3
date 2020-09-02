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
#### Benefits

## Decision Tree
Decision tree learning is a supervised machine learning technique for inducing a decision tree from training data. A decision tree is a predictive model which is a mapping from observations about an item to conclusions about its target value. In the tree structures, leaves represent classifications, nonleaf nodes are features, and branches represent conjunctions of features that lead to the classifications. 
Iterative Dichotomiser 3 is the implementation based on the concept of Decision tree. As the name suggests he algorithm iteratively performs analysis on the features/ attributes and divides (dichotomizes) into two or more group. It performs the greedy approach by creating tree using the top-down approach. ID3 does this so by aplying the concept of entropy and information gain which can be described as:
- Entropy: It measures the amount of uncertainity in the dataset and can be calculated using the formula,
<div align=center><img src=https://github.com/ghatoleyash/Comparative-Analysis-of-NB-and-ID3/blob/master/entropy_formula.png></div>
Where, S is the current dataset changes with every iteration to the subset of previous data, c is the set of classes is S, Pi is the probability of being class c with total classes present in S
- Information gain: It measures that which attribute in a given set of training feature vectors is useful to discriminate between two classes that needed to be learned which can be calculated by, 
<div align=center><img src=https://github.com/ghatoleyash/Comparative-Analysis-of-NB-and-ID3/blob/master/information_gain.png></div>
Where, H(S) is the entropy of Set S, D is the subset created by spltting Set from attribute D, |V| is the number of elements of a particular class belonging to the attribute D, and |S| is the total number of elements in set S, H(V) is the entropy of subset V  
#### Benefits


## Feature Selection
## Data Preprocessing


## Experimental Results

