# Introduction to Natural Language Processing

**Stage: workshop notebooks and learning material.** Explore how text becomes numerical features and how a sentiment classifier is evaluated.

## Process

Normalize text, split it into tokens, examine stop words and word forms, then convert documents into feature vectors. For the movie-review example, split the data, fit the vectorizer on training text, train logistic regression, and evaluate on held-out reviews. The notebook also contains optional lexicon-based sentiment exploration.

## Problem

Raw language is not directly usable by a conventional classifier. Cleaning and representation choices affect which information remains. Evaluation can also become misleading if the test set influences feature learning. The workshop makes these choices visible in a small learning workflow.

## Example

The notebook uses Internet Movie Database (IMDb) reviews for sentiment classification. Word counts and term frequency–inverse document frequency (TF-IDF) show different ways to represent a review. Logistic regression then predicts the review label from its features. This is a learning example; no live customer-feedback product or newly measured accuracy is claimed.

## Impact

The material connects text preparation with classification and several ways to assess errors. The intended benefit is understanding the tradeoffs in a text-analysis pipeline. Business value and production behavior remain untested; full notebook execution was not part of this review.

## Confirm

**Learning question:** Can the learner explain which text transformations were applied, why the vectorizer is fit only on training data, and what precision and recall reveal?

**Review evidence:** source was inspected on November 20, 2026. Older scikit-learn calls require updates before a current run-all claim is appropriate; see [compatibility notes](COMPATIBILITY.md). A future rerun should record versions, dataset availability, the held-out split, and actual metrics.

## Relevant features

| Existing feature | What it teaches |
| --- | --- |
| Tokenization, stop words, stemming, and lemmatization | Makes text-normalization choices explicit |
| Count and TF-IDF representations | Shows how documents become numerical inputs |
| Training-only vectorizer fit | Keeps held-out text out of feature learning |
| Logistic regression and classification metrics | Connects features with predictions and error analysis |
| Receiver operating characteristic and precision–recall curves | Compares performance across thresholds |
| Optional sentiment lexicon exercise | Introduces a different sentiment-analysis approach |

## Open the material

Begin with [intro_to_nlp_workshop.ipynb](intro_to_nlp_workshop.ipynb); its Colab link is embedded in the file. Professor and copy versions remain in the repository and have not been consolidated or audited for equivalence. A current dependency environment is not pinned here.

The workshop credits Galvanize and Andrew Means. Those credits are retained. The next useful improvement is a reproducible modern run of one clearly selected notebook.
