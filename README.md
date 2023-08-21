# finding-funny-scene-using-Reinforcement-learning
Step 1: The proposed RL framework leverages a pre-trained CNN facial expression embedding model alongside an affective information encoding vector. These components are used to generate embeddings for input data.

Step 2: The DQN (Deep Q-Network) model takes in the embeddings produced in the previous step as inputs. It predicts Q-values for all possible actions.

Step 3: Among the predicted Q-values, the action associated with the highest Q-value is chosen. This selected action corresponds to a one-hot encoding vector.

Step 4: The chosen action is utilized to construct an affective information encoding vector, which is then passed on for the next iteration.

Step 5: The reward function is established using a function called H. This function calculates rewards based on the consensus of frame-level outcomes up to the present time step.

Step 6: The magnitude of the reward significantly influences the convergence of training. A balanced ratio between reward values for intermediate and terminal steps is determined.

Step 7: In the context of this application, specific values are assigned for Rinter (±0.05) and Rend (±1) to serve as rewards.

Step 8: A positive reward is assigned when the action output matches the true label, indicating agreement between predicted and actual values.

Step 9: Conversely, a negative reward is given when there's a disparity between the predicted and actual label
