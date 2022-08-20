# Gradient Descent Algo
In this repository, I implemented Gradient Descent Algorithm and its types namely Batch GD, Stochastic GD and Mini-Batch GD from scratch. 

Gradient Descent is an iterative optimization algorithm used to find a local minimum/maximum of a given function. <br>
In this case, we will use GD and its different variations, to fit a straight line through randomly generated data using numpy.<br><br>
There are three different types of GD:
-  Batch Gradient Descent
-  Stochastic Gradient Descent
-  Mini-Batch Gradient Descent

## Why use GD?

Normal equations are good when it comes to data having relatively less features. But it gets computationally complex as the number of features increases <br><br>
The time complexity of inverting a matrix in case of normal equations is O(N^3), where N is the number of features.
<br>
Time complexity of computing pseudo inverse using SVD is O(N^2)
<br><br>
Hence, we need an iterative technique which is computationally less complex. This is where GD comes into play.

## Batch Gradient Descent
In case of Batch Gradient Descent, we take the whole training set and use it to compute the cost function. This not only makes it slow but it also makes Batch GD prone to getting stuck at local minima. <br>
<br> In case of Linear Regression, we don't have to care about local minima because the Cost Function for LR is a convex function. 

## Stochastic Gradient Descent
In case of Stochastic Gradient Descent, we take a random instance from our training set and use it to compute our cost function. <br>
<br>
This makes SGD able to escape any local minima because random instances makes Cost Function change erratically. But we don't want it to change this erratically all the time, so we decrease the learning rate slowly. <br>

## Mini-Batch Gradient Descent
In case of Mini-Batch Algorithm, we try to find the middle way between BGD and SGD. <br>
Instead of taking whole dataset or a random instance from the dataset, we take subsets of the dataset (called mini-batches, hence the name Mini-Batch GD) and use them to compute the cost function.
