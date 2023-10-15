---
layout: post
title:  "QnA - Performance Measure of Models"
date:   2018-06-28 17:17:39 +0530
categories: 
---

<p>Collection of questions and answers on performance measure of models<!--more--></p>
<p><strong>Which is more important to you– model accuracy, or model performance?</strong></p>
<blockquote>
<p>Lets answer this with respect to classification problems. Model Performance is more important. Model accuracy cannot be considered in cases where we have imbalanced dataset (where there are more positives then negatives). Accuracy also assign equal weight to labels which is a disadvantage in cases of imbalanced dataset.<br /><br />Classification model performance can be evaluated from metrics such as Log-Loss, Accuracy, AUC(Area under Curve) and precision, recall (generally used by search engines)</p>
</blockquote>
<p> </p>
<p><strong>Can you cite some examples where a false positive is important than a false negative?</strong></p>
<blockquote>
<p>Consider a model where, 1 (positive) means that a mail is Spam, 0 (negative) means that the mail is not Spam. If False Positives are high then important mails will go to the Spam folder and it may become difficult to retrieve that mail from the huge chunk of mails in Spam folder. Low False Negative would mean, that a spam mail lands up in the Primary mailbox.</p>
<p>Now it is not difficult, to mark a mail as Spam from the mail at Primary mailbox. But, as mentioned earlier, it is very difficult, to retrieve a mail from Spam folder. hence, in cases like this, False Positive is more important then False Negative</p>
</blockquote>
<p> </p>
<p><strong>Can you cite some examples where a false negative important than a false positive?</strong></p>
<blockquote>
<p>In Cancer diagnosis, let 1 (positive) denote positive for Cancer, 0 (negative) denote negative for Cancer. A False Negative would mean a patient who has cancer has been diagnosed as negative for Cancer. This situation is very dangerous as a patient who has Cancer was detected as negative by ML model and as a result, the patient will not be subjected to follow up investigation.<br /><br />On the other hand, False Positive is not as dangerous Flase Negative. Even if the patient does not have Cancer, the ML model will show positive and the patient will be subjected to further follow-up investigation.</p>
</blockquote>
<p> </p>
<p><strong>Can you cite some examples where both false positive and false negatives are equally important?</strong></p>
<blockquote>
<p>Consider, posting articles in a blog. If this article is read by more then average number of readers in my blog then it is positive. Else, negative.<br />A false positive would mean that more readers then the average number of readers in my blog have read this article, but the truth is that less then average readers have read this article. Here, false positive gives me a wrong motivation but the same motivation ensures that I keep writing. Writing helps me stay in practice.<br />A flase negative would means that the article did not do any better than all the other article but the truth being that it garnered more readers than the average readership of my blog. Here, false negative gives me a sense of introspection on the quality of my writing and ultimately helps me improve myself.</p>
</blockquote>
<p> </p>
<p><strong>What is the most frequent metric to assess model accuracy for classification problems?</strong></p>
<blockquote>
<p>The answer to this question is very domain specefic. For a overall idea we can say that confusion matrix is better then simple accuracy because of more output parameters in confusion matrix. RO curve could prove to be more helpful becuase it includes integration over the whole range of precision/recall tradeoffs. Log-loss is another metic to measure accuracy and it is the only one that considers probabilistic score directly.</p>
</blockquote>
<p> </p>
<p><strong>Why is Area Under ROC Curve (AUROC) better than raw accuracy as an out-of- sample evaluation metric?</strong></p>
<blockquote>
<p>A ROC curve plots the true positives (sensitivity) vs. false positives (1 − specificity), for a binary classifier system as its discrimination threshold is varied. An AUROC has many interpretations compared to raw accuracy.<br /><br />A ROC curve plots the true positives (sensitivity) vs. false positives (1 − specificity), for a binary classifier system as its discrimination threshold is varied. An AUROC has many interpretations compared to raw accuracy. A <a href="https://stats.stackexchange.com/questions/132777/what-does-auc-stand-for-and-what-is-it" target="_blank" rel="noopener">beautiful explanation</a> on Confusion Matrix.<br /><br />The area equals the probability that a randomly chosen positive example ranks above (is deemed to have a higher probability of being positive than) a randomly chosen negative example.</p>
</blockquote>
<p> </p>
<p><strong>What is Accuracy ?</strong></p>
<blockquote>
<p>Accuracy can be defined as:<br /><code>(Number of correctly classified points)/(Total number of points)</code></p>
<p>1) Imbalanced Data:A dumb model could get a very high accuracy. So never use accuracy as measure in imbalanced dataset.<br />2) Accuracy cannot use probabilistic score.</p>
</blockquote>
<p> </p>
<p><strong>Explain about Confusion matrix, TPR, FPR, FNR, TNR?</strong></p>
<blockquote>
<p>Confusion matrix is a square matrix comprising of predicted/actual class label values. Dimension of the square is equal to the number of class labels. Confusion matrix does not consider probabilistic scores.</p>
<p>A good model, will have high TNR and TPR. Elements in principal diagonal matrix will be high for a good model<br />Important parameters related to Confusion Matrix<br />TPR: True Positive Rate<br />FPR: False Positive Rate<br />FNR: False Negative Rate<br />TNR: True Negative Rate<br />TP: Number of true positive points<br />FP: Number of false positive points<br />TN: Number of true negative points<br />FN: Number of false negative points<br />P:Total actual positive points<br />N:Total actual negative points<br />TPR = TP/P; TNR = TN/N; FPR = FP/N; FNR = FN/P</p>
[caption id="attachment_1566" align="aligncenter" width="300"]<a href="#"><img class="" src="/images/revolution-analytics-300x279.png" alt="" width="300" height="279" /></a> Source: blog.revolutionanalytics.com/[/caption]
<p>Therefore, with TPR, TNR, FPR, FNR, we get a better insight of data rather then only accuracy. It is upto the domain to decide as to which among TPR, TNR, FPR, FNR is more important.</p>
</blockquote>
<p> </p>
<p><strong>What do you understand about Precision &amp; recall, F1-score?</strong></p>
<blockquote>
<p>Precision and recall are often used in information retrieval problems.They are related to the positive class/label of a dateset. <strong>Precision is</strong>: <code>TP/(TP+FP)</code>. It means that of all the points predicted to be positives, what percentage of them are actually positive</p>
<p>Recall is nothing but True Positive Rate(TPR). It means, out of all the positive labels, how many are correctly predicted to be positive.</p>
<p>We want precesion to be high which means that there are less points which are wrongly implicated to be positive. We also want, recall to be high, out of all the actual positive points, more points were rightly detected to be positive</p>
<p>Precision(Pr) and Recall(R) are combined in F1-Score.<br />$$F1Score = 2*\frac{Pr*R}{Pr+R}$$</p>
</blockquote>
<p> </p>
<p><strong>What is the ROC Curve and what is AUC (a.k.a. AUROC)</strong></p>
<blockquote>
<p>Receiver Operating Characteristic Curve (ROC) and Area Under RO Curve (AUC) are <strong>binary classification</strong> metric. It is a plot between TPR and FPR. An AUC score includes integration over the whole range of precision/recall tradeoffs, while the F1 score takes one specific precision and recall pair, which could be viewed as a sample or average. Area under RO curve can lie between 0 and 1. 1 signifies very good model. 0 means terrible.</p>
<p>1. If we have imbalanced data, AUC can be high even for a dumb model.<br />2. AUC does not care about the actual score assigned to a data point label.<br />3. AUC of a random model is 0.5.</p>
</blockquote>
<p> </p>
<p><strong>What is Log-loss and how it helps to improve performance?.</strong></p>
<blockquote>
<p>Given a test set, log-loss is defined as:<br />$$-\frac{1}{n}\sum_{i=1}^{n}\{(log(P_i)*y_i)+(1-y_i)*log(1-P_i)\} $$<br /><code>y<sub>i</sub></code> is the label of dataset and <code>P<sub>i</sub> is the probabilistic score of the label</code>.</p>
<p>Log-loss value is small where P<sub>i</sub> value is large for positive class/label. Also Log-loss value is small where P<sub>i</sub> value is small for negative class/label. Loss loss value can lie between 0 to Infinity. 0 is the best case. Loss loss takes into consideration the actual probabilistic values.</p>
<p>Log-Loss is average of negative log of probability of correct class label. Log-loss can be extended to multi class labels.</p>
</blockquote>
<p><strong>Explain about R-Squared/ Coefficient of determination</strong></p>
<blockquote>
<p>Coefficient of determination is a performance measure for models where predicted label values can belong to any real number (regression). Let the actual value be <code>y<sub>i</sub></code> and predicted value be <code>y'<sub>i</sub></code>, then we can calculate <strong>error</strong> as <code>e<sub>i</sub> = y<sub>i</sub> - y'<sub>i</sub></code></p>
<p>Now, we define a term <strong>Total Sum of Square</strong>, SS as<br />$$SS = \sum_{i=1}^{n}(y_i - \bar{y_i})^2$$<br />where,<br />$$\bar{y_i} = \frac{1}{n}\sum_{i=1}^{n}y_i$$ = average value of actual <code>y<sub>i</sub></code> in test data.</p>
<p>In a simplest regression model, given a query point we can return its output as the mean of all the other outputs. For example, to predict height of a person among 10 persons, we can calculate the mean of height of all the other 9 person and assign it as the height of the person under consideration.</p>
<p>Total sum of square is the sum of square errors using a simple mean model. Now we define <strong>Sum of Square Residual</strong><br />$$SS = \sum_{i=1}^{n}(y_i - y'_i)^2$$<br />where,<br /><code>y'<sub>i</sub></code> is the predicted class value.</p>
<p><code>SS<sub>total</sub></code> is for a simple mean model whereas, <code>SS<sub>residual</sub></code> is for the model that is under operation. Now, we can define <code>R<sup>2</sup></code> as:<br />$$R^2 = 1-\frac{SS_{res}}{SS_{total}}$$.</p>
<p> </p>
<p><strong>Case 1</strong>: When <code>SS<sub>res</sub> = 0</code>. This will happen when predicted value is exactly same as actual value, that means error, <code>e<sub>i</sub> = 0</code>. In this case <code>R<sup>2</sup> = 1</code>, which means that our model is phenomenal.</p>
<p> </p>
<p><strong>Case 2:</strong> When <code>SS<sub>res</sub> &lt; SS<sub>total</sub></code>. In this case, <code>R<sup>2</sup></code> will be between 0 and 1.</p>
<p> </p>
<p><strong>Case 3:</strong>: <code>SS<sub>res</sub> = SS<sub>total</sub></code>, then <code>R<sup>2</sup></code> is 0, which means our model is same as simple mean model.</p>
<p> </p>
<p><strong>Case 3:</strong>: <code>SS<sub>res</sub> &gt; SS<sub>total</sub></code>, then <code>R<sup>2</sup></code> becomes negative, which means our model is worse then a simple mean model</p>
</blockquote>
<p> </p>
<p><strong>Explain about Median absolute deviation (MAD) ?Importance of MAD?</strong></p>
<blockquote>
<p>Errors, <code>e<sub>i</sub></code> and <code>SS</code> can suffer from outlier points, i.e. if one point is very large, our entire <code>R<sup>2</sup></code> can go for a toss. <code>R<sup>2</sup></code> is not very robust to outliers.</p>
<p>Now, error, <code>e<sub>i</sub></code> is a random variable. We can choose to select the mean of <code>e<sub>i</sub></code>, i.e. <code>median(e<sub>i</sub>) = central value of errors</code>.<br />Median Absolute Deviation, <code>MAD(e<sub>i</sub>) = Median(e<sub>i</sub> - median(e<sub>i</sub>))</code><br />Median is a robust measure of mean, and MAD is a robust measure of standard-deviation.</p>
</blockquote>
<p> </p>
<p>[mathjax]</p>