# HR-Analytics-Dashboard
Interactive HR Analytics Dashboard built in Power BI using Power Query and DAX. Analyzes employee attrition, workforce demographics, salary, satisfaction, experience, and department trends with dynamic KPIs, charts, and slicers.
#  HR Analytics Dashboard — Power BI

An interactive **HR Analytics Dashboard built using Microsoft Power BI** to analyze employee attrition, workforce demographics, salary distribution, job satisfaction, experience, and department-wise employee trends.

<img width="1650" height="1275" alt="hr_page-0001" src="https://github.com/user-attachments/assets/223f072b-4baa-46c6-b566-8dd8a1c82987" />


This project demonstrates the complete data analytics workflow — from **data cleaning and transformation using Power Query** to **DAX calculations, data visualization, dashboard design, and interactive filtering**.

---

## Project Overview

Human Resource teams need clear and actionable insights to understand workforce composition and employee attrition.

This Power BI dashboard transforms raw employee-level HR data into an interactive analytical report that helps identify:

* Overall employee strength
* Active employee count
* Employee attrition count and rate
* Workforce age distribution
* Average employee age
* Average years at the company
* Attrition by department
* Attrition by salary slab
* Attrition by job role and satisfaction
* Attrition by gender
* Attrition trends by experience
* Department-wise employee distribution

The dashboard allows users to interactively explore the data using **Department** and **Age Group** slicers.

---

## Objectives

The primary objectives of this project are to:

1. Analyze overall workforce composition.
2. Measure employee attrition and attrition rate.
3. Identify departments with higher employee attrition.
4. Understand the relationship between salary levels and attrition.
5. Analyze attrition across different job roles.
6. Examine employee satisfaction and its relationship with attrition.
7. Understand workforce demographics by age and gender.
8. Analyze attrition patterns across experience levels.
9. Provide an interactive dashboard for HR decision-making.

---

## 🗂️ Dataset

The dataset contains employee-level HR information with approximately:

* **1,481 employee records**
* **37 columns**

### Important Fields

| Field            | Description                            |
| ---------------- | -------------------------------------- |
| Employee ID      | Unique identifier for employees        |
| Age              | Employee age                           |
| Age Group        | Categorized employee age               |
| Department       | Employee's department                  |
| Job Role         | Employee's job position                |
| Monthly Income   | Monthly employee income                |
| Salary Slab      | Salary range/category                  |
| Attrition        | Indicates whether an employee left     |
| Job Satisfaction | Employee satisfaction rating           |
| Total Experience | Total years of professional experience |
| Years at Company | Number of years with the organization  |
| Gender           | Employee gender                        |
| Business Travel  | Employee travel frequency              |

---

## Data Cleaning & Transformation

Data preparation was performed using **Power Query** before building the dashboard.

### Cleaning steps included:

* Removed unnecessary blank rows.
* Checked column quality and missing values.
* Identified duplicate records.
* Removed duplicate rows based on the complete dataset.
* Standardized inconsistent text values.
* Corrected spelling inconsistencies such as `travel_rarely` and `travel rarely`.
* Detected and corrected incorrect data types.
* Created a new `Attrition Count` column.
* Converted numerical fields to appropriate numeric data types.
* Applied all transformations using **Close & Apply**.

These steps ensured the dataset was clean, consistent, and suitable for analysis.

---

## DAX Measures

DAX was used to create calculated metrics for the dashboard.

### Attrition Rate

```DAX
Attrition Rate % =
DIVIDE(
    SUM('HR Data'[Attrition Count]),
    COUNT('HR Data'[Employee ID]),
    0
)
```

The measure calculates the percentage of employees who have left the organization.

### Attrition Count

An `Attrition Count` field was created based on the Attrition status:

```text
Attrition = Yes → 1
Attrition = No  → 0
```

The values are then aggregated using `SUM` to calculate total employee attrition.

---

## 📊 Key Performance Indicators

The dashboard includes six major KPI cards:

### 👥 Total Employees

Displays the total number of employees in the dataset.

### 🟢 Active Employees

Shows employees who are currently active by filtering:

```text
Attrition = No
```

### 🔴 Attrition Count

Displays the total number of employees who have left the organization.

### 📉 Attrition Rate

Shows employee attrition as a percentage of the overall workforce.

### Average Age

Displays the average age of employees.

### 💼 Average Experience

Displays the average number of years employees have spent with the company.

---

## 📈 Dashboard Visualizations

### 1. Attrition by Department

A donut chart showing the distribution of employee attrition across different departments.

**Purpose:**

* Identify departments experiencing higher attrition.
* Compare attrition levels across departments.

---

### 2. Attrition by Salary Slab

A clustered bar chart comparing employees who stayed versus employees who left across different salary ranges.

**Purpose:**

* Understand how salary levels relate to attrition.
* Identify salary groups with higher employee turnover.

---

### 3. Attrition by Job Role & Satisfaction

A matrix visual displaying attrition across different job roles and job satisfaction levels.

Conditional formatting is used to highlight higher and lower attrition values.

**Purpose:**

* Identify job roles with higher attrition.
* Analyze employee satisfaction patterns.
* Discover potential relationships between satisfaction and employee turnover.

---

### 4. Age Group Distribution

A stacked column chart showing the number of employees across different age groups.

**Purpose:**

* Understand workforce demographics.
* Analyze the distribution of employees across age categories.
* Support workforce planning and demographic analysis.

