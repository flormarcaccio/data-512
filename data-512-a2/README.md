# A2 - Bias in data

### Project Goal
The goal of this project is to identify possible sources of bias in the Wikipedia Talk corpus, which consists of datasets labelled for "toxicity", "aggression", and "personal attacks". Each of these datasets contains comments from discussion posts made by Wikipedia editors that crowdworkers labelled on whether or not they contain hostile speech. For more information on this research and the corpus please visit the [Detox wiki page](https://meta.wikimedia.org/wiki/Research:Detox).

These annotated datasets are used by Google data scientists to train machine learning models that have been used in many software products and made freely accessible to anyone through the Perspective API ( [Github](https://meta.wikimedia.org/wiki/Research:Detox), [landing](https://www.perspectiveapi.com/#/)). 

### Analysis Questions
This analysis is going to be focused on answering two main question:

* **Does the gender of a worker affect the toxicity score they assign to comments?**

* **Is the age of the worker a factor when identifying aggressive comments?**


### Data Sources

For this analysis I will be using two of the three datasets, Toxicity and Aggression, which can be found on [this Figshare site](https://figshare.com/projects/Wikipedia_Talk/16731).

To reproduce the analysis, yo can either download from the previous link all six files (three per dataset), or you can execute the commands in the "Downloading Toxicity and Agression datasets" section in the hcds-a2-data-bias.ipynb file.

* [Toxicity dataset](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release#Toxicity): Crowdworkers annotated 160k comments (most times a comment was annotated by multiple workers to improve accuracy) on a spectrum of how toxic the comment is to how healthy to conversation the contribution is. There are three files associated with this dataset:
    * [Schema for toxicity_annotations.tsv](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release#Schema_for_toxicity_annotations.tsv)
    * [Schema for toxicity_annotated_comments.tsv](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release#Schema_for_{attack/aggression/toxicity}_annotated_comments.tsv)
    * [Schema for toxicity_worker_demographics.tsv](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release#Schema_for_{attack/aggression/toxicity}_worker_demographics.tsv)  

* [Aggression dataset](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release#Aggression): Crowdworkers annotated 100k comments (most times a comment was annotated by multiple workers to improve accuracy) on how aggressive the comment was perceived to be. There are three files associated with this dataset:
    * [Schema for aggression_annotations.tsv](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release#Schema_for_aggression_annotations.tsv)
    * [Schema for aggression_annotated_comments.tsv](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release#Schema_for_{attack/aggression/toxicity}_annotated_comments.tsv)
    * [Schema for aggression_worker_demographics.tsv](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release#Schema_for_{attack/aggression/toxicity}_worker_demographics.tsv)


### Project License

Plese refer to the project [MIT license](LICENSE) for more details.


