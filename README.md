# bib-merge
Merges bibtex files after checking for duplicate citekeys and similar titles

Usage:
```
usage: bib-merge [-h] [-f] [-o OUTPUT] [--download] paper.bib [paper.bib ...]

safe merge of bibtex files

positional arguments:
  paper.bib             input bibtex files

optional arguments:
  -h, --help               show this help message and exit
  -f, --force              force output of merged bib file
  -o FILE, --output FILE   write output to file instead of stdout
  --download               download required nltk datasets

```
Requirements:
* python3
* python packages: 
  * nltk (Natural Language ToolKit)
  * bibtexparser
* nltk datasets ('stopwords', 'punkt', 'wordnet', 'averaged_perceptron_tagger')

`bib-merge` writes detected conflicts to stderr.  Conflicts consist of duplicated citekeys or similar publication titles.  The tool detects similar titles with a few natural language primitives (e.g dropping stop words and lemmatizing the remaining words).   
