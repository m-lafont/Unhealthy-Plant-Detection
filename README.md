# Unhealthy-Plant-Detection

## Overview
The Unhealthy Plant Detection project was developed as part of the Artificial Neural Networks and Deep Learning (AN2DL) course for the 2023-2024 academic year. The goal was to create a binary classification model to distinguish between healthy and unhealthy plants based on image data.

This project utilizes a fine-tuned EfficientNet B0 model with extensive preprocessing and data augmentation techniques to achieve high classification accuracy. The work was conducted by a team of students leveraging transfer learning, advanced preprocessing, and optimization strategies.

---

## Features
- **Binary Classification**: Classifies images as "healthy" or "unhealthy".
- **Transfer Learning**: Uses EfficientNet B0 for high performance on a small dataset.
- **Data Augmentation**: Includes cutout, mixup, color jittering, and transformations (flipping, zooming, etc.).
- **Optimization Techniques**: Fine-tuning with AdamW optimizer, batch normalization, and early stopping.
- **Performance Tracking**: Evaluation through metrics like accuracy and confusion matrices.

---

## Project Structure
- **`notebooks/Unhealthy_Plant_Detection.ipynb`**: Main Jupyter notebook containing code for data preprocessing, model training, evaluation, and visualization.
- **`report/Unhealthy_Plant_Detection_Report.pdf`**: Detailed report outlining methodology, experiments, and results.

The data was not uploaded due to its size.

---

## Dataset
The dataset contains 5,200 images of plants labeled as "healthy" or "unhealthy". Preprocessing steps include:
1. **Normalization**: Scaling pixel values to [0,1].
2. **Outlier Removal**: Identifying and removing images with incorrect content using MobileNet.
3. **Duplicate Removal**: Ensuring unique entries in the dataset.
4. **Data Splitting**: Training set (67%) and validation set (33%).

Post-cleaning, the dataset comprises:
- Training images: 3,227
- Validation images: 1,614

---

## Methodology
1. **Model Architecture**:
   - EfficientNet B0 with a dropout layer to reduce overfitting.
   - Fine-tuning of the last 4 blocks for improved accuracy.

2. **Data Augmentation**:
   - Cutout, mixup, and color jittering on the training set.
   - Random flipping, zooming, translation, and rotation applied during training.

3. **Training Parameters**:
   - Optimizer: AdamW
   - Batch size: 70
   - Max epochs: 250 (with early stopping, patience = 45)
   - Learning rate adjustments during fine-tuning.

---

## Results
- **Validation Accuracy**: 89.17% (after duplicate removal).
- **Test Accuracy (Codalab)**: 78.5%.
- **Confusion Matrix Analysis**: Higher accuracy for healthy plants, reflecting dataset imbalance.

---

## Future Improvements
- Implement cross-validation.
- Adjust decision thresholds based on ROC analysis.
- Use advanced augmentation techniques during testing.
- Experiment with larger EfficientNet models or alternative architectures.

---

## Acknowledgments
We thank Professors Boracchi and Matteucci for their lectures and Eugenio Lomurno for his laboratory support.

---

## References
1. Giacomo Boracchi - Famous CNN Architectures and Visualization
2. Yixing Fu - EfficientNet Fine-tuning (Keras Example)
3. Eugenio Lomurno - AN2DL Logbook

