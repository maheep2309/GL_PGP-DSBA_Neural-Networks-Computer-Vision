# GL_PGP-DSBA_Neural-Networks-Computer-Vision
This project builds a deep-learning–based helmet detection system for workplace safety. It preprocesses images, evaluates multiple ANN/CNN/VGG16 models, and selects the best classifier to identify workers with or without helmets, improving real-time safety compliance and reducing manual monitoring errors.

# Project Summary
This project develops an automated image-classification solution to detect whether workers are wearing safety helmets—critical for reducing accidents in industrial and construction environments. The dataset contains 631 images across two classes: With Helmet and Without Helmet, captured under diverse lighting, angles, and work activities. The project begins with detailed EDA, class-balance checks, and visualization of sample images. Preprocessing includes RGB conversion, grayscale transformation, Gaussian blur, Laplacian filtering, normalization, and label encoding, followed by an 80-10-10 train-validation-test split.
Five deep learning models are built and evaluated using Accuracy, Recall, and Confusion Matrices, with Recall prioritized to avoid missing unsafe workers:
  1. Simple ANN (Flattened Images) – Learns basic patterns but shows overfitting and lower generalization.
  2. Simple ANN with Grayscale – Better balance and improved validation performance.
  3. Basic CNN – Strong feature extraction; achieves 100% metrics but may overfit due to small dataset.
  4. VGG-16 + FFNN (Transfer Learning) – Perfect performance on training and validation but still vulnerable to overfitting.
  5. VGG-16 + FFNN + Data Augmentation – Achieves consistently perfect accuracy and recall across train, validation, and test sets, with improved robustness to real-world variability.

Data augmentation (rotation, shifts, shear, zoom) greatly enhances the model’s generalization by simulating real-world noise from CCTV footage and outdoor sites. This makes Model 5 the most production-ready classifier.

Final recommendations include deploying the model as a real-time CCTV helmet-compliance system, running multi-site pilots, building ongoing feedback loops for retraining, adding dashboards for monitoring violations, and extending the framework to detect additional safety gear (vests, gloves, goggles). This positions SafeGuard Corp to automate risk monitoring and strengthen worker protection using AI-driven computer vision.
