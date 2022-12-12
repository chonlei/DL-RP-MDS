# DL-RP-MDS

Source code and data used in the article "DL-RP-MDS: Integration of Deep Learning with Ramachandran Plot-Molecular Dynamics Simulation for Genetic Variant Classification" (Tam et al. _iScience_, 2023).

This repository aims to apply a deep learning classification algorithm to determine deleterious variants from VUS based on features extracted from MD simulations using benign and pathogenic variants.

By: Benjamin Tam, Zixin Qin, Bojin Zhao, San Ming Wang, Chon Lok Lei

### Requirements

The code requires Python (3.6+ and was tested with 3.7.6) and the following dependencies:
[scikit-learn](https://scikit-learn.org/stable/install.html),
[tensorflow](https://www.tensorflow.org/install),
[keras-tuner](https://keras.io/guides/keras_tuner/getting_started/),
[imbalanced-learn](https://imbalanced-learn.org/stable/install.html#install).
Installing Tensorflow in Windows may require [Microsoft Visual C++ Redistributable for Visual Studio 2015, 2017 and 2019](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads).
It also needs [seaborn](https://seaborn.pydata.org/installing.html) for plotting.

To install, navigate to the path where you downloaded this repo and run:
```
$ pip install --upgrade pip
$ pip install -e .
```

## Structure of the repo

### Main
- `dl-pred.py`: For now use mainly this to do DL-RP-MDS predictions.
- `dl-kfold.py`: Run k-fold validation for DL-RP-MDS models.
- `dl-tune.py`: Run hyperparameter tuning for DL-RP-MDS models.

### Folders
- `data`: Contains MD simulation data and labels.
- `method`: A module containing useful methods, functions, and helper classes for this project;
            for further details, see [here](./method/README.md).
- `out`: Output of the models.

## Acknowledging this work

If you publish any work based on the contents of this repository please cite ([CITATION file](CITATION)):

Tam _et al._
(2023).
[DL-RP-MDS: Integration of Deep Learning with Ramachandran Plot-Molecular Dynamics Simulation for Genetic Variant Classification](.).
_iScience_, accepted.