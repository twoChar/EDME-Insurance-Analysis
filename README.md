# 📊 Insurance GDP Trend Analysis

Analyze **Gross Direct Premium (GDP)** trends for three major Indian insurance providers from multi-page PDF reports, and visualize **quarterly vs cumulative growth**.

![Sample Trendline](https://github.com/twoChar/EDME-Insurance-GDP-Analysis/blob/main/output.png)  


---

## Overview

This project automates the extraction of premium data from **quarterly insurance reports** and generates **trendline visualizations**.

Key highlights:

- Handles **multi-page PDFs** (50–60 pages each) for 12 quarters per company  
- Extracts **`FORM NL-4 PREMIUM SCHEDULE`** tables  
- Detects and cleans **Gross Direct Premium (GDP)** data  
- Plots **Quarterly vs Up-to-the-Quarter trends** for comparison

---

## Features

- Automated **PDF table extraction** using `pdfplumber`
- **Smart parsing** of:
  - `Particulars` header
  - `Gross Direct Premium` row
  - Last two numeric columns (Quarter & Cumulative)
- **Data normalization**:
  - Cleans messy numbers like `1,96,877` or `(12,345)`  
  - Infers year/quarter from filename
- **Visualization**:
  - Company-wise trendlines
  - Combined comparisons

---

## Example Companies

- **SBI General Insurance**
- **Aditya Birla Health Insurance**
- **Shriram General Insurance**

---

## Sample Output

| Date       | Gross Premium (Quarter) | Gross Premium (Up to Quarter) |
|------------|--------------------------|-------------------------------|
| 2023-12-31 | 77,176                   | 104,059                       |
| 2024-12-31 | 96,877                   | 175,038                       |

---

## Tech Stack

- **Python 3.12**
- **Libraries**:
  - `pdfplumber`, `pdfminer` → PDF parsing
  - `pandas` → data wrangling
  - `matplotlib` → trendline visualization
  - `re`, `os`, `logging` → utilities






---

## Installation & Setup

### Prerequisites

- Python 3.10+
- Install project dependencies:

```bash
pip install pdfplumber pandas matplotlib
```

### Run the Analysis

1. Place all **company PDFs** in their respective folders.
2. Open the notebook:

```bash
jupyter notebook notebooks/extract_and_plot.ipynb
```

3. Run all cells to:
   - Extract GDP data
   - Generate `quarter_df` and `upto_df` DataFrames
   - Plot trendlines per company and combined

---

## Visualization Highlights

- **Company-wise plots**:  
  Shows **Quarter vs Up-to-the-Quarter** GDP trends for each insurer.

- **Combined plots**:  
  All three companies on one graph for **direct comparison**.

---

## Future Improvements

- Export cleaned GDP data to **CSV / Excel**
- Generate **automated PDF reports** of visualizations
- Add **interactive dashboards** using Plotly/Streamlit
- Extend support to **other insurance companies**

---

## Author

**Aaditya Dahiya**  
[GitHub](https://github.com/Aaditya1617) • [LinkedIn](https://www.linkedin.com/in/aaditya-dahiya-100755229a)

---

If you like this project, ⭐ **star the repo** and share!
