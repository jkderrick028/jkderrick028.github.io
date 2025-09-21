---
title: "Projects"
permalink: /projects/
layout: single
author_profile: false
toc: false
---

## Multitask representation in the prefrontal cortex 
<div style="display:flex; align-items: center; gap: 1%">
<img src="/projects/topoPFC/topo_maps.jpeg" alt="topo_maps" align='left' width="50%"/> 

<div markdown="1">
The topographic maps reveal how neurons carrying out similar computations are organized in the brain. For instance, in the primary visual cortex, neurons preferring similar polar angles and eccentricities are organized in pin-wheel patterns, mapping the external world onto the visual cortex.  

How about the prefrontal cortex (PFC)? PFC supports multiple higher-order cognitive functions, such as working memory, decision making, and motor planning. PFC neurons flexibly adapt their activity according to rules, contextual associations and feedback. Do topographic maps exist in PFC as in visual regions? If so, how do they look like? How are different tasks inter-related in the brain? Addressing these questions will allow us to understand how our brain supports so many higher-order cognitive tasks flexibly. 

Xiang et al. (2025). Toward task mapping of primate prefrontal cortex. *Neuropsychologia*. [paper](https://doi.org/10.1016/j.neuropsychologia.2025.109234)

Xiang et al. (2025). Task-specific topographic maps of neural activity in the primate lateral prefrontal cortex. *Nature Communications*. (under review) [paper](https://www.biorxiv.org/content/10.1101/2024.05.10.591729v2)

</div>
</div>





## Compositional representation of tasks in human brain

<div style="display:flex; align-items: center; gap: 1%">
<img src="/projects/compositional_coding/compositional_coding.jpg" alt="visual_nets" align='left' width="50%"/> 
<div markdown="1">

The execution of complex cognitive tasks repeatedly activates an extensive networks of frontal and parietal regions, known as the multiple-demand (MD) system, whose distributed activity patterns carry information about the task. However, the functional organization of task representation remains unclear. Do certain tasks elicit more similar activity patterns than others? If so, what drives the functional organization? 

Computational work suggests that asks may be represented in a compositional fashion in PFC, where the representation of a task can be expressed as the algebraic sum of vectors representing the underlying sensory, cognitive and motor processes. Empirical evidence for compositional coding is limited. It remains to be tested if this principle generalizes to tasks that require context-dependent decisions. In this work, we provide empirical support for composition coding. 

Figure adapted from Yang et al., (2019) *Nature Neuroscience*

Xiang et al. (2024). Compositional representation of tasks in human multiple-demand cortex. *Organization for Human Brain Mapping*. [abstract](https://jkderrick028.github.io/assets/files/2024_OHBM_abstract_Xiang.pdf), [poster](https://jkderrick028.github.io/assets/files/20240623_OHBM_poster.pdf)

</div>
</div>



## Model selection and inference

<div style="display:flex; align-items: center; gap: 1%" class="math-container">
<img src="/projects/model_family/venn_diagram.jpg" alt="visual_nets" align='left' width="50%"/> 
<div markdown="1">

In the context of statistical modelling, one often comes across the idea of variance partitioning, which quantifies how variance of a variable can be explained by an experimental feature. The idea of variance partitioning in linear models goes back to Fisher's ANOVA (Fisher, 1925). The proportion of variance explained by a certain set of predictors is the value for that model. In the case of a balanced ANOVA, where $X_1$ and $X_2$ are orthogonal, the variance explained by the joint model that combines the two regressors ($R^2_{1\cup2}$) is the sum of the variance explained by each one alone ($R^2_{1}+R^2_{2}$) (panel a).

The trouble starts when we try to generalize this intuition to the more general case in which $X_1$ and $X_2$ are correlated (panel b). One of the problems is that the shared variance $R^2_{1\cap2}$ could go negative, due to suppression effect, which could render results uninterpretable or mislead conclusions. The explained variances for simple models and their combinations do not behave like a Venn-diagram. We propose a quantitative framework for model selection and inference.  


Xiang et al. (2025). Variance explained by different model components does not behave like a Venn diagram. *Cognitive Computational Neuroscience*. [abstract](https://2025.ccneuro.org/abstract_pdf/Xiang_2025_Variance_explained_different_model_components_behave.pdf), [poster](https://jkderrick028.github.io/assets/files/20250812_CCN_poster.pdf), [blog](https://diedrichsenlab.org/BrainDataScience/variance_partitioning/index.htm)

</div>
</div>


## Comparing computer vision models vs. human visual perception

<div style="display:flex; align-items: center; gap: 1%">
<img src="/projects/deepnets_RSA/visual_stream.png" alt="visual_nets" align='left' width="50%"/> 
<div markdown="1">

Computer vision models, such as deep neural networks, can achieve human-level performance in many tasks, e.g. visual classification. Do neural networks and human visual brain regions carry out similar computations? If two objects are represented similarly by a neural network, are they also represented similarly in human brain? 

</div>
</div>

