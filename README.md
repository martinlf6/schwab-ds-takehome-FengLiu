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
