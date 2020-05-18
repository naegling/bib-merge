# bib-merge
Merges bibtex files after checking for duplicate citekeys and similar titles

Requirements:
* python3
* python packages: 
  * nltk (Natural Language ToolKit)
  * bibtexparser
* nltk downloads('stopwords', 'punkt', 'wordnet', 'averaged_perceptron_tagger')

bib-merge compares citekeys directly, character by character.

bib-merge compares titles as a series of tokens derived by dropping stop words from the title and lemmatizing the remaining words.
