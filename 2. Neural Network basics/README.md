<h2> Notes for this lesson : </h2>

+ Logistic regression is an algorithm for binary classification.
+ The input vector for classification of a RGB image of dimensions 64*64 will be a matrix of size 122488*1 (because 64*64*3= 122488)
+ consider the size of each input is Nx and the number of training examples is m. then input matrix is of size Nx * m
+ We use the sigmoid function to determine the probability of the output being the required label. It is of the form sigmoid(theta.T * X + b)
+ We don't use a squared loss function because in that case, gradient descent may not find a global minimum.
+ Loss function = -[(1-y)log(1-yc) + ylog(yc)] where yc is the calculated label and y is the actual label of the given input.
+ The loss function computes the error for a single training example; the cost function is the average of the loss functions of the entire training set
+ Gradient descent is a way of finding the global minimum of the cost function.
+ In forward propagation step, we compute the output of the neural network. This is then followed by a backward pass or back propagation step,
which we use to compute gradients or compute derivatives.
+ In python, vectorization makes it faster to compute the dot products of two very large vectors.
+ Both CPUs and GPUs have parallization instructions called SIMD instructions (Single Instruction Multiple Data). Vectorization in python enables the parallization on CPU, hence making computations much faster than a for loop.
+ If we add a real number to a vector in python, the real number is automatically added to each and every element of the vector. This is called Broadcasting in python.

+ In python, "np.dot(a,b)" performs a matrix multiplication on a and b, whereas "a*b" performs an element-wise multiplication

+ dL/dz = (dL/da) * (da/dz) 
where L = -[(1-y)log(1-yc) + ylog(yc)]
      z = wx + b
      a = sigmoid(z)

Hence, dL/dz = dL/da * da/dz = [(-y/a) + (1-y)/(1-a)] * [a(1-a)] = a-y 
also, dL/dw = dL/dz * dz/dw = (a-y)*X

+ The shorthands dz, db and dw refer to dL/dz, dL/db and dL/dw respectively.



