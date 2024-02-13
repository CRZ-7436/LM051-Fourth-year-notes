### Question 1

#### Q1 a) Discuss the challenges that arise in a traditional Sense-Plan-Act (SPA) cycle as shown in Figure-Q-1-a. What is the solution suggested in subsumption architectures?

1 mark.

**Answer:** The traditional Sense-Plan-Act (SPA) cycle in robotics and AI systems faces several challenges:

- **Complexity and Computationally Intensive**: The SPA cycle often involves complex models and algorithms for planning, which can be computationally intensive and slow, especially in dynamic environments.
- **Inflexibility**: SPA systems can struggle with unexpected changes or uncertainties in the environment, as the plan is typically based on initial sensing and may not adapt well to changes.
- **Solution in Subsumption Architectures**: Subsumption architecture, proposed by Rodney Brooks, addresses these challenges by layering simple behavior modules that directly connect sensing to actions. Each layer operates independently and can override lower layers, allowing for more flexible and adaptive behavior without the need for complex planning.

#### Q1 b) What is machine learning? What are the challenges faced by an ML implementation?

1 mark.

**Answer:** Machine Learning (ML) is a field of artificial intelligence that focuses on building systems that can learn from and make decisions based on data. ML systems improve their performance on specific tasks over time with experience (data).

Challenges in ML implementation include:

- **Data Quality and Quantity**: ML models require large amounts of high-quality, representative data. Insufficient or biased data can lead to poor model performance.
- **Overfitting and Generalization**: Ensuring that models generalize well to new, unseen data while avoiding overfitting to the training data is a key challenge.
- **Computational Resources**: Training complex models, especially deep learning models, requires significant computational resources.
- **Interpretability**: Many ML models, particularly deep learning models, act as "black boxes," making it difficult to interpret their decisions.


### Question 2

#### Q2 a) Update Rule for a Linear Perceptron

- **Question:** What is the update rule for a linear perceptron?
- **Answer:** The update rule for a linear perceptron is used to adjust the weights based on the error between the predicted and actual outputs. It is given by: wnew=wold+α×(y−y^)×xwnew​=wold​+α×(y−y^​)×x where wnewwnew​ and woldwold​ are the new and old weights, respectively, αα is the learning rate, yy is the actual output, y^y^​ is the predicted output, and xx is the input.

#### Q2 b) Perceptron Code and Logical Gate

- **Question:** Write the code for a perceptron with fixed weights w1 = w2 =1, and bias -0.5. Name the logical gate modeled by this perceptron.
- **Answer:**
    - **Perceptron Code:**
    def perceptron(x1, x2):
    w1, w2 = 1, 1  # Fixed weights
    bias = -0.5
    output = w1*x1 + w2*x2 + bias
    return 1 if output >= 0 else 0
    - - **Logical Gate Modeled:** This perceptron models an AND gate. It outputs 1 only when both inputs (x1 and x2) are 1.

These formatted notes provide concise answers to Question 2 of the exam, focusing on the linear perceptron's update rule and its implementation as an AND gate, suitable for study and review.


### Question 3

#### Q3 a) Differentiable Activation Units in MLPs

- **Question:** Why are differentiable activation units used in Multi-Layered Perceptrons (MLPs)?
- **Answer:** Differentiable activation units are crucial in MLPs for enabling the use of gradient-based optimization methods, such as backpropagation. These units introduce non-linearity into the network, allowing it to learn complex patterns. The differentiability of these units is essential because it allows for the computation of gradients, which are used to update the weights of the network in a direction that minimizes the loss function.

#### Q3 b) δ, η, and α in Backpropagation Weight Update Rule

- **Question:** What is δ, η, and α in the following weight update rule used in backpropagation?
- **Answer:**
    - **δ (Delta):** Represents the error term in the backpropagation algorithm. It is the derivative of the loss function with respect to the activation of a neuron and is used to calculate the gradient of the loss function.
    - **η (Eta):** Denotes the learning rate in the algorithm. It is a hyperparameter that determines the step size at each iteration while moving toward a minimum of the loss function.
    - **α (Alpha):** Often represents the momentum term in some variations of the backpropagation algorithm. It helps to accelerate gradients vectors in the right direction, leading to faster converging.

