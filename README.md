# Topic Modeling on IMDb Movie Reviews

## Overview

This project applies **Latent Dirichlet Allocation (LDA)** to analyze IMDb movie reviews and uncover latent themes within large-scale textual data. The goal is to identify common discussion topics such as storyline, characters, emotional impact, and overall movie quality through unsupervised learning.

---

## Dataset

- **Source:** IMDb Movie Reviews Dataset  
- **Size:** 50,000 reviews  
- **Feature used:** Review text only  

All missing and empty entries were removed prior to modeling.

---

## Methodology

### 1. Text Preprocessing
Text preprocessing was performed using **NLTK**, including:
- Lowercasing
- Removal of non-alphabetic characters
- Tokenization
- Stopword removal
- Lemmatization

### 2. Feature Engineering
- Constructed a **Document-Term Matrix (DTM)** using `CountVectorizer`
- Parameters:
  - `max_df = 0.9`
  - `min_df = 10`
  - English stopwords removed

### 3. Topic Modeling
- Applied **Latent Dirichlet Allocation (LDA)**
- Initial model tested with 3, 5, and 7 topics
- **GridSearchCV** used for hyperparameter tuning

### 4. Model Optimization
- Optimal configuration:
  - **Number of topics:** 3
  - **Learning decay:** 0.5

---

## Results

### Extracted Topics

- **Topic 1:** story, character, scene, movie, film  
- **Topic 2:** love, life, character, story, movie  
- **Topic 3:** good, bad, watch, movie, film  

The results indicate that IMDb reviews primarily focus on narrative elements, emotional responses, and overall viewing experience.

---

## Visualization

- **pyLDAvis** for interactive topic exploration
- **Word clouds** to highlight dominant keywords per topic

---

## Discussion

- **Strengths:**  
  - LDA effectively captured broad and interpretable themes  
  - Large dataset improved topic stability  

- **Limitations:**  
  - Topic overlap due to common movie-related vocabulary  
  - Short reviews reduced topic separation clarity  

---

## Conclusion

This project demonstrates the effectiveness of LDA in extracting meaningful themes from unstructured text data. Future work may incorporate contextual topic models or integrate sentiment analysis for deeper insights.

---

## Author

**Yun Chia Lee**  
