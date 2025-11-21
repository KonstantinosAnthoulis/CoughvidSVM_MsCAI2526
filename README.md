## Covid Diagnosis via  classifying cough audio using SVMs <br> 

[Dataset Publication](https://www.nature.com/articles/s41597-021-00937-4) <Br>

**Goal:** classify cough audio into one of 3 categories (Healthy, Symptomatic, Covid) using Support Vector Machines <br>

### Project outline <Br>
1) Analyze the audio data prior to training (Fourier, Mel Spectograms etc) <br> 
2) use [PyAudioAnalysis](https://github.com/tyiannak/pyAudioAnalysis) for feature extraction <br>
3) train SVM on the data, compare results with original study and SotA deep learning alternatives 

### Why ML over deep learning?
Besides deep learning being off limits for the purposes of this project, non-deep machine learning models such as SVMs are more transparent in their operation and do not suffer from the black-box problem, making them ideal for a task as sensitive as a diagnosis. Furthermore, these models do not require billions of trainiable parameters to fit to a dataset, making them more lightweight both during training and subsequent distribution (eg model running locally on mobile devices), avoiding both compute cost during training and making the final model more easily accessible. 

