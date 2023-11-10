kaggle is a default repository for data sets

jeffery henton

hyper parameters num of layers etc

model, weights, parameters, all the same thing

MLP code for MNIST
	notation x to denote a training input(image)
	regard each input as a 28 by 28 = 748 dimension(column) vector
	each component of the vector represents
		the grey value for a single pixel in the image
			please see week 3 slide 5/6

NumPy package
	see slide 8 of week 3 slides

arrays are know as tensors in DL community
Tensor flow.....

research and understand
	derivative
	gradient secent
	delta rule
	perceptrons

vanishing gradients see slide 10 of week 3
	see the graph, when it reaches 1, the output becomes 0 and it outputs no data


Labs are online

nabla = partial derivative
notation = upside down triangle

self taught weights and self taught bias

why do you divide by the length of mini batch in SDG in python?
	to normalise the gradient updates

epochs are how many time you go through the training data

eta determines the step sizes you take

convolution is applying a kernel or filter to a .....

the weights correspond to kernel values, the weights become your kernel
youre learning what kernel is optimal
every dataset a bespoke combination of kernels
the weights become the kernel values