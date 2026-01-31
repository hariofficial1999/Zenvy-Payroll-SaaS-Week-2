# 🚀 Zenvy Payroll SaaS - Analytics & Insights (Week 2)

Welcome to the **Zenvy Payroll SaaS** project repository. This project focuses on building a professional-grade payroll management and workforce analytics system using Power BI and Python.

---

## 📂 Project Structure & Files

| File/Folder | Description |
| :--- | :--- |
| **`power bi.pbix`** | Core Power BI Dashboard containing Workforce, Finance, and Operations analytics. |
| **`zenvy_master_combined.csv`** | The "Golden Dataset" containing filtered, merged, and cleaned data for all visuals. |
| **`Zenvy_Week2_Analytics.ipynb`** | Jupyter Notebook used for data cleaning, feature engineering, and automated reporting. |
| **`dim_employees.csv`** | Primary dimension table for employee metadata. |
| **`zenvy_full_dataset.png`** | High-resolution image of the complete master dataset (20 rows x 23 columns). |
| **`Power bi visualization/`** | Directory containing specific dashboard snapshots and assets. |

---

## 📊 Dashboard Modules

This project features three high-impact dashboard pages designed for different stakeholders:

### 1. 💰 Workforce Insights (Salary Distribution)
*   **Goal:** Visualize how compensation is spread across the organization.
*   **Key Visuals:** Salary Spread (Histogram), Pay by Designation (Treemap), and Monthly Payout Trends.

### 2. 🏦 Finance Analytics (Department Expenses)
*   **Goal:** Track department-wise ROI and expense composition.
*   **Key Visuals:** Expense Composition (Donut Chart), Dept Total Payout (Bar Chart), and Monthly Budget Flow (Ribbon Chart).

### 3. ⏳ Operations Analytics (Overtime Tracking)
*   **Goal:** Monitor employee burnout and operational efficiency.
*   **Key Visuals:** Dept-wise OT Pulse (Small Multiples), OT vs Attendance (Scatter Chart), and Peak Burnout Alert (Gauge).

---

## 🛠️ Tech Stack & Implementation
*   **Data Analysis:** Python (Pandas, Matplotlib)
*   **Business Intelligence:** Microsoft Power BI
*   **Design:** Dark/Neon Premium UI Theme
*   **Data Model:** Star Schema (Dim Tables connected to Payroll Fact Table)

---

## 🎨 Aesthetic Guidelines
All dashboards follow a **Premium Dark Theme** to ensure a high-end SaaS feel:
*   **Background:** `#1A1C2E` (Deep Night Blue)
*   **Accents:** Neon Cyan (`#00F2FF`) and Sunset Orange.
*   **UI:** 12px Rounded Corners, Glassmorphism Effects, and Subtle Shadows.

---

## 🚀 How to Use
1.  **Data:** Ensure `zenvy_master_combined.csv` is in the same folder as the `.pbix` file.
2.  **Power BI:** Open `power bi.pbix` to view and interact with the live analytics.
3.  **Python:** Run `Zenvy_Week2_Analytics.ipynb` to see the data processing pipeline.

**Project Documentation - Zenvy Payroll SaaS**
