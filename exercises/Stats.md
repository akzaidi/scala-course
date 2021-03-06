# Statistical modelling

## Practical exercises

### 1. Linear regression modelling

* Run the [regression example](../examples/C6-Regression/) for the [yacht hydrodynamics dataset](http://archive.ics.uci.edu/ml/datasets/Yacht+Hydrodynamics), and go through the code carefully to understand exactly how it works. 
* When you are happy with it, make a copy and edit it to do a regression analysis for the [airfoil self-noise dataset](http://archive.ics.uci.edu/ml/datasets/Airfoil+Self-Noise). Which variables are significant for predicting scaled sound pressure?

### 2. IRLS code optimisation

* Make sure you can run the logistic regression example from the notes using the simple IRLS function that was provided.
* The IRLS function is illustrative rather than efficient. There are many way in which the code could be made more efficient. We will start with the weight matrix, `W`. This is an `n` x `n` matrix, which is bad-news if `n` is large. But it's diagonal, so it could easily be represented by an `n`-vector. Modify the code to make `W` a vector rather than a matrix, and check it gives the same results as the previous version. Time it on some big problems to see if it's perceptibly faster.
* (optional) Google the efficient implementation of IRLS (using QR decomposition), and implement it. Check it works and that it's faster.

### 3. Scala-Glm library

I've created a small library for fitting linear and generalised linear models, based on the code examples from this course. See the [scala-glm](https://github.com/darrenjw/scala-glm) repo for further details. Try it out and make sure you know how it works.


#### eof

