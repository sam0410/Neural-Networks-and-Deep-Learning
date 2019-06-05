<h2> Notes for this lesson : </h2>

+ In neural networks, the superscript denotes the layer number.
+ The input is X, the first layer processes an output a1 which is then fed into the second layer and so on.
+ The first layer is the input layer and the last layer is the output layer. All the layers in between are called hidden layers.
+ if there are 2 hidden layer, 1 output layer and 1 input layer in a NN, it is called a 3 layer NN (because input layer isn't counted as a layer).

+ For making NN work better, we can use tanh activation function for the hidden and input layers. But in case of binary classification, sigmoid activation function has to be used for the output layer(as we want the output to be between 0 and 1)
+ Disadvantages of both the tanh and sigmoid functions is that when z = large, the slope is very small. This makes the gradient descent slow.
+ ReLU activation function- a= max(0,z). For this activation function, the slope is much different than 0 when z>0. Because of this, the learning with ReLU is much faster than with sigmoid or tanh activations. One disadvantage of ReLU is that the slope when z is less than 0 is zero. But as most of the z is greater than 0, ReLU works fine.
+ To overcome this disadvantage of ReLU, leaky ReLU was designed (where slope when z is less than 0 is slightly different than 0). Although leaky ReLU is rarely used. This is because ReLU works fine in practice.
+ The tanh activation usually works better than sigmoid activation function for hidden units because the mean of its output is closer to zero, and so it centers the data better for the next layer. Hence sigmoid is rarely used in the layers other than the output layer in case of binary classification.
+ Most commonly used activation function is the ReLU activation.

+ A=np.random.randn(4,3), B = np.sum(A, axis = 1, keepdims = True)
we use (keepdims = True) to make sure that A.shape is (4,1) and not (4, ). It makes our code more rigorous.

+ Consider there are n0, n1 and n2 layer sizes in a 2 layer NN (here n2=1 as it is the output layer). Let (w1, b1) and (w2, b2) be the parameters of layer 1 and layer 2 respectively. Then, the sizes will be ([n1,n0],[n1,1]) and ([n2,n1],[n2,1])

+ It is okay to initialize 'b' as a vector having all zeros initially. But we need to initialize 'w' as a matrix having random values. This is because the back propogation will result in symmetric allotment of values of w of all the neurons of a hidden layer. 
+ w = np.random.randn([2,2])* 0.01. We generally multiply the random vector with a small value (such as 0.01 in this case). This is because if w is very big, it may result in slow gradient descent (i.e slow learning) in activation functions such as tanh or sigmoid functions.

+ Logistic Regression doesn't have a hidden layer. If you initialize the weights to zeros, the first example x fed in the logistic regression will output zero but the derivatives of the Logistic Regression depend on the input x (because there's no hidden layer) which is not zero. So at the second iteration, the weights values follow x's distribution and are different from each other if x is not a constant vector. Hence, it is not a necessity to initialize all random values in Logistic regression.
