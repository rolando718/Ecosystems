# What can Latent Dirichlet Allocation topic modeling say about ecosystems?

1. [Descriptive analysis.](http://innovadata.ca/ecosystem/descriptive.html)
2. [Topic model](http://innovadata.ca/ecosystem/topic.html)


```python
import metaknowledge as mk
import pandas as pd
```


```python
eco = pd.read_excel('2_generated_datasets/Ecosystems.xlsx', sheet_name='ecosystems')
```


```python
eco[list(eco.loc[:, "BusE": "Rev"])].sum()
```




    BusE      665
    DatE      194
    DigE      510
    EntE      379
    HE        343
    IndE      259
    InfE      128
    InnE      631
    KnowE      84
    OSE        29
    PlatE     116
    SerE      380
    SofE      427
    Doc      4145
    Rev         0
    dtype: int64




```python
rev = pd.read_excel('2_generated_datasets/Reviews.xlsx', sheet_name='rev')
```


```python
rev[list(rev.loc[:, "BusE": "Rev"])].sum()
```




    BusE      49
    DatE       6
    DigE      10
    EntE      20
    HE        11
    IndE       7
    InfE       2
    InnE      43
    KnowE      5
    OSE        2
    PlatE      3
    SerE      13
    SofE      21
    Doc        0
    Rev      192
    dtype: int64