---

### 5. Attrition by Gender

A pie chart showing employee attrition distribution by gender.

**Purpose:**

* Compare attrition patterns across gender groups.
* Understand workforce turnover distribution.

---

### 6. Attrition Trend by Experience

An area chart analyzing employee attrition across different total experience levels.

**Purpose:**

* Identify experience levels associated with higher attrition.
* Understand whether attrition is more common among early-career, mid-career, or experienced employees.

---

### 7. Department-wise Employee Count

A funnel chart showing employee distribution across departments.

**Purpose:**

* Compare workforce size between departments.
* Identify departments with the highest and lowest employee counts.

---

## 🎛️ Interactive Filters

The dashboard includes interactive slicers that allow users to dynamically filter the report.

### Department Slicer

Users can select a specific department to analyze department-level workforce and attrition insights.

### Age Group Slicer

Users can filter the dashboard based on employee age groups.

These slicers make the dashboard interactive and allow users to perform focused analysis without manually filtering individual charts.

---

## **Dashboard Design**

The dashboard was designed with a clean and professional HR analytics theme.

### Design Features

* KPI cards for high-level metrics
* Consistent color palette
* Rounded visual borders
* Shadow effects
* Professional header section
* Dashboard logo
* Consistent chart formatting
* Data labels for improved readability
* Conditional formatting
* Interactive slicers
* Structured visual layout

The formatting was standardized across visuals using Power BI's **Format Painter** to maintain consistency.

---

## 🔍 Key Business Insights

The dashboard can help HR teams answer questions such as:

* How many employees currently work in the organization?
* What is the overall employee attrition rate?
* Which departments have the highest attrition?
* Which salary slabs experience greater employee turnover?
* Which job roles have higher attrition?
* Does employee satisfaction appear to be associated with attrition?
* Which age groups represent the largest portion of the workforce?
* How does attrition differ across gender groups?
* At which experience levels is attrition more common?
* Which departments have the largest workforce?

These insights can support **employee retention strategies, workforce planning, compensation analysis, and HR decision-making**.

---

## 🛠️ Tools & Technologies

| Tool                   | Purpose                                   |
| ---------------------- | ----------------------------------------- |
| **Microsoft Power BI** | Dashboard development and visualization   |
| **Power Query**        | Data cleaning and transformation          |
| **DAX**                | Calculated measures and KPIs              |
| **Excel/CSV**          | Source data                               |
| **GitHub**             | Project documentation and version control |

---

## 📂 Project Structure

```text
HR-Analytics-PowerBI/
│
├── 📊 HR_Analytics_Dashboard.pbix
├── 📁 Dataset/
│   └── HR_Analytics_Data.csv
│
├── 🖼️ Dashboard/
│   └── HR_Analytics_Dashboard.png
│
└── 📄 README.md
```

> File names may vary depending on the final project structure.

---

## 🚀 How to Use the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/HR-Analytics-PowerBI.git
```

### 2. Open the Power BI File

Open:

```text
HR_Analytics_Dashboard.pbix
```

using **Microsoft Power BI Desktop**.

### 3. Check the Data Source

If the dataset path has changed, update the data source location in Power BI.

Go to:

```text
Home → Transform Data → Data Source Settings
```

and update the source path if required.

### 4. Explore the Dashboard

Use the Department and Age Group slicers to interact with the dashboard and explore different workforce segments.

---

## 💡 Skills Demonstrated

This project demonstrates practical skills in:

* Power BI Dashboard Development
* Data Cleaning
* Power Query
* Data Transformation
* DAX
* KPI Development
* Data Visualization
* HR Analytics
* Attrition Analysis
* Workforce Analytics
* Interactive Filtering
* Dashboard UI/UX Design
* Business Intelligence
* Data Storytelling

---

##  **Project Highlights**

* ✅ Cleaned and transformed raw HR data using Power Query
* ✅ Identified and removed duplicate records
* ✅ Standardized inconsistent categorical values
* ✅ Corrected data types
* ✅ Created calculated fields
* ✅ Developed DAX measures
* ✅ Built interactive KPI cards
* ✅ Created multiple analytical visuals
* ✅ Added conditional formatting
* ✅ Implemented interactive slicers
* ✅ Designed a professional Power BI dashboard
* ✅ Converted raw employee data into actionable HR insights

---

## 📷 Dashboard Preview

Add your dashboard screenshot here:

```markdown
![HR Analytics Dashboard](Dashboard/HR_Analytics_Dashboard.png)
```

---

## 🔮 Future Improvements

Potential improvements for future versions include:

* Adding monthly or yearly attrition trends.
* Adding employee tenure buckets.
* Creating a dedicated executive summary page.
* Adding salary and compensation analysis.
* Including recruitment and hiring metrics.
* Adding drill-through pages for individual departments.
* Implementing more advanced DAX calculations.
* Adding bookmarks for different analytical views.
* Connecting the dashboard to a live or regularly refreshed HR data source.

---

## 👤 Author

**Khadija Hamidani**

Data Analytics | Power BI | SQL | Excel | Data Visualization

If you found this project useful, feel free to ⭐ **star the repository** and explore the other projects in my portfolio.

---

## 📄 Disclaimer

This project is created for **learning, portfolio, and demonstration purposes**. The dataset and analysis should not be interpreted as representing the actual workforce or HR practices of a specific organization.
