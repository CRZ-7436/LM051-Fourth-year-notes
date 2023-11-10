Physical symbol system hypothesis(PSSH)

- Newell and simon
    
- basis of old AI, symbolic AI
    

  

ANNs(?)

- See week 2 lecture slides
    

  

Perceptron

- activation function, signum or sign function (threshold?)
    

  

He might ask about the second AI winter(guaranteed to show up)

First AI winter was caused by the XOR function, as it cannot be computed with one thingy(?)

second was caused by.....

  

perceptron training - comes up in exam (particularly the formula for update)

- the delta rule...
    
- learn the weights that minimise the squared error
    
- big D is the training set
    
- small d is the training data single
    

  

slide 9 the world linear in important

  

know the gradient descent- the delta rule

see slide 9, know the bottom function

  

vector: input of values

e.g if x was a vector of an image it would be 256 x 256 of pixels

  

algorithm- supervised learning. Each training example is a pair form, where x is a vector of input value. its set to a low value e.g 0.05

  

cant use gradient descent on a signum function, cant derive a continous function as it approaches 0

  

batch mode gradient descent

- do until terminating condition satisfied
    

  

Incremental mode gradient descent

  

What is better batch or incremental? and why is it better

batch is better but idk why lmao

it is best at minimizing the mean squared error

  

Multi-layer perceptron(MLP)

- example speech recognition
    
- activation function uses sigmoid
    
- continuous(differentiable) and non linear
    
- known as back propagation(BP)
    
- slide 16
    

- sigmoid is hugely problematic
    
- from about 1980 to 2010 everyone was using it but confused why the results werent great
    
- saturation, when the data is low or high then the output is either zero or one
    

  

key points gradient descent

- finding weights that minimize the error
    

  

Backpropagation(BP) Algorithm

- repeat until terminating condition satisfied
    

- the derivative of the sigmoid is used here
    
- who invented BP
    

  

network weights should  converge to the minimum

decaying learning rates(will be covered and talked about later one)

  

weights referred to as the MODEL or parameters

  

loss function- mean squared error(MSE), use to calculate gradient(slope)

  

Cross validation: training set, test set and validation set

  

ways to decrease overfitting

simplily

more date

better quality data

renderisation

renderiser

  

cross entrop

- from information theory