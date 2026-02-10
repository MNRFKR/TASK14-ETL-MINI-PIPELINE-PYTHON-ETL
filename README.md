# TASK14-ETL-MINI-PIPELINE-PYTHON-ETL
# E-commerce Dataset ETL Workflow

## Step 1: Import File
- Upload dataset in Colab using `files.upload()`.
- Load into DataFrame with `pd.read_csv()`.

## Step 2: Preview Data
- Use `df.head()` to inspect first rows.
- Confirm column structure and datatypes.

## Step 3: Clean Missing Values + Duplicates
- Check missing values with `df.isnull().sum()`.
- Drop or fill NaN values depending on column context.
- Remove duplicate rows using `df.drop_duplicates()`.

## Step 4: Standardize Column Names & Datatypes
- Convert column names to lowercase with underscores.
- Cast datatypes: dates → datetime, numeric → float/int, categorical → category.

## Step 5: Create Derived Columns
- `margin = profit / sales`.
- Flags: `high_value_customer`, `discount_flag`, `priority_flag`.

## Step 6: Split into Separate Outputs
- `customers_df`: unique customer attributes.
- `orders_df`: order-level details with flags.
- `products_df`: product/category metrics with profitability.

## Step 7: Export Outputs
- Save splits as CSV: `customers.csv`, `orders.csv`, `products.csv`.

## Step 8: Validate Counts
- Compare original vs cleaned row counts.
- Confirm splits sizes (customers < orders/products).
- Ensure relational integrity (customer IDs in orders exist in customers_df).

## Step 9: Documentation
- This README serves as a stepwise ETL record.
- Each step is reproducible in Python Colab.
