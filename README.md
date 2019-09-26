# pyclustertend [![Build Status](https://travis-ci.com/lachhebo/pyclustertend.svg?branch=master)](https://travis-ci.com/lachhebo/pyclustertend)  [![PyPi Status](https://img.shields.io/pypi/v/pyclustertend.svg?color=brightgreen)](https://pypi.org/project/pyclustertend/) [![Documentation Status](https://readthedocs.org/projects/pyclustertend/badge/?version=master)](https://pyclustertend.readthedocs.io/en/master/) [![Downloads](https://pepy.tech/badge/pyclustertend)](https://pepy.tech/project/pyclustertend) [![codecov](https://codecov.io/gh/lachhebo/pyclustertend/branch/master/graph/badge.svg)](https://codecov.io/gh/lachhebo/pyclustertend)




## Presentation : 

pyclustertend is a python package to do cluster tendency. Cluster tendency consist to assess if clustering algorithms are relevant for a dataset.


Three methods for assessing cluster tendency are currently implemented  :

- [x] Hopkins Statistics 
- [x] VAT
- [x] iVAT
- [x] Metric based method (silhouette, calinksi, davies bouldin)

## Installation : 

```shell
    pip install pyclustertend
```

## Usage : 

### Example Hopkins : 

```python
    >>>from sklearn import datasets
    >>>from pyclustertend import hopkins
    >>>from sklearn.preprocessing import scale
    >>>X = scale(datasets.load_iris().data)
    >>>hopkins(X,150)
    0.18950453452838564
```

### Example VAT :

```python
    >>>from sklearn import datasets
    >>>from pyclustertend import vat
    >>>from sklearn.preprocessing import scale
    >>>X = scale(datasets.load_iris().data)
    >>>vat(X)
```

<img height="350" src="https://raw.githubusercontent.com/lachhebo/pyclustertend/screenshots/vat.png" />


### Example Metric : 


```python
    >>>from sklearn import datasets
    >>>from pyclustertend import assess_tendency_by_metrics
    >>>from sklearn.preprocessing import scale
    >>>X = scale(datasets.load_iris().data)
    >>>assess_tendency_by_metrics(X)
    2.0
```
