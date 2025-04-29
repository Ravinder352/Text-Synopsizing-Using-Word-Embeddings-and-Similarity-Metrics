# Text-Synopsizing-Using-Word-Embeddings-and-Similarity-Metrics
# Text Summarization Project  

## Overview  
This project focuses on **extractive summarization**, which selects important sentences directly from the original text to generate a concise summary.  

### Types of Summarization:  
- **Extractive Summarization:** Picks key sentences as they are.  
- **Abstractive Summarization:** Generates new sentences conveying the same meaning (more akin to human summarization).  
------------------------------------------------------
## Here I am implementing Extractive Summarization
------------------------------------------------------
## How the System Works  

### 1. Text Pre-processing  
- Breaks text into paragraphs, sentences, and words.  
- Converts all text to lowercase.  
- Removes stopwords (e.g., "the", "is"), punctuation, and unwanted characters.  
- Cleans data to prepare for feature extraction.  

### 2. Word Embedding (Using Word2Vec)  
- Converts words into numerical vectors.  
- Captures semantic meanings—similar words have similar vectors, e.g., “man” and “boy”.  

### 3. Feature Extraction (TF-IDF)  
- Computes Term Frequency-Inverse Document Frequency.  
- Identifies significant words in the text; high TF-IDF scores imply importance.  
- These important words form the centroid (central idea) of the text.  

### 4. Sentence Scoring (Cosine Similarity)  
- Measures similarity between each sentence and the centroid.  
- Sentences most similar to the centroid are deemed more important.  

### 5. Sentence Selection and Redundancy Check  
- Selects top-ranked sentences.  
- Eliminates redundant or repetitive sentences to improve diversity.  

### 6. Summary Generation  
- Assembles the selected sentences in a logical order.  
- Produces the final, concise summary.  

## Dataset Used  
**BBC News Dataset** (from Kaggle)  
Contains news articles from five categories:  
- Business  
- Politics  
- Entertainment  
- Sports  
- Technology  

## Performance Evaluation  
Uses the **ROUGE** metric (Recall-Oriented Understudy for Gisting Evaluation) to assess summarization quality:  
- **Precision (P):** Relevance of selected sentences.  
- **Recall (R):** Coverage of relevant sentences.  
- **F-Score (F):** Harmonic mean balancing Precision and Recall.  

---  

Feel free to customize further or add installation instructions, usage examples, and authorship details!  
