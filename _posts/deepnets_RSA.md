---
layout: single
toc: true
title: Comparing the representational similarity of objects in human brain and deep neural networks 
tags: neuroAI, RSA 
---
## Comparing the representational similarity of objects in human brain and deep neural networks

Deep neural networks can achieve human-level performance in visual classification tasks. I'm curious about if two objects are represented differently by a neural network, are they also represented differently in human brain? In other words, are deep neural networks good candidates for studying how human brain represents visual objects? 

In this post, I'm presenting a toy project where I compare the representational similarity of objects in human brain regions and deep convolutional neural networks (using AlexNet as an example).  

## Stimuli 

* 16 manmade objects 
* 16 words describing these objects 

<figure>
<!-- <img src="/projects/deepnets_RSA/stimuli.jpg" width="1000" class="center"> -->

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

<img src="/projects/deepnets_RSA/RDMs_V1.jpg" class="center" width="50%">
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

To answer this question, we can assess the similarity of RDMs for each deep net layer and human brain region, by computing the Pearson correlation of these RDMs. 


<figure>

<img src="/projects/deepnets_RSA/inference_V1.jpg" class="center">
<figcaption>RDMs the layers of AlexNet</figcaption>

</figure>


