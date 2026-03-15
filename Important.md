Sure! Here are simple examples for each classification metric using a **spam email detector** scenario. This will help you remember what each metric measures and when to use it.

---

### 1. Accuracy  
**What it measures:** Overall correctness – how many emails were classified correctly (spam as spam, non-spam as non-spam).  

**Example:**  
Out of 100 emails, the model correctly identifies 90 as spam and 5 as non-spam, but it misclassifies 3 spam as non-spam and 2 non-spam as spam.  
Accuracy = (90 + 5) / 100 = **95%**.

---

### 2. Precision  
**What it measures:** Of the emails flagged as spam, how many are *actually* spam? (Avoids false alarms.)  

**Example:**  
Model flags 50 emails as spam. 45 of them are truly spam, 5 are legitimate.  
Precision = 45 / 50 = **90%**.

---

### 3. Recall (Sensitivity)  
**What it measures:** Of all actual spam emails, how many did the model catch? (Avoids missing spam.)  

**Example:**  
There are 60 actual spam emails. The model correctly flagged 45 of them, but missed 15.  
Recall = 45 / 60 = **75%**.

---

### 4. F1-Score  
**What it measures:** The harmonic mean of precision and recall – a single score balancing both.  

**Example:**  
Precision = 90%, Recall = 75%  
F1 = 2 × (0.9 × 0.75) / (0.9 + 0.75) ≈ **0.818** (or 81.8%).

---

### 5. ROC-AUC  
**What it measures:** How well the model separates spam from non-spam across all possible decision thresholds.  

**Example:**  
The model assigns a spam probability score to each email. If you randomly pick one spam and one non-spam, the spam has a higher score 95% of the time.  
AUC = **0.95** → excellent discrimination.

---

### 6. Log Loss (Cross-Entropy Loss)  
**What it measures:** How confident and correct the predicted probabilities are. Penalizes confident wrong predictions more.  

**Example:**  
For a spam email, the model predicts 90% probability of spam. That’s good – log loss contribution is small. But if it had predicted only 40% for the same spam, the penalty would be much larger.  
Lower log loss = better calibrated probabilities.

---

### 7. Confusion Matrix  
**What it measures:** A table showing all four prediction outcomes: True Positives, False Positives, False Negatives, True Negatives.  

**Example (100 emails):**  

|                | Predicted Spam | Predicted Not Spam |
|----------------|----------------|---------------------|
| **Actual Spam**   | 45 (TP)        | 15 (FN)             |
| **Actual Not Spam** | 5 (FP)         | 35 (TN)             |

This gives a quick visual of where the model goes wrong.

---

### 8. Specificity (True Negative Rate)  
**What it measures:** Of all legitimate (non-spam) emails, how many are correctly identified as non-spam?  

**Example:**  
There are 40 legitimate emails. The model correctly labels 35 as non-spam and mistakenly marks 5 as spam.  
Specificity = 35 / 40 = **87.5%**.

---

### 9. Cohen’s Kappa  
**What it measures:** Agreement between predictions and actual labels, adjusted for the agreement that could happen by chance.  

**Example:**  
The model has 80% accuracy, but since spam is common, random guessing might get 50% accuracy.  
Kappa = (0.80 – 0.50) / (1 – 0.50) = **0.60** → moderate agreement beyond chance.

---

These examples should help you recall each metric's purpose and calculation. Choose the one that best fits your problem's goals and class balance!
