# Noise-Robust Non-Negative Matrix Factorization (NMF) for Image Processing

## Project Overview
This project focuses on evaluating the robustness of **Non-Negative Matrix Factorization (NMF)** algorithms when applied to image datasets contaminated by various types of noise. The goal is to compare the performance of three NMF algorithms—**\(L_{2}\)-NMF**, **Cauchy-NMF**, and **Huber-NMF**—on two real-world face image datasets: **ORL** and **Extended YaleB (CroppedYaleB)**. The datasets are contaminated with **Gaussian noise**, **salt and pepper noise**, and **block occlusion noise** to simulate real-world noise conditions. The project aims to identify which NMF algorithm performs best under different noise scenarios, providing insights into the robustness of these algorithms for image processing tasks.

## Key Features
- **NMF Algorithms**: Implement and compare three NMF algorithms:
  - **\(L_{2}\)-NMF**: Traditional NMF using the Frobenius norm, suitable for Gaussian noise.
  - **Cauchy-NMF**: Robust to extreme outliers and heavy-tailed noise using the Cauchy loss function.
  - **Huber-NMF**: Balances robustness and efficiency using the Huber loss function, effective for salt and pepper noise and block occlusion.
- **Noise Types**: Introduce three types of noise to simulate real-world image corruption:
  - **Gaussian Noise**: Simulates sensor noise during image acquisition.
  - **Salt and Pepper Noise**: Simulates bit errors during transmission or conversion.
  - **Block Occlusion Noise**: Simulates large occlusions in images.
- **Datasets**: Evaluate the algorithms on two face image datasets:
  - **ORL Dataset**: 400 images of 40 subjects, resized to 46×56 pixels.
  - **CroppedYaleB Dataset**: 2414 images of 38 subjects, resized to 42×48 pixels.
- **Evaluation Metrics**: Use **Root Mean Square Error (RMSE)**, **Average Accuracy (Acc)**, and **Normalized Mutual Information (NMI)** to compare the performance of the algorithms.

## Technical Details
- **Programming Language**: Python 3
- **Preprocessing**: Normalize image data using Min-Max Scaling to improve numerical stability and convergence.
- **Noise Generation**: Implement custom noise generation functions for Gaussian, salt and pepper, and block occlusion noise.
- **Evaluation**: Perform 10-fold cross-validation to ensure robust performance evaluation, reporting mean and standard deviation of metrics.

## Project Tasks
1. **Data Preprocessing**: Normalize the ORL and CroppedYaleB datasets using Min-Max Scaling.
2. **Noise Introduction**: Contaminate the datasets with Gaussian, salt and pepper, and block occlusion noise.
3. **NMF Implementation**: Implement \(L_{2}\)-NMF, Cauchy-NMF, and Huber-NMF algorithms from scratch.
4. **Performance Evaluation**: Evaluate the algorithms using RMSE, Acc, and NMI metrics on both datasets.
5. **Results Analysis**: Compare the robustness of the algorithms under different noise conditions and draw conclusions.

## Results and Discussion
- **\(L_{2}\)-NMF**: Performs well under Gaussian noise but struggles with salt and pepper and block occlusion noise.
- **Cauchy-NMF**: Shows robustness to extreme outliers and heavy-tailed noise, performing slightly better than \(L_{2}\)-NMF in block occlusion scenarios.
- **Huber-NMF**: Excels in handling salt and pepper and block occlusion noise, outperforming both \(L_{2}\)-NMF and Cauchy-NMF in these conditions. However, it underperforms under Gaussian noise.
- **Overall**: The choice of NMF algorithm should be tailored to the specific noise conditions of the dataset.

## Acknowledgments
This project was developed as part of the **COMP5328 - Advanced Machine Learning** course, focusing on the robustness of NMF algorithms in noisy environments. The goal is to provide insights into the practical application of NMF in real-world image processing tasks, where noise is a common challenge.

## Future Work
- Explore more robust NMF variants such as **Truncated Cauchy NMF** and **Cauchy-balanced NMF**.
- Investigate **Deep NMF**, which combines NMF principles with deep learning architectures, to enhance the capability of NMF in handling complex noise and outliers.
