+++
title = 'Subtask 1A'
date = 2024-05-20T14:45:28-03:00
draft = false
showDate = false
+++


## Development set (dataset DCLDE2013)

The development data for this task is derived from the DCLDE 2013 dataset, specifically the selection that contains North Atlantic right whale (NARW) upcalls (leaving aside the gunshot vocalizations). The development annotation file `annotations_DCLDE2013.csv` can be found on the challenge downloading [space](https://drive.google.com/drive/folders/1BGKkMnaxnWV0U09m9ViIlPCs7eAaSub8?usp=sharing). Annotations labeled as uncertain have been excluded from the dataset. The original dataset and additional dataset details can be accessed here: [DCLDE 2013 dataset page](https://research-portal.st-andrews.ac.uk/en/datasets/dclde-2013-workshop-dataset).


## Evaluation set (dataset GSL)

The test data was collected in the Gulf of St. Lawrence and is a subset of the data used in a recent publication, which can be reviewed [here](https://pubs.aip.org/asa/jasa/article/147/4/2636/1058640/Performance-of-a-deep-neural-network-at-detecting). The test set includes 25 hours of recordings at 32KHz, with 1157 annotated NARW upcalls. The testing annotation file `annotations_GSL.csv` can be found on the challenge downloading [space](https://drive.google.com/drive/folders/1BGKkMnaxnWV0U09m9ViIlPCs7eAaSub8?usp=sharing). The original data set from this publication is available [here](https://doi.org/10.20383/101.0241).

Different underwater environemtns in terms of geographic location, and depth, various sources of transient sounds/noise (human activity and other biological sounds), distinct ambient sounds (noise from breaking waves, wind, rain, etc.), differences in sound propagation (a vocalization may sound different due to reverberations, diffraction, attenuation and reflections), differences in recording hardware and system self-noise, etc.

## Getting started and baseline codes

### Getting started

We have prepared a sample code on [GitHub](https://github.com/GabrielDubus/MeridianOSmOSE_AutomaticDetectionOfCetaceans_Benchmark/blob/task1/task1/README.md) to serve as an example and to provide general guidance for approaching this task. This approach is intended solely as a reference, and you are not required to follow any specific steps outlined in it, except for running the metrics file. Nonetheless, this serves as a useful guideline for participating in the challenge.

### Baseline 

The proposed baseline is a shallow 2-layer CNN, exhibiting the following results: 

- Precision: 0.5770114942528736
- Recall: 0.21694036300777875
- F1 Score: 0.31532663316582915