These formatted notes provide concise yet comprehensive answers to Question 3 of the exam, focusing on the role of differentiable activation units in MLPs and the significance of δ, η, and α in the backpropagation weight update rule.



### Question 4

#### Q4 a) Purpose of Receptive Fields in Neural Networks

- **Question:** What is the purpose of receptive fields shown in Figure Q-4-a?
- **Answer:** The purpose of receptive fields in neural networks, particularly in Convolutional Neural Networks (CNNs), is to capture local patterns within the input data. Each neuron in a convolutional layer is connected to a small region (the receptive field) of the previous layer, allowing the network to detect features like edges, textures, or specific shapes within that region. This localized perception enables the network to build complex patterns by combining these local features in subsequent layers.

#### Q4 b) Overfitting and Its Illustration

- **Question:** What is overfitting? Draw a plot that illustrates.
- **Answer:**
    - **Definition of Overfitting:** Overfitting occurs when a machine learning model learns the details and noise in the training data to the extent that it negatively impacts the performance of the model on new data. This means the model is too complex and fits the training data too closely, capturing noise and fluctuations that do not generalize to unseen data.
    - **Illustration of Overfitting:** A common illustration of overfitting is a plot comparing the model's performance on the training and validation datasets over training epochs. In an overfitting scenario, the training accuracy continues to increase, while the validation accuracy plateaus or decreases, indicating that the model is not generalizing well to new data.


### Question 5

#### Q5 a) Comparison of Loss Functions: MSE vs. Cross Entropy

- **Question:** Which is the better loss function: Mean Squared Error (MSE) or Cross Entropy?
- **Answer:** The choice between Mean Squared Error (MSE) and Cross Entropy as a loss function depends on the specific problem and the model being used.
    - **MSE:** Typically used for regression problems. It measures the average squared difference between the estimated values and the actual value.
    - **Cross Entropy:** More suitable for classification problems, especially with softmax activation in the output layer. It measures the performance of a classification model whose output is a probability value between 0 and 1.

#### Q5 b) Regularisation Techniques to Reduce Overfitting

- **Question:** Describe three regularisation techniques that can help reduce overfitting.
- **Answer:**
    - **L1 and L2 Regularisation:** These add a penalty term to the loss function, which is proportional to the absolute (L1) or square (L2) of the weight values. This discourages the model from fitting the training data too closely.
    - **Dropout:** Randomly sets a fraction of the input units to 0 at each update during training, which helps prevent complex co-adaptations on training data.
    - **Early Stopping:** Involves stopping the training process before the learner passes the point where it begins to overfit. This is done by monitoring the model's performance on a validation set.


### Questions 6

#### Q6 a) Concept of Convolution in CNNs

- **Question:** Describe the concept of convolution in a Convolutional Neural Network (CNN).
- **Answer:** In CNNs, convolution involves applying a filter or kernel to the input data to extract features. The kernel slides over the input data, and at each position, a dot product is computed between the kernel and the part of the image it covers. This process creates a feature map that highlights specific features in the input, such as edges or textures.

#### Q6 b) Code for Convolutional Layer in CNN

- **Question:** Write the code for a convolutional layer in a CNN. Briefly describe the loss function and optimizer used.
- **Answer:**
    - **Code Example:**
    from keras.layers import Conv2D
    model.add(Conv2D(filters=32, kernel_size=(3, 3), activation='relu', input_shape=(28, 28, 1)))
    **Loss Function and Optimizer:** Commonly, a cross-entropy loss function is used for classification tasks, and an optimizer like Adam or SGD (Stochastic Gradient Descent) is used to minimize the loss function during training.

### Questions 7

#### a) Softmax Function

- **Question:** What is Softmax?
- **Answer:** Softmax is a function that converts a vector of values into a probability distribution. The outputs of the Softmax function are in the range (0, 1) and sum up to 1. It is commonly used in the output layer of a neural network for multi-class classification problems.

#### Q7 b) Code for Output Layer of CNN for CIFAR-10

- **Question:** Write the code for the output layer of a CNN used to classify CIFAR-10 dataset.
- **Answer:**
from keras.layers import Dense
model.add(Dense(10, activation='softmax'))

