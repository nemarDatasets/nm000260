[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.nm000260-blue)](https://doi.org/10.82901/nemar.nm000260)

BrainInvaders2012
=================

P300 dataset BI2012 from a "Brain Invaders" experiment.

Dataset Overview
----------------
  Code: BrainInvaders2012
  Paradigm: p300
  DOI: https://doi.org/10.5281/zenodo.2649006
  Subjects: 25
  Sessions per subject: 1
  Events: Target=2, NonTarget=1
  Trial interval: [0, 1] s
  Runs per session: 2
  Session IDs: 0
  File format: mat, csv
  Contributing labs: GIPSA-lab

Acquisition
-----------
  Sampling rate: 128.0 Hz
  Number of channels: 16
  Channel types: eeg=16
  Channel names: F7, F3, F4, F8, T7, C3, Cz, C4, T8, P7, P3, Pz, P4, P8, O1, O2
  Montage: standard_1020
  Hardware: NeXus-32 (MindMedia/TMSi)
  Software: OpenVibe
  Reference: hardware common average reference
  Ground: FZ
  Sensor type: EEG
  Line frequency: 50.0 Hz
  Electrode type: wet
  Electrode material: Silver/Silver Chloride

Participants
------------
  Number of subjects: 25
  Health status: healthy
  Age: mean=24.4, std=2.76, min=21, max=31
  BCI experience: half played games occasionally (around 4.5 hours a week)
  Species: human

Experimental Protocol
---------------------
  Paradigm: p300
  Task type: brain_invaders
  Number of classes: 2
  Class labels: Target, NonTarget
  Study design: longitudinal and transversal design with training-test mode of operation
  Feedback type: visual (game interface)
  Stimulus type: visual flashes of alien groups
  Stimulus modalities: visual
  Primary modality: visual
  Synchronicity: synchronous
  Mode: both
  Training/test split: True
  Instructions: limit eye blinks, head movements and face muscular contractions; silently count the number of Target flashes
  Stimulus presentation: repetition_structure=12 flashes per repetition (2 Target, 10 non-Target), flash_groups=12 groups of 6 aliens (36 total aliens), target_ratio=1:5 (Target to non-Target), screen_distance=75 to 115 cm

HED Event Annotations
---------------------
  Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

  Target
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Target

  NonTarget
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Non-target

Paradigm-Specific Parameters
----------------------------
  Detected paradigm: p300
  Number of repetitions: 8

Data Structure
--------------
  Trials: {'Target': 128, 'non-Target': 640}
  Trials per class: Target=128, non-Target=640
  Trials context: per session (Training session); variable in Online session depending on user performance

Preprocessing
-------------
  Data state: raw EEG with software tagging (note: tagging introduces jitter and latency)
  Preprocessing applied: False
  Notes: Software tagging introduces a jitter and a latency which artificially modify the ERPs onset. Strong drift over time resulting in higher jitter. Only possible to compare ERP acquired within the same experimental conditions when latency is not corrected.

Signal Processing
-----------------
  Classifiers: xDAWN, Riemannian
  Feature extraction: Covariance/Riemannian, xDAWN
  Spatial filters: xDAWN

Performance (Original Study)
----------------------------

BCI Application
---------------
  Applications: gaming
  Environment: laboratory
  Online feedback: True

Tags
----
  Pathology: Healthy
  Modality: Visual
  Type: Perception

Documentation
-------------
  Description: EEG recordings of 25 subjects testing the Brain Invaders, a visual P300 Brain-Computer Interface inspired by the famous vintage video game Space Invaders
  DOI: 10.5281/zenodo.2649006
  Associated paper DOI: 10.5281/zenodo.2649006
  License: CC-BY-4.0
  Investigators: G.F.P. Van Veen, A. Barachant, A. Andreev, G. Cattan, P. Rodrigues, M. Congedo
  Senior author: M. Congedo
  Institution: GIPSA-lab, CNRS, University Grenoble-Alpes, Grenoble INP
  Address: GIPSA-lab, 11 rue des Mathématiques, Grenoble Campus BP46, F-38402, France
  Country: FR
  Repository: Zenodo
  Data URL: https://doi.org/10.5281/zenodo.2649006
  Publication year: 2019
  Acknowledgements: All subjects were volunteers recruited by means of flyers and of the mailing list of the University of Grenoble-Alpes. All participants provided written informed consent confirming the notification of the experimental process, the data management procedures and the right to withdraw from the experiment at any moment.
  Keywords: Electroencephalography (EEG), P300, Brain-Computer Interface, Experiment

Abstract
--------
We describe the experimental procedures for a dataset that we have made publicly available at https://doi.org/10.5281/zenodo.2649006 in mat and csv formats. This dataset contains electroencephalographic (EEG) recordings of 25 subjects testing the Brain Invaders (1), a visual P300 Brain-Computer Interface inspired by the famous vintage video game Space Invaders (Taito, Tokyo, Japan). The visual P300 is an event-related potential elicited by a visual stimulation, peaking 240-600 ms after stimulus onset. EEG data were recorded by 16 electrodes in an experiment that took place in the GIPSA-lab, Grenoble, France, in 2012 (2,3). Python code for manipulating the data is available at https://github.com/plcrodrigues/py.BI.EEG.2012-GIPSA. The ID of this dataset is BI.EEG.2012-GIPSA.

Methodology
-----------
The visual P300 is an event-related potential (ERP) elicited by a visual stimulation, peaking 240-600 ms after stimulus onset. The experiment features a training-test mode of operation and both a longitudinal and transversal design. Training session: Target alien chosen randomly at each repetition, 8 Targets total, 8 repetitions each, resulting in 128 Target trials and 640 non-Target flashes. Online session: consisted of three levels with different distractor configurations, minimum 3.5 minutes per level, counter-balanced order across subjects. Interface: 36 aliens flashing in 12 groups of 6, each repetition has 12 flashes (2 Target, 10 non-Target). P300 peak latency: 240-600 ms post-stimulus.

References
----------
Van Veen, G., Barachant, A., Andreev, A., Cattan, G., Rodrigues, P. C., & Congedo, M. (2019). Building Brain Invaders: EEG data of an experimental validation. arXiv preprint arXiv:1905.05182.
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.5.0 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb
