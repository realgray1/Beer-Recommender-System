# Car Brand Analysis

This project analyzes user comments from an automotive forum to quantify the popularity of different car brands and explore how they are discussed together. The workflow includes:

- **Data collection:** Comments are scraped from an online car discussion forum (see `car_brand_analysis.ipynb` for the scraping pipeline).
- **Data preprocessing:** Comments are cleaned and tokenized. A lookup table (`car_models_and_brands.csv`) maps car models to their brands.
- **Brand identification:** Each comment is scanned for model names and converted to their corresponding brands.
- **Frequency analysis:** The frequency of each brand’s mentions is calculated to identify the most talked–about brands.
- **Co‑occurrence analysis:** Brand co‑occurrence pairs are generated to examine which brands are frequently discussed together.

## Files

| File | Description |
| --- | --- |
| `car_brand_analysis.ipynb` | Jupyter notebook containing the scraping pipeline and analysis. |
| `car_models_and_brands.csv` | Lookup table mapping car models to brands. |
| `car_forum_comments.csv` | Sample of scraped forum comments used in this analysis. |

## Requirements

The notebook uses Python 3 and the following key libraries:

- `pandas` for data manipulation
- `nltk` for tokenization and stop words
- `itertools` and `collections.Counter` for co‑occurrence counting
- `selenium` for web scraping (only needed if re–scraping the forum)

Install dependencies with pip:

```bash
pip install pandas nltk selenium
```

## Usage

1. Open `car_brand_analysis.ipynb` in Jupyter Notebook or VS Code.
2. Run the cells sequentially. The notebook scrapes comments (if executed), loads the provided dataset, performs frequency and co‑occurrence analyses, and displays the results.
3. Modify or extend the analysis as desired.

## Notes

- Web scraping is subject to website terms and may require throttling or user authentication. The provided dataset (`car_forum_comments.csv`) allows you to reproduce the analysis without scraping.