This code adds a dense layer with 10 units (one for each class in CIFAR-10) and uses the Softmax activation function.

### Questions 8
#### a) Vanishing Gradient Problem

- **Question:** What is a vanishing gradient and identify common causes of the same?
- **Answer:** The vanishing gradient problem occurs when gradients become very small, effectively preventing the weights from changing their values during training. This is often caused by the use of certain activation functions like sigmoid or tanh, which saturate and produce gradients close to zero.

#### Q8 b) Approaches to Reduce Impact of Vanishing Gradients

- **Question:** Briefly describe the approaches used to reduce the impact of vanishing gradients.
- **Answer:**
    - **Use of ReLU Activation Function:** ReLU and its variants help prevent vanishing gradients as they do not saturate in the positive domain.
    - **Proper Initialization:** Using techniques like He or Xavier initialization ensures that the weights are neither too small nor too large.
    - **Batch Normalization:** Normalizes the output of a previous activation layer by subtracting the batch mean and dividing by the batch standard deviation.
    - **Skip Connections:** Used in architectures like ResNet, skip connections help gradients flow through the network by adding outputs from previous layers to the outputs of stacked layers.


### Questions 9
#### Q9 a) Ensuring Representative Train and Test Sets

- **Question:** How does one ensure that compositions in train and test sets are representative of the dataset?
- **Answer:** To ensure that train and test sets are representative of the dataset, one should use random sampling or stratified sampling techniques. Stratified sampling is particularly useful when the dataset has imbalanced classes, as it ensures that each class is proportionally represented in both training and testing sets. Additionally, cross-validation techniques can be employed to further ensure the robustness of the model.

#### Q9 b) Purpose and Structure of Inception Module in Google LeNet

- **Question:** Describe the purpose and structure of an inception module. Explain the rationale for a kernel of size 1.
- **Answer:**
    - **Purpose:** The inception module, used in Google LeNet, aims to efficiently utilize computing resources by applying different-sized filters (kernels) simultaneously within the same module.
    - **Structure:** It consists of several parallel paths with different kernel sizes (e.g., 1x1, 3x3, 5x5) and a pooling path. These paths are then concatenated.
    - **Rationale for 1x1 Kernel:** The 1x1 kernel is used for dimensionality reduction, reducing computational complexity while retaining important information.
### Questions 10
#### Q10 a) Precision and Recall

- **Question:** What is precision and recall?
- **Answer:**
    - **Precision:** The ratio of correctly predicted positive observations to the total predicted positives. It is a measure of a classifier's exactness.
    - **Recall (Sensitivity):** The ratio of correctly predicted positive observations to all observations in the actual class. It is a measure of a classifier's completeness.

#### Q10 b) Residual Learning in ResNet

- **Question:** Describe residual learning that constitutes a key architectural constraint in ResNet.
- **Answer:**
    - **Residual Learning:** In ResNet, residual learning involves learning the residual (difference) between the input and the output of a layer rather than learning the output directly. This is achieved through skip connections that add the input of a layer to its output.
    - **Purpose:** This approach helps in alleviating the vanishing gradient problem and allows the construction of much deeper networks by enabling easier training and better performance.
### Questions 11
#### Q11 a) Transfer Learning

- **Question:** What is transfer learning?
- **Answer:** Transfer learning is a machine learning technique where a model developed for one task is reused as the starting point for a model on a second task. It is particularly useful when the dataset for the second task is small, as it leverages the knowledge gained from a related task with a larger dataset.

#### Q11 b) Code for Transfer Learning

- **Question:** Write the code for transfer learning used in the second CS4287 assignment.
- **Answer:**
from keras.applications import VGG16
from keras.models import Model
from keras.layers import Dense, Flatten

//Load pre-trained VGG16 model without the top layer
base_model = VGG16(weights='imagenet', include_top=False, input_shape=(224, 224, 3))

//Add new layers for the new task
x = Flatten()(base_model.output)
x = Dense(1024, activation='relu')(x)
predictions = Dense(10, activation='softmax')(x)

//Define the new model
model = Model(inputs=base_model.input, outputs=predictions)

### Questions 12
#### Q12 a) Key Characteristics of Reinforcement Learning (RL)

