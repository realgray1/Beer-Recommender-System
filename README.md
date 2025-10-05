# Unstructured Data Projects
University of Texas at Austin – MSBA Program

This repository contains two applied NLP projects completed for the *Unstructured Data Analytics* course at the McCombs School of Business. Both projects focus on transforming raw text into structured insights using data science methods. The goal was to design reproducible workflows that extract, clean, and model unstructured text data for measurable outcomes.

Each project showcases the full data science lifecycle of web scraping, data preparation, natural language processing, and insight generation applied to real-world, messy datasets.

---

## Project 1: Car Brand Perception Analysis

### Overview
This project analyzes user-generated automotive forum data to understand how consumers talk about different car brands and how brand names co-occur in conversation.  
The focus was on identifying key discussion clusters, relationships between competing brands, and overall consumer sentiment based on word frequency and co-occurrence patterns.

### Key Steps
- **Data Collection:** Automated scraping of 8,000+ comments using Selenium and XPath.  
- **Text Preprocessing:** Cleaned and tokenized text, removed stopwords, and standardized model/brand mentions using NLTK.  
- **Entity Mapping:** Built a reference table to link car models to parent brands for more accurate aggregation.  
- **Brand Network Analysis:** Constructed co-mention matrices and visualized brand relationships using `itertools` and `Counter`.  
- **Insight Extraction:** Identified dominant brands, competitive overlaps, and recurring sentiment patterns.

### Impact
- Automated the collection and analysis of large-scale unstructured consumer feedback.  
- Quantified cross-brand relationships that could inform marketing and competitive positioning strategies.  
- Demonstrated scalable NLP techniques applicable to other product-review and brand-monitoring problems.

### Technical Stack
Python, Selenium, Pandas, NLTK, Regex, Matplotlib

### Files
- `car_brand_analysis.ipynb` – analysis workflow  
- `car_forum_comments.csv` – scraped dataset  
- `car_models_and_brands.csv` – model-to-brand mapping  

---

## Project 2: Beer Review Recommendation System

### Overview
This project builds a text-based recommendation system using semantic similarity in user reviews. It compares multiple NLP techniques to identify which representation best captures nuanced product characteristics like flavor, texture, and aroma.

### Key Steps
- **Data Collection:** Scraped 10,000+ beer reviews and metadata from BeerAdvocate.  
- **Text Processing:** Tokenized and normalized review text, removed noise, and ensured consistent formatting.  
- **Feature Engineering:**  
  - TF-IDF vectorization for baseline similarity.  
  - SpaCy embeddings (`en_core_web_md`) for semantic similarity.  
  - Custom Word2Vec embeddings trained with Gensim on beer-specific text to capture domain language.  
- **Recommendation Engine:** Modeled user flavor preferences (e.g., *coffee, chocolate, vanilla*) and generated ranked beer recommendations.  
- **Model Evaluation:** Compared similarity outputs across embedding types and visualized top-N overlap between methods.

### Impact
- Built a reproducible pipeline demonstrating end-to-end NLP model development.  
- Showed how embedding methods can influence recommendation quality and interpretability.  
- Illustrates the type of domain adaptation often required in real-world NLP applications.

### Technical Stack
Python, Pandas, Scikit-Learn, SpaCy, Gensim, TF-IDF, Cosine Similarity

### Files
- `beer_recommendation.ipynb` – core pipeline and model comparison  
- `custom_word_embeddings.ipynb` – Word2Vec embedding model implementation  
- `beer_reviews.csv`, `beer_stats.csv` – datasets used for training and evaluation  

---

## Skills and Methods Demonstrated

| Category | Tools & Techniques |
|-----------|-------------------|
| Data Acquisition | Selenium Web Scraping, HTML Parsing, XPath Automation |
| Text Processing | Tokenization, Stopword Removal, Lemmatization |
| Feature Engineering | TF-IDF, Word2Vec, Embedding Aggregation |
| Similarity Modeling | Cosine Similarity, Vector Space Modeling |
| NLP Modeling | SpaCy Embeddings, Gensim Word2Vec |
| Data Visualization | Pandas, Matplotlib |
| Reproducibility | Clean Notebook Pipelines, Modular Code Design |

---

## Repository Structure
```
unstructured-data-projects/
│
├── car_brand_analysis/
│   ├── car_brand_analysis.ipynb
│   ├── car_forum_comments.csv
│   ├── car_models_and_brands.csv
│
├── beer_recommendation/
│   ├── beer_recommendation.ipynb
│   ├── custom_word_embeddings.ipynb
│   ├── beer_reviews.csv
│   ├── beer_stats.csv
│
└── README.md
```

---

## Author
**Dean Carpenter**  
M.S. in Business Analytics (Class of 2026)  
McCombs School of Business, University of Texas at Austin  
Location: Austin, TX  
Email: dc53332@my.utexas.edu  
LinkedIn: [https://www.linkedin.com/in/dean-carpenter-ut/](https://www.linkedin.com/in/dean-carpenter-ut/)
