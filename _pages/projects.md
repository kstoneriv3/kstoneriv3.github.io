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


## Publication

Please refer to the <a href="../publications">Publication</a> section.

<br>


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

<br>


## Softwares

<div style="margin-left: 2%;"> 

  <details>
    <summary>
      confounding-robust-inference (<a href="https://github.com/kstoneriv3/confounding-robust-inference">code</a>,
      <a href="https://github.com/kstoneriv3/confounding-robust-inference">documentation</a>)
    </summary>
    <p style="margin-left: 3%;">
      Slightly over-engineered code for our paper <a href="https://github.com/kstoneriv3/confounding-robust-inference">A Convex Framework for Confounding Robust Inference</a>, from which I learned how to properly set up a python package, CI/CD, a test suite, and documentation.
    </p>
  </details>
  
  <details>
    <summary>
      pca-impute (<a href="https://github.com/kstoneriv3/pca-impute">code</a>)
    </summary>
    <p style="margin-left: 3%;">
      A simple but fast missing value imputation with iterative PCA (i.e. iterative SVD) with a scikit-learn style API.
    </p>
  </details>
  
  <details>
    <summary>
      imputax (<a href="https://github.com/kstoneriv3/imputax">code</a>)
    </summary>
    <p style="margin-left: 3%;">
      Bayesian missing value imputation with the probabilistic PCA and the factor model, implemented in Jax.
    </p>
  </details>
  
  <details>
    <summary>
      OSS contributions
    </summary>
    <p style="margin-left: 3%;"> 
      <ul>
        <li>scikit-learn
          (A bug fix for kernel PCA, <a href="https://github.com/scikit-learn/scikit-learn/pull/19732">#19732</a>.)</li>
        <li>Scipy(A bug fix for LatinHypercubes, <a href="https://github.com/scipy/scipy/pull/13654">#13654</a>.)</li>
        <li>Optuna
          (Add multivariate TPE sampler, <a href="https://github.com/optuna/optuna/pull/1767">#1767</a>.
          Add QMC sampler, <a href="https://github.com/optuna/optuna/pull/2423">#2423</a>.
          Support batched sampling with BoTorch <a href="https://github.com/optuna/optuna/pull/4591">#4591</a>.)</li>
      </ul>
    </p>
  </details>

</div>

<br>


## Reading club

Slide decks I presented in previous reading clubs.

<div style="margin-left: 2%;"> 
  
  <details>
    <summary>
      "Temporal Parallelization of Bayesian Smoothers", presented on August 2023 (<a href="../assets/pdf/Temporal_Parallelization_of_Bayesian_Smoothers-20230804.pdf">slides</a>)
    </summary>
    <p style="margin-left: 3%;"> 
      This paper improves the parallel complexity of Baysian filtering and smoothing from O(n) (of the traditional forward-backward algorithm) to O(log n), which is a quite striking result.
    </p>
  </details>

  <details>
    <summary>
      "Reinforcement Learning via Fenchel-Rockafellar Duality", presented on January 2023 (<a href="../assets/pdf/RL_via_FR_duality-20230126.pdf">slides</a>)
    </summary>
    <p style="margin-left: 3%;"> 
      A summary of the DICE (stationary DIstribution Correction Estimation) techniques in offline RL. The stationary distribution for a fix policy is known to become the solution of a linear operator equation, and they provide a sysmetatic recipe to solve this equation using convex duality.
    </p>
  </details>

  <details>
    <summary>
      "Kernel Instrumental Variable Regression", presented on May 2020 (<a href="../assets/pdf/kernel_instrumental_variable_regression-20200515.pdf">slides</a>)
    </summary>
    <p style="margin-left: 3%;"> 
      An extension of the classic linear instrumental variable regression with the kernel methods. One of the pioneering causal ML papers that "kernelized" the classic linear methods for causal inference. An interesting technical point is that their method involves learning a linear operator from a feature space of a kernel to a feature of another kernel, which is not very trivial but is still feasible analytically.
    </p>
  </details>

  <details>
    <summary>
      "A brief review on over-smoothing in graph neural networks", presented on May 2021 (<a href="../assets/pdf/GNN_Oversmoothing-20210504.pdf">slides</a>)
    </summary>
    <p style="margin-left: 3%;"> 
      The over-smoothing in graph neural networks (GNNs) is a phenomena where a GNN's performance degrades when the GNNs becomes too deep. I summarized the up-to-date theoretical insights and proposed solutions as of early 2021. In theory, the oversmoothing was attributed to the spectral decay due to the incremental application of the same message passing operator, analogous to the power iteration. Proposed solutions at the time were either residual skip connection or sparsification of the message passing, to reduce the spectral decay of the operator.
    </p>
  </details>

</div>

<br>

## My two cents on career and academics

I sometimes provide mentorship/advice to aspiring students (mostly Japanese) interested in STEM education/careers abroad and I've written a few articles on these topics, which turned out to be quite popular.

<div style="margin-left: 2%;"> 
  
  <details>
    <summary>
      "Tips for studying and working abroad for Japanese students" (<a href="https://github.com/kstoneriv3/tips-for-studying-and-working-abroad-ja">posts on github</a>)
    </summary>
    <p style="margin-left: 3%;"> 
      I wrote a series of "things I wish I knew when I was 18" type of posts. There are significantly fewer Japanese compared to other groups (such as Chinese and Koreans) in the Western STEM field. 
      This underrepresentation is partially due to a scarcity of information available in Japanese, so posts like these could be helpful. 
      Indeed, they attracted a considerable level of engagement and got nearly 100 stars on github ⭐ (but even more popular than any of my software 🥲)!
    </p>
  </details>

</div>


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
