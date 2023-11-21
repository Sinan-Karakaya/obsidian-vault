In a **Linear Regression**, we want to take a set of data and fit a **Linear Model** in it.

![[Pasted image 20231121150319.png]]

The line, known as the **Line of Best Fit**, can be represented like this:
$$ y = b_0 + b_1 x $$
$$ b_0: \text{The point where the line meets x=0} $$
$$ b_1 : \text{Defines the slope of the line} $$
- **Residual** (sometimes called **error**): How far off is our prediction from a data point that we already have

![[Pasted image 20231121151101.png]]
$$ residual = |y_i - \hat{y_i}| $$
Our goal is to find the smallest residual value. The way to do this is to minimize the sum of the residuals using the lowest value of b0 and b1.
This is known as **simple linear regression**.
$$ y = b_0 + b_1 x $$
If we have more than one value in our feature vector, then this become a **multiple linear regression**.
$$ y = b_0 + b_1 x_1 + b_2 x_2 + ... + b_{n} x_n $$

## Assumptions
