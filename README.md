## Covid Diagnosis via  classifying cough audio using SVMs <br> 

[Dataset Publication](https://www.nature.com/articles/s41597-021-00937-4) <Br>

**Goal:** classify cough audio into one of 3 categories (Healthy, Symptomatic, Covid) using Support Vector Machines <br>

### Why ML over deep learning?
Besides deep learning being off limits for the purposes of this project, non-deep machine learning models such as SVMs are more transparent in their operation and do not suffer from the black-box problem, making them ideal for a task as sensitive as a diagnosis. Furthermore, these models do not require billions of trainiable parameters to fit to a dataset, making them more lightweight both during training and subsequent distribution (eg model running locally on mobile devices), avoiding both compute cost during training and making the final model more easily accessible. 

## Process Outline
1) Extract the labelled entries (~3k either symptomatic or covid, ~8k healthy) from the entire dataset (~25k entries) <br>
2) Random undersampling applied from the Healthy labelled categories up to 2000 entires to eliminate class imbalance <Br>
3) Convert from .webm to .wav for better compatibility with Librosa, Pyaudioanalysis
4) **Current** Examine various feature extraction and signal processing methods for creating the input features for the SVM
5) Evaluate mehtods of step 4
6) Design the SVM architecture (based on similar tasks/networks?)
7) Train SVM
8) Compare results to deep learning counterparts as well as the results of the original study
