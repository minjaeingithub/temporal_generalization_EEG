# temporal_generalization_EEG

#### Multivariate pattern analysis of EEG data in a multi-attribute decision making task
This repo contains part of a study on identifying the temporal pattern of neural activation during multi-attribue decision making 

### Introduction
We often have to consider multiple factors when we make value-based decisions. For example, when we decide what to eat for lunch, we might consider attributes like how tasty or healthy a food is, our dieting goals, current hunger levels, and so forth. Each of these attributes constitutes evidence for or against eating the food, with different attributes given differential weight depending on a person’s momentary goals. Studying he temporal pattern by which different attributes contribute to decisions is essential for understanding how decisions are formed in the brain and regulated in presence of self-control.
In the past few years, the application of pattern classifiers to recordings of brain activity with a high temporal resolution, such as electrpencephalogram (EEG) and magnetoencephalogram (MEG), has contributed to a major advancement in characterizing the temporal organization of information processing stages (King & Dahaene, 2014). Here, we used this method to study the temporal pattern of multi-attribute decision making.

### Methods 
We designed a decision-making task where partcipants learned the value of two different attributes as separate stimlui (faces and colors) and then made decisions about accepting or rejecting a set of combined stimuli (a face on a colored background) whose value was the sum of the face and color attributes. They received feedback for each decision and later money based on their accumulated points. We recorded EEG when particpants made decisions, i.e., from the moment the stimulus was presented to after the decision feedback was presented.

### Codes
The codes in this repo apply sklearn and MNE tools to train SVM classifiers for every 10ms time window to discriminate across faces, colors, face values, color values, and the overall value of the stimulus. These classifiers were then tested on all other 10ms time bins on the task timeline to find time periods where a "patten" of neural activity repeated suggesting re-occurence of the same mental representations.


### Data
These codes work on the data that were pre-processed using MNE, namely filtered, segmented, and cleaned from artefatcs.


