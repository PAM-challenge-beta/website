+++
title = 'Subtask 1A'
date = 2024-05-20T14:45:28-03:00
draft = false
showDate = false
+++


## Development set

The training data for this task is derived from the DCLDE 2013 dataset, specifically the selection that contains North Atlantic right whale (NARW) upcalls. The original dataset can be accessed here: [DCLDE 2013 dataset page](https://research-portal.st-andrews.ac.uk/en/datasets/dclde-2013-workshop-dataset).
- Training annotation file: `annotations_DCLDE2013.csv`

Annotations labeled as uncertain have been excluded from the dataset. Additional dataset details are available on the [DCLDE 2013 dataset page](https://research-portal.st-andrews.ac.uk/en/datasets/dclde-2013-workshop-dataset).


## Evaluation set


The test data was collected in the Gulf of St. Lawrence and is a subset of the data used in a recent publication, which can be reviewed [here](https://pubs.aip.org/asa/jasa/article/147/4/2636/1058640/Performance-of-a-deep-neural-network-at-detecting). The original data set from this publication is available [here](https://doi.org/10.20383/101.0241).


Both the training and test data have been reorganized and are available in a single downloadable package.

- Testing annotation file: `annotations_GSL.csv`

The test data was collected in the Gulf of St. Lawrence and is a subset of the data used in a recent publication, which can be reviewed here. The test set includes 25 hours of recordings at 32KHz, with 1157 annotated NARW upcalls.






## Evaluation metrics

Models will be evaluated based on precision, recall, F1 score, and false positive rate (FPR) per hour of recording. Please compute the performance metrics using the provided `metrics.py` script as follows:

```shell
python metrics.py annotations/annotations_test.csv detections.csv
```

If you are using a Windows operating system, you will need to replace the forward slashes (`/`) in the directory paths with backslashes (`\`).

A True Positive (TP) is recorded when a detection timestamp intersects with a ground truth buffer. A False Positive (FP) is incremented when a detection timestamp does not overlap with any ground truth buffer. Finally a False Negative (FN) is noted when there is a ground truth event that does not have a corresponding detection timestamp.

Note: The true positive count will only be incremented once per detection timestamp. For instance if multiple detection timestamps aligns with only one ground truth, the true positive count will be incremented only once. Similarly, if one detection timestamp aligns with multiple ground truths, the true positive count will be incremented for each ground truth.

The following images illustrates these scenarios:

![Multiple detection tiemestamps for one ground truth](imgs/scenario1.png "Multiple detection tiemestamps for one ground truth")

In the image above, several detection timestamps are indicated by red lines, all of which fall within the same ground truth buffer marked by a green line and a blue box. Under this scenario, the count of true positives will be incremented only once, despite multiple detections.

![Single detection tiemestamp for multiple ground truths](imgs/scenario2.png "Single detection tiemestamp for multiple ground truths")

In the image above, a single detection timestamp (red line) intersects with several ground truth buffers (blue boxes). In this case, the count of true positives will be incremented for each ground truth that the detection timestamp overlaps, despite there being "only one" detection.


## Codes to get started

We have prepared a sample code on [GitHub](https://github.com/GabrielDubus/MeridianOSmOSE_AutomaticDetectionOfCetaceans_Benchmark/blob/task1/task1/README.md) to serve as an example and to provide general guidance for approaching this task. This approach is intended solely as a reference, and you are not required to follow any specific steps outlined in it, except for running the metrics file. Nonetheless, this serves as a useful guideline for participating in the challenge.



