
# CISC881 Final Project: Generalizing and Automating the Classification of Prostate Cancer Severity

## Kaggle Challenge Link:
https://www.kaggle.com/c/prostate-cancer-grade-assessment



### Provided files:
1. tiles_subset_16x64x64.npy  
2. labels_subset_16x64x64.npy
These files correspond with our x and y numpy arrays for training, validation and testing. Composed of a subset of 100 tiles and labels. These subsets have been fully preprocessed and are ready for training/testing

### Instructions to run:
1. Downsample and convert all images into concatenated tiles (1_tile_creation.ipynb)
This notebook reads in all of the prostate biopsies, downsamples them to 8x resolution, extracts tiles and creates an image of concatenated tiles glued together

2. Balance classes and augment data (2_data_augmentation.ipynb)
This notebook will enforce a strict class balance of 3000 samples per class by randomly selecting one of 5 possible augmentations until all classes have 3000 samples. These will all be exported as a numpy array that can be directly used for training/testing

3. Training and evaluation of the four architectures (3_training.ipynb)
Training of each architecture across all samples takes place in this notebook. Models take between 30min-2hours to run depending on the complexity of the architecture. The provided files: tiles_subset_16x64x64.npy  and labels_subset_16x64x64.npy  can be used directly to train and evaluate the models. Metrics and confusion matrices are also reported within this notebook.

### This project was built with:
- scikit-learn, Jupyter, Tensorflow, Keras, NumPy, Pandas, OpenCV, and Matplotlib

