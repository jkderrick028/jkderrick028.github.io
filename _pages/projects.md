---
title: "Projects"
permalink: /projects/
layout: single
author_profile: false
toc: false
---


## Task-specific topographic maps in primate lateral prefrontal cortex (LPFC) 

The topographical maps in visual cortex are commonly used to describe how neurons with similar response preferences to stimulus features, such as eccentricities (Brewer et al. 2002), polar angles (Fang et al. 2022), and object categories (Bell et al. 2009), are organized. These maps extend multiple spatial scales and are largely independent of internal mental state. 

LPFC supports multiple higher-order cognitive functions, such as working memory, decision making, and is part of the multiple-demand cortex. LPFC neurons flexibly adapt their activity according to rules, contextual associations and feedback. For instance, the same neuron may have different response preferences to objects and locations depending on whether the subject is doing an object task or a location task. Another way of phrasing it is that LPFC neurons exhibit selectivity to mixtures of task features. 

Because of the adaptivity and mixed selectivity, the topographic maps should naturally extend from those in visual cortex, and reflect how neurons with similar responses to combinations of task features (a.k.a the tuning profiles) are organized. 

We show that such topographic maps in LPFC do exist and are adaptive across tasks. In addition, the maps are organized at a fine-grained spatial scale that resembles the long-range afferent input patterns into LPFC. The fine-grained topographic maps could potentially be resolvable by advanced neuroimaging techniques in humans and allow us to understand how LPFC supports so many higher-order cognitive functions flexibly.  

<figure>

<img src="/projects/topoPFC/maps.jpg" align="center" style="width:100%">

<figcaption>Topographic maps in primate visual regions and prefrontal cortex. Maps for LPFC are based on multi-electrode utah arrays (4 mm x 4 mm coverage, 10 x 10 electrodes) </figcaption>

</figure>

[[paper](https://www.biorxiv.org/content/10.1101/2024.05.10.591729v1)][[code](https://github.com/jkderrick028/topoPFC)]




## Comparing the representational similarity of objects in human brain and deep neural networks

Deep neural networks can achieve human-level performance in visual classification tasks. I'm curious about if two objects are represented differently by a neural network, are they also represented differently in human brain? In other words, are deep neural networks good candidates for studying how human brain represents visual objects? 

In this post, I'm presenting a toy project where I compare the representational similarity of objects in human brain regions and deep convolutional neural networks (using AlexNet as an example).  

<figure>
<img src="/projects/deepnets_RSA/visual_stream.png" align="center" style="width:50%">
</figure>

[[code](https://github.com/jkderrick028/interp_deepnets/blob/main/demo.ipynb)]

<details markdown="1">
<summary>
Read more
</summary>

<br>

## Stimuli 

* 16 manmade objects 
* 16 words describing these objects 

<figure>

<img src="/projects/deepnets_RSA/stimuli.jpg" class="center">

</figure>


## fMRI data 

The participants were asked to maintain fixation while these images were displayed at the centre of fixation, on a uniform grey background, at a width of 9⁰ of visual angle. 

* 32 stimuli -> 32 conditions
* stimulus duration = 500 ms
* 12 trials per condition
* 14 subjects
* whole-brain coverage
* voxel size = 3 mm3	
* regions of interests (ROIs)

<figure>

<img src="/projects/deepnets_RSA/ROIs.png" class="center">
<figcaption>Fig. 2 Regions of interest</figcaption>

</figure>

## Representational similarity analysis (RSA)

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


</details>

