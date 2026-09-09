# 📊 E-Commerce Customer Retention & RFM Analytics Pipeline

An end-to-end Exploratory Data Analysis (EDA) and customer segmentation pipeline engineered in **Python** using **VS Code**. This project converts over **500,000 rows** of raw, chaotic e-commerce transactional data into high-impact, actionable business intelligence profiles.

---

## 🎯 Project Overview & Business Value
In the e-commerce industry, distributing marketing budgets uniformly across all customers leads to high acquisition costs and severe customer churn. This project provides a programmatic solution by:
1. **Cleaning and structuralizing** raw transaction ledgers.
2. **Isolating operations trends** (temporal bottlenecks and product return concentrations).
3. **Clustering the customer base** using an RFM (Recency, Frequency, Monetary) data framework to drive high-ROI retention campaigns.

---

## 🛠️ Repository Architecture

```text
├── data/                    		# Directory for raw datasets
├── notebooks/               		# Ordered Jupyter Notebooks
│   ├── 01_data_cleaning.ipynb		# Data hygiene, parsing, & filtering
│   └── 02_eda_and_segmentation.ipynb	# Visual exploration & RFM modelling
├── venv/                    		# Isolated virtual environment
├── .gitignore               		# Standard files ignored by version control
├── requirements.txt         		# Python package dependencies
└── README.md                		# Project documentation page
```

---

## 🚀 Key Technical Insights 

*   **The 80/20 Revenue Engine:** Applied the **Pareto Principle** to discover that **just 18.4% of unique products** drive 80% of total company gross sales, revealing significant inventory optimization opportunities.
*   **Temporal Traffic Spikes:** Identified an operational peak **every Tuesday between 11:00 AM and 1:00 PM**, experiencing a **45% surge** in transaction density—marking the exact window for high-engagement push notifications.
*   **The "At-Risk" Capital:** Isolated a critical cohort of "At-Risk Loyalists" (historically high spending, but zero transaction activity in over 60 days) representing **$240K in latent revenue** ready for automated email win-back campaigns.

---

## 🔧 Tech Stack & Libraries
*   **IDE:** Visual Studio Code (VS Code) with Jupyter Extension
*   **Language:** Python 3.11+
*   **Data Manipulation:** Pandas, NumPy
*   **Data Visualization:** Matplotlib, Seaborn

---

## 📈 Phase-by-Phase Execution

### 🧹 1. Programmatic Data Cleaning
Real-world data is messy. The pipeline built cleans it safely:
*   It identified and removed **135,000+ records** missing critical `CustomerID` logs.
*   A structural filter engineered to isolate negative `Quantity` records has been incorporated to separat customer cancellations and returns from core revenue data.
*   The irregular string date columns into optimized `datetime64[ns]` schemas for time-series extraction.

### 👥 2. Advanced RFM Clustering
Collapsed individual item invoices down to profile unique human behavior across three distinct axes:
*   **Recency ($R$):** Days elapsed since the user's last recorded transaction.
*   **Frequency ($F$):** The complete count of unique invoices generated.
*   **Monetary ($M$):** The total net lifetime capital spent by the user.

Customers are grouped into 4 definitive strategic archetypes: *Champions, At-Risk Loyalists, Hibernating, and Standard Customers*.

---

## 💻 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd ecommerce-eda-rfm
   ```

2. **Activate your virtual environment and install dependencies:**
   ```bash
   # On Windows
   venv\Scripts\activate
   # On Mac/Linux
   source venv/bin/activate

   pip install -r requirements.txt
   ```

3. **Run inside VS Code:**
   Open the `/notebooks` folder, select your local `venv` kernel in the top right corner of VS Code, and run the notebook cells sequentially.
