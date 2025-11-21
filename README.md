# QR Decomposition for Handwriting Recognition

This repository examines **handwriting recognition task** on **EMNIST Letters** dataset using **QR decomposition** .
## Project Overview

* **Dataset Preparation:**
  For each class, the first 200 samples are used as training data, forming a data matrix for that class. An additional 20 samples per class are used as a test set to evaluate the model's performance.

* **Part 1 – QR Decomposition with Householder Matrices:**

  * Construct the data matrix for each class using the training samples.
  * Compute the **QR decomposition** of the matrix using **Householder transformations**.
  * Solve the least squares problem to predict labels for the test data and evaluate model performance.

* **Part 2 – Incremental QR Decomposition with Givens Rotations:**

  * Simulate adding 20 new samples per class incrementally, equivalent to appending columns to the data matrix.
  * Instead of recomputing the QR decomposition from scratch, update it using **Givens rotations**.
  * Solve the updated least squares problem to predict test labels and compare results with the previous method.

This project demonstrates how QR decomposition can be applied both in **batch and incremental learning scenarios** for handwriting recognition task.