- **Question:** What are the key characteristics of Reinforcement Learning (RL)? Compare and contrast RL with supervised and unsupervised learning.
- **Answer:**
    - **Key Characteristics of RL:** RL involves learning to make decisions by interacting with an environment to achieve a goal. It focuses on learning optimal policies through trial and error, using rewards as feedback.
    - **Comparison with Supervised Learning:** Unlike supervised learning, which relies on labeled data, RL learns from the consequences of actions, not from direct instruction.
    - **Comparison with Unsupervised Learning:** While unsupervised learning finds patterns in data without labels, RL is goal-oriented, learning to achieve a specific objective through interactions.

#### Q12 b) Sampling Averaging Method in K 1-armed Bandit Problem

- **Question:** Explain why the sampling averaging method with optimistic starts outperforms ε-greedy in the K 1-armed non-associative bandit problem.
- **Answer:**
    - **Sampling Averaging with Optimistic Starts:** This method initializes estimates optimistically, encouraging exploration early in training. It tends to explore more efficiently than ε-greedy, which has a fixed exploration rate.
    - **Advantage Over ε-greedy:** The optimistic initial values drive the agent to explore all options before converging, leading to better performance in finding the optimal action compared to the constant exploration rate of ε-greedy.
### Questions 13
#### Q13 a) Challenges Faced by a Reinforcement Learning Agent

- **Question:** Describe 3 challenges faced by a Reinforcement Learning agent.
- **Answer:**
    - **Exploration vs. Exploitation Dilemma:** Balancing the need to explore unknown actions versus exploiting known rewarding actions.
    - **Credit Assignment Problem:** Determining which actions are responsible for receiving rewards, especially when rewards are delayed.
    - **Stability and Convergence:** Ensuring that the learning process is stable and converges to an optimal policy.

#### Q13 b) Dynamic Programming (DP) and Monte Carlo (MC) in RL

- **Question:** Briefly describe the key characteristics of Dynamic Programming (DP) and Monte Carlo (MC) approaches to solving Bellman’s equations in RL.
- **Answer:**
    - **Dynamic Programming:** DP methods, like value iteration and policy iteration, are model-based and require a complete and accurate model of the environment. They break down the Bellman equations into smaller subproblems for efficiency.
    - **Monte Carlo Methods:** MC methods are model-free and estimate values based on averaging complete returns (rewards until the end of an episode). They do not require knowledge of the environment's dynamics and are useful in situations where the model is unknown or too complex.
### Questions 14
#### Q14 a) Update for Q Learning and Its Classification

- **Question:** What is the update for Q learning? Why is Q Learning categorized as an off-policy learning method?
- **Answer:**
- ![[Pasted image 20231214201631.png]]

#### Q14 b) Different Paths in Temporal Difference Algorithms

- **Question:** Explain why temporal difference algorithms like Sarsa and Q learning give rise to different paths in a grid world scenario.
- **Answer:**
    - **Sarsa (On-policy):** Sarsa learns the value of the policy being followed, including exploration. It tends to take safer, more conservative paths.
    - **Q Learning (Off-policy):** Q learning learns the value of the optimal policy, often leading to more direct but riskier paths, as it always considers the best possible future action regardless of the current policy.
### Questions 15
#### Q15 a) Data Presentation in DQN for Atari

- **Question:** Describe how the data is captured and presented to a DQN architecture for the game of Atari.
- **Answer:**
    - **Data Capture:** In Atari games, the input to the DQN is the raw pixel data from the game screen. This data is often preprocessed, such as by resizing, cropping, and converting to grayscale.
    - **Data Presentation:** The preprocessed frames are stacked (usually the last four frames) to provide the network with information about the motion in the game, which is crucial for decision-making.

#### Q15 b) Concept of Dueling DQNs

- **Question:** Describe the concept of Dueling DQNs with reference to the game of Atari.
- **Answer:**
    - **Dueling DQNs:** This architecture splits the Q-network into two streams: one for estimating the state value function and another for estimating the advantage for each action. The two streams are then combined to estimate the Q-values.
    - **Advantage in Atari Games:** This structure allows the network to learn which states are valuable without having to learn the effect of each action at each state, leading to more efficient learning in complex environments like Atari games.
