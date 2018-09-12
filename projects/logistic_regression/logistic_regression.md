# Overview
Will be exploring Logistic regression in Spark , Keras, and  scikit-learn.

# Introduction

Logistic regression is a popular method to predict a categorical response. It is a special case of Generalized Linear models that predicts the probability of the outcomes. In spark.ml logistic regression can be used to predict a binary outcome by using binomial logistic regression, or it can be used to predict a multiclass outcome by using multinomial logistic regression.

# Classification

Classification is a family of supervised machine learning algorithms that identify which category an item belongs to (for example, whether a cancer tissue observation is malignant or not), based on labeled examples of known items (for example, observations known to be malignant or not). Classification takes a set of data with known labels and pre-determined features and learns how to label new records based on that information. Features are the “if questions” that you ask. The label is the answer to those questions is basically if it walks, swims, and quacks like a duck, then the label is "duck."

# Logistic Regression

<p>In this notebook we are going to use Apache Spark MLib to predict whether a client is a smoker or not. This is called a binary classification problem.We are going to use the Logistic Regression algorithm and other features provided by Mlib.
Logistic regression is widely used to predict a binary response. It is a linear method as described above in equation, with the loss function in the formulation given by the logistic loss:
<pre>                                             L(w;x,y):=log(1+exp(−ywTx))</pre>

For binary classification problems, the algorithm outputs a binary logistic regression model. Given a new data point, denoted by x, the model makes predictions by applying the logistic function
<pre>                                              f(z)=11+e−z </pre>
where <pre> z=wTx. By default, if f(wTx)>0.5, </pre>
the outcome is positive, or negative otherwise, though unlike linear SVMs, the raw output of the logistic regression model, f(z), has a probabilistic interpretation (i.e., the probability that x is positive).
A Logistic Regression algorithm in Spark requires a dataframe of numerical feautures and a label column as input and outputs a predictions dataframe.</p> Our work flow is as follows;<ul>
<li> Load dataset</li>
<li>Select features we are going to use</li>
<li>Convert features</li>
<li>Split dataset to train and test</li>
<li>Train and fit our model</li>
<li>Evaluate our model on test set</li>
<li>Conclusion</li>
</ul>   
</p>

<p>Our data consists of the insurance dataset publickly available at https://www.kaggle.com/mirichoi0218/insurance and run with Spark local mode and pyspark.

</p>
