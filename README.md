# Cognitive AI – Aspect-Based Sentiment on Financial Text

## Overview
We analyze financial text to produce advisor-ready insights using **aspect-based sentiment analysis (ABSA)** on the `financial_phrasebank` dataset.
We (1) explore data, (2) extract aspects (entities/features), and (3) fine-tune finance-domain transformers for sentence and aspect sentiment, and aggregate insights for proactive client engagement.

## Dataset
- Hugging Face: `financial_phrasebank`.
- Labels: negative / neutral / positive.

## Approach
- **EDA**: label distributions, length stats, token frequencies.
- **Aspect extraction**: spaCy NER + noun-phrase rules for finance facets.
- **Models**:
  - Sentence sentiment (FinBERT).
  - Aspect–sentiment pair classifier `[CLS] sentence [SEP] aspect [SEP]`.
- **Evaluation**: Accuracy, macro-F1, precision, recall; slice metrics; qualitative error analysis.

# Inference
**Key Findings (sample)**
-	Class balance is [fill from EDA].
-	Sentence model macro-F1: [x.xx].
-	ABSA macro-F1 (validation pairs): [x.xx].
-	Frequent negative aspects: fees, guidance, outages.
-	Positive aspects: dividends, margins, cost control.

**Advisor-facing Recommendations**
-	Alert on spikes in negative aspect sentiment for covered holdings (30/60/90d).
-	Provide per-client aspect summaries (top concerns/interests).
-	Integrate ABSA signals into CRM with explainable highlights.

**Challenges & Limitations**
-	Dataset is sentence-level; ABSA labels partly weakly supervised.
-	Domain drift and entity coverage biases (large-cap skew).
-	Future work: human-in-the-loop labeling; improved aspect shifter handling; temporal models.

**Ethics & Bias**
-	Use with consent; minimize PII.
-	Monitor for coverage bias; keep advisor in the loop.
-	Provide transparent rationales for decisions.

**Results & Visuals**
See results/ for metrics, confusion matrices, and sample explanations.
