# Insurance GDP Trend Analysis

This project analyzes the **Gross Direct Premium (GDP)** trends of three major Indian insurance companies using data extracted from quarterly PDF reports.

### 🔍 Objective

To visualize and compare the *quarterly* and *cumulative* (up to quarter) gross premium trends of:

- **SBI General Insurance**
- **Aditya Birla Health Insurance**
- **Shriram General Insurance**

### 📁 Input Data

Each company provides quarterly reports as PDF files, typically:

- 12 PDFs per company
- 50–60 pages per PDF
- Reports include a `FORM NL-4 PREMIUM SCHEDULE` section with the required GDP table

### ⚙️ What This Project Does

1. **PDF Extraction**  
   Parses each PDF using `pdfplumber` to find the NL-4 Premium Schedule table.

2. **Target Row Detection**  
   Locates the row containing *Gross Direct Premium*.

3. **Data Cleaning & Normalization**  
   Extracts the last two numeric values from each row:
   - First: Premium for the quarter
   - Second: Cumulative premium up to the quarter

4. **Date Parsing**  
   Infers the date from the PDF filename (e.g. `Q1 2024.pdf` → `2024-12-31`)

5. **Visualization**  
   Plots:
   - Individual trend lines for each company
   - Combined graphs for comparison

### 📊 Output

Each company has two tidy datasets:

- `*_quarter_df`: GDP for the current quarter  
- `*_upto_df`: Cumulative GDP up to that quarter

And three separate trendline plots showing:

- Quarter vs Up to Quarter GDP for each company

### 📦 Libraries Used

- `pdfplumber`
- `pandas`
- `matplotlib`
- `re`
- `os`, `logging`

### 🧠 Insights

By structuring and visualizing the premium data:
- You can observe how individual companies perform over time
- Spot seasonal spikes or steady growth
- Compare cumulative vs quarterly contributions

### 📁 Folder Structure

