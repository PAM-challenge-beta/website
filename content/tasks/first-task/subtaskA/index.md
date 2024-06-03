+++
title = 'Subtask 1A'
date = 2024-05-20T14:45:28-03:00
draft = false
showDate = false
+++


## Development set 

The development data for this task is derived from the DCLDE 2013 dataset, specifically the selection that contains North Atlantic right whale (NARW) upcalls (leaving aside the gunshot vocalizations). The development annotation file `annotations_DCLDE2013.csv` and associated audio data can be found [here](https://drive.google.com/drive/folders/1pN9Og61KJ6Cqtvt0EpGxRZT-4eLI8Ta1). Annotations that have been labeled as uncertain during the DCLDE2013 annotation session were excluded from the development dataset. The original annotation protocol can be accessed here: [here](https://risweb.st-andrews.ac.uk/ws/portalfiles/portal/264470592/WorkshopDataset2013.pdf). See the general dataset presentation [page](https://github.com/PAM-challenge-beta/website/blob/main/content/datasets.md) for more details on the DCLDE2013 dataset.

## Evaluation set 

The test data were collected in the Gulf of St. Lawrence and is a subset of the data used in a recent publication, which can be reviewed [here](https://pubs.aip.org/asa/jasa/article/147/4/2636/1058640/Performance-of-a-deep-neural-network-at-detecting). The test set includes 25 hours of recordings at 32KHz, with 1157 annotated NARW upcalls. The test annotation file `annotations_GSL.csv` and associated audio data can be found [here](https://drive.google.com/drive/folders/12vlL_Lj4L5pVfEeBPBAzcl_GnUHgUOQf).  See the general dataset presentation [page](https://github.com/PAM-challenge-beta/website/blob/main/content/datasets.md) for more details on the DCLDE2013 dataset.

Different underwater environemtns in terms of geographic location, and depth, various sources of transient sounds/noise (human activity and other biological sounds), distinct ambient sounds (noise from breaking waves, wind, rain, etc.), differences in sound propagation (a vocalization may sound different due to reverberations, diffraction, attenuation and reflections), differences in recording hardware and system self-noise, etc.

## Evaluation protocol

Models will be evaluated based on Precision, Recall and F1 score average over each label. A complete explanation of these metrics can be found on the main task [page](https://pam-challenge-beta.github.io/website/tasks/first-task/#evaluation-metrics). A 3-second buffer will be applied, where detections within this range from the annotation will be considered a true positive. As explained in the next section, a complete code is provided to run these metrics.

## Getting started 

We have prepared a sample code on [GitHub](https://github.com/PAM-challenge-beta/2024-task1) to serve as an example and to provide general guidance for approaching this task. This approach is intended solely as a reference, and you are not required to follow any specific steps outlined in it, except for running the metrics file. Nonetheless, this serves as a useful guideline for participating in the challenge.

## Baseline 

The proposed baseline is a shallow 2-layer CNN, exhibiting the following results: 

- Precision: 0.5770114942528736
- Recall: 0.21694036300777875
- F1 Score: 0.31532663316582915





