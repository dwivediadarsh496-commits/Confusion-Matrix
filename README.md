Introduction
The Confusion Matrix is a tool used to evaluate the performance of classification models.

What is a Confusion Matrix?
It is a table that compares:

Actual values
Predicted values
Main Terms
True Positive (TP): Correct positive prediction
True Negative (TN): Correct negative prediction
False Positive (FP): Wrong positive prediction
False Negative (FN): Wrong negative prediction
Why is it Important?
Accuracy alone can be misleading. Confusion Matrix helps calculate:

Precision
Recall
F1-Score
Example
In disease prediction:

TP → Sick person correctly identified
FN → Sick person predicted as healthy
Conclusion
Confusion Matrix gives a clear picture of model performance and is very important in real-world applications.

code
import numpy as np

Download the Medium app
from sklearn.metrics import confusion_matrix

import seaborn as sns

pv = np.array([“dog”,”dog”,”dog”,”dog”,”not dog”,”not dog”])

av = np.array([“dog”,”dog”,”dog”,”dog”,”not dog”,”not dog”])

c = confusion_matrix(pv,av)

sns.heatmap(c , annot = True , xticklabels=[“dog”,”not dog”],

yticklabels=[“dog”,”not dog”])

output
# Confusion-Matrix
