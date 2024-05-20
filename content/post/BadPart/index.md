---
title: Adversarial Attack Causing Error Beyond Wrong Classification
subtitle: Welcome 👋 This is a blog post for our paper in ICML 2024. Let's get started!

# Summary for listings and search engines
summary: Welcome 👋 We know that first impressions are important, so we've populated your new site with some initial content to help you get familiar with everything in no time.

# Link this post with a project
projects: []

# Date published
date: '2024-05-20T00:00:00Z'

# Date updated
lastmod: '2024-05-20T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Attack Result'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - Robustness

categories:
  - Research Blog

---

## What is Adversarial Patch Attack?

Vision Nerual Networks have showcast promising capability of allowing computers to see. Among the study for the past decades, image classification is one of the most representative vison tasks that neworks are designed for. It is, for instance, given an input image $x$ of a cat, the nerual network $f_c(x)$ distinguish this image and give the right decision of categarizing it as a cat. But in 2014, Szegedy et.al found that these Nerual Networks are sensetive to the perturbation of the input. Adding some particular perturbation which is hard to be perceived by humans to the input image would greatly disturb the jugement of the nerual network, causing wrong output. After this, coming studies show that these perturbation can even lead the network output a pre-definded target output rather than just causing wrong output casually. Thus by adding appropriate perturbation into the input to trigger the vulnerability of these nerual networks is called adversarial attack while these disturbed inputs are called adversarial examples. 

The shape of the perturbation is non-trivial. It's common that the adversaral noise are the same size as the input image. But in this blog, we consider a variant that only covers a portion of the input image. This is adversarial patch attack and that portion of adversarial noise is called adversarial patch.

Note that while the vulnerability we discussed above was first discovered in vison tasks, recent studies find that this it is not confined in realm of vison but a general vulnerability lies in nerual networks covering wide range of tasks e.g. text, speech and so on. In this post blog, we only talk about the adversarial attack in vison networks.

## Adversarial Attack Causing Error Beyond Wrong Image Classification

Image classification, as a relatively simple vison task, seems limited application. Thus, a bunch of nerual networks are proposed for some more complicated pixel-wise regression tasks e.g. Depth Estimation and Optical Flow Estimation. <!-- These pixel-wise regression models input a image and outputs a score map with each pixel in input has corresponding score in score map.  -->Specificly, for depth estimation models, they input a image and output a depth map with each value in the depth map standing for the distance this pixel to the camera. For optical flow estimation models, they input a sequntial two frames of the scene and output a displacement map with each value in the map standing for the displacement between two frames. These two models are widely deployed to make self-driving possible with the depth model detecting the distance between sorrouding objects and the car and optical flow model calculating the speed of moving objects.

Unfortunately, the above pixel-wise regression models are still exposed to the adversarial attacks. Adversarial **patch** attack even makes results unaffordable in real world circumstance. Let's think a scenario like this: a depth model embeded self-driving car is running on the road. The model runs on images captured by camera to sense the sorrouding situation. As the model are sensitive to advervasiral noise, the attacker can craft a particular adversarial patch to make the depth of the patched area (impact can spread beyoud this area actually) far than it actually is. The attacker can prints this adversarial patch and paste it on a barrier along the road. Once the camera captures this adversarial patch, the car can wrongly estimate the distance between itself and the front barrier, thinking they are far from each other but close instead. The consequence is obvious —— crashing into the barrier.

## Adversarial Patch Optimization

Not all noise can be effective for triggering the vulnerability. It must have some particular pattern and distribution that the target nerual network are sensitive to. So, the qestion is how to find that particular distribution?

### Threat model

Taking what capabilities the attacker can possess, the attack can be divided into two catageries: white-box and black-box attack. 

1. In white-box attack scenario, the assumption is that the attacker have access to the whole target nerual network. Thus the adversarial patch can be optimized by gradient descent because the gradients are available. 

2. In black-box scenario, the target nerual network are transparent to the attacker. The attacker can only feed the model an input and get the corresponding feedback to adjust his adversarial patch.

Although white-box method can achive superior attack performance compared with black-box attacks, the assumption of accessibility of target model is too strong to fulfill in real situations. In contrary, the black-box setting is realistic that many widely applyed commercial networks are closed source and only provides services (i.e. taking the input and give the output). Thus great danger will be caused if attack can be launched under this black-box setting.

### BadPart

Given the above confinements, we propose the first black-box adversarial patch attack framework against pixel-wise regression models:

> BadPart: Unified Black-box Adversarial Patch Attacks against Pixel-wise Regression Tasks.

By our method, we show the possibility that the attacker can successfully launch an adversarial attack towards pixel-wise task models. BadPart novelly employs probabilistic square sampling and score-based gradient estimation techniques to generate adversarial patch. The method overview is presented below. More details of our algorithm can be found in our [paper](https://arxiv.org/abs/2404.00924).

![BadPart](badpart_overview.png "BadPart")