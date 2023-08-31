---
layout: page
title: Projects
permalink: /projects/
description: A collection of projects, software, etc. that I think is worth showcasing.
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

Slide decks I presented in previous reading clubs.

- Temporal Parallelization of Bayesian Smoothers, August 2023 ([Slides](../assets/pdf/Temporal_Parallelization_of_Bayesian_Smoothers-20230804.pdf))
- Reinforcement Learning via Fenchel-Rockafellar Duality, January 2023 ([Slides](../assets/pdf/RL_via_FR_duality-20230126.pdf))
- A brief review on over-smoothing in GNNs, May 2021 ([Slides](../assets/pdf/GNN_Oversmoothing-20210504.pdf))
- Kernel Instrumental Variable Regression, May 2020 ([Slides](../assets/pdf/kernel_instrumental_variable_regression-20200515.pdf))


## Mentoring and advising

I provide mentorship and advice to aspiring Japanese students interested in STEM education and careers abroad sometimes (though not very frequently).

<details>
  <summary>
    "Tips for studying and working abroad for Japanese students" (<a href="https://github.com/kstoneriv3/tips-for-studying-and-working-abroad-ja">posts on github</a>)
  </summary>
  <p style="margin-left: 5%;"> 
  I wrote a series of "things I wish I knew when I was 18" type of posts. There are significantly fewer Japanese compared to other groups (such as Chinese and Koreans) in the Western STEM field. This underrepresentation is partly due to a scarcity of information available in Japanese, so posts like these could be helpful. Indeed, they turned out to be quite popular and got close to 100 stars on github ⭐ (but even more popular than any of my software 🥲)!
  </p>
</details>

<details>
  <summary>
    Mentorship in application document writing
  </summary>
  Occasionally I support aspiring Jananese students in writing application documents such as motivation letters for grad school or scholarship.</li>
</details>



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
