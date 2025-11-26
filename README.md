# AQA-Training

This is a training repo. Not the final Project

This workspace will be used for testing, learning and prototyping.

# IBM Data Analysis with Python - Module Breakdown

This course introduces Python-based data analysis practices using real-world datasets (Laptop Pricing dataset). The modules build from foundational concepts to full analytical workflows, preparing you for real analysis tasks such as operator trending, environmental monitoring, and predictive quality work relevant to AQA.

### Module 1 — Importing Data Sets

Focus: Learning how to load, inspect, and understand datasets from CSV, Excel, SQL databases, and other sources.

Key Topics:

- A dataset consists of rows (individual records) and columns (attributes), typically separated by commas in CSV files.
- Understanding column attributes is essential before performing any analysis.
- Python libraries provide ready-made scientific, visualisation, and machine-learning functionality (NumPy, SciPy, Pandas, Matplotlib, Scikit-Learn).
- Many libraries in the Python ecosystem are interconnected (e.g., Scikit-Learn builds on NumPy/SciPy/Matplotlib).
- Pandas can read multiple data formats (CSV, Excel, JSON) using functions like read_csv.
- Data types in Pandas include object, float, Int64, and datetime.
- The dtype and info() methods help you inspect and validate data types.
- Misclassified data types require correction to ensure valid analysis.
- The describe() function provides statistical summaries for numerical columns and,with include='all', for categorical columns.
- Missing values appear as NaN and may prevent calculations for affected columns.
- Python can connect to databases through SQL APIs and the Python DB-API.
- DB-API uses connection and cursor objects to run SQL queries.
- Key commands include: cursor(), commit(), rollback(), and close().
- A complete workflow includes importing the module, connecting to the database, executing queries, retrieving results, and closing the connection.

Relevance to AQA:
Forms the foundation for bringing operator logs, environmental data, and production records into the AQA system for analysis.

### Module 2 — Data Wrangling

Focus: Cleaning, transforming, normalising, and encoding data to ensure consistency and prepare it for analysis or modelling.

Key Topics:

- Data formatting is essential when combining datasets from multiple sources.
- Python can convert units of measurement for consistency (e.g., MPG → L/100km).
- Correcting and standardising data types ensures accurate statistical analysis.
- Data normalisation makes variables comparable and reduces model bias.

You have learned three normalisation techniques:

- Feature scaling
- Min–Max scaling
- Z-Score standardisation

These can be applied in Pandas during preprocessing.

- Binning improves model performance and enhances visualisation by grouping continuous variables into intervals.
- You can perform binning using numpy.linspace and pandas.cut.
- Histograms help visualise the distribution of binned data.
- Machine learning models require numerical inputs — categorical data must be encoded.
- One-hot encoding transforms categories (e.g., fuel type) into numeric variables using pandas.get_dummies.

Relevance to AQA:
Ensures the aseptic data collected (operator entries, batch logs, environmental readings) is standardised and reliable enough for accurate trending and decision-making.

### Module 3 — Exploratory Data Analysis (EDA)

Focus: Using statistics and visualisation to explore variable relationships, detect patterns, and identify correlations within datasets.

Key Topics:

- describe() quickly produces statistical summaries (mean, std dev, quartiles) for numerical data.
- value_counts() summarises categorical data and identifies category distributions.
- Box plots visually show distribution, quartiles, and outliers.
- Scatter plots reveal relationships between continuous variables (e.g., engine size vs. price).
- groupby is used to explore interactions between categorical and numerical variables.
- Pivot tables and heatmaps improve multi-variable visualisation.
- Correlation measures the relationship strength between variables.
- Scatter plots with regression lines (e.g., Seaborn’s regplot) show correlation visually.

Pearson correlation provides:

- Coefficient (strength & direction of relationship)
- P-value (certainty of relationship)

- Coefficients near +1 or –1 indicate strong correlation; near 0 indicates weak/no correlation.
- P-values < 0.001 indicate high certainty.

Relevance to AQA:
Enables early identification of trends or issues such as operator variability, increased AER rates, or environmental anomalies in aseptic processing.
