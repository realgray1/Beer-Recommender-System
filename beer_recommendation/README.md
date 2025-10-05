# Beer Recommendation System

This repository implements a content‑based recommendation system for craft beers using scraped reviews from BeerAdvocate. The goal is to suggest beers that match a user’s desired flavor, aroma, and texture descriptors.

## Key components

- **Data scraping (Task A):** `beer_recommendation.ipynb` includes optional Selenium code to scrape beer names, breweries, statistics, and reviews from BeerAdvocate. The provided datasets (`beer_reviews.csv` and `beer_stats.csv`) enable you to run the analysis without scraping.
- **Text preprocessing (Task B):** Reviews are cleaned, lower‑cased, and vectorized using TF‑IDF. Cosine similarity between beers is computed based on aggregated review texts.
- **SpaCy embeddings (Task C):** When available, SpaCy’s pretrained word vectors provide semantic similarity between beer descriptions.
- **Custom embeddings (Task D):** `custom_word_embeddings.ipynb` trains Word2Vec models on the beer corpus to generate domain‑specific embeddings. These embeddings capture nuanced relationships (e.g., between “roasty” and “coffee”) and improve recommendation quality.
- **Interactive recommendation:** By specifying a list of attributes (e.g., `['chocolate','vanilla','smooth']`), the system ranks beers that best match the requested profile.

## Files

| File | Description |
| --- | --- |
| `beer_recommendation.ipynb` | Main notebook: scraping, preprocessing, TF‑IDF similarity, SpaCy and custom embedding integration. |
| `custom_word_embeddings.ipynb` | Notebook demonstrating how to train Word2Vec embeddings on the beer reviews. |
| `beer_reviews.csv` | Cleaned beer review data with product name, review text, user rating, and normalized clean text. |
| `beer_stats.csv` | Beer metadata (name, brewery, and statistics). |

## Requirements

This project requires Python 3 and the following packages:

- `pandas` and `numpy`
- `scikit‑learn` for TF‑IDF and cosine similarity
- `nltk` for text preprocessing and sentiment analysis
- `gensim` for training custom word embeddings
- `spacy` for pretrained embeddings (optional)
- `selenium` for web scraping (optional)

Install dependencies using pip:

```bash
pip install pandas numpy scikit-learn nltk gensim spacy selenium
```

To use SpaCy embeddings, download the model via:

```bash
python -m spacy download en_core_web_md
```

## Usage

1. Launch Jupyter Notebook or VS Code.
2. Open `beer_recommendation.ipynb`. If you have the data ready, skip the scraping section.
3. Follow the notebook to preprocess reviews, compute similarities, and input your desired attributes to obtain recommendations.
4. Optionally, run `custom_word_embeddings.ipynb` to train domain‑specific embeddings and incorporate them into the similarity computation.

## Notes

- The scraping code is provided for completeness but may need adaptation if website structures change.
- Training Word2Vec models can take several minutes depending on corpus size and parameters.

