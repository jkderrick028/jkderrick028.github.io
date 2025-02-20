---
title: "Projects"
permalink: /projects/
layout: single
author_profile: false
toc: false
---


## Task-specific topographic maps in primate lateral prefrontal cortex (LPFC) 

The topographic maps in visual cortex are commonly used to describe how neurons with similar response preferences to stimulus features, such as eccentricities (Brewer et al. 2002), polar angles (Fang et al. 2022), and object categories (Bell et al. 2009), are organized. They provide information on how the external world is represented in the brain. These maps extend multiple spatial scales and are largely independent of internal mental state. 

How about LPFC? LPFC supports multiple higher-order cognitive functions, such as working memory, decision making, and motor planning. LPFC neurons flexibly adapt their activity according to rules, contextual associations and feedback. For instance, the same neuron may have different response preferences to objects and locations depending on whether the subject is doing an object task or a location task. Another way of phrasing it is that LPFC neurons exhibit selectivity to mixtures of task features (instead of to simple low-level stimulus features like early sensory regions do). 

Do topographic maps exist in LPFC as in sensory regions? If so, how do they look like? Are they similar or different across tasks? What's the spatial scale? 

Addressing these questions will allow us to understand how LPFC neurons performing similar computations are organized, as well as how LPFC supports so many higher-order cognitive functions flexibly. 

<figure>
<img src="/projects/topoPFC/maps.jpg" align="center" style="width:100%">
<figcaption>Topographic maps in primate visual regions. Figures adapted from Brewer et al 2002, Fang et al 2022, Bell et al 2019. </figcaption>
</figure>

[[paper](https://www.biorxiv.org/content/10.1101/2024.05.10.591729v1)][[code](https://github.com/jkderrick028/topoPFC)]


<details markdown="1">
<summary>
Read more
</summary>


Because of the adaptive coding and mixed selectivity, the topographic maps should naturally extend from those in visual cortex, and reflect how neurons with similar responses to combinations of task features (a.k.a the tuning profiles) are organized. 

Such topographic maps in LPFC do exist and are adaptive across tasks. In addition, the maps are organized at a fine-grained spatial scale that resembles the long-range afferent input patterns into LPFC. The fine-grained topographic maps are potentially resolvable by advanced neuroimaging techniques in humans and allow for examining a systematically manipulated task space.  

<figure>
<img src="/projects/topoPFC/4_spatial-scale-maps.jpg" align="center" style="width:100%">
<figcaption>
a) Spatial autocorrelation functions (ACFs) for 3 tasks (oculomotor delayed response, visuospatial working memory, context-dependent decision making). Solid lines represent the ACFs for individual sessions in each task. Colors indicate arrays: light blue for mB ventral array, dark blue for mB dorsal array, and pink for mT ventral array. Gray shaded areas indicate the width between two immediately neighboring channels on the array (0.4 mm). Vertical dashed lines show the median full-width-at-half-maximum (FWHM) of Laplacian functions fit to ACFs of individual sessions.

b) Steps taken to visualize tuning similarity on the array. Channels with similar tuning profiles in a given task are similarly colored. The multi-electrode arrays are of 4 mm $\times$ 4 mm coverage, 10 $\times$ 10 electrodes.   
    
c) Array maps for the mB dorsal array in all three tasks, using two example sessions per task.

d) Array maps in panel c after smoothing with 2D Gaussian kernels whose FWHMs match that of the fitted Laplacian functions. 
</figcaption>
</figure>

</details>


## Comparing the representational similarity of objects in human brain and deep neural networks

Deep neural networks can achieve human-level performance in visual classification tasks. I'm curious about if two objects are represented differently by a neural network, are they also represented differently in human brain? In other words, are deep neural networks good candidates for studying how human brain represents visual objects? 

In this post, I'm presenting a toy project where I compare the representational similarity of objects in human brain regions and deep convolutional neural networks (using AlexNet as an example).  

<figure>
<img src="/projects/deepnets_RSA/visual_stream.png" align="center" style="width:60%">
</figure>

