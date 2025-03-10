﻿# 📊 QVI Retail Store Trial Analysis

## 🏪 Project Overview
This project analyzes the impact of a retail trial on chip sales using transactional data. The goal is to identify a suitable **control store** for comparison and assess whether the trial significantly increased sales.

## 📂 Dataset Description
The analysis is based on **QVI_data.csv**, containing:
- **Transaction Dates** (`DATE`)
- **Store Numbers** (`STORE_NBR`)
- **Total Sales** (`TOT_SALES`)
- **Unique Customers** (`LYLTY_CARD_NBR`)

## 🔬 Methodology
### 1️⃣ Data Preparation
- Converted `DATE` to datetime format.
- Filtered invalid dates and missing values.
- Aggregated monthly sales & customer metrics.

### 2️⃣ Control Store Selection
To find a **suitable control store**, we:
- Computed similarity based on **total sales, unique customers, and avg. transactions**.
- Used a distance metric to rank potential control stores.

### 3️⃣ Trial Analysis
- Compared **trial vs. control store sales** over the trial period.
- Performed **t-tests** to check statistical significance.
- Examined price sensitivity and promotional effects.

## 📊 Key Insights & Results
| Trial Store | Control Store | T-Statistic | P-Value  |
|------------|--------------|------------|----------|
| **77**    | 233          | 2.10       | 0.103    |
| **86**    | 196          | 0.62       | 0.567    |
| **88**    | 237          | 2.14       | 0.099    |

- **Mainstream Young Singles (28% sales share)** → Prefer premium packs, highest transaction value.
- **Budget Older Families (highest units/customer)** → Value packs, promo-sensitive (65% buy on discount).
- **Premium Empty Nesters (22% higher price sensitivity)** → Seasonal promo timing crucial.

### 🚀 Strategic Recommendations
✅ **Target Mainstream Young Singles** with premium limited-edition flavors.  
✅ **Introduce 300g family packs** for Budget Older Families.  
✅ **Launch weekend flash sales** for Premium Empty Nesters.  

## 📈 Statistical Improvements (Next Steps)
🔹 **Time-Series Correlation**: To enhance control store matching.  
🔹 **Mann-Whitney U Test**: More robust than t-tests for non-normal data.  
🔹 **Causal Impact Analysis**: Bayesian model for external factor control.  

## 🚀 How to Run the Analysis
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/QVI-Retail-Analysis.git
   cd QVI-Retail-Analysis
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scipy
   ```
3. Place the dataset in the project folder (`QVI_data.csv`).
4. Run the script:
   ```bash
   python analysis.py
   ```
5. Review the results in the terminal & generated visualizations.

## 📷 Sample Visualizations
_(Add plots like sales trends, customer segmentation, etc.)_

## 📌 Contributors
- **[Shrungal Kulkarni]** – Data Analysis, Report & Code

## 📜 License
This project is under the MIT License.

---
🔥 _For suggestions or improvements, feel free to fork and contribute!_
