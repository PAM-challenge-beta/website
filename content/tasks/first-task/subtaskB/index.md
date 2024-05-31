+++
title = 'Subtask 1B'
date = 2024-05-20T14:45:28-03:00
draft = false
showDate = false
+++

## Development set (all datasets except Balleny Island 2015)

Note that the proposition is a beta-test. We strongly believe that a cross validation over the 11 datasets should be done in future versions

## Evaluation set (dataset Balleny Island 2015)

Among the eleven datasets in the original publication, the dataset Balleny Island 2015 was chosen for evaluation. This dataset represents a unique geographical location, the recording device used is only shared with one other dataset and finally, all seven labels are significatively present in it.

The test set includes 200 hours of recordings at 1KHz (but it can be downsampled at 250Hz as no target vocalization gets higher than 120Hz), with:
- 923 BmA 
- 44 BmB
- 31 BmZ
- 46 BmD
- 951 Bp20Hz
- 148 Bp20Plus
- 78 BpDS


## Evaluation metrics



Models will be evaluated based on Precision, Recall and F1 score average over each label. 

A 10-second buffer will be applied, where detections within this range from the annotation will be considered a true positive.
