+++
title = 'Datasets'
date = 2024-05-20T15:07:16-03:00
draft = false
+++

All open source datasets used in our challenge are available for downloading within a single online storage [space](https://drive.google.com/drive/folders/1W1yF3_wbndhBikcQjYjp81TnK5-qIBaT). Note that already existing datasets such as the DCLDE datasets have been reorganized and standardized into a same format.



## Dataset organization and format

### File organization

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



### Annotation format

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





## Dataset description



| Long name                                  | DCLDE2013<br>dataset                                                                                                                                                                                                                                          | Gulf of St. Lawrence                                                                                                                                                                                                                        | SORP dataset                                                                                                                                                                                                                    | DCLDE2015<br>LF dataset |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------- |
| Short name                                 | DC13                                                                                                                                                                                                                                                          | GSL                                                                                                                                                                                                                                         | SORP                                                                                                                                                                                                                            | DC15                    |
| Temporal coverage                          |                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                 |                         |
| Spatial location(s)                        | Gulf of Maine                                                                                                                                                                                                                                                 | Gulf of St. Lawrence                                                                                                                                                                                                                        |                                                                                                                                                                                                                                 |                         |
| Annotation classes (nber of events)        | NARWuc ()                                                                                                                                                                                                                                                     | NARWuc ()                                                                                                                                                                                                                                   | BWdcall ()<br>FW20 ()                                                                                                                                                                                                           | BWdcall ()<br>FW40 ()   |
| Sampling rate (Hz)                         |                                                                                                                                                                                                                                                               | 32000                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                 |                         |
| Nber of audio files                        |                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                 |                         |
| Total events                               |                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                 |                         |
| Ratio event / duration ??                  |                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                 |                         |
| Original URL source (use original: yes/no) | [](https://research-portal.st-andrews.ac.uk/en/datasets/dclde-2013-workshop-dataset)[https://research-portal.st-andrews.ac.uk/en/datasets/dclde-2013-workshop-dataset](https://research-portal.st-andrews.ac.uk/en/datasets/dclde-2013-workshop-dataset) (no) | [](https://www.frdr-dfdr.ca/repo/dataset/4a3113e6-1d58-6bb4-aaf2-a9adf75165be)[https://www.frdr-dfdr.ca/repo/dataset/4a3113e6-1d58-6bb4-aaf2-a9adf75165be](https://www.frdr-dfdr.ca/repo/dataset/4a3113e6-1d58-6bb4-aaf2-a9adf75165be) (no) | [](https://data.aad.gov.au/metadata/records/AcousticTrends<br>_BlueFinLibrary)[https://data.aad.gov.au/metadata/records/AcousticTrends_BlueFinLibrary](https://data.aad.gov.au/metadata/records/AcousticTrends_BlueFinLibrary) (no) |                         |
| Associated research papers                 |                                                                                                                                                                                                                                                               | [https://pubs.aip.org/asa/jasa/article/147/4/2636/1058640/Performance-of-a-deep-neural-network-at-detecting](https://pubs.aip.org/asa/jasa/article/147/4/2636/1058640/Performance-of-a-deep-neural-network-at-detecting)                    |                                                                                                                                                                                                                                 |                         |


Here are the long names of annotation classes:
- BWdcall : Blue Whale Dcall
- NARWuc : North Atlantic Right Whale upcall
- FW20 : Fin Whale 20 Hz
