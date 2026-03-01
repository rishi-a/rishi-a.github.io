---
layout: post
title:  "QnA - Classification Algorithms In Various Situations"
date:   2018-06-27 17:17:39 +0530
categories: 
---

<p>Here are a few questions and answers related to Classification Algorithms In Various Situations<!--more--></p>
<p><strong>What is Imbalanced and balanced dataset</strong></p>
<blockquote>
<p>If a dataset has unequal positive and negative data points than the dataset is imbalanced. Balanced dataset has equal positive and negative labels.<br />For Example: In data sets of patient having cancer or not, there will be a very high negative data points (for patients without cancer) and less positive data points (patients with cancer).<br /><br />K-NN results could be biased if the dataset is heavily imbalanced.</p>
</blockquote>
<p> </p>
<p><strong>Define Multi-class classification?</strong></p>
<blockquote>
<p>In MNIST dataset, we have 10 class/labels. So, MNIST dataset is a multi-class dataset.<br />In a c-class classifier, for a query point Xq, Xq may belong to any of the c-class. Now, for 7-NN, Xq will belong to that class, where majority of 7-NN belong to.</p>
</blockquote>
<p> </p>
<p><strong>Explain Impact of Outliers?</strong></p>
<blockquote>
<p>In KNN, when K=1, than an outlier can easily impact our model. This happens because our decision surface has changed with an outpier. As a comparison, K=5 will be less prone to error as compared to k=1. So, if we get the same accuracy in Dtest for K=5 and K=1, then we must prefer K=5.</p>
</blockquote>
<p> </p>
<p><strong>What is Local Outlier Factor?</strong></p>
<blockquote>
<p>The objective of local outlier factor is to detect outliers in data. It is inspired by KNN. For every query point (also for the outlier point), find the mean distance of all its K-Nearest Neighbor. Now sort all mean distances. If any of the mean distance is exceptionally high then the corresponding point is definitely an outlier.</p>
</blockquote>
<p> </p>
<p><strong>What is k-distance (A), N(A)</strong></p>
<blockquote>
<p>k-distance of a point A is the distance to the k-th nearest neighbor of A from A. <strong>N(A) denotes neighborhood of A</strong>. It is set of all points that belong to the KNN of A.</p>
</blockquote>
<p> </p>
<p><strong>Define reachability-distance(A, B)?</strong></p>
<blockquote>
<p>Mathematically, it is defined as:<br /><code>reachability-distance(A, B) = max(k-distance(B), dist(A,B))</code><br /><code>dist(A,B)</code> is the actual distance between A and B<br />Note that, if A is in the neighborhood of B then:<br /><code>reachability-distance(A, B) = k-distance(B)</code></p>
</blockquote>
<p> </p>
<p><strong>What is Local-reachability-density(A) or LRD(A)?</strong></p>
<blockquote>
<p>Local-reachability-density(A) is the inverse of average reachability distance of A from its neighbor.<br />Mathematically:<br />$$LRD(A) = \frac{1}{\sum_{B\in N(A)}^{}{\frac{reachability-distance(A,B)}{\|N(B)\|}}}$$</p>
</blockquote>
<p> </p>
<p><strong>Define LOF(A)</strong></p>
<blockquote>
<p>Local Outlier Factor of A, or LOF(A) is a quantity that is large when LRD(A) is small but LRD of neighborhood points of A is large. In other words, LOF(A) is large when density of points around A is small but density of points around the neighborhood of A is large.</p>
<p>When LOF(A) is large then we can conclude that A is an outlier.<br />Mathematically:<br />$$LOF(A) = \frac{\sum_{B\in N(A)}^{}LRD(B)}{\|N(B)\|} * \frac{1}{LRD(A)}$$</p>
</blockquote>
<p> </p>
<p><strong>Impact of Scale &amp; Column standardization?</strong></p>
<blockquote>
<p>If the scale of feature column are different then it impacts the euclidean distance measure. Euclidean distance measure is important in algorithms like KNN. Thus column standardization is done to bring all features under same scale</p>
</blockquote>
<p> </p>
<p><strong>What is Interpretability?</strong></p>
<blockquote>
<p>Suppose a ML model outputs weather a patient will survive cancer or not. Now, a professional Doctor cannot trust this model blindly. Nor is the Doctor trained to understand a ML model.<br /><br />So, in addition to YES/NO output from a ML model, the ML model should also give a reasonable justification as to why a particular output occurred. The reasoning will be useful for the Doctor to analyze the result. Such models are called interpretable model. KNN is interpretable if K is small.</p>
</blockquote>
<p> </p>
<p><strong>How To Handling categorical and numerical features?</strong></p>
<blockquote>
<p>Suppose we have a categorical feature called <strong>Hair Color</strong>. Now, all type of hair color needs to be converted into a number so that a machine learning model can compute over it. <br /><strong>One-hot encoding</strong>: Creates a binary vector of the size of number of distinct elements. f the number of distinct values for a categorical feature is large then One-Hot-Encoding can create sparse and large vectors.<br />Ordinal Features<br /><strong>In ordinal features</strong>, you can assign numbers (logical ordering) to each category of the feature and they just work fine. For example, 'very-good' could have a numeral value 5, 'very-bad' could have a numeral value 1.</p>
</blockquote>
<p> </p>
<p><strong>How To Handle Handling missing values by imputation?</strong></p>
<blockquote>
<p>There are various ways to handle missing values and it depends on the domain as to which method to choose to apply. Some of the ways are <br /><br />1. Take all the non-missing values and put its <strong>mean/median/mode</strong> in the missing value position.<br />2. Imputation based on class label. Suppose we have the class label and a known feature f1 for a data point. We can compute the unknown feature f2, from class-label and f1.<br />3. Create missing value feature. Missing values are sometimes source of information. Impute missing values using technique 1 or 2. Then create additional binary features, where missing values are represented as 1 and non-missing values are represented as 0.</p>
</blockquote>
<p> </p>
<p><strong>What is Bias-Variance tradeoff?</strong></p>
<blockquote>
<p>In theory of ML, we calculate a generalization error. It is the error on future unseen data. It is calculated as a sum of bias<sup>2</sup>+variance+irreducible-error.</p>
<p>Bias error occurs due to simplifying assumptions about a model. High-bias error imply <strong>underfitting</strong>.</p>
<p>Variance gives a measure of how much a model changes as training data changes. Large changes in model causes high variance resulting into <strong>overfitting</strong>. Small changes in training dataset causes decision surface to change a lot thus changing the mode.</p>
<p>As K increases, variance reduces. Our target should be to reduce generalization error. This can be cone so by reducing bias and variance. We can reduce bias by preventing underfit. Reduce variance by not overfitting. There is always a trade-off between underfitting and overfitting and thus the bias-variance tradeoff.</p>
</blockquote>
<p>[mathjax]</p>