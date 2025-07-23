# A Perplexity-Based Analysis of Translation Artifacts in XNLI

### Proposed Study: 

This study examines whether untranslated English terms (e.g., "NASA") and culture-specific concepts (e.g., "Thanksgiving") in XNLI’s non-English splits introduce biases when evaluating multilingual models, particularly for low-resource languages. The study hypothesise that such terms increase sentence perplexity (PPL) in target languages, artificially inflating model difficulty.

### Method:

- **Data**: Extract Chinese XNLI dev sentences with untranslated English tokens (experimental group) vs. fully translated sentences (control group).

- **Metric**: Compute PPL for both groups using a pretrained Chinese LM (e.g., `bert-base-chinese`).

- **Analysis**: Compare mean PPL (`Welch’s t-test`) and (if necessary) visualize distributions. _*If time permits, repeat for a low-resource language (e.g., Hindi)._

### Expected Outcomes:

- Higher PPL in experimental group → Untranslated terms degrade data quality.

- Stronger effect in low-resource languages → XNLI may underestimate model performance for these languages.

- Significance: Highlights potential biases in cross-lingual benchmarks and suggests filtering strategies for fairer evaluation.

- Feasibility: Minimal coding (regex + HF Transformers), 1-2 experiments.

