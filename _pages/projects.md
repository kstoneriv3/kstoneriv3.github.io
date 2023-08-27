---
layout: page
title: Projects
permalink: /projects/
description: A random collection of projects, softwares, ... etc. that I think is worth showcasing.
nav: true
nav_order: 2
display_categories: []
horizontal: false
---
<!-- display_categories: [work, fun] -->

This page is under construction...

## Mini-research projects

Mini research projects that did not end up publication so far.

- Fake voice detection
- Low-rank GP on discrete domain
- Non-linear Debiasing of Sentence Embeddings with Kernel PCA ([code](https://github.com/kstoneriv3/debiasing-bert-by-kernel-pca), [report](https://github.com/kstoneriv3/debiasing-bert-by-kernel-pca/blob/main/final_report.pdf))
  - with Vincent Bardenhagen
- Can Higher-Order Monte Carlo Methods Help Reinforcemenet Learning? ([code](https://github.com/kstoneriv3/autonomous-learning-library-with-rrpg), [report](https://github.com/kstoneriv3/autonomous-learning-library-with-rrpg/blob/main/Can%20Higher-Order%20Monte%20Carlo%20Methods%20Help%20Reinforcemenet%20Learning%3F.pdf))
  - Unrelated to my work but this paper seems to be a more sensible way to use QMC in RL: [Policy Learning and Evaluation with Randomized Quasi-Monte Carlo](https://arxiv.org/pdf/2202.07808.pdf).
- MLQMC for neural SDEs
- An SDE analysis of the sharpness-aware minimization


## Softwares

- confounding-robust-inference
- pca-impute
- imputax

- PRs to OSS
  - scikit-learn
  - optuna
  - scipy


## Reading club

Slide decks I presented in reading clubs in the past.

- Temporal Parallelization of Bayesian Smoothers, August 2023 ([Slides](../assets/pdf/Temporal_Parallelization_of_Bayesian_Smoothers-20230804.pdf))
- Reinforcement Learning via Fenchel-Rockafellar Duality, January 2023 ([Slides](../assets/pdf/RL_via_FR_duality-20230126.pdf))
- A study of oversmoothing in GNNs, May 2021 ([Slides](../assets/pdf/GNN_Oversmoothing-20210504.pdf))
- Kernel Instrumental Variable Regression, May 2020 ([Slides](../assets/pdf/kernel_instrumental_variable_regression-20200515.pdf))


## Notes

- https://github.com/kstoneriv3/tips-for-studying-and-working-abroad-ja

<!---
<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
