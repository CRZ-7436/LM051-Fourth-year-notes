### Question 1

#### Q1 a) Reinforcement Learning and Key Issues

- **Question:** What is Reinforcement Learning? What are the key issues that an RL agent must address? Illustrate the discussion with an example.
- **Answer:**
    - **Reinforcement Learning (RL):** RL is a type of machine learning where an agent learns to make decisions by performing actions in an environment to achieve a goal. The learning is guided by rewards or penalties.
    - **Key Issues:**
        - **Exploration vs. Exploitation**: Balancing the need to explore new actions to find more rewarding strategies versus exploiting known rewarding actions.
        - **Credit Assignment Problem**: Determining which actions lead to rewards or penalties, especially when rewards are delayed.
    - **Example:** In a maze-solving task, the RL agent must explore different paths (exploration) and learn to use the most efficient path to reach the goal (exploitation).

#### Q1 b) Temporal Difference Methods: Bridging DP and MC

- **Question:** Explain how Temporal Difference (TD) methods bridge Dynamic Programming (DP) and Monte Carlo (MC) methods. Include a backup diagram for DP in the discussion.
- **Answer:**
    - **TD Methods:** TD methods combine ideas from both DP and MC. Like DP, they bootstrap by updating estimates based on other estimates. Like MC, they can learn directly from raw experience without a model of the environment.
    - **Backup Diagram for DP:**
    ![[Pasted image 20231214202059.png]]

    This diagram shows the transition from state S to S' and the update of state value V(S) based on the reward and the discounted value of the next state V(S').

#### Q1 c) On-policy vs. Off-policy in TD Methods

- **Question:** What is meant by the terms on-policy and off-policy in the context of TD methods? Include the equations for an on-policy and off-policy update.
- **Answer:**
    - **On-policy Methods:** Learn the value of the policy being followed. The Sarsa algorithm is an example, with the update rule: Q(S,A)←Q(S,A)+α[R+γQ(S′,A′)−Q(S,A)]Q(S,A)←Q(S,A)+α[R+γQ(S′,A′)−Q(S,A)].
    - **Off-policy Methods:** Learn the value of an optimal policy, independent of the agent's actions. Q-learning is an example, with the update rule: Q(S,A)←Q(S,A)+α[R+γmax⁡aQ(S′,a)−Q(S,A)]Q(S,A)←Q(S,A)+α[R+γmaxa​Q(S′,a)−Q(S,A)].

#### Q1 d) Paths in Cliff Walking: Sarsa vs. Q Learning

- **Question:** Identify the path learned by Sarsa and Q in the cliff walking problem. Explain why the paths differ and refer to the update in part (c) in the answer.
- **Answer:**
    - **Sarsa's Path:** More conservative, avoiding the cliff closely. This is due to its on-policy nature, where the policy includes exploration.
    - **Q Learning's Path:** More optimal but riskier, closer to the cliff. As an off-policy method, Q-learning directly learns the optimal policy, which may include risky moves that are closer to the cliff but faster.
    - **Difference:** Arises from the on-policy nature of Sarsa, which considers the current policy's exploratory actions, versus the off-policy nature of Q-learning, which learns the optimal policy regardless of the current exploration strategy.


### Question 2

#### Q2 a) Weights and Connections in AlexNet's First Hidden Layer

- **Question:** How many weights and connections in the first hidden layer of AlexNet given filters of size 11 x 11 that generate 96 feature maps from an input of size [224, 224]? Please show the calculations. Why is the number of connections greater than the number of weights?
- **Answer:**
    - **Calculating Weights:**
        - Each filter size: 11×1111×11
        - Depth of input layer (assuming RGB): 33
        - Total filters: 9696
        - Weights per filter: 11×11×311×11×3
        - Total weights: 11×11×3×96=34,84811×11×3×96=34,848
    - **Calculating Connections:**
        - Size of output feature map (assuming stride 1 and no padding): (224−11+1)×(224−11+1)=214×214(224−11+1)×(224−11+1)=214×214
        - Connections per filter: 11×11×3×214×21411×11×3×214×214
        - Total connections: 11×11×3×214×214×96=164,299,77611×11×3×214×214×96=164,299,776
    - **Reason for More Connections Than Weights:** Due to weight sharing in convolutional layers, the same weights are used across different positions in the input, leading to a higher number of connections compared to the actual number of unique weights.

#### Q2 b) Vanishing Gradients and Batch Normalisation

- **Question:** Describe the concept of vanishing gradients and explain how this phenomenon arises. How many parameters in the two Batch Normalisation layers in Figure Question-2? Of these, how many are trainable?
- **Answer:**
    - **Vanishing Gradients:** This phenomenon occurs when gradients become very small during backpropagation, especially in deep networks. It arises due to the multiplication of gradients through layers, which can lead to extremely small values, hindering the network's ability to learn.
    - **Batch Normalisation:** Introduced by Ioffe and Szegedy (2015), it normalizes the input of each layer to stabilize the learning process and mitigate the vanishing gradient problem.
    - **Parameters in Batch Normalisation Layers:** Each Batch Normalisation layer has two sets of parameters for each feature: scale (gamma) and shift (beta). Assuming the model in Figure Question-2, the first layer normalizes the flattened input (784 features), and the second layer normalizes the output of a 300-unit dense layer. Therefore, the total number of parameters is 2×784+2×300=2,1682×784+2×300=2,168, all of which are trainable.

#### Q2 c) Estimate and Target Values in DQN

