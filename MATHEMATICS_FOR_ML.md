# Mathematics for Machine Learning

This guide is a companion to the numbered notebooks. Its purpose is to make the maths used by ML understandable, not to turn the course into a pure mathematics degree.

## 1. Scalars, vectors and matrices

A **scalar** is one number, such as 5. A **vector** is an ordered list of numbers, such as [2, 4, 6]. A **matrix** is a rectangular table of numbers.

In ML, one row of a dataset is often represented as a vector of features. A batch of rows can be represented as a matrix.

For example, if each student has two features — hours studied and attendance — then three students can be represented as:

```
X = [[2, 80],
     [4, 90],
     [1, 65]]
```

The matrix has shape (3, 2): three rows and two columns. Shape matters because matrix operations require compatible dimensions.

## 2. Dot product and linear predictions

For vectors x = [x1, x2] and weights w = [w1, w2], the dot product is:

`x · w = x1*w1 + x2*w2`

With x = [2, 80] and w = [3, 0.5], the weighted sum is 2*3 + 80*0.5 = 46. A linear model adds a bias term b:

`prediction = x · w + b`

Weights express how the model combines inputs. The bias shifts the prediction.

## 3. Mean and variance

The **mean** is the arithmetic average. For [2, 4, 6], mean = (2 + 4 + 6)/3 = 4.

Variance measures the average squared distance from the mean. Population variance for these values is ((2-4)^2 + (4-4)^2 + (6-4)^2)/3 = 8/3. Standard deviation is the square root of variance and is expressed in the same units as the original data.

These are used to describe data spread and understand scaling.

## 4. Probability and conditional probability

Probability describes how likely an event is, from 0 (impossible) to 1 (certain).

Conditional probability asks how likely A is when B is already known:

`P(A | B) = P(A and B) / P(B)`, when P(B) is greater than zero.

**Bayes' theorem** reverses the condition:

`P(A | B) = P(B | A) * P(A) / P(B)`

Naive Bayes classifiers use this relationship to estimate class probabilities from observed features.

## 5. Derivatives and gradients

A **derivative** describes how quickly a function changes when its input changes. A partial derivative measures the change with respect to one input while holding other inputs fixed.

A **gradient** collects partial derivatives for a function with many parameters. It points in the direction of steepest increase. Gradient descent moves parameters in the opposite direction:

`new_parameter = old_parameter - learning_rate * gradient`

The learning rate controls the step size. A very large value may jump past a good solution; a very small value may make learning painfully slow.

## 6. Loss and optimization

A **loss function** turns prediction errors into a number the learning algorithm can try to reduce. For a single regression example, squared error is:

`(actual - predicted)^2`

Training is an optimization problem: find parameter values that make the chosen loss small on training data. Lower training loss alone does not guarantee good predictions on new data, so validation and test data are important.

## 7. Correlation is not causation

Correlation measures how two variables move together. A high correlation does not prove that one variable causes the other. A third factor may influence both, or the relationship may be coincidental.

## Further study

- [3Blue1Brown Linear Algebra](https://www.3blue1brown.com/topics/linear-algebra)
- [Khan Academy Statistics and Probability](https://www.khanacademy.org/math/statistics-probability)
- [StatQuest](https://statquest.org/)
