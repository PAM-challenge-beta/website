+++
title = 'Task 1 : Supervised sound detection with strong labelling'
date = 2024-05-20T14:45:28-03:00
draft = false
showDate = false
+++

## User scenario 

The model benchmark produced in this task should provide evidence-based answers to the following user needs:

“ I have developed a detection model showing a 99% accuracy and 99 % recall on my study site and my target whale species, recorded during last winter. And now, I would like to implement it onboard a mobile platform to monitor the same species year-round over a wider spatial area.

Doing so, I will NOT have access to the new recorded data at all! Will my model be able to keep the same level of performance ? Is my model choice OK or should I transition to another one ? ”


## Task setup

This is a classical supervised sound event detection task using strong labeling. This task aims to challenge and assess the ability of models to adapt and perform in varying acoustic environments, reflecting the real-world variability encountered in marine mammal monitoring. Also, to force the model to be species and dataset agnostic, two subtasks are proposed below.

## Annotation format

All annotations of the development sets have been standardized as follows:

| filename                  | start | end  | label |
|---------------------------|-------|------|-------|
| NARW_20230601_0845.wav    | 123.5 | 125.2 | up | 

Where:
- `filename`: Name of the file containing a target sound event (here `NARW_20230601_0845.wav`)
- `start` : Start time in seconds from the beginning of the file where the upcall begins.
- `end`: End time in seconds where the upcall concludes.
- `label`: the label for the annotated sound event (here `up` standing for the north atlantic right whale upcall) 


The annotations for the test set include:

| filename   | timestamp |
| ---------- | --------- |

Where:
- `filename`: The name of the file where the detection occurred.
- `timestamp`: The detection time from the start of the file.
- `label`: `up` the label for this annotation. Note that for this particular challenge, all entries have the same label. The label column is included just for consistency.

You may find both train an test set annotatiosn in the annotations folder.
