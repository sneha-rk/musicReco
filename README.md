# musicReco

In this repo we have methods to download, clean the last.fm 1k and use the 
dataset to evaluate recommendation and rating prediction methods.

Requirements:

1) Python 2.7
2) numpy
3) mrec
4) sklearn
5) scipy


Files:

1) Baselines.ipynb - We can run the baselines, wrmf and bmf using this notebook.
Dataset is downloaded if not present and cleaned for use.
2) bmf.py - Class object for BMF. 
		  - For WRMF, mrec may be used.
3) metrics.py - Library computing metrics used in paper.
4) msbmf.py - Class object incorporating music sequence information 
into the training the latent factors using bmf.
5) mswrmf.py - Class object incorporating music sequence information. Based off the mrec library. 
into the training the latent factors using bmf.
6) preprocess.py - Script to load and preprocess dataset.
7) run_ms.py - Script to run msbmf. Assumes 6) and 10) have
been run.
8) run_msw.py - Script to run mswrmf. Assumes 6) and 10) have
been run.
9) utils.py - Utility functions for loading dataset and trained song vectors.
10) word2vec.py - To train music sentences using song2vec

To run:
 python word2vec.py -train musics-sentences.txt -model song2vec.txt -cbow 1 -dim 100 -window 5 -min-count 5

 