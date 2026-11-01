# Sales Performance Analysis

A Jupyter Notebook project that explores order-level sales data and turns it into revenue, product, category, and regional summaries using Python.

## Overview

The project uses a small sample dataset to demonstrate a practical analysis workflow:

1. Load and inspect order-level data.
2. Parse order dates and calculate revenue as `quantity × price`.
3. Calculate total revenue, number of orders, and average order value.
4. Compare monthly revenue, regional performance, product contribution, and category share.
5. Visualize the results with Matplotlib.

## Repository Contents

| File | Description |
| --- | --- |
| `data.csv` | Sample order-level dataset |
| `sales_data analysis.ipynb` | Data preparation, KPI calculations, analysis, and charts |

## Dataset

The current CSV contains 10 sample orders from January to March 2024.

| Column | Description |
| --- | --- |
| `order_id` | Order identifier |
| `order_date` | Date the order was placed |
| `product` | Product name |
| `category` | Product category |
| `quantity` | Units ordered |
| `price` | Unit price |
| `region` | Sales region |

Revenue is derived in the notebook:

```python
df["revenue"] = df["quantity"] * df["price"]
```

### Sample-data summary

The figures below describe only the small CSV currently included in this repository.

| Metric | Value |
| --- | ---: |
| Orders | 10 |
| Total revenue | 160,250 |
| Average order value | 16,025 |

## Analysis and Visualizations

- KPI summary: total revenue, total orders, and average order value.
- Monthly revenue trend.
- Revenue by region.
- Revenue by product.
- Category-wise revenue contribution.

## Run Locally

Requires Python 3.9 or later.

```bash
git clone https://github.com/UmerTukdi/sales-data-analysis-dashboard.git
cd sales-data-analysis-dashboard

python -m venv .venv
```

Activate the environment:

```bash
# Windows
.venv\Scripts\activate

# macOS / Linux
source .venv/bin/activate
```

Install the dependencies and launch Jupyter:

```bash
pip install pandas matplotlib notebook
jupyter notebook
```

Open `sales_data analysis.ipynb` and run the cells from top to bottom. Keep `data.csv` in the repository root because the notebook reads it using a relative path.

## Scope

This is an exploratory notebook built around a small sample dataset. The results demonstrate the analysis workflow and should not be interpreted as representative business performance.
