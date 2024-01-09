# Enhancing-Gutenberg-Book-Classification-using-Advanced-NLP-Techniques
The project aimed to classify Gutenberg texts accurately. Employing advanced NLP methodologies, it covered collection, preprocessing, feature engineering, and model evaluation for literary work classification. as part of the University of Ottawa's 2023 NLP course.
  - Required libraries: scikit-learn, pandas, matplotlib.
  - Execute cells in a Jupyter Notebook environment.

## Multi-class classification problem
Text Classification Task  to categorize a 5 Gutenberg texts into their respective literary works or books.

```python
selected_books = ['austen-emma.txt','carroll-alice.txt','chesterton-brown.txt','edgeworth-parents.txt','shakespeare-hamlet.txt']
```

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
        
3. **Feature Engineering:**
4. **Modeling:**
5. **Model Evaluation**
6. **Error Analysis of Champion Model**
