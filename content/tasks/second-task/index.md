+++
title = 'Second Task'
date = 2024-05-20T16:14:58-03:00
draft = false
+++

# Task 2 - Automatic undetermined detection of pygmy blue whale with small number of trainning data


The goal of this task is to propose an efficient workflow for automatic detection of cetaceans vocalization in case of low supervised study, through the example of pygmy blue whale vocalizations recorded in the Indian Ocean.

Based on general observations of the state of the art in the DCLDE community, the perfect detector doesn't exist yet.
In most practical cases, from a new dataset, a manual annotation is still needed in order to constitute a training set and apply a specific trained detector on the rest of the dataset.

The quality of the detection is directly related to 1) the quality of the manual annotation, 2) the number of annotated samples and 3) the representativeness of the training set regarding the whole dataset. 
In number of study cases, the number and the quality of annotated sample is limited as manual annotation is an expensive and time consuming task. Moreover, the annotated part of the dataset is generally randomly selected. 

This task proposed to improve the result of automatic detection in a context of limited, but wisely selected the training set.

- The two main exercices will be to :
    - Select a few subset of the dataset (1500 samples over 27444) through unsupervised method. You are not allowed to use the manual annotation in this part.
    - Once the selection is done, you can use the annotation to train an automatic detection methods for the vocalization of pygmy blue whales. Considering the small number of samples available in the training set, this part is close from to literature of few-shot learning. 


The final objectives of this benchmark will be to establish a state of the art method to optimize the preprocessing time (data selection and manual annotation) while maintaining the quality of the detection in PAM studies applied on cetaceans.

See more details on the [GitHub repository]()