- **Question:** Describe how the estimate and target values are calculated in a Deep Q Network (DQN). Illustrate the discussion with coding fragments or pseudocode.
- **Answer:**
    - **Estimate Value:** The estimate value in a DQN is the current Q-value obtained from the network for a given state-action pair. It is calculated using the current state and the action chosen by the policy.
    Q_estimate = Q_network(current_state, action)
    **Target Value:** The target value is calculated as the immediate reward received after taking an action, plus the discounted maximum Q-value for the next state, obtained from the target network.
    Q_target = reward + gamma * max(Q_target_network(next_state))
    **Note:** The target network is a copy of the main network, updated less frequently to stabilize training.






### Question 3

#### Q3 a) Parameters in GoogleLeNet vs. AlexNet

- **Question:** Explain why the number of parameters in GoogleLeNet using Inception modules is significantly less than AlexNet - 6 million as opposed to 60 million. Illustrate the answer with a diagram and calculations.
- **Answer:**
    - **GoogleLeNet and Inception Modules:** GoogleLeNet uses Inception modules, which consist of parallel paths with different-sized filters (1x1, 3x3, 5x5) and a pooling path. This design allows for efficient computation and a reduction in the number of parameters.
    - **Comparison with AlexNet:** AlexNet uses larger filters and fully connected layers, leading to a higher number of parameters. In contrast, Inception modules in GoogleLeNet perform convolutions of different sizes in parallel, reducing the dimensionality and the number of parameters.
    - **Diagram:**(simplified Inception module)
    ![[Pasted image 20231214202517.png]]
    This diagram represents the parallel paths in an Inception module, each performing a different operation, and then concatenating the outputs.

#### Q3 b) Regularisation in Deep Learning

- **Question:** What is regularisation? Describe three regularisation techniques. Include coding fragments or pseudocode and diagrams where relevant.
- **Answer:**
    - **Regularisation:** Regularisation is a technique used to prevent overfitting in machine learning models by penalizing model complexity.
    - **Techniques:**
        - **L1/L2 Regularisation:** Adds a penalty proportional to the absolute (L1) or square (L2) of the weight values to the loss function.
        from keras.regularizers import l1_l2
        model.add(Dense(64, activation='relu', kernel_regularizer=l1_l2(l1=0.01, l2=0.01)))
        - **Dropout:** Randomly sets a fraction of input units to 0 at each update during training.
        from keras.layers import Dropout
        model.add(Dropout(0.5))
        - **Early Stopping:** Stops training when the model's performance on a validation set starts to degrade.
        from keras.callbacks import EarlyStopping
        early_stopping = EarlyStopping(monitor='val_loss', patience=5)

#### Q3 c) Key Concepts in ResNet

- **Question:** Describe the key concept(s) in ResNet. Include a discussion on the purpose of using a kernel of size 1x1 with stride 2. Illustrate the discussion with a diagram.
- **Answer:**
    - **ResNet Key Concepts:** ResNet introduces the concept of residual learning, where layers learn residual functions with reference to the layer inputs. This is achieved through skip connections that add the input of a layer to its output.
    - **1x1 Kernel with Stride 2:** The 1x1 kernel with stride 2 is used for dimensionality reduction. It helps in reducing the spatial dimensions of the input while increasing depth, without a significant increase in computational complexity.
    - **Diagram:**
    ![[Pasted image 20231214202646.png]]
    This diagram shows a basic ResNet block with convolutional layers and a shortcut connection that adds the input to the output of the block.



### Question 4

#### Q4 a) Symbolic AI vs. Machine Learning Paradigms

- **Question:** Compare and contrast the Symbolic AI and Machine Learning (ML) paradigms, and illustrate the answer with examples.
- **Answer:**
    - **Symbolic AI:** Focuses on encoding expert knowledge and logic into a system using rules and symbols. It's deterministic and interpretable but lacks flexibility and scalability. Example: Expert systems in medical diagnosis.
    - **Machine Learning:** Relies on learning patterns from data. It's adaptable and can handle complex tasks but often lacks interpretability. Example: Neural networks for image recognition.
    - **Contrast:** Symbolic AI is rule-based and rigid, while ML is data-driven and flexible. Symbolic AI excels in interpretability, whereas ML offers better performance in complex tasks.

#### Q4 b) Metric-Based Approaches in ML Performance Quantification

- **Question:** Discuss four metric-based approaches used to quantify the performance of an ML algorithm, one example being precision and recall.
- **Answer:**
    - **Precision and Recall:** Precision measures the accuracy of positive predictions, while recall measures the ability to find all positive instances.
    - **Accuracy:** The ratio of correctly predicted observations to the total observations.
    - **F1 Score:** The harmonic mean of precision and recall, providing a balance between the two.
    - **ROC-AUC:** Receiver Operating Characteristic curve and Area Under the Curve, measuring the ability to distinguish between classes.

#### Q4 c) Linear Perceptron Update Rule and Logical Gate

- **Question:** What is the update rule for a linear perceptron? Write the code for a perceptron with fixed weights w1 = w2 =1, and bias -0.5. Name the logical gate modeled by this perceptron.
- **Answer:**
- ![[Pasted image 20231214202909.png]]
- **Perceptron Code:**

def perceptron(x1, x2):
    w1, w2 = 1, 1  # Fixed weights
    bias = -0.5
    output = w1*x1 + w2*x2 + bias
    return 1 if output >= 0 else 0

- **Logical Gate Modeled:** This perceptron models an AND gate, outputting 1 only if both inputs are 1.