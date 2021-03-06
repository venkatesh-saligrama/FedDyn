# Federated Learning Based on Dynamic Regularization

This is implementation of [Federated Learning Based on Dynamic Regularization](https://openreview.net/pdf?id=B7v4QMR6Z9w).

### Requirements

Please install the required packages. The code is compiled with Python 3.7 dependencies in a virtual environment via

```pip install -r requirements.txt```

### Instructions

Example codes to run FedDyn as well as baseline methods (FedAvg, FedProx and SCAFFOLD) with the synthetic dataset and CIFAR10 is given in ```example_code_synthetic.py``` and ```example_code_cifar10.py```.

#### Generate IID and Dirichlet distributions on various datasets:<br/>
CIFAR-10 IID, 100 partitions, balanced data
```
data_obj = DatasetObject(dataset='CIFAR10', n_client=100, rule='iid', unbalanced_sgm=0)
```
CIFAR-10 Dirichlet (0.6), 100 partitions, balanced data
```
data_obj = DatasetObject(dataset='CIFAR10', n_client=100, unbalanced_sgm=0, rule='Dirichlet', rule_arg=0.6)
```
EMNIST needs to be downloaded from this [link](https://www.nist.gov/itl/products-and-services/emnist-dataset).<br/>
Shakespeare is generated by using [LEAF](https://github.com/TalwalkarLab/leaf). 

The example codes construct the federated datasets, train methods and plot convergence curve.

### Citation

```
@inproceedings{
acar2021federated,
title={Federated Learning Based on Dynamic Regularization},
author={Durmus Alp Emre Acar and Yue Zhao and Ramon Matas and Matthew Mattina and Paul Whatmough and Venkatesh Saligrama},
booktitle={International Conference on Learning Representations},
year={2021},
url={https://openreview.net/forum?id=B7v4QMR6Z9w}
}
```