+++
title = 'Datasets'
date = 2024-05-20T15:07:16-03:00
draft = false
+++

All open source datasets used in our challenge are available for downloading within a single online storage [space](https://drive.google.com/drive/folders/1BGKkMnaxnWV0U09m9ViIlPCs7eAaSub8?usp=sharing). Note that already existing datasets such as the DCLDE datasets have been reorganized and standardized into a same format.



## File organization

Here is the folder tree structure we are using to organize audio and annotation files within our datasets.

```
DCLDE2013
│
└───audio
│   │
│   └───NOPP6_EST_20090329
│       │   NOPP6_EST_20090329_000000.wav
│       │   ...
│   │
│   └───annotations
|       │   └───annotations_DCLDE2013.csv
BlueFinLibrary
│
└───BlueFinLibrary_BallenyIslands2015
│   │
│   └───audio
│       │   20150115_170000.wav
│       │   ...
│   │
│   └───annotations
|       │   └───annotations_BallenyIslands2015.csv
│
└───BlueFinLibrary_casey2014
│   │
│   └───audio
│       │   200_2013-12-25_06-00-00.wav
│       │   ...
│   │
│   └───annotations
|       │   └───annotations_BallenyIslands2015.csv
```



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





## General description

| Dataset name                                   | DCLDE13                                                                                                                                                                                                                                                       | GSL                                                                                                                                                                                                                                         | SORP                                                                                                                                                                                                                            | DCLDE15LF                                                                                                                     |
| ---------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Temporal coverage                              | 2009                                                                                                                                                                                                                                                          | 2015-2019                                                                                                                                                                                                                                   | 2005-2017                                                                                                                                                                                                                       | 2009-2013                                                                                                                     |
| Spatial location(s)                            | Gulf of Maine                                                                                                                                                                                                                                                 | Gulf of St. Lawrence                                                                                                                                                                                                                        | All around Antarctica                                                                                                                                                                                                           | Offshore<br>Southern California                                                                                               |
| Annotation classes<br>(~ nber of events)       | \- up (10 k)                                                                                                                                                                                                                                                  | \- up (1 k)                                                                                                                                                                                                                                 | \- BmA<br>\- BmB<br>\- BmZ<br>\- BmD<br>\- Bp20Hz<br>\- Bp20Plus<br>\- BpDS                                                                                                                                                     | \- BmD (5 k)<br>\- 40Hz (0.1 k)                                                                                               |
| Sampling rate (Hz)                             | 2000                                                                                                                                                                                                                                                          | 32000                                                                                                                                                                                                                                       | 250                                                                                                                                                                                                                             | 1000                                                                                                                          |
| Original URL source (same as original: yes/no) | [](https://research-portal.st-andrews.ac.uk/en/datasets/dclde-2013-workshop-dataset)[https://research-portal.st-andrews.ac.uk/en/datasets/dclde-2013-workshop-dataset](https://research-portal.st-andrews.ac.uk/en/datasets/dclde-2013-workshop-dataset) (no) | [](https://www.frdr-dfdr.ca/repo/dataset/4a3113e6-1d58-6bb4-aaf2-a9adf75165be)[https://www.frdr-dfdr.ca/repo/dataset/4a3113e6-1d58-6bb4-aaf2-a9adf75165be](https://www.frdr-dfdr.ca/repo/dataset/4a3113e6-1d58-6bb4-aaf2-a9adf75165be) (no) | [](https://data.aad.gov.au/metadata/records/AcousticTrends_BlueFinLibrary)[https://data.aad.gov.au/metadata/records/AcousticTrends_BlueFinLibrary](https://data.aad.gov.au/metadata/records/AcousticTrends_BlueFinLibrary) (no) | [https://www.cetus.ucsd.edu/dclde/datasetDocumentation.html](https://www.cetus.ucsd.edu/dclde/datasetDocumentation.html) (no) |
| Associated research papers                     |                                                                                                                                                                                                                                                               | [https://pubs.aip.org/asa/jasa/article/147/4/2636/1058640/Performance-of-a-deep-neural-network-at-detecting](https://pubs.aip.org/asa/jasa/article/147/4/2636/1058640/Performance-of-a-deep-neural-network-at-detecting)                    | [https://research-repository.st-andrews.ac.uk/handle/10023/21390?show=full](https://research-repository.st-andrews.ac.uk/handle/10023/21390?show=full)                                                                          |                                                                                                                               |

Here are the long names of annotation classes:
- up : North Atlantic Right Whale Upcall 
- BmA: Antarctic blue whale unit A
- BmB: Antarctic blue whale unit AB
- BmZ: Antarctic blue whale z-call
- BmD: Blue whale FM (AKA D-calls)
- Bp20Hz: Fin whale 20 Hz pulse
- Bp20Plus: Fin whale 20 Hz pulse with energy at higher frequencies (e.g. 89 or 99 Hz components)
- BpDS: Fin whale FM calls (AKA ‘high frequency’ downsweep; AKA 40 Hz pulse). 
- BmD : Blue whale Dcall
- 40Hz : Fin whale 40 Hz call
