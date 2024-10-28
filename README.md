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

A dataset of article metadata was downloaded from OpenAlex. OpenAlex was chosen as the data source, as this will allow for comparisons with other research running within the same project at this institute. The search string used was:
`Scholarly document processing AND (bibliometry OR bibliometrics) AND type is article AND open access is true`

[This search yielded 5540 results](https://openalex.org/works?page=1&filter=default.search%3Ascholarly%20document%20processing%20AND%20%28bibliometry%20OR%20bibliometrics%29,type%3Atypes%2Farticle,open_access.is_oa%3Atrue). The dataset was downloaded in EndNote format. The data was [uploaded into HubMeta](https://dashboard.hubmeta.com/project/5413/import-articles/files) for further processing using the tools provided by HubMeta:
* Duplicate removal (123 duplicates were removed)
* AI-assisted title and abstract screening
  
