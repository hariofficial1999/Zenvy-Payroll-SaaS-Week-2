# DS/Analytics Dashboard Planning - Zenvy Payroll

This document outlines the specific data visualizations and metrics planned for the Zenvy Payroll SaaS platform.

## 1. Salary Distribution Dashboard
**Goal:** To visualize the equity and distribution of pay across the workforce.

*   **Key Metrics:**
    *   Median Salary
    *   Salary Range (Min/Max)
    *   Standard Deviation of Salary
    *   Comp-a-ratio (Current Salary / Market Midpoint)
*   **Visualizations:**
    *   **Normal Distribution Curve:** To see if the organization follows a standard pay curve.
    *   **Violin Plots:** To visualize the density of salaries across different departments or job titles.
    *   **Scatter Plot:** Salary vs. Years of Experience to identify potential outliers or pay gaps.

## 2. Department-wise Expenses Dashboard
**Goal:** To provide management with a clear breakdown of where budget is being spent.

*   **Key Metrics:**
    *   Total Departmental Spending
    *   Budget vs. Actual Variance
    *   Average Cost per Employee per Department
*   **Visualizations:**
    *   **Sunburst Chart:** Showing a hierarchical view of expenses (Company -> Division -> Department).
    *   **Waterfall Chart:** To show the cumulative effect of different spend categories (Base, Bonus, Benefits) on the total budget.
    *   **Treemap:** Comparing the relative size of department budgets at a glance.

## 3. Overtime (OT) Tracking Dashboard
**Goal:** To monitor labor efficiency and prevent budget overruns due to excessive overtime.

*   **Key Metrics:**
    *   Total OT Hours
    *   OT-to-Base Ratio (%)
    *   Estimated OT Cost
    *   OT Burden Rate
*   **Visualizations:**
    *   **Calendar Heatmap:** Identifying peak OT days during the month (e.g., month-end crunch).
    *   **Clustered Bar Chart:** Comparing OT hours vs. Regular hours by department.
    *   **Top 10 OT Employees Table:** Highlighting individuals who might be at risk of burnout or where staffing might be insufficient.

---

## Data Requirements (Draft)
| Dashboard | Required Data Fields |
| :--- | :--- |
| **Salary Distribution** | `EmployeeID`, `BaseSalary`, `JobLevel`, `Department`, `ExperienceYears` |
| **Dept Expenses** | `DepartmentID`, `PayrollAmount`, `BonusAmount`, `BenefitsCost`, `MonthYear` |
| **OT Tracking** | `EmployeeID`, `Date`, `RegularHours`, `OvertimeHours`, `OT_Rate` |
