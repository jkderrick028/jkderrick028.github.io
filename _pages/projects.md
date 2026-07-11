---
title: "Selected projects & publications"
permalink: /projects/
layout: single
author_profile: false
toc: false
---

## Individualized functional organization of the human prefrontal cortex

<div markdown="1" style="font-size: 0.8rem; line-height: 1.7;">

The human prefrontal cortex (PFC) supports a wide range of higher-order cognitive functions, including reasoning, decision making, planning, and cognitive control. While previous studies have emphasized large-scale functional gradients across the PFC, it remains unclear whether these gradients fully explain its organization or whether distinct functional boundaries also exist.

Using six richly sampled multi-task fMRI datasets, we developed individualized parcellation methods that reveal fine-grained functional subdivisions in each participant. We found that functional organization is highly individualized: group averaging largely recovers broad gradients but obscures sharp functional boundaries that are consistently observed within individuals. These individualized parcellations generalize across independent task sets and provide a more precise description of functional organization than conventional group atlases.

This work highlights the importance of individualized analyses for understanding higher-order cognition and provides new tools for studying the functional architecture of the human prefrontal cortex.

**Xiang et al. (2026)** Individualized parcellation reveals functional boundaries in human prefrontal cortex. *Nature Communications* (under review). [paper](https://www.biorxiv.org/content/10.64898/2026.07.04.736504v1)

<img
  src="/projects/pfc_parcellation/PFC_parcellation.jpg"
  alt="individualized_parcellation"
  style="display:block; margin:auto;"
  width="100%">

</div>


## Multitask representation in the prefrontal cortex 

<div markdown="1" style="font-size: 0.8rem; line-height: 1.7;">

The prefrontal cortex flexibly supports diverse cognitive functions, including working memory, decision making, and motor planning. Unlike sensory cortices, however, it remains unclear whether neurons are organized into meaningful topographic maps.

Using large-scale monkey electrophysiology recorded across multiple cognitive tasks, we investigate how neurons performing similar computations are spatially organized. Our work reveals task-specific topographic maps in the lateral prefrontal cortex, providing new insights into how multiple cognitive functions are implemented within the same neural circuitry.

**Xiang et al. (2025)** Toward task mapping of primate prefrontal cortex. *Neuropsychologia*. [paper](https://doi.org/10.1016/j.neuropsychologia.2025.109234)

**Xiang et al. (2025)** Task-specific topographic maps of neural activity in the primate lateral prefrontal cortex. *Journal of Neuroscience*. (under review) [paper](https://www.biorxiv.org/content/10.1101/2024.05.10.591729v2)

<img
  src="/projects/topoPFC/topo_maps.jpeg"
  alt="topo_maps"
  style="display:block; margin:auto;"
  width="50%">

</div>


## Multi-task batteries for precision functional mapping

<div markdown="1" style="font-size: 0.8rem; line-height: 1.7;">

Understanding how the human brain is functionally organized requires measurements that are both comprehensive and reliable. Conventional fMRI studies often rely on a small number of tasks, limiting the range of cognitive processes that can be investigated.

This work introduces a large-scale multi-task fMRI battery designed for precision functional mapping. By sampling diverse cognitive domains within the same individuals, the dataset enables detailed characterization of functional organization and provides a valuable resource for studying individual variability in human cognition.

**Arafat et al. (2026)** Multi-task batteries for precision functional mapping, *Nature Methods* (under review). [paper](https://www.biorxiv.org/content/10.64898/2026.03.20.713227v1.abstract)

<img
  src="/projects/multitask/multitask_battery.png"
  alt="topo_maps"
  style="display:block; margin:auto;"
  width="50%">

</div>


## Multi-task fMRI reveals task-invariant functional organization

<div markdown="1" style="font-size: 0.8rem; line-height: 1.7;">

Resting-state fMRI has become the standard approach for mapping functional organization in the human brain. But can actively performing diverse cognitive tasks provide an even clearer picture?

Using precision fMRI datasets collected across many cognitive tasks, this work demonstrates that multi-task fMRI more accurately recovers task-invariant functional organization than resting-state data alone. The findings suggest that integrating information across multiple task contexts provides a richer and more reliable characterization of the brain's intrinsic functional architecture.

**Nettekoven et al. (2026)** Multi-task fMRI outperforms resting-state fMRI for revealing task-invariant organization of the human brain. *Nature Neuroscience* (under review). [paper](https://www.biorxiv.org/content/10.64898/2026.03.09.710558v1.abstract)

<img
  src="/projects/multitask/task_invariant.png"
  alt="task_invariant"
  style="display:block; margin:auto;"
  width="100%">

</div>


## Compositional representation of tasks in human brain

<div markdown="1" style="font-size: 0.8rem; line-height: 1.7;">

Humans effortlessly perform multiple tasks and solve new tasks. Inspired by computational theories of compositional representations, we ask whether the human brain organizes task representations in a similarly compositional manner.

Using multi-task fMRI and representational analyses, we provide empirical evidence that task representations in the multiple-demand network can be explained by combinations of underlying sensory, cognitive, and motor components, supporting a compositional account of flexible cognition. 

Figure adapted from Yang et al. (2019). *Nature Neuroscience*

**Xiang et al. (2024)** Compositional representation of tasks in human multiple-demand cortex. *Organization for Human Brain Mapping*. [abstract](https://jkderrick028.github.io/assets/files/2024_OHBM_abstract_Xiang.pdf), [poster](https://jkderrick028.github.io/assets/files/20240623_OHBM_poster.pdf)

<div style="display:flex; align-items: center; gap: 1%">
<img src="/projects/compositional_coding/compositional_coding.jpg" alt="visual_nets" align='bottom' width="100%"/> 
</div>
</div>


## Model selection and inference 

<div markdown="1" style="font-size: 0.8rem; line-height: 1.7;">

Many studies partition explained variance among competing computational models, but standard variance partitioning methods can produce misleading or even negative estimates when predictors are correlated.

We develop a principled statistical framework for model selection and inference that avoids these pitfalls and provides more interpretable comparisons between competing models. The framework is broadly applicable across neuroscience and machine learning.

**Xiang et al. (2025)** Variance explained by different model components does not behave like a Venn diagram. *Cognitive Computational Neuroscience*. [abstract](https://2025.ccneuro.org/abstract_pdf/Xiang_2025_Variance_explained_different_model_components_behave.pdf), [poster](https://jkderrick028.github.io/assets/files/20250812_CCN_poster.pdf), [blog](https://diedrichsenlab.org/BrainDataScience/variance_partitioning/index.htm)

<img
  src="/projects/model_family/venn_diagram.jpg"
  alt="visual_nets"
  style="display:block; margin:auto;"
  width="50%">

</div>


## Comparing computer vision models vs. human visual perception

<div markdown="1" style="font-size: 0.8rem; line-height: 1.7;">

Deep neural networks have achieved remarkable success in computer vision, but do they process visual information in the same way as the human brain? In this project, we compare object representations learned by modern computer vision models with neural representations measured using human fMRI. By applying representational similarity analysis, we investigate which stages of visual processing are captured by artificial neural networks and where biological and artificial vision diverge. This work contributes to understanding the computational principles shared between deep learning models and the human visual system.

<img
  src="/projects/deepnets_RSA/visual_stream.png"
  alt="visual_nets"
  style="display:block; margin:auto;"
  width="80%">

</div>


## Behavioral inflexibility in addictions

<div markdown="1" style="font-size: 0.8rem; line-height: 1.7;">

Behavioral flexibility, the ability to adapt actions when the environment changes, is essential for goal-directed behavior and is often impaired in substance use disorders. Individuals with addiction may persist with previously rewarded behaviors even when better alternatives become available. Using a neural population coding framework, we investigated how changes in population representations could account for this behavioral inflexibility in an animal model of cocaine exposure. Our results provide a mechanistic link between altered neural representations in the prefrontal cortex and impaired adaptive decision making.

Figure adapted from Mueller et al. (2021). *Journal of Neuroscience* 

**Xiang et al. (2021)** Behavioral inflexibility from a neuronal population perspective. *Journal of Neuroscience* [paper](https://www.jneurosci.org/content/41/25/5350)

<img
  src="/projects/behavioural_inflexibility/Screenshot 2025-09-21 at 7.14.29 PM.png"
  alt="visual_nets"
  style="display:block; margin:auto;"
  width="80%">

</div>
