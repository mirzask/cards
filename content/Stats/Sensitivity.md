---
tags:
  - stats
aliases:
  - Recall
  - True Positive Rate
---
Related: [[Specificity]], [[Precision]]

$$
\text{Sensitivity} = \Pr(\text{+ test | +disease})
$$

- The sensitivity is the proportion of patients with the event that are classified as high risk

$$
\text{Sensitivity} = \text{Recall} = \text{TPR} = \frac{TP}{TP+FN}
$$
- Simple description: "how often is the prediction correct when positive value is predicted?"
- Worst value = 0; Best value = 1
- The sensitivity (aka true positive rate) is defined as $p(\text{test result} = 1|\text{actual event} = 1)$, i.e., the probability of a positive test given that the truth is positive.
- Sensitivity/Recall measures completeness—how many actual positives were predicted positives
- The **False Negative Rate** is defined as one minus the sensitivity, i.e. $\text{FNR} = 1 - \text{Sensitivity}$.
