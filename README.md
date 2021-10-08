# Voltages of battery electrodes
Using the CGCNN transfer learning model to pridict the voltages of Li, Na, K, Mg, Ca, Zn, Y, and Al-ion battery electrodes

The package provides all the files that are used in the article of "Accurately predicting voltage of electrode materials in metal-ion batteries using interpretable
 deep transfer learning"
 
## Table of Contents

- [How to cite](#how-to-cite)
- [Prerequisites](#prerequisites)
- [Files](#Files)
  - [CGCNN]
  - [CGCNN_visulization]
  - [Transfer_learning]
  - [Trained_model]
  - [data]
  - [SVR_KRR_RFR]
- [Web tool](#web-tool)


## How to cite

Please cite the following work if you want to use this model.

```
@article{PhysRevLett.120.145301,
  title = {Accurately predicting voltage of electrode materials in metal-ion batteries using interpretable deep transfer learning},
  author = {Zhang Xiuying and Shen Lei},
  journal = {},
  volume = {},
  issue = {},
  pages = {},
  numpages = {},
  year = {2021},
  month = {},
  publisher = {},
  doi = {},
  url = {}
}
```

```
@article{PhysRevLett.120.145301,
  title = {Crystal Graph Convolutional Neural Networks for an Accurate and Interpretable Prediction of Material Properties},
  author = {Xie, Tian and Grossman, Jeffrey C.},
  journal = {Phys. Rev. Lett.},
  volume = {120},
  issue = {14},
  pages = {145301},
  numpages = {6},
  year = {2018},
  month = {Apr},
  publisher = {American Physical Society},
  doi = {10.1103/PhysRevLett.120.145301},
  url = {https://link.aps.org/doi/10.1103/PhysRevLett.120.145301}
}
```

##  Prerequisites

This package requires:

- [PyTorch](http://pytorch.org)
- [scikit-learn](http://scikit-learn.org/stable/)
- [pymatgen](http://pymatgen.org)
- [numpy](http://numpy.org/)

If you are new to Python, the easiest way of installing the prerequisites is via [conda](https://conda.io/docs/index.html). After installing [conda](http://conda.pydata.org/), run the following command to create a new [environment](https://conda.io/docs/user-guide/tasks/manage-environments.html) named `cgcnn` and install all prerequisites.

## Files
- CGCNN folder

The files in this folder just the same as the correspoiding files in the CGCNN model that Xie Tian et.al gives (http://github.com/txie-93/cgcnn).
We used files in this folder to train the model for the voltage prediction of Li-ion battery electrodes.
- CGCNN_visulization

The files in this folder are used to have a visulization of the CGCNN model. 

The embedding_features.py is to visulize the features from the embedding layer in the CGCNN model.

The local_voltage_plt.py is to visulize the local voltages, which are obtained after the three convelutional layers.

The element_features.csv and OMO_local.csv are the data files that are used in the embedding_features.py and local_voltage_plt.py respectively. The element_features_csv.py and OMO_local_csv.py are the coresponding codes to get the two csv data files. 

The other files in this folder are the usefull files in the embedding_features.py and the local_voltage_plt.py. 
- Transfer_learning

The files in this folder are the main file for the model training for the prediction of Na, K, Mg, Ca, Zn, Y, and Al-ion battery electrod voltages respectively.
- Trained_model

Here are the trained models for the voltage predictions of the corresponding metal-ion battery electrodes.
The model_best.pth file is trained on Li-ion battery electrodes dataset. It can be used for the Li-ion battery electrode voltage prediction. It also used to predict the voltages for the Rb and Cs-ion battery electrodes.
The model_best_Na.pth file is trained on Na-ion battery electrodes dataset and also used for the Na-ion battery electrode voltage prediction.
The model_best_K.pth file is trained on K-ion battery electrodes dataset and also used for the K-ion battery electrode voltage prediction.
The model_best_Mg.pth file is trained on Mg-ion battery electrodes dataset and also used for the Mg-ion battery electrode voltage prediction.
The model_best_Ca.pth file is trained on Ca-ion battery electrodes dataset and also used for the Ca-ion battery electrode voltage prediction.
The model_best_Zn.pth file is trained on Zn-ion battery electrodes dataset and also used for the Zn-ion battery electrode voltage prediction.
The model_best_Y.pth file is trained on Y-ion battery electrodes dataset and also used for the Y-ion battery electrode voltage prediction.
The model_best_Al.pth file is trained on Al-ion battery electrodes dataset and also used for the Al-ion battery electrode voltage prediction.
- data

This folder contains the required data for the model training and the coresponding code to get these data files.
- SVR_KRR_RFR

Here are the SVR (Supporting Vector Regression), KRR (Kernel Ridge Regression), and RFR (Random Forest Regression) model that are used in our work. 

## Web-tool
A convenient web tool has been builed for the voltage prediction of all the metal-ion battery electrodes.


