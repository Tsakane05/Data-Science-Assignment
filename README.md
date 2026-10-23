Data_Science_Assignment/
│
├── README.md                        <- This file
├── BooksToScrape_v3.ipynb           <- The main Jupyter Notebook containing all code
├── books_raw_v3.csv                 <- The raw data scraped directly from the website
├── books_clean_v3.csv               <- The final, cleaned dataset used for modelling
├── BooksToScrape_Report_v3.pdf      <- The final professional report
│
└── images/                          <- Generated visualisations (saved automatically)
    ├── v3_price_distribution.png
    ├── v3_ratings_count.png
    ├── v3_price_by_rating.png
    ├── v3_top_categories.png
    ├── v3_correlation_heatmap.png
    ├── v3_stock_vs_price.png
    └── v3_actual_vs_predicted.png
Workflow & Methodology
The project in BooksToScrape_v3.ipynb follows a standard data science pipeline:

Data Acquisition: Programmatically scraped 8 specific genres (Fiction, Mystery, Romance, Science Fiction, History, Young Adult, Poetry, Travel) using requests and BeautifulSoup. Handled pagination and implemented error-handling to extract ~215 books.

Data Cleaning & Preparation: Handled missing descriptions, converted numeric fields, and engineered new features (title_length, description_length, description_word_count, has_description).

Visual Exploration: Generated 6 visualisations using matplotlib and seaborn to analyse price distributions, rating frequencies, and category trends.

Predictive Modelling: Built a scikit-learn Pipeline (using StandardScaler, OneHotEncoder, and LinearRegression) to estimate book prices based on numeric and categorical features.

Key Findings
Genre Dominates: A book's genre is the strongest signal for its price, with specific categories consistently sitting at higher price points.

Ratings are Weak: Star ratings show almost zero correlation with price.

Model Limitations: The Linear Regression model produced an R² of -0.085 and an MAE of £15.49. This negative R² indicates that product-page features alone are insufficient to predict price accurately, and a non-linear model or richer dataset (e.g., author, publisher, page count) would be required for production use.

Requirements & Setup
To run the Jupyter Notebook, you will need:

Python 3.x

Jupyter Notebook

Required libraries (install via pip):

bash
pip install requests beautifulsoup4 pandas numpy matplotlib seaborn scikit-learn tqdm
Author
Tsakane Khoza
Student ITS No: 402416511
Data Science 500 Assignment - 23 October 2026

