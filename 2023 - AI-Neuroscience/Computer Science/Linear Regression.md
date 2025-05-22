![[linear-regression.gif]]
Linear regression example. The line (model) is fitting the data more and more on each iteration

Linear Regression is a [[Machine learning]] [[Model]] utilized to analyze the relationship between dependen and independent variables and make predictions by finding the best-fitting line or hyperplane that minimizes the error between the predicted and actual value.

Linear regression models predict continuous values given x number of variables. These values can be anything, from prices, weather, counts, etc..

## Formula
$$
y = m \cdot x + b
$$
Where:
$Y$ = Dependent variable (depends on the variables $X$)
$m$ = Coefficient <- *Learnable parameter*
$X$ = Independent variable
$b$ = bias <- *Learnable parameter*

The goal of linear regression is to find the best coefficients $m \text{ and } b$ such that the line fits the data points as best as possible. *This means that we are optimizing all the $m \text{ and } b$ values*

### Calculating the error (loss function)
As you can see in the featured gif above, the line starts very far from the actual data, this is because we initialize the line (function) with random values. 

Now, since we want to update $m$ and $b$, we need some way to measure how off we are compared to the actual values, in other words, we need to calculate the error so we can later minimize it, and hopefully find the best possible linear function (line) that fits the data

The error function we use is called *mean squared error*, and this just averages the sums of the the difference between the actual line against each point
![[Pasted image 20230608134523.png]]
Error for each point - Green solid line

$$
E = \frac{1}{n} \cdot \sum (y_i - (m \cdot x_i + b))^2
$$

That function can be run for each epoch and you will see the value descending as the function fits the data better

### Updating $m$ and $b$
Now, since we are using the error function mean square error to calculate how far we are from the data, we need to use derivatives to calculate the slope of the error function with respect to $m$ and $b$. By getting the slope we will be able to take a step in the descending direction to minimize the error. For this we need to take the derivative of the error function with respect to $m$ and $b$.
$$
\frac{\variation}{a}
$$


## Python script



Related topics: [[Logistic Regression]]