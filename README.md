# What can Latent Dirichlet Allocation topic modeling say about ecosystems?

The files presented in this repository complement the work carried out on the poster `What can Latent Dirichlet Allocation topic modeling say about ecosystems?`. Each of the files found is explained below:

1. `raw data`, contains the original downloaded files from the Web of Science (WOS)
2. `README.md`, it is this document, which allows observing the number of documents collected by each ecosystem. It also contains the links for the descriptive analysis and the topic model carried out.
3. `stopwords_personal.csv`, contains unwanted words to be removed in the analysis of the topics.
4. `topic_model.csv`, contains the database with all the documents of WOS.


### Ecosystems analyzed

* `BusE` Business ecosystem
* `DatE` Data
* `DigE` Digital
* `EntE` Entreprenurial
* `HE` Health or Healthcare
* `IndE` Industrial
* `InfE` Information
* `InnE` Innovation
* `KnowE` Knowledge
* `OSE` Open source
* `PlatE` Platform
* `SerE` Service
* `SofE` Software
* `Doc`, it conglomerates the articles and proceedings found in WOS, without taking into account the literature reviews.
* `Rev`, gathers only literature reviews


```python
import metaknowledge as mk
import pandas as pd
```

**Number of documents found for each ecosystem**, without considering literature reviews.


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



**Number of literature reviews found for each ecosystem**


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



**The following links show the process carried out.**

1. [Descriptive analysis.](http://innovadata.ca/ecosystem/descriptive.html)
2. [Topic model](http://innovadata.ca/ecosystem/topic.html)
