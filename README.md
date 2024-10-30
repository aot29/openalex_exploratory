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

## Using plain Python
```
cd ~/
python3 -m venv openalex_exp
source openalex_exp/bin/activate
cd workspace/openalex_exploratory/
pip3 install -r requirements.txt
```

```
source openalex_exp/bin/activate
cd workspace/openalex_exploratory/
jupyter lab
```

## Get the dataset
Metadata on publications in a scientific field, obtained from OpenAlex, is used to construct a topic network map of the field. 
Some prospective fields:
* Scholarly document processing

A dataset of article metadata was downloaded from OpenAlex. OpenAlex was chosen as the data source, as this will allow for comparisons with other research running within the same project at this institute. The search string used was:
`"scholarly document processing" OR "scientific document processing" OR "scholarly publishing" AND type is article AND (topic is "Bibliometric Analysis and Research Evaluation" OR field is "Computer Science")`

This search yielded 4411 results. The dataset was downloaded in EndNote format. The data was [uploaded into HubMeta](https://dashboard.hubmeta.com/project/5413/import-articles/files) for further processing using the tools provided by HubMeta:
* Duplicate removal (280 duplicates were removed)
* Titles and abstracts were screened manually. Criteria for inclusion: the paper is about scholarly document processing. Criteria for exclusion: the paper has no abstract, the paper is in a language other than english.
* The metadata and abstracts of selected 1689 papers (42% of original data set) were exported in RIS format

## Notebooks

1. Cleanup the data: 01_clean_and_tokenize.ipynb
2. Fit a model: 02_fit_ensemble_LDA.ipynb
3. Use LLM to name the topics: 03_mistral.ipynb
4. Create a topic network graph: 04_Topic_graph.ipynb
