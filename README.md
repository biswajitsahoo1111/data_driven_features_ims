![Tensorflow 2.0](https://img.shields.io/badge/Tensorflow-2.0-success.svg)
![Python 3.7](https://img.shields.io/badge/Python-3.7-blue.svg)
# Multiclass bearing fault classification using features learned by a deep neural network

This repository contains codes for a paper submitted to the [International Congress and Workshop on Industrial AI 2020 (IAI - 2020)](https://www.ltu.se/research/subjects/Drift-och-underhall/Konferenser/Industrial-AI-Conference-2020?l=en) that uses learned data-driven featuers from a deep neural network and SVM to interpret the features and for fault classification. 

## Data:

We use the publicly available [IMS bearing dataset](https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/#bearing). The dataset is actually prepared for prognosis applications. However, we use it for fault diagnosis task. We consider four fault types: Normal, Inner race fault, Outer race fault, and Ball fault. The original data is collected over several months until failure occurs in one of the bearings. So for normal case, we have taken data collected towards the beginning of the experiment. Similarly, for faulty case, we have taken data towards the end of the experiment, that is closer to the point in time when fault occurs. Exact details of files used in our experiment can be found below.

The compressed file containing original data, upon extraction, gives three folders: 1st_test, 2nd_test, and 3rd_test and a documentation file. Inside the folder of 3rd_test, there is another folder named 4th_test. We refer to this data as test 4 data. 

Data taken from channel 1 of test 1 from 12:06:24 on 23/10/2003 to 13:05:58 on 09/11/2003 were considered normal. For inner race fault and rolling element fault, data were taken from 08:22:30 on 18/11/2003 to 23:57:32 on 24/11/2003 from channel 5 and channel 7 respectively. Outer race fault data were taken from channel 3 of test 4 from 14:51:57 on 12/4/2004 to 02:42:55 on 18/4/2004. There are a total of 750 files in each category.

## Folder Structure:
```
--/data
    |
    |__ /ims
          |
          |__ /normal
          |       |-- 2003.10.22.12.06.24
          |           2003.10.22.12.09.13
          |           2003.10.22.12.14.13
          |                  ...
          |                  ...
          |                  ...
          |           2003.11.09.12.45.58
          |           2003.11.09.12.55.58
          |           2003.11.09.13.05.58
          |   
          |
          |__ /inner
          |       |-- 2003.11.18.08.22.30
          |           2003.11.18.08.32.30
          |           2003.11.18.08.42.30
          |                  ...
          |                  ...
          |                  ...
          |           2003.11.24.23.37.32
          |           2003.11.24.23.47.32
          |           2003.11.24.23.57.32
          |
          |__ /outer
          |       |-- 2004.04.12.14.51.57
          |           2004.04.12.15.01.57
          |           2004.04.12.15.11.57
          |                  ...
          |                  ...
          |                  ...
          |           2004.04.18.02.22.55
          |           2004.04.18.02.32.55
          |           2004.04.18.02.42.55
          |
          |__ /ball
                  |-- 2003.11.18.08.22.30
                      2003.11.18.08.32.30
                      2003.11.18.08.42.30
                            ...
                            ...
                            ...
                      2003.11.24.23.37.32
                      2003.11.24.23.47.32
                      2003.11.24.23.57.32
```                     
Arrange the files and folders as given in the structure and then run the notebooks. Make slight modifications while reading data from the folders. For example, in my system, data are stored in `'/home/biswajit/data/ims/'`. Change this appropriately for your case. 

For other data-driven condition monitoring results, visit my [project page](https://biswajitsahoo1111.github.io/cbm_codes_open/) and [personal website](https://biswajitsahoo1111.github.io/).

Cite the data source as
```
BibTeX citation
@misc{imsbearingdata,
  url = {https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/#bearing},
  note = {This data come from National Aeronautics and Space Administration Website.}
}
```

Cite this work (for the time being, until the publication of paper) as
```
BibTeX citation
@misc{sahoo2016datadriven,
  author = {Sahoo, Biswajit},
  title = {Data-Driven Machinery Fault Diagnosis},
  url = {https://biswajitsahoo1111.github.io/cbm_codes_open/},
  year = {2016}
}
```
