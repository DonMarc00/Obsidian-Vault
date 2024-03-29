- **Unstructured data: **
- **Corpus: **
- **Term: ** A word enriched with several attributes
- **Stemming: ** Stem results in truncated/chopped words (not necessarily a complete word) Stemming is syntactic and fast - follows an algorithm
	-Example: amuse, amusing, amused --> amus
- **Lemmatization: ** Lemma results in an actual language word (inflection free) Lemmatization is semantic and slow - follows linguistic dictionary
	-Example: am, is, are --> be
- **Stop words: **
- **Tokens: **
- **Part of speech tags: ** Labels that can be assigned to a word to describe its linguistic function i.e. adjective, noun, verb, personal pronoun, adverb etc.
- **Bag of Words: ** Tuples of documents and terms. Each term is assigned separately to a document like this:
   ![[Pasted image 20240201233457.png]] ^d42882
- **Term by document matrix: ** Flat file where the cells are populated with the term frequencies -> Each column represents a term/word
- **Document vectors: ** Numerical representations of documents:
  ![[Pasted image 20240202143521.png]]
**Frequencies: ** Number of occurrences of terms. Distinction between absolute and relative as well as locally (in documents - TF ) and globally (in corpus - IDF )  ^61f236