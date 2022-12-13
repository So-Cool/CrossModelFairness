[![Licence](https://img.shields.io/github/license/So-Cool/IndividualFairness)](LICENCE)
[![Python](https://img.shields.io/badge/python-v3.8.2-blue)](https://github.com/So-Cool/IndividualFairness)

# Fairness and Ethics Under Model Multiplicity in Machine Learning #

This repository holds Jupyter Notebooks that can be used to reproduce experimental results and plots included in the *[Fairness and Ethics Under Model Multiplicity in Machine Learning][arxiv]* paper.

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

**Fairness and Ethics Under Model Multiplicity in Machine Learning**

> While data-driven predictive models are a strictly technological construct,
  they may operate within a social context in which benign engineering choices
  entail implicit, indirect and unexpected real-life consequences.
  Fairness of such systems -- pertaining both to individuals and groups -- is
  one relevant consideration in this space; it surfaces when data capture
  *protected* characteristics upon which people may be discriminated.
  To date, this notion has predominantly been studied for a *fixed* predictive
  model, often under different classification thresholds, striving to identify
  and eradicate undesirable, and possibly unlawful, aspects of its operation.
  Here, we backtrack on this assumption to propose and explore a novel
  definition of fairness where individuals can be harmed when one predictor is
  chosen ad hoc from a group of equally-well performing models, i.e., in view of
  utility-based *model multiplicity*.
  Since a person may be classified differently across models that are otherwise
  considered equivalent, this individual could argue for a predictor with the
  most favourable outcome, employing which may have adverse effects on others.
  We introduce this scenario with a two-dimensional example based on linear
  classification; then, we investigate its analytical properties in a broader
  context; and, finally, we present experimental results on data sets that are
  popular in fairness studies.
  Our findings suggest that such unfairness can be found in real-life situations
  and may be difficult to mitigate by technical means alone, as doing so
  degrades certain metrics of predictive performance.

*Keywords:* individual fairness, ethics, model view, model multiplicity,
Rashomon effect, machine learning, artificial intelligence,
automated decision-making.

*Highlights:*

- Utility-based individual fairness guarantees that a person receives the same
  prediction across a collection of models with identical or comparable
  predictive performance.
- When at least one prediction output by multiple equivalent models for a single
  individual is perceived as favourable, the person might argue for the
  precedence of this outcome.
- This notion of fairness is consistent with the Blackstone's ratio and
  "presumption of innocence" -- lack of convincing evidence ought to warrant the
  most favourable treatment.
- Granting each person the most favourable decision afforded by a collection of
  equivalent models may degrade the overall predictive performance on the
  underlying task, especially when the employed family of models is highly
  expressive.
- A possible solution is to limit the number of admissible predictors by
  imposing appropriate modelling restrictions, which are consistent with the
  social context and the natural process governing the generation of the
  underlying data.

[arxiv]: https://arxiv.org/abs/2203.07139
[openml]: https://docs.openml.org/Python-guide/
