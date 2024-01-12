# **Enhancing Gutenberg Book Classification using Advanced NLP Techniques**
The project aimed to classify Gutenberg texts accurately. Employing advanced NLP methodologies, it covered collection, preprocessing, feature engineering, and model evaluation for literary work classification. as part of the University of Ottawa's 2023 NLP course.
  - Required libraries: scikit-learn, pandas, matplotlib.
  - Execute cells in a Jupyter Notebook environment.
  - The uploaded code has been executed and tested successfully within the [Google Colab](https://colab.google/) environment.


## Multi-class classification problem
Text Classification Task  to categorize a 5 Gutenberg texts into their respective literary works or books.

```python
selected_books = ['austen-emma.txt','carroll-alice.txt','chesterton-brown.txt','edgeworth-parents.txt','shakespeare-hamlet.txt']
```
## **System workflow**
![image](https://github.com/RimTouny/Enhancing-Gutenberg-Book-Classification-using-Advanced-NLP-Techniques/assets/48333870/50da9f32-1b51-487b-9ad1-88d7c54fcc9c)

## **Key Tasks Undertaken**

1. **Data Preparation, Preprocessing and, Cleaning:**
   - Listing all the books in Gutenberg’s library.
     ```python
     {'austen-emma.txt': 'Jane Austen',
     'austen-persuasion.txt': 'Jane Austen',
     'austen-sense.txt': 'Jane Austen',
     'carroll-alice.txt': 'Lewis Carroll',
     'chesterton-ball.txt': 'G.K. Chesterton',
     'chesterton-brown.txt': 'G. K. Chesterton',
     'chesterton-thursday.txt': 'G. K. Chesterton',
     'edgeworth-parents.txt': 'Maria Edgeworth',
     'melville-moby_dick.txt': 'Dick  Herman Melville',
     'shakespeare-caesar.txt': 'William Shakespeare',
     'shakespeare-hamlet.txt': 'William Shakespeare',
     'whitman-leaves.txt': 'Walt Whitman'}
     ```
   - Choose five different books by five different authors belong to the same category (History).
   - Data preparation:
      + Removing stop words.
      + Converting all words to the lower case.
      + Tokenize the text.
      +  Lemmatization is the next step that reduces a word to its base form.

   - Data Partitioning: partition each book into 200 documents, each document is a 100 word record.
     ![image](https://github.com/RimTouny/Enhancing-Gutenberg-Book-Classification-using-Advanced-NLP-Techniques/assets/48333870/22767ff2-c591-448e-beb3-c83c80404050)

   - Data labeling as follows:
      +  austen-emma→ a
      + chesterton-thursday→ b
      +  shakespeare-hamlet→ c
      +  chesterton-ball→ d
      + carroll-alice→ e
    
    - Word Cloud Generation: Generates word clouds displaying the most frequent 100 words in books for each author.
      ![merge_from_ofoct](https://github.com/RimTouny/Enhancing-Gutenberg-Book-Classification-using-Advanced-NLP-Techniques/assets/48333870/042aa42d-2587-4f8b-8a5f-81666ab9f453)

    - Shuffle Dataset
        
2. **Feature Engineering:**
   - Transformation
     + Bag of Word (BOW):It represents the occurrence of words within a document, it involves two things:
        * A vocabulary of known words.
        * A measure of the presence of known words.
     + Term Frequency - Inverse Document Frequency (TF-IDF):a technique to quantify words in a set of documents. We compute         a score for each word to signify its importance in the document and corpus.
     + N-grams
     + Word Embedding (Word2Vec)


![merge_from_ofoct](https://github.com/RimTouny/Enhancing-Gutenberg-Book-Classification-using-Advanced-NLP-Techniques/assets/48333870/731f785c-196d-482f-9c65-cfab0f824dba)

   - Encoding
3. **Modeling:** For each technique of the above, these following models are trained and tested.
   + Random Forest
   + Gaussian Naive Bayes
   + K Nearest Neighbors
     
4. **Model Evaluation**
   - BOW
      <p align="center">
        <img src="https://github.com/RimTouny/Enhancing-Gutenberg-Book-Classification-using-Advanced-NLP-Techniques/assets/48333870/3f909d6f-87f7-4f76-87d6-a257740eb5c7"/>
      </p>

   - TF-IDF
      <p align="center">
        <img src="https://github.com/RimTouny/Enhancing-Gutenberg-Book-Classification-using-Advanced-NLP-Techniques/assets/48333870/19265217-c676-4406-ab2d-301aafb7efc2"/>
      </p>

   - N-grams
      <p align="center">
        <img src="(https://github.com/RimTouny/Enhancing-Gutenberg-Book-Classification-using-Advanced-NLP-Techniques/assets/48333870/cd056c7b-a18c-4f1d-ab5f-a0d55d90d125"/>
      </p>
     
   - Word2Vec
      <p align="center">
        <img src="https://github.com/RimTouny/Enhancing-Gutenberg-Book-Classification-using-Advanced-NLP-Techniques/assets/48333870/ca1deacc-8aac-4b4c-972d-dc3d44727d09"/>
      </p>

    
5. **Error Analysis of Champion Model**:
```python
Best Model= Gaussian Naive Bayes
Accacruy and Champion Embedding: [0.98, 'N-Grams']
```
    
  - By reducing the number of words, it will lead to reduce the accuracy of our champion model

     <p align="center">
      <img src="https://github.com/RimTouny/Enhancing-Gutenberg-Book-Classification-using-Advanced-NLP-Techniques/assets/48333870/e4f814b2-9010-4fd8-b6fd-b63411ff5112"/>
    </p>

- Indicate that the n estimators’ parameter is not significantly impacting the model's performance on our dataset.

     <p align="center">
      <img src="https://github.com/RimTouny/Enhancing-Gutenberg-Book-Classification-using-Advanced-NLP-Techniques/assets/48333870/e4b80ce7-e39c-4fbc-a28b-897b336dbcc7)"/>
    </p>

