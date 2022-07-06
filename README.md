[![Licence](https://img.shields.io/github/license/So-Cool/IndividualFairness)](LICENCE)
[![Python](https://img.shields.io/badge/python-v3.8.2-blue)](https://github.com/So-Cool/IndividualFairness)

# Fairness and Ethics Under Model Multiplicity #

This repository holds Jupyter Notebooks that can be used to reproduce experimental results and plots included in the *[Fairness and Ethics Under Model Multiplicity][arxiv]* paper.

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

**Fairness and Ethics Under Model Multiplicity**

> While predictive models are a purely technological feat, they may operate in a social context in which benign engineering choices entail unexpected real-life consequences.
  Fairness -- pertaining both to individuals and groups -- is one of such considerations; it surfaces when data capture protected characteristics of people who may be discriminated upon these attributes.
  This notion has predominantly been studied for a fixed predictive model, sometimes under different classification thresholds, striving to identify and eradicate its undesirable behaviour.
  Here we backtrack on this assumption and explore a novel definition of fairness where individuals can be harmed when one predictor is chosen ad hoc from a group of equally well performing models, i.e., in view of model multiplicity.
  Since a person may be classified differently across models that are otherwise considered equivalent, this individual could argue for a model with a more favourable outcome, possibly causing others to be adversely affected.
  We introduce this scenario with a two-dimensional example based on linear classification; then investigate its analytical properties in a broader context; and finally present experimental results on data sets popular in fairness studies.
  Our findings suggest that such unfairness can be found in real-life situations and may be difficult to mitigate with technical measures alone, as doing so degrades certain metrics of predictive performance.

[arxiv]: https://arxiv.org/abs/2203.07139
[openml]: https://docs.openml.org/Python-guide/
