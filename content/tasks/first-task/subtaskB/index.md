+++
title = 'Subtask 1B'
date = 2024-05-20T14:45:28-03:00
draft = false
showDate = false
+++

## Development set

Our development set is composed of all SORP datasets except the Balleny Island 2015 dataset, kept for evaluation. The development annotation files and associated audio data can be found [here](https://drive.google.com/drive/folders/16Vaq4dzsCOnxoQAMxV8GMJhNYz0Ogukz?usp=sharing). See the general dataset presentation [page](https://github.com/PAM-challenge-beta/website/blob/main/content/datasets.md) for more details on the SORP dataset.



## Evaluation set

Among the eleven datasets in the original publication, the dataset Balleny Island 2015 was chosen for evaluation. The development annotation files and associated audio data can be found [here](https://drive.google.com/drive/folders/16Vaq4dzsCOnxoQAMxV8GMJhNYz0Ogukz?usp=sharing). This dataset represents a unique geographical location, the recording device used is only shared with one other dataset and finally, all seven labels are significatively present in it.

The evaluation set includes 200 hours of recordings at 1KHz (but it can be downsampled at 250Hz as no target vocalization gets higher than 120Hz), with:
- 923 BmA 
- 44 BmB
- 31 BmZ
- 46 BmD
- 951 Bp20Hz
- 148 Bp20Plus
- 78 BpDS

The test annotation file `annotations_BallenyIsland2015.csv` and associated audio data can be found [here]().  See the general dataset presentation [page](https://github.com/PAM-challenge-beta/website/blob/main/content/datasets.md) for more details on the DCLDE2013 dataset.



## Evaluation protocol

Models will be evaluated based on Precision, Recall and F1 score average over each label. A complete explanation of these metrics can be found on the main task [page](https://pam-challenge-beta.github.io/website/tasks/first-task/#evaluation-metrics). A 10-second buffer will be applied, where detections within this range from the annotation will be considered a true positive. As explained in the next section, a complete code is provided to run these metrics.



## Getting started and baseline codes

### Getting started

We have prepared a sample code on [GitHub](https://github.com/GabrielDubus/MeridianOSmOSE_AutomaticDetectionOfCetaceans_Benchmark/blob/task1/task1/README.md) to serve as an example and to provide general guidance for approaching this task. This approach is intended solely as a reference, and you are not required to follow any specific steps outlined in it, except for running the metrics file. Nonetheless, this serves as a useful guideline for participating in the challenge.

### Baseline 

The proposed baseline is a shallow 3-layer CNN, exhibiting the following results: 

- Precision: 0.4146943733143282
- Recall: 0.3907905837775654
- F1 Score: 0.40238779088282717


