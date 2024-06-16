## Distributional Word Vectors Project

### Overview
This project involves implementing and experimenting with methods for creating word vectors based on distributional semantics. The project uses a dataset of sentences from English Wikipedia and evaluates the created word vectors using provided datasets.

### Objectives
1. **Implement Distributional Counting**: Count the number of times a word appears in a context window around another word.
2. **Incorporate Inverse Document Frequency (IDF)**: Modify word vectors to account for the frequency of context words.
3. **Calculate Pointwise Mutual Information (PMI)**: Measure the association between words and their contexts.
4. **Evaluate Word Vectors**: Quantitatively and qualitatively analyze the word vectors using similarity datasets and nearest neighbor searches.

### Data Files
- **wiki-1percent.txt**: A sample of English Wikipedia with one sentence per line.
- **men.tsv**: MEN word similarity dataset.
- **simlex-999.tsv**: SimLex-999 word similarity dataset.
- **vocab-5k.txt**: The 5,000 most common words in Wikipedia.
- **vocab-15kws.txt**: 15,000 common words in Wikipedia and evaluation datasets.

### Implementation Steps

#### 1. Distributional Counting
- Count word occurrences within a context window for given vocabularies.
- Use sparse data structures to optimize memory usage.
- Report counts for specified word pairs with different window sizes.

#### 2. IDF-Based Word Vectors
- Extend the counting implementation to incorporate IDF.
- Calculate word vectors with IDF weighting to reduce the impact of common words.
- Evaluate these vectors using word similarity datasets and report improvements.

#### 3. PMI Calculation
- Implement the PMI formula to measure word-context associations.
- Calculate PMIs for a specified word and report context words with the highest and lowest PMI values.
- Evaluate PMI-based word vectors using similarity datasets.

#### 4. Quantitative Comparisons
- Evaluate word vectors created using different methods, window sizes, and context vocabularies.
- Analyze the results and report findings, discussing observed trends and differences between datasets.

#### 5. Qualitative Analysis
- Compute nearest neighbors for specific query words using different window sizes.
- Analyze the part-of-speech patterns and multi-sense word behavior among nearest neighbors.
- Discuss findings and provide examples to support observations.

### Evaluation Metrics
- **Spearman’s Rank Correlation**: Used to compare computed word similarities with human-annotated similarities.
- **Cosine Similarity**: Measures similarity between word vectors.
