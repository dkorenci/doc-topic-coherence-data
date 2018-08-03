This package contains data for the experiments from the article
"Document-based Topic Coherence Measures for News Media Text"
https://doi.org/10.1016/j.eswa.2018.07.063
If you use the data for scientific research, please cite the original article. 

All the data in this package, as well as the linked data described below
is licensed under Attribution-ShareAlike 4.0 International license.

The companion code is located at: https://github.com/dkorenci/doc-topic-coherence

This package contains the basic dataset consising of serialized topic models, 
model topic annotations, and xlsx tables linking semantic topics to model topics. 
It also contains serialized dictionaries used to build the models.
The 'uspol' folder contains the US news topics dataset and 
the 'croelect' folder contains the Croatian news topics dataset.

The dataset of labeled topics is created by loading model topics
from serialized topic models and labeling them, using data from 
the model annotations and tables linking semantic topics to model topics.
This labeling procedure is described in the Section 4.1 of the article.
Final topics labels and the test-dev split of US topics are fixed, 
serialized in the files alltopics_labeled.pickle and dev_test_split.pickle 
The serialized versions are used for the experiments. 
More information is provided in the code package. 

Other resources needed to replicate the experiments consist of 
word2vec and glove embeddings, lucene wikipedia indices for palmetto, and resources 
such as bag-of-words and tf-idf vectors and documents indexed with topic weights. 
These resources are provided as external download.

All resources except the lucene indices are here: https://rebrand.ly/doc-coh-resource-cache
Lucene indices are here: https://rebrand.ly/doc-coh-lucene-indices

More information about setting up the resources can be found in the code package.

The settings.py has to be configured to point to all the resources
in order for the experiments to work properly. 
More information about setting up the resources can be found in the code package.

We do not provide the original corpora since we do not hold the copyright to the news articles. 
However, the resources package (resource_cache folder) contains all the
corpora-derived resources needed for coherence calculation: 
bag-of-words and tf-idf matrices, documents indexed with topic weights etc. 
These cached resources are loaded if present in which case the corpora need not to be accessed.
