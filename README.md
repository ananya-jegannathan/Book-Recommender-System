# Book-Recommender-System

A book recommendation system built using collaborative filtering on Goodreads data. The system constructs a sparse user-book ratings matrix and applies two matrix completion algorithms to fill in missing ratings, then compares their performance.

## Data Files

The original Goodreads dataset is large; this repo uses curated subsets to keep it lightweight and reproducible.

Four data files are used:
1. **some_goodreads_interactions.csv** — Ratings assigned by 1,000 users to a large number of books.
2. **some_goodreads_books.csv** — Metadata for a select set of books.
3. **some_book_id_map.csv** — Maps book IDs in the interactions file to IDs in the book metadata file.
4. **goodreads_book_authors.csv** — Author information for the books.

### Dataset Note

This repo uses a representative subset of the full Goodreads dataset. The hyperparameters in `main.py` are tuned for this subset. If you substitute the full dataset, expect longer runtimes and you may want to re-tune the matrix completion parameters accordingly.

## Instructions

Install the required dependencies using:

```bash
pip install -r requirements.txt
```

Or install the core library individually:

```bash
pip install fancyimpute
```

Once dependencies are installed, clone the repository and run:

```bash
python code/main.py
```

`main.py` contains separate functions for running the recommender system and for evaluating algorithm performance. Comment out whichever you don't need before running.

## Details and Results

For the theory, methodology, and results, see the [Project Report](https://github.com/ananya-jegannathan/Book-Recommender-System/blob/main/ECE697_Final_Project_Report.pdf).

## Credits

1. Dataset source: [UCSD Book Graph](https://sites.google.com/eng.ucsd.edu/ucsdbookgraph/home)
2. fancyimpute library: [iskandr/fancyimpute](https://github.com/iskandr/fancyimpute)
