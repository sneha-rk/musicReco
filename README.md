# musicReco

Implementation of Cheng, Zhiyong, et al. "Exploiting Music Play Sequence for Music Recommendation." IJCAI International Joint Conference on Artificial Intelligence. International Joint Conferences on Artificial Intelligence, 2017.

### Requirements: 
Python 2.7, numpy, mrec, sklearn, scipy


### To load and preprocess dataset
preprocess.py

### To train word vectors
word2vec.py - To train music sentences using song2vec

To run: python word2vec.py -train musics-sentences.txt -model song2vec.txt -cbow 1 -dim 100 -window 5 -min-count 5

### Recommendation Methods

bmf.py  - BMF. For WRMF, mrec may be used.

msbmf.py - Recommender incorporating music sequence information into the training the latent factors using bmf.

mswrmf.py - Recommender incorporating music sequence information into the training the latent factors using bmf. Based off the mrec library.


### Putting it all together
Baselines.ipynb - Run the baselines, wrmf and bmf. Dataset is downloaded if not present and cleaned for use.

run_ms.py - Script to run msbmf. Assumes data has been preprocessed and word vectors have been trained.

run_msw.py - Script to run mswrmf. Assumes data has been preprocessed and word vectors have been trained.

### Others
metrics.py, 
utils.py - Loading dataset and trained song vectors

 
