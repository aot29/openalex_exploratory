# openalex_exploratory
Explore a subset of OpenAlex

## Using Conda
```
conda create -n openalex_exp python=3.12.2
conda activate openalex_exp
pip install -r requirements.txt
```

```
conda activate openalex_exp
jupyter lab
```

## Get the dataset
Metadata on publications in a scientific field, obtained from OpenAlex, is used to construct a topic network map of the field. 
Some prospective fields:
* Scholarly document processing

A dataset of article metadata was downloaded from OpenAlex. OpenAlex was chosen as the data source, as this will allow for comparisons with other research running within the same project at this institute. The serach string used was:
`"Scholarly document processing" AND type is article AND field is "Computer Science"`

This search yielded 15540 results. The dataset was downloaded in EndNote format. The data was uploaded into HubMeta for further processing using the tools provided by HubMeta:
* Duplicate removal
* AI-assisted title (and abstract) screening
  
