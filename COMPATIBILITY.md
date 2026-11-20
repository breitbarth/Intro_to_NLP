# Notebook Compatibility Review

Source review: November 20, 2026. This was a code-reading review, not an end-to-end notebook execution. Multiple notebook copies remain; start with `intro_to_nlp_workshop.ipynb`.

| Observed call or dependency | Current migration direction | Verification still needed |
| --- | --- | --- |
| Vectorizer `.get_feature_names()` | Use `.get_feature_names_out()` and account for its array output | Check downstream display and indexing |
| `metrics.plot_roc_curve` | Use `RocCurveDisplay.from_estimator` or `.from_predictions` | Verify positive class and score inputs |
| `metrics.plot_precision_recall_curve` | Use `PrecisionRecallDisplay.from_estimator` or `.from_predictions` | Verify positive class and score inputs |
| TensorFlow Datasets, Gensim, Natural Language Toolkit, and optional downloaded review data | Select a supported, pinned environment and document required downloads | Test access and runtime together before claiming a reproducible run |

The old plotting functions were deprecated in scikit-learn 1.0 and removed in 1.2. Feature-name access also changed. The migration directions above are a modernization backlog; the historical notebook files have not been edited here.

Primary references: [scikit-learn 1.0 changes](https://scikit-learn.org/1.0/whats_new/v1.0.html), [historical ROC plotting deprecation](https://scikit-learn.org/1.1/modules/generated/sklearn.metrics.plot_roc_curve.html), and [historical precision–recall plotting deprecation](https://scikit-learn.org/1.1/modules/generated/sklearn.metrics.plot_precision_recall_curve.html).
