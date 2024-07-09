[![Licence](https://img.shields.io/github/license/So-Cool/CrossModelFairness)][licence]
[![Python](https://img.shields.io/badge/python-v3.8.2-blue)][code]
[![View Notebooks](https://img.shields.io/badge/view-notebooks-orange.svg?logo=jupyter)][notebooks]  
[![Read Paper ACM](https://img.shields.io/badge/ACM-10.1145/3677173-violet)][acm]
[![Read Paper arXiv](https://img.shields.io/badge/arXiv-10.48550/arXiv.2203.07139-green.svg?logo=arxiv)][arxiv]

# Cross-model Fairness: Empirical Study of Fairness and Ethics Under Model Multiplicity #

This repository holds Jupyter Notebooks to reproduce experimental results and
plots from the
*[Cross-model Fairness: Empirical Study of Fairness and Ethics Under Model Multiplicity][acm]*
paper published in the *ACM Journal on Responsible Computing*.

## Code ##

[![Licence](https://img.shields.io/github/license/So-Cool/CrossModelFairness)][licence]
[![Python](https://img.shields.io/badge/python-v3.8.2-blue)][code]
[![View Notebooks](https://img.shields.io/badge/view-notebooks-orange.svg?logo=jupyter)][notebooks]

The experiments have been executed with Python 3.8.2.
The packages and their versions are captured by the `requirements.txt` file
(`pip install -r requirements.txt`).
Accessing OpenML requires an [API token][openml].
This can either be set up directly in the [`openml.ipynb`][nb-openml]
Jupyter Notebook or placed in a BASH variable named
`OPENML_APIKEY` (`export OPENML_APIKEY=myOpenmlAPIkey`).
The following notebooks are provided:

* [`toy_plots.ipynb`][nb-toy] -- generates *toy example* plots.
* [`openml.ipynb`][nb-openml] -- fetches data from *OpenML*.
* [`plot_profile.ipynb`][nb-plot] -- plots *fairness profiles*.
* [`ambiguity.ipynb`][nb-ambiguity] -- computes and graphs
  *ambiguity* and *discrepancy*.
* [`fair_model.ipynb`][nb-fair] -- analyses performance of
  *individually fair* models.

> Note that downloading experiments from OpenML may take a long time given that
they are made available as a large number of relatively small files
(roughly 10GB in total).

## Paper ##

[![Read Paper ACM](https://img.shields.io/badge/ACM-10.1145/3677173-violet)][acm]
[![Read Paper arXiv](https://img.shields.io/badge/arXiv-10.48550/arXiv.2203.07139-green.svg?logo=arxiv)][arxiv]

**Cross-model Fairness: Empirical Study of Fairness and Ethics Under Model Multiplicity**

*Abstract:*

> While data-driven predictive models are a strictly technological construct,
  they may operate within a social context in which benign engineering choices
  entail implicit, indirect and unexpected real-life consequences.
  Fairness of such systems -- pertaining both to individuals and groups -- is
  one relevant consideration in this space;
  algorithms can discriminate people across various *protected* characteristics
  regardless of whether these properties are included in the data or discernible
  through proxy variables.
  To date, this notion has predominantly been studied for a *fixed* model, often
  under different classification thresholds, striving to identify and eradicate
  undesirable, discriminative and possibly unlawful aspects of its operation.
  Here, we backtrack on this fixed model assumption to propose and explore a
  novel definition of *cross-model fairness* where individuals can be harmed
  when one predictor is chosen ad hoc from a group of equally well performing
  models, i.e., in view of utility-based *model multiplicity*.
  Since a person may be classified differently across models that are otherwise
  considered equivalent, this individual could argue for a predictor granting
  them the most favourable outcome, employing which may have adverse effects on
  other people.
  We introduce this scenario with a two-dimensional example and linear
  classification;
  then, we present a comprehensive empirical study based on real-life predictive
  models and data sets that are popular with the algorithmic fairness community;
  finally, we investigate analytical properties of cross-model fairness and its
  ramifications in a broader context.
  Our findings suggest that such unfairness can be readily found in real life
  and it may be difficult to mitigate by technical means alone as doing so is
  likely to degrade predictive performance.

*Keywords:* Rashomon effect, epistemic uncertainty, robustness,
machine learning, artificial intelligence.

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
  imposing appropriate modelling *restrictions* that are consistent with the
  social context and the natural process governing the generation of the
  underlying data, as well as to employ a *justified* prediction aggregation
  strategy across classifiers with identical or comparable performance.

*Citation:*

```bibtex
@article{sokol2024cross,
  title={Cross-model Fairness:
         {Empirical} Study of Fairness and Ethics Under Model Multiplicity},
  author={Sokol, Kacper and Kull, Meelis and Chan, Jeffrey and Salim, Flora},
  journal={ACM Journal on Responsible Computing},
  publisher={ACM New York, NY},
  doi={10.1145/3677173},
  year={2024}
}
```

[licence]: https://github.com/So-Cool/CrossModelFairness/blob/master/LICENCE
[code]: https://github.com/So-Cool/CrossModelFairness
[notebooks]: https://github.com/So-Cool/CrossModelFairness/tree/master/notebooks
[arxiv]: https://arxiv.org/abs/2203.07139
[acm]: https://doi.org/10.1145/3677173
[doi]: https://doi.org/10.1145/3677173
[openml]: https://docs.openml.org/integrations/apikey/
[nb-openml]: https://github.com/So-Cool/CrossModelFairness/blob/master/notebooks/openml.ipynb
[nb-toy]: https://github.com/So-Cool/CrossModelFairness/blob/master/notebooks/toy_plots.ipynb
[nb-plot]: https://github.com/So-Cool/CrossModelFairness/blob/master/notebooks/plot_profile.ipynb
[nb-ambiguity]: https://github.com/So-Cool/CrossModelFairness/blob/master/notebooks/ambiguity.ipynb
[nb-fair]: https://github.com/So-Cool/CrossModelFairness/blob/master/notebooks/fair_model.ipynb
