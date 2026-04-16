# LW5_Comparative-Analysis-of-Pre-trained-CNN-Models-for-Custom-Image-Classification

---

### Google Colab Link: https://colab.research.google.com/drive/1hCnTACVf2xuoun13sY_XLnMiO9Xuj8c2?usp=sharing

--- 

# Performance Comparison Table


| Model - Sample | Train Accuracy | Train Loss | Test Accuracy | Test Loss | Precision | Recall | F1-score | ROC | AUC |
| -------------- | -------------- | ---------- | --------------| --------- | --------- | ------ | -------- | --- | --- |
| Pre-Trained    |                |            |
| Model 1 (VGG16)|                |            |
| -------------- | -------------- | ---------- | --------------| --------- | --------- | ------ | -------- | --- | --- |
| Pre-Trained    |                |            |
| Model 2        |                |            |
| (ResNet50)     |                |            |
| -------------- | -------------- | ---------- | --------------| --------- | --------- | ------ | -------- | --- | --- |
| Pre-Trained    |                |
| Model 3        |                |
| (MobileNet V2) |                |
| -------------- | -------------- | ---------- | --------------| --------- | --------- | ------ | -------- | --- | --- |
| Model from     |                |
| Teachable      |                |
| Machine        |                |
| -------------- | -------------- | ---------- | --------------| --------- | --------- | ------ | -------- | --- | --- |
| Your 1st Model |                |
| -------------- | -------------- | ---------- | --------------| --------- | --------- | ------ | -------- | --- | --- |
| Your 2nd Model |                |
| Enhancement    |                |
| -------------- | -------------- | ---------- | --------------| --------- | --------- | ------ | -------- | --- | --- |
| Your 3rd Model |                |
| The Good Model |                |
| -------------- | -------------- | ---------- | --------------| --------- | --------- | ------ | -------- | --- | --- |

# GUIDE QUESTIONS (FINAL REFLECTION)

## A. Model Performance
**1. Which pre-trained model achieved the highest accuracy? Why?**

The pre-trained model that achieved the highest accuracy is the one that was able to classify the images most correctly among all tested models. This may be because its architecture is deeper or more effective in extracting important    image features such as edges, textures, and shapes. It may also have better generalization because it was already trained on a large dataset before fine-tuning on your own dataset.

**2. Which model had the lowest performance? What could be the reason?**

The model with the lowest performance is the one with the smallest accuracy and weaker evaluation scores. Possible reasons include limited ability to capture complex image patterns, underfitting, overfitting, insufficient training time, poor hyperparameter settings, or difficulty adapting to your dataset.

**3. How did loss values compare across models?**

Loss values show how far the model’s predictions are from the actual labels. A model with lower validation loss generally performed better because it made fewer errors during prediction. If one model had low training loss but high validation loss, this may indicate overfitting.

---

## B. Evaluation Metrics
**4. Why is accuracy not enough to evaluate a model?**

Accuracy alone is not enough because it only shows the overall percentage of correct predictions. It does not explain whether the model performs well for each class. In cases of imbalanced datasets, a model may achieve high accuracy while still performing poorly on minority classes.

**5. Which model had the best F1-score? What does it indicate?**

The model with the best F1-score is the one that had the best balance between precision and recall. A high F1-score indicates that the model not only predicts correctly but also avoids too many false positives and false negatives. This means the model is more reliable in classification tasks.

**6. How did Precision and Recall differ across models?**

Precision measures how many predicted positive results were actually correct, while recall measures how many actual positive cases were successfully identified. Some models may have higher precision but lower recall, meaning they are more careful but may miss some true cases. Others may have higher recall but lower precision, meaning they detect more positives but also produce more false alarms.

---

## C. Confusion Matrix Analysis
7. Which classes were frequently misclassified?

The classes that were frequently misclassified are usually those with similar visual features. These classes may share similar colors, textures, or shapes, making it difficult for the model to distinguish between them.

8. What patterns did you observe in the confusion matrix?

The confusion matrix may show that some classes were predicted correctly most of the time, while others were often confused with visually related classes. This suggests that the model learned certain categories well but struggled with classes that had overlapping characteristics.

--- 

## D. ROC and AUC
9. Which model had the highest AUC score?

The model with the highest AUC score is the one that best separated the classes across different threshold settings. This means it was more effective in distinguishing positive from negative predictions.

10. What does AUC tell us about model performance?

AUC, or Area Under the Curve, measures the model’s ability to discriminate between classes. A higher AUC means better classification performance because the model is more capable of ranking correct classes above incorrect ones. It gives a broader view of performance than accuracy alone.

---

## E. Explainability (Grad-CAM)
11. What did Grad-CAM reveal about model decision-making?

Grad-CAM revealed which parts of the image influenced the model’s prediction the most. It helps explain whether the model focused on meaningful regions or irrelevant background areas when making decisions.

12. Did the model focus on relevant image regions?

If the heatmaps highlighted the main object or important image features, then the model focused on relevant regions. However, if the heatmaps emphasized background areas or unimportant details, it may suggest weak decision-making or bias in the model.

13. Which model produced the most meaningful heatmaps?

The model that produced the most meaningful heatmaps is the one whose Grad-CAM visualizations clearly highlighted the correct object or important parts of the image. This indicates stronger interpretability and more trustworthy predictions.

---

F. Model Comparison & Improvement
14. Which model would you recommend for deployment? Why?

The model I would recommend for deployment is the one with the best overall performance based on accuracy, F1-score, AUC, and confusion matrix results. It should also produce meaningful Grad-CAM heatmaps, because this shows that it is not only accurate but also interpretable and reliable.

15. How can you further improve your best-performing model?

The best-performing model can still be improved by increasing the dataset size, applying better data augmentation, tuning hyperparameters, adjusting learning rate, adding regularization techniques like dropout, using class balancing methods, or training for more epochs with early stopping.

---

## G. Real-World Application
16. How can your model be applied in real-world scenarios?

This model can be applied in real-world scenarios such as image-based classification systems in healthcare, agriculture, security, education, manufacturing, or mobile applications. It can help automate decision-making, improve efficiency, and reduce manual work.

17. What are the risks of deploying an inaccurate model?

Deploying an inaccurate model can lead to wrong predictions, poor decisions, reduced trust from users, and possible harm depending on the application. For example, in medical or safety-related tasks, incorrect predictions may have serious consequences.

18. How can this system be integrated into a mobile/web app?

This system can be integrated into a web application, mobile app, or desktop system through a trained model API. The user uploads an image, the system processes it, predicts the class, and then displays the result together with confidence scores or Grad-CAM visualizations for explanation.
