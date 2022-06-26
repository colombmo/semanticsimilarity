# Semantic Similarity for Spectral Similarity

This is a library allowing to compute the spectral semantic similarity between adjectives and adverbs based on the overlaps of their second order synonyms, as presented in:

	Colombo, Moreno, and Edy Portmann. "Semantic Similarity Between Adjectives and Adverbs—The Introduction of a New Measure." Soft Computing for Biomedical Applications and Related Topics. Springer, Cham, 2021. 103-116. https://doi.org/10.1007/978-3-030-49536-7_10

## Setup

The first thing to do is to clone the repository:

```sh
$ git clone https://github.com/colombmo/semanticsimilarity.git
$ cd semanticsimilarity
```

Create a virtual environment to install dependencies in and activate it:

```sh
$ virtualenv2 --no-site-packages env
$ source env/bin/activate
```

Then install the dependencies:

```sh
(env)$ pip install -r requirements.txt
```

Note the `(env)` in front of the prompt. This indicates that this terminal
session operates in a virtual environment set up by `virtualenv2`.

The similarity package has to be instantiated as follows before using its functions:
```python
from util.similarity import Similarity
self.similarity = Similarity()
``` 

Then, the following functions from the `similarity.py` module can be used:

```python
similarity.sim_lvl1(word1, word2) # Find the similarity between word1 and word2 based on the overlap of their first-level synonyms
similarity.sim_lvl2(word1, word2) # Find the similarity between word1 and word2 based on the overlap of their second-level synonyms
```