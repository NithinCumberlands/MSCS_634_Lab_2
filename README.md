# KNN_RNN_Classifier_Lab_2

## Purpose
In this lab, I evaluated the performance of K-Nearest Neighbors (KNN) and Radius Neighbors (RNN) classifiers on the Wine dataset from scikit-learn. My goal was to examine how varying **k** in KNN and the **radius** in RNN affects classification accuracy, and to understand the influence of these parameters on each model’s performance.

## Key Findings
- **KNN:** Accuracy was highest with very small **k** (around 1) and then stabilized as **k** increased. I observed a notable drop in accuracy for **k** below 5, followed by incremental improvements at larger **k** values.
- **RNN:** Model performance was extremely sensitive to the radius choice. Once the radius exceeded approximately 400 (after feature scaling), accuracy fell sharply and remained low for larger radii. The optimal radius was about 350.

## Challenges
- **Radius Tuning for RNN:** Because RNN accuracy depended so heavily on the search radius, finding the optimal value required extensive trial and error. Radii that were too large included distant points and degraded performance, while radii that were too small left too few neighbors.
- **KNN Variability at Low k:** Low **k** values led to overfitting, whereas very high **k** values risked oversmoothing. Striking the right balance to avoid both over- and underfitting was crucial.
