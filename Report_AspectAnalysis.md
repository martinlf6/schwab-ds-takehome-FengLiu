# Classification Report
This shows precision, recall, F1-score, and support for each class.
## Negative (43 samples)
-	Precision = 0.91: When predicting negative, 91% are correct.
-	Recall = 0.95: Of all true negative cases, 95% are captured.
-	F1-score = 0.93: Balance between precision & recall especially when dealing with imbalanced datasets. Strong performance
## Neutral (34 samples)
-	Precision = 1.00: Every time the model predicts neutral, it’s correct.
-	Recall = 0.97: Of all true netural cases, 97% are captured.
-	F1-score = 0.99: Very strong performance
## Positive (59 samples)
- Precision = 0.95: When predicting positive, 95% are correct (5% false positives).
-	Recall = 0.93: Of all true positive cases, 93% are captured.
-	F1-score = 0.94: Strong performance
## Overall Metrics
-	Accuracy = 0.95: Out of all 136 test samples, 95% are correct.
-	Macro avg = averages metrics equally across classes F1 = 0.95
-	Weighted avg = averages weighted by class size F1 = 0.95
## Key Takeaways
-	The model performs exceptionally well (95% accuracy, F1 = 0.95 across all classes).
-	Overall balance is strong, meaning class imbalance is not hurting performance much.

# Business/Real-World Interpretation
## Why These Metrics Matter in Business Context?
### Negative Class (Customer complaints, risk alerts, bad financial news)
-	Recall = 0.95: The model catches 95% of negatives, only misses 5%.
-	Business impact: Missing a negative (false negative) could mean overlooking a serious issue (e.g., financial risk, compliance violation, or customer dissatisfaction).
-	In risk-sensitive industries (finance, insurance, healthcare), high recall is crucial. Would rather flag too many negatives than miss one.
### Neutral Class (Normal or uninformative content)
-	Precision = 1.00, Recall = 0.97: The model is almost perfect here.
-	Business impact: Neutral predictions are low risk. If the model mistakes a few, it doesn’t matter much since these don’t trigger critical business actions.
### Positive Class (Opportunities, good sentiment, positive financial signals)
-	Precision = 0.95, Recall = 0.93: The model catches 93% of positives, and misses 7%..
-	Business impact: If this model is used for market sentiment or customer engagement, then missing positives (false negatives) could mean overlooking opportunities (e.g., happy customers you could upsell).
## Metric Priorities Depend on Use Case
### If used for risk detection (fraud, complaints):
-	Maximize recall for negatives, better to catch every possible negative, even if some are false alarms.
### If used for opportunity mining (marketing, investments, client engagement):
-	Maximize recall for positives, and do not miss many good opportunities.
### If used for overall sentiment monitoring (balanced insights):
-	The current model is well-balanced: 95% accuracy, F1 = 0.95 across classes means it’s strong enough for dashboards, analytics, and trend reporting.
## Summary in Business Terms:
-	The model is excellent overall.
-	For general analytics, this model is already production-ready.

