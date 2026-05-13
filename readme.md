# LW4_Improving-CNN-Performance

# Google Colab Link Here: https://colab.research.google.com/drive/1H3MNrrOFaJV_yaMGlZ3X1ASjrgpsooYo?usp=sharing

# GUIDE QUESTIONS (Student Explanation & Reflection)

# A. Model Evaluation Analysis

# 1. What were the weakest-performing classes based on the confusion matrix?
- The weakest-performing classes were artichoke, groundnut_peanut, hemp, ramie, and water_chestnut, as they showed lower recall and F1-scores in the confusion matrix. These classes were more frequently misclassified, indicating that the model struggled to distinguish them correctly.

# 2. How did Precision, Recall, and F1-score vary across classes?
- Precision, Recall, and F1-score varied significantly across classes. Some classes such as flax, cherry_tomatoes, saffron, and water_hyacinth achieved relatively high scores, while classes like artichoke, hemp, and groundnut_peanut had lower values due to frequent classification errors.

# 3. What does a low recall indicate in your model?
- A low recall indicates that the model failed to correctly identify many actual samples of a class. This means the model produced a higher number of false negatives, missing important instances during prediction.

# 4. How does AUC score reflect model performance compared to accuracy?
- The AUC score reflects the model’s ability to distinguish between classes across different thresholds, while accuracy only measures the percentage of correct predictions. In this model, the improved AUC score of 0.9117 suggests strong classification capability even though the accuracy was lower (52.95%).

# B. Model Improvement

# 5. How did data augmentation affect validation accuracy?
- Data augmentation aimed to improve validation accuracy by increasing the diversity of training images through transformations such as flipping, rotation, and zooming. However, in this case, validation accuracy decreased to around 52.95%, suggesting that the model struggled to generalize after modification.

# 6. Why is Batch Normalization important in CNNs?
- Batch Normalization is important because it stabilizes the learning process by normalizing layer inputs. It helps improve training speed, reduces sensitivity to initialization, and may improve model generalization.

# 7. What role did Dropout play in improving your model?
- Dropout helped reduce overfitting by randomly disabling neurons during training. This prevented the model from depending too much on specific features and encouraged better feature learning.

# 8. How did Early Stopping prevent overfitting?
- Early Stopping prevented overfitting by monitoring validation performance and stopping training when no further improvement was observed. This avoided excessive training that could reduce the model’s performance on unseen data.

# C. Performance Comparison

# 9. What improvements were observed after modifying the model?
- After modifying the model, additional techniques such as data augmentation, Batch Normalization, Dropout, and Early Stopping were introduced to improve generalization and reduce overfitting. However, performance decreased compared to the baseline model, with accuracy dropping from 98.82% to 52.95%.

# 10. Which enhancement contributed the most to performance improvement? Why?
- Among the enhancements, Early Stopping and Dropout contributed the most to preventing overfitting because they helped control excessive learning and improved generalization. However, the overall modifications did not outperform the baseline model in this experiment.

# 11. Did the gap between training and validation accuracy decrease? Explain.
- Yes, the gap between training and validation accuracy became more controlled due to regularization techniques. However, the model still showed signs of poor generalization since validation accuracy remained much lower than training accuracy.

# D. Explainability (Grad-CAM Integration)

# 12. How did Grad-CAM help in understanding model predictions?
- Grad-CAM helped in understanding model predictions by highlighting the image regions that influenced the model’s decision. It provided visual explanations of which crop features the model focused on during classification.

# 13. Did the improved model focus on more relevant regions? Provide evidence.
- The improved model showed attention to crop-related regions, but the focus was not always consistent. Evidence from the Grad-CAM heatmaps suggested that some predictions highlighted relevant plant structures, while weaker classifications focused on less meaningful areas, contributing to lower performance.

# 14. Why is explainability important in real-world AI applications?
- Explainability is important because it increases transparency and trust in AI systems. It helps users understand how decisions are made, detect possible errors or biases, and ensure reliable model behavior in real-world applications such as agriculture and healthcare.
