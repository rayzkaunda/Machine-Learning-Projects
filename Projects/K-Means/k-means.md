# Overview
Will be exploring K-means Clustering in Spark , Keras, and  scikit-learn.

# Introduction

So imagine you have a set of numerical data of cancer tumors in 4 different stages from 1 to 4, and you need to study all the tumors in each stage. However, you have no idea how to identify the tumors that are at the same stage because nobody had the time to label the entire set of features (most data in the world are unlabeled). In this case, you need K-means algorithm because it works on unlabeled numerical data and it will automatically and quickly group them together into 4 clusters.

For this example, we chose k=4 because, we already know, we have 4 tumors’ stages, but if we want to cluster them based on their structure, growth speed, or growth type, then maybe k will be different than 4.

If you don’t know how many groups you want, it’s problematical, because K-means needs a specific number k of clusters in order to use it. So, the first lesson, whenever, you have to optimize and solve a problem, you should know your data and on what basis you want to group them. Then, you will be able to determine the number of clusters you need.
