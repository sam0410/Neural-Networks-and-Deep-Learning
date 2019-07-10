<h2> Notes for this lesson : </h2>

+ Depth of a neural network is the number of hidden layers present in the NN.
+ Number of layers = depth + 1 (as it includes the output)
+ n[l] is the number of units in the layer `l`. n[0] denotes number of input units and n[l] denotes number of output units.
+ The following `for` loopis required to compute the output of the neural network (forward propogation)
  (Here a[0]=x and a[l]= output)

	for i = 1 to l
		z[i] = w[i]* a[i-1]
		a[i]= g(z[i])

+ The following `for` loop is for backward propogation
  (Here a[0]=x and a[l]= output)

	for i = 1 to l
		z[i] = w[i]* a[i-1]
		a[i]= g(z[i])


+ Dimensions of z[i] = n(i) * 1
+ Dimensions of w[i] = n(i) * n(i-1)
+ There are functions you can compute with a small 'L' layer deep neural network that shallower networks require exponentially more hidden layers to compute.
+ the "cache" records values from the forward propagation units and sends it to the backward propagation units because it is needed to compute the chain rule derivatives.
+ During backpropagation you need to know which activation was used in the forward propagation to be able to compute the correct derivative.
+ Parameters : w and b
+ Hyperparameters : number of iterations, learning rate(alpha), number of hidden layers, number of hidden units, choice of activation functions.
Other hyperparameters include momentum term, mini-batch size, regularizations etc.
+ It is quite possible that the best value for the hyperparameters might change over time. So, it is recommended that we keep varying hyperparameters to the best possible value every few months for a particular application.

