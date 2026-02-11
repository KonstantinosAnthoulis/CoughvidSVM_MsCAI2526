## Covid Diagnosis via classifying cough audio using SVMs <br> 

[Dataset Publication](https://www.nature.com/articles/s41597-021-00937-4) <Br>

### Why traditional ML over deep learning?
Besides deep learning being off limits for the purposes of this project, non-deep machine learning models such as SVMs are more transparent in their operation and do not suffer from the black-box problem, making them ideal for a task as sensitive as a diagnosis. Furthermore, these models do not require billions of trainiable parameters to fit to a dataset, making them more lightweight both during training and subsequent distribution (eg model running locally on mobile devices), avoiding both compute cost during training and making the final model more easily accessible. Despite their advantages, it is evident in both this project and in adjacent bibliography that their usage cannot easily be applied and/or replicated for non-tabular data such as audio, especially in the case of noisy, crowdsourced audio such as the Coughvid dataset.

## Replication Instructions
This repository contains a `config.yaml` file in which you are to set the path where you want the raw data to be downloaded, processed and stored (at least 10GB needed to be on the safe side). This work is using version 3 of the dataset as found [here](https://zenodo.org/records/4048312), though for the sake of easy replication of the testing environment I've included code to download a copy of the dataset I've stored on a Google Drive archive.

There is also a `requirements.txt` file for all the dependencies needed to run the code found in the notebooks in this project, I strongly advise creating a separate pip/conda environment for the sake of keeping any project/dependency lists organised.

Notebooks are to be executed in their annotated order, with indices starting from 1 indicating data processing, inspection and feature extraction while the separate index 2.1 is reserved specifically for model training.

Due to the unsatisfactory results of the experiment (more information in report + to be added here), there is no inference code to use on trained models, though given `scikit-learn` is the main tool used for training models it is something easily implementable for those interested.

Report and presentation powerpoint to be added soon, along with additional information in this readme 
