# Introduction
This repository provides the code for the manuscript titled "Modeling and Predicting Individual Transitions within the Homelessness System" by Charalampos Chelmis and Khandker Sadia Rahman.

<!-- ## Citation
To cite our paper, please use the following reference:

Charalampos Chelmis and Khandker Sadia Rahman "Learning to Predict Transitions within the Homelessness System from Network Trajectories." IEEE/ACM International Conference on Advances in Social Networks Analysis and Mining (ASONAM '22).

BibTeX:
``` 
@article{rahman2022asonam, 
  author = {Rahman, Khandker Sadia and Chelmis, Charalampos},
  title = {Learning to Predict Transitions within the Homelessness System from Network Trajectories},
  year = {2022},
  publisher = {Association for Computing Machinery},
  address = {New York, NY, USA},
  booktitle = {Proceedings of the 2022 IEEE/ACM International Conference on Advances in Social Networks Analysis and Mining},
  keywords = {socially important data science, computational social science, applied network science, human services},
  location = {Virtual Event, Netherlands},
  series = {ASONAM '22}
}
```
-->

## Quick Overview
This paper proposes a similarity score between the ordered sequences of services individuals receive that leverages the structure of the inferred network in addition to historical observations to identify individuals with similar trajectories. In doing so, the service an individual will be assigned to next can be predicted. Extensive experiments show that the proposed approach performs well not only on predicting exit from the system, or simply guessing high frequency services (as most baselines), but is also successful in less frequent scenarios. 


### Prerequisites
Python 2.7 or above and the following libraries
```
pandas, numpy, networkx, random, datetime, matplotlib, seaborn, os, 
```

### Files
```
   ToyDataset.csv: A sample dataset with the features and trajectories (toy data for TRACE)
   ToyDataset_Prediction - M_exit exit points.csv: A sample dataset with the prediction of M_exit model for exit points (toy data for MetaTier)
   ToyDataset_Prediction - M_exit interim points.csv: A sample dataset with the prediction of M_exit model for interim points (toy data for MetaTier)
   ToyDataset_Prediction - M_int exit points.csv: A sample dataset with the prediction of M_int model for exit points (toy data for MetaTier)
   ToyDataset_Prediction - M_int interim points.csv: A sample dataset with the prediction of M_int model for interim points (toy data for MetaTier)
   Functions.ipynb: Contains the functions associated with the rest of files
   Evaluation.ipynb: Evaluates proposed methods in comparison to the baselines
   Train_Test_set: Splits the data into train and test set
   Pre processing - Transition graph.ipynb: Creates the transition graphs
   Historical data and overlap computation: Extracts the trajectories with temporal overlap with the test set and computes the overlap
   Method 1_Similarity info computation: Computes the information necessary for similarity computaion for TRACE_1
   Method 1_Similarity computation and Prediction: Computes the similarity and the corresponding prediction for TRACE_1
   Method 2_Similarity info computation: Computes the information necessary for similarity computaion for TRACE_2
   Method 2_Similarity computation and Prediction: Computes the similarity and the corresponding prediction for TRACE_2
   Baseline_Similarity info computation: Computes the information necessary for similarity computaion for the baselines
   Baseline_Similarity computation and Prediction: Computes the similarity and the corresponding prediction for the baselines
   MetaTier: Computes the prediction for MetaTier model
```

### How to use

The toy dataset shows a snippet of the data used after data cleaning and feature preprocessing have been done. This data can be directly run through the jupyter notebook files for the following purposes:

1. Split the data into train and test set
2. Extract the trajectories with temporal overlap with the test set and compute overlap
3. Compute the various transition graphs
4. Compute the information necessary for similarity computation and corresponding similarity for the proposed method and the baselines
5. Predict the next k assignments using the TRACE models and the baselines
6. Evaluate the precision and recall for each model and compare them
7. Predict the next step using the MetaTier model
