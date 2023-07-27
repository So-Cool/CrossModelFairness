[![Licence](https://img.shields.io/github/license/So-Cool/CrossModelFairness)](LICENCE)
[![Python](https://img.shields.io/badge/python-v3.8.2-blue)](https://github.com/So-Cool/CrossModelFairness)

# Cross-model Fairness: Empirical Study of Fairness and Ethics Under Model Multiplicity #

This repository holds Jupyter Notebooks that can be used to reproduce experimental results and plots included in the *[Cross-model Fairness: Empirical Study of Fairness and Ethics Under Model Multiplicity][arxiv]* paper.

## Code ##

[![View Notebooks](https://img.shields.io/badge/view-notebooks-orange.svg?logo=jupyter)](notebooks)

The experiments have been executed with Python 3.8.2.
The packages and their versions are captured by the `requirements.txt` file (`pip install -r requirements.txt`).
Accessing OpenML requires an [API token][openml].
This can either be set up directly in the [`openml.ipynb`](notebooks/openml.ipynb) Jupyter Notebook or placed in a BASH variable named `OPENML_APIKEY` (`export OPENML_APIKEY=myOpenmlAPIkey`).
The following notebooks are provided:

* [`toy_plots.ipynb`](notebooks/toy_plots.ipynb) -- generates *toy example* plots.
* [`openml.ipynb`](notebooks/openml.ipynb) -- fetches data from *OpenML*.
* [`plot_profile.ipynb`](notebooks/plot_profile.ipynb) -- plots *fairness profiles*.
* [`ambiguity.ipynb`](notebooks/ambiguity.ipynb) -- computes and graphs *ambiguity* and *discrepancy*.
* [`fair_model.ipynb`](notebooks/fair_model.ipynb) -- analyses performance of *individually fair* models.

> Note that downloading experiments from OpenML may take a long time given that they are made available as a large number of relatively small files (roughly 10GB in total).

## Paper ##

[![Read Paper](https://img.shields.io/badge/read-paper-green.svg?logo=arxiv)][arxiv]

**Cross-model Fairness: Empirical Study of Fairness and Ethics Under Model Multiplicity**

> While data-driven predictive models are a strictly technological construct,
  they may operate within a social context in which benign engineering choices
  entail implicit, indirect and unexpected real-life consequences.
  Fairness of such systems -- pertaining both to individuals and groups -- is
  one relevant consideration in this space; it arises when data capture
  *protected* characteristics upon which people may be discriminated.
  To date, this notion has predominantly been studied for a *fixed* model, often
  under different classification thresholds, striving to identify and eradicate
  undesirable, discriminative and possibly unlawful aspects of its operation.
  Here, we backtrack on this assumption to propose and explore a novel
  definition of *cross-model fairness* where individuals can be harmed when one
  predictor is chosen ad hoc from a group of equally-well performing models,
  i.e., in view of utility-based *model multiplicity*.
  Since a person may be classified differently across models that are otherwise
  considered equivalent, this individual could argue for a predictor granting
  them the most favourable outcome, employing which may have adverse effects on
  others.
  We introduce this scenario with a two-dimensional example and linear
  classification; then, we present a comprehensive empirical study based on
  real-life predictive models and data sets that are popular with the
  algorithmic fairness community; finally, we investigate analytical properties
  of cross-model fairness and its ramifications in a broader context.
  Our findings suggest that such unfairness can be readily found in the real
  life and it may be difficult to mitigate by technical means alone as doing
  so is likely to degrade predictive performance.

*Keywords:* Rashomon effect, machine learning, artificial intelligence.

*Highlights:*

- Cross-model fairness guarantees that a person receives the same prediction
  for a collection of classifiers with identical or comparable predictive
  performance, i.e., under utility-based model multiplicity.
- When at least one prediction output by multiple equivalent models for
  a single individual is perceived as favourable, the person might argue
  for the precedence of this outcome.
- Cross-model fairness is consistent with the Blackstone's ratio and
  "presumption of innocence" -- lack of convincing evidence ought to warrant
  the most favourable treatment.
- Granting each person the most favourable decision afforded by a collection
  of equivalent models may degrade the overall predictive performance on the
  underlying task, especially when the employed family of models is highly
  expressive.
- A possible solution is to limit the number of admissible predictors by
  imposing appropriate modelling restrictions that are consistent with the
  social context and the natural process governing the generation of the
  underlying data.

[arxiv]: https://arxiv.org/abs/2203.07139
[openml]: https://docs.openml.org/Python-guide/