[[code](https://github.com/jkderrick028/interp_deepnets/blob/main/demo.ipynb)]

<details markdown="1">
<summary>
Read more
</summary>

### Stimuli 

* 16 manmade objects 
* 16 words describing these objects 

<figure>

<img src="/projects/deepnets_RSA/stimuli.jpg" class="center">

</figure>


### fMRI data 

The participants were asked to maintain fixation while these images were displayed at the centre of fixation, on a uniform grey background, at a width of 9⁰ of visual angle. 

* 32 stimuli -> 32 conditions
* stimulus duration = 500 ms
* 12 trials per condition
* 14 subjects
* whole-brain coverage
* voxel size = 3 mm isotropic 	
* regions of interests (ROIs)

<figure>

<img src="/projects/deepnets_RSA/ROIs.png" class="center">
<figcaption>Regions of interest</figcaption>

</figure>

### Representational similarity analysis (RSA)

Each element of the representational dissimilarity matrix (RDM) reflects the differences in responses across all voxels elicited by a pair of conditions. By definition, the RDM is symmetrical and the diagonals should be zeros (responses elicited by the same condition should be the same). 

Here is an example RDM for V1, averaged across subjects. Each element of the matrix reflects how different V1 responds to a pair of stimuli. The first half of the stimuli are images of objects. The latter half are words describing these objects. We can normalize the RDM using the min and max so that the values are between 0 and 1. The more different V1 respond to a pair of stimuli, the higher the dissimilarity value is and color-coded yellow. The more similar V1 respond to a pair of stimuli, the lower the dissimilarity value is and color-coded blue. 

As we can see, the words tend to elicit similar response in V1. These responses are different when subjects are viewing images of objects. 

<figure>
<img src="/projects/deepnets_RSA/RDMs_V1.jpg" class="center" style="width:50%">
<figcaption>RDM for V1 averaged across subjects</figcaption>
</figure>

These are the RDMs for all ROIs, averaged across subjects. As we can see, the representational structure tend to be clearer in low-level visual regions than higher-order cognitive regions such as IPS and IFJ.  

<figure>

<img src="/projects/deepnets_RSA/RDMs_brain.jpg" class="center">
<figcaption>RDMs for all the ROIs, averaged across subjects</figcaption>

</figure>


Similarly we can compute the RDMs for different layers of AlexNet. 


<figure>

<img src="/projects/deepnets_RSA/RDMs_models.jpg" class="center">
<figcaption>RDMs for the layers of AlexNet</figcaption>

</figure>

Naturally here comes the question: are layers of AlexNet good models for object representation in human brain?  

To answer this question, we can assess the similarity of model RDMs and human brain regions RDMs, using Pearson correlation. 
 
Below we show the performance of model RDMs in explaining object representation in human V1. The height of the bars shows the mean Pearson correlation of model RDM and V1 RDM across subjects. Error bars show standard error of the mean. Gray horizontal bars show the upper and lower bound of the noise ceiling. Gray dots show significantly lower performance compared to the noise ceiling. While dots show significantly higher than 0 performance. Black horizontal lines show pair-wise model comparison results. 

<figure>
<img src="/projects/deepnets_RSA/inference_V1.jpg" class="center">
<figcaption>Performance of model RDMs in explaining human V1 object representation</figcaption>
</figure>

Overall the layers of AlexNet can predict data RDMs reasonably well for early visual regions, such as V1 and V2. However, when it comes to higher-order cognitive regions such as the IPS, IFJ, the prediction accuracies are low. It is partly because that the computations in higher-order cognitive regions are more complicated - they integrate not just visual information but also from other sensory modalities, such as auditory and touch. The neurons in these higher-order cognitive regions are modulated not by low-level stimulus features, but more abstract task features, such as rules, feedback, task context, and their interactions.  

We also see a wider noise ceiling towards higher-order cognitive regions. It is because there tend to be more measurement noise and subject idiosyncrasies in these regions.  

<figure>
<img src="/projects/deepnets_RSA/inference_V2.jpg" class="center">
</figure>

<figure>
<img src="/projects/deepnets_RSA/inference_V3.jpg" class="center">
</figure>

<figure>
<img src="/projects/deepnets_RSA/inference_V4.jpg" class="center">
</figure>

<figure>
<img src="/projects/deepnets_RSA/inference_IT.jpg" class="center">
</figure>

<figure>
<img src="/projects/deepnets_RSA/inference_IPS.jpg" class="center">
</figure>

<figure>
<img src="/projects/deepnets_RSA/inference_IFJ.jpg" class="center">
</figure>


</details>





## Compositional representation of tasks in human multiple‑demand cortex

The execution of complex cognitive tasks activates an extensive networks of frontal and parietal regions, known as the multiple-demand (MD) system, whose distributed activity patterns carry information about the task. 

However, the functional organization of task representation remains unclear. Do certain tasks elicit more similar activity patterns than others? If so, what drives the functional organization? 


Computational work suggests that asks may be represented in a compositional fashion in prefrontal cortex, where the representation of a task can be expressed as the algebraic sum of vectors representing the underlying sensory, cognitive and motor processes. 

Empirical evidence for compositional coding is limited. It remains to be tested if this principle generalizes to tasks that require context-dependent decisions. 

<figure>
<img src="/projects/compositional_coding/compositional_coding.jpg" class="center">
<figcaption>Compositional representation of tasks. Adapted from Yang et al 2019. </figcaption>
</figure>

<details markdown="1">
<summary>
Read more
</summary>

<iframe
    src="assets/files/20240623_OHBM_poster.pdf"
    frameBorder="0"
    scrolling="auto"
    height="100%"
    width="100%"
></iframe>

</details>