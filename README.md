
# **DeepSense: Gaussian Anomaly Detection**

## **Overview**

This project implements an **unsupervised anomaly detection system** using a **Gaussian probability model**. The goal is to identify data points that deviate significantly from the expected statistical pattern. By modeling each feature with its mean and variance, the algorithm calculates how likely each observation is under a normal distribution. Points with extremely low probabilities are flagged as anomalies.

This method is efficient, interpretable, and widely used for detecting irregularities in real-world systems such as sensor data, transaction records, or network logs.

---

## **How It Works**

1. **Estimate Gaussian Parameters:**
   The model computes the mean (`μ`) and variance (`σ²`) of each feature based on training data representing normal behavior.

2. **Compute Anomaly Probabilities:**
   It uses the multivariate Gaussian distribution to calculate the likelihood of each new data point.

3. **Select Threshold (ε):**
   A threshold value for the probability is chosen using a validation set to maximize the F1 score. Any observation with a probability below this threshold is considered an anomaly.

4. **Detect and Visualize Anomalies:**
   Once trained, the system can identify outliers in unseen data and visualize their position relative to normal patterns.

---

## **Why This Is Fascinating**

What makes this project truly exciting is its real-world relevance, especially in **cybersecurity**. The same statistical approach can be applied to detect **unusual activity on computer networks**: a sudden spike in traffic, an unexpected access pattern, or behavior that doesn’t match historical data. Because the method doesn’t require labeled attack examples, it can spot *new, unseen threats* in real time.

This blend of **machine learning and security** showcases how simple mathematical principles, like the Gaussian distribution, can evolve into powerful tools for protecting digital systems.



