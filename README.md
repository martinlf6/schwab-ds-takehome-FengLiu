# Cognitive AI – Aspect-Based Sentiment on Financial Text

## Overview
We analyzed financial text to generate advisor-ready insights using aspect-based sentiment analysis (ABSA) on the financial_phrasebank dataset. Our workflow included: (1) exploring the data, (2) extracting aspects (entities/features), and (3) fine-tuning finance-domain transformers for both sentence-level and aspect-level sentiment analysis, with aggregated insights supporting proactive client engagement.

## Dataset
- Hugging Face: `financial_phrasebank`.
- Labels: negative / neutral / positive.

## Approach
- **EDA**: label distributions, length stats, token frequencies.
- **Aspect extraction**: spaCy NER + noun-phrase rules for finance facets.
- **Models**:
  - Sentence sentiment (FinBERT).
  - Aspect–sentiment pair classifier `[CLS] sentence [SEP] aspect [SEP]`.
- **Evaluation**: Accuracy, macro-F1, precision, recall; slice metrics.

# Inference
## Key Findings
-	Class is imbalanced with much more neutral sentiment than positive which is more than negative.
-	Sentence model macro-F1: 0.96.
-	ABSA macro-F1: 0.99.
-	Frequent negative aspects: eur, profit, net, sales.
-	Positive aspects: eur, profit, net.

## Challenges & Limitations
-	Interpret results with caution due to the small sample size.
-	Dataset is sentence-level; ABSA labels are weakly supervised.
-	Future directions: expand sample size through synthetic data generation, incorporate human-in-the-loop labeling, and enhance aspect shifter handling (e.g., sentiment changes triggered by negations such as “not”).

## Ethics & Bias
-	Use with consent; minimize PII.
-	Monitor for coverage bias; keep advisor in the loop.
-	Provide transparent rationales for decisions.

## Results & Recommendations
See reports (e.g., Report_SentenceAnalysis.md) for detailed results (metrics) and advisor-facing recommendations.
