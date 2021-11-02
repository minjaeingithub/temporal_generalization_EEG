# temporal_generalization_EEG

#### Multivariate pattern analysis of EEG data in a multi-attribute decision making task
This repo contains part of a study on identifying the temporal pattern of neural activation during multi-attribue decision making 

### Introduction
We often have to consider multiple factors when we make value-based decisions. For example, when we decide what to eat for lunch, we might consider attributes like how tasty or healthy a food is, our dieting goals, current hunger levels, and so forth. Each of these attributes constitutes evidence for or against eating the food, with different attributes given differential weight depending on a person’s momentary goals. Studying he temporal pattern by which different attributes contribute to decisions is essential for understanding how decisions are formed in the brain and regulated in presence of self-control.
In the past few years, the application of pattern classifiers to recordings of brain activity with a high temporal resolution, such as electrpencephalogram (EEG) and magnetoencephalogram (MEG), has contributed to a major advancement in characterizing the temporal organization of information processing stages (King & Dahaene, 2014). Here, we used this method to study the temporal pattern of multi-attribute decision making.

### Methods 
We designed a decision-making task where partcipants learned the value of two different attributes as separate stimlui (faces and colors) and then made decisions about accepting or rejecting a set of combined stimuli (a face on a colored background) whose value was the sum of the face and color attributes. They received feedback for each decision and later money based on their accumulated points. We recorded EEG when particpants made decisions, i.e., from the moment the stimulus was presented to after the decision feedback was presented.

### Code
The codes in this repo apply sklearn and MNE tools to train SVM classifiers for every 10ms time window to discriminate across faces, colors, face values, color values, and the overall value of the stimulus. These classifiers were then tested on all other 10ms time bins on the task timeline to find time periods where a "patten" of neural activity repeated suggesting re-occurence of the same mental representations.

temp_gen_binary.ipynb performs binary classification with temporal generalization for all subjects.

temp_gen_multi.ipynb performs multi-class classification with temporal generalization for all subjects.

temp_gen_plot.ipynb  contains functions that plot the results of temporal generalization analysis per subject and averaged across all subjects.

temp_gen_explore_1.ipynb plots the results of testing all time bins on the classifier at the time bin with maximum classification accuracy. The idea is to see if the neural representations of face, color, or value are repeated after the stimuli disappear.

EEG_auxiliary_module_sptm_wICA.ipynb contains all the helper functions


### Data
The input is the subject data that were pre-processed using MNE, namely filtered, segmented, and cleaned from artefatcs. 


