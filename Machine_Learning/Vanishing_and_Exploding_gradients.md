# Vanishing Gradient Problem
- The vanishing gradient problem occurs when the gradients become very small during backpropagation, causing the weights in earlier layers of the network to stop updating effectively.
- This often happens when using activation functions like sigmoid or tanh that squash the output into a small range, leading to gradients close to zero.
Vanishing Gradient Problem (Gradients become too small)
- How to solve:-
  - Use ReLU activation: ReLU (Rectified Linear Unit) helps avoid vanishing gradients because it doesn't squash values into a small range. For positive values, ReLU just passes them through.
  - Proper weight initialization:
    - Xavier/Glorot initialization for sigmoid/tanh layers.
    - He initialization for ReLU layers. This helps maintain the flow of gradients.
  - Gradient Clipping:
    - Clip the gradients if they become too small to ensure they are large enough for effective learning.
    - Gradient clipping is a technique used to prevent exploding gradients by limiting the size of gradients during backpropagation. If the gradients exceed a predefined threshold, they are scaled down to keep them within a manageable range. This ensures that the updates to the weights don’t become too large and destabilize training.

# Exploding Gradient Problem 
- The exploding gradient problem occurs when gradients grow very large during backpropagation, causing the model’s weights to become too large, which destabilizes the training process.
- How to solve it
  - Gradient Clipping:
    - Limit (clip) the size of gradients to prevent them from becoming too large, which helps stabilize training.
    - Gradient clipping is a technique used to prevent exploding gradients by limiting the size of gradients during backpropagation. If the gradients exceed a predefined threshold, they are scaled down to keep them within a manageable range. This ensures that the updates to the weights don’t become too large and destabilize training.
  Proper weight initialization:
  - Proper weight initialization
    - Same as for vanishing gradients, using Xavier/Glorot or He initialization helps avoid exploding gradients.
  - Use a smaller learning rate:
    - A smaller learning rate reduces the size of updates, preventing gradients from becoming too large.
  - Use Batch Normalization:
    - Helps stabilize training by normalizing the output of each layer, making gradients more manageable.
  - Use ReLU activation:
    - ReLU also helps in preventing gradients from exploding compared to sigmoid or tanh.
