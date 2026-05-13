# LW4_Improving-CNN-Performance

# Google Colab Link Here: https://colab.research.google.com/drive/1H3MNrrOFaJV_yaMGlZ3X1ASjrgpsooYo?usp=sharing

# GUIDE QUESTIONS (Student Explanation & Reflection)

# A. Model Evaluation Analysis

# 1. What were the weakest-performing classes based on the confusion matrix?
- The weakest-performing classes were those with the highest number of misclassifications in the confusion matrix. These classes showed lower prediction accuracy because the model frequently confused them with other categories, indicating difficulty in distinguishing similar features.

# 2. How did Precision, Recall, and F1-score vary across classes?
- Precision, Recall, and F1-score varied among classes depending on how well the model recognized each category. Some classes achieved high scores, indicating strong classification performance, while weaker classes had lower scores due to false positives and false negatives.

# 3. What does a low recall indicate in your model?
- A low recall indicates that the model failed to correctly identify many actual positive samples. This means the model produced a higher number of false negatives, missing important instances during classification.

# 4. How does AUC score reflect model performance compared to accuracy?
- The AUC score reflects the model’s ability to distinguish between classes across different threshold values, while accuracy only measures the percentage of correct predictions. A high AUC score suggests better classification capability even if accuracy alone appears moderate.



# B. Model Improvement

# 5. How did data augmentation affect validation accuracy?
- Data augmentation improved validation accuracy by increasing the diversity of training data. Techniques such as image rotation, flipping, and zooming helped the model generalize better and reduced overfitting.

# 6. Why is Batch Normalization important in CNNs?
- Batch Normalization is important because it stabilizes and speeds up the training process by normalizing input values between layers. It also helps improve model performance and reduces sensitivity to weight initialization.

# 7. What role did Dropout play in improving your model?
- Dropout helped improve the model by randomly disabling neurons during training, preventing the network from relying too heavily on specific features. This reduced overfitting and improved generalization performance.

# 8. How did Early Stopping prevent overfitting?
- Early Stopping prevented overfitting by monitoring validation performance and stopping training once improvement stopped. This avoided excessive learning from training data that could reduce model performance on unseen data.


# C. Performance Comparison

# 9. What improvements were observed after modifying the model?
- After modifying the model, improvements were observed in accuracy, precision, recall, and F1-score. The model also showed better generalization performance and fewer classification errors.

# 10. Which enhancement contributed the most to performance improvement? Why?
- Data augmentation contributed the most to performance improvement because it exposed the model to more diverse training samples, allowing it to learn more robust features and reduce overfitting.

# 11. Did the gap between training and validation accuracy decrease? Explain.
_ Yes, the gap between training and validation accuracy decreased after modifications. This indicates that the model generalized better and experienced less overfitting, resulting in more consistent performance on unseen data.


# D. Explainability (Grad-CAM Integration)

# 12. How did Grad-CAM help in understanding model predictions?
- Grad-CAM helped in understanding model predictions by highlighting important regions of the image that influenced the model’s decision. This visualization made it easier to interpret how the model classified images.

# 13. Did the improved model focus on more relevant regions? Provide evidence.
- Yes, the improved model focused on more relevant regions. Grad-CAM visualizations showed stronger attention to significant image areas related to the target class, while irrelevant background regions received less focus.

# 14. Why is explainability important in real-world AI applications?
- Explainability is important because it increases transparency and trust in AI systems. It helps users understand model decisions, identify errors or biases, and ensure reliable performance in critical applications such as healthcare and security.
