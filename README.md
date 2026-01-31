# Bayesian-Deep-Learning-for-Smart-Grid-Intrusion-Detection
📌 Project Overview
This project implements a Bayesian Convolutional Neural Network (B-CNN) designed to detect and discriminate cyber-physical intrusions within smart grid systems. Unlike traditional "black-box" AI, this approach utilizes Variational Inference to quantify predictive uncertainty.

In critical infrastructure like power grids, it is vital to distinguish between a malicious attack and a natural disturbance (noise/faults). This model provides a "Confidence Interval" for every prediction, allowing grid operators to ignore low-certainty alarms and prioritize high-certainty threats.

🚀 Key Features
- Convolutional Feature Engineering: 1D-CNN layers automatically extract temporal patterns from multivariate sensor data (Voltage/Current).

- Uncertainty Quantification: Uses DenseFlipout layers to provide a mean prediction and a standard deviation (variance).

- Intrusion Discrimination: Effectively separates known attack signatures from high-noise natural events using Bayesian Variance.

- Monte Carlo Sampling: Implements stochastic forward passes to approximate the true posterior distribution of the network weights.

🛠️ Tech Stack
- Language: Python

- Deep Learning: TensorFlow & Keras

- Probabilistic Programming: TensorFlow Probability (TFP)

- Data Science: NumPy, Pandas, Scikit-Learn

- Visualization: Matplotlib

📊 Mathematical FoundationThe model optimizes the Evidence Lower Bound (ELBO), balancing the log-likelihood of the data with the Kullback-Leibler (KL) Divergence:

<img width="670" height="79" alt="image" src="https://github.com/user-attachments/assets/8a96b855-8ad9-4ace-b9bc-116435ab8e87" />

This ensures the model is penalized for overconfidence, a critical safety feature for cyber-physical systems.

📈 Results & Visualization

- The system generates a time-series plot where:

- Blue Line: Represents the probability of an intrusion.

- Shaded Area: Represents the Uncertainty (95% Confidence Interval).

- Wide Shading: Indicates a "Natural Disturbance" or unknown state (Discrimination).
  
<img width="1156" height="548" alt="image" src="https://github.com/user-attachments/assets/d0fd423d-9934-4973-8484-c20a13ec8948" />


