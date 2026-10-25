# Customer Journey Reconstruction Engine

**Reconstructing customer purchasing journeys from historical retail transaction data.**

## Overview

The Customer Journey Reconstruction Engine is a data science project that analyzes historical retail transactions to understand how customers interact with a business over time.

Using the Online Retail II dataset, the project aims to transform raw transaction records into meaningful customer-level insights, identify purchasing patterns, and reconstruct the sequence of customer purchases.

The goal is to move beyond traditional sales analysis and understand **what customers purchase, how their behavior changes over time, and when they return to make another purchase.**

## Objectives

- Explore and understand historical retail transaction data.
- Clean and preprocess transaction records for reliable analysis.
- Reconstruct chronological purchasing histories for individual customers.
- Analyze repeat purchases, purchase intervals, and spending behavior.
- Identify customer segments and behavioral patterns.
- Develop visualizations that communicate customer journey insights.
- Explore predictive approaches to understanding future customer behavior.

## Dataset

This project uses the **Online Retail II** dataset, which contains transaction records from a UK-based online retailer covering two periods:

- 2009–2010
- 2010–2011

The dataset includes information such as invoice numbers, product codes, quantities, prices, invoice dates, customer identifiers, and country.

The Excel workbook is named `online_retail_II.xlsx`.

> **Note:** The dataset is used for analysis and is not included in this repository by default. Obtain it from its original source and place it in the project directory before running the notebook.

### Dataset source

UCI Machine Learning Repository: [Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii)

## Tech Stack

| Technology | Purpose |
|---|---|
| Python | Data processing and analysis |
| Pandas | Data loading, cleaning, and manipulation |
| NumPy | Numerical operations |
| Openpyxl | Reading Excel workbooks |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Jupyter Notebook | Interactive analysis and experimentation |
| Git and GitHub | Version control and project collaboration |

## Project Structure

```text
Customer-Journey-Reconstruction-Engine/
│
├── 01_data_inspection.ipynb   # Initial data loading and inspection
├── online_retail_II.xlsx      # Local dataset; not committed by default
├── README.md                  # Project documentation
└── requirements.txt           # Python dependencies (planned)
```

The project structure will evolve as data preprocessing, customer journey reconstruction, analysis, and modeling are developed.

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Anushkarawat4/Customer-Journey-Reconstruction-Engine.git
cd Customer-Journey-Reconstruction-Engine
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
python -m pip install pandas numpy openpyxl matplotlib seaborn jupyter
```

### 4. Download the dataset

Download Online Retail II from the UCI Machine Learning Repository and place `online_retail_II.xlsx` in the project root.

### 5. Launch Jupyter Notebook

```bash
python -m jupyter notebook
```

Open `01_data_inspection.ipynb` and execute the cells in order.

Ensure that the notebook reads the dataset using a relative path, such as:

```python
from pathlib import Path

DATA_PATH = Path("online_retail_II.xlsx")
```

If you open the notebook from another working directory, adjust the path to match the project's actual location.

## Current Progress

### Phase 1 — Data Inspection

- [x] Load the two Excel worksheets.
- [x] Add a source-period label to each worksheet.
- [x] Combine the worksheets into a single DataFrame.
- [x] Inspect the combined dataset's dimensions and initial records.
- [x] Analyze missing values and duplicate records.
- [x] Examine column data types and transaction date ranges.

### Planned Development

**Phase 2 — Data Cleaning and Preparation**
- [x] Handle missing customer identifiers and invalid records.
- [x] Examine cancellations, returns, and unusual quantities or prices.
- [x] Prepare transaction dates and calculate transaction-level revenue where appropriate.

**Phase 3 — Customer Journey Reconstruction**
- Order transactions chronologically.
- Build customer-level purchase histories.
- Calculate time gaps between purchases.
- Analyze repeat purchasing and changes in customer behavior.

**Phase 4 — Customer Intelligence**
- Develop customer-level behavioral features.
- Explore customer segmentation and purchasing patterns.
- Identify useful signals of customer retention and inactivity.

**Phase 5 — Modeling and Visualization**
- Evaluate suitable predictive approaches for customer behavior.
- Build visualizations and a dashboard to communicate insights.
- Document results, limitations, and possible business applications.

Planned features will be marked complete only after they have been implemented and evaluated.

## Expected Outcomes

The intended outcome is an analytical system that can help answer questions such as:

- How frequently do customers return?
- Which customers make repeat purchases?
- How does spending behavior change over time?
- What products or product categories appear in successive purchases?
- Which customers show signs of becoming inactive?
- Can historical purchasing behavior help predict a future purchase or customer state?

These are project goals, not yet validated findings.

## Why This Project?

Traditional retail analysis often focuses on total revenue, product performance, and aggregate sales trends. This project takes a customer-centric approach by examining the sequence and timing of individual purchases.

Reconstructing customer journeys can provide a foundation for understanding customer retention, repeat purchasing, and behavioral changes.

## Limitations

- Historical transaction data does not capture every customer interaction, such as website visits or abandoned carts.
- Some transactions may not have an identifiable customer ID.
- Returns and cancellations require careful treatment.
- Historical associations do not necessarily establish causal relationships.
- Predictive performance must be measured on appropriate held-out data before practical claims can be made.

## Future Improvements

- Customer journey visualizations and interactive filtering.
- More robust customer segmentation.
- Time-aware purchase prediction.
- Customer inactivity and retention analysis.
- A reproducible data preprocessing pipeline.
- A deployable dashboard for exploring customer insights.

## Author

**Anushkarawat4**

GitHub: [@Anushkarawat4](https://github.com/Anushkarawat4)

## License

A license for this project's code has not yet been specified. The dataset remains subject to its original source's terms and conditions.
