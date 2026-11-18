# Insurance-Dashboard

### Dashboard Link : https://drive.google.com/file/d/1q71CEhIaBC8eU6OkIOuoUFReR618WMM9/view?usp=sharing

## Problem Statement

This dashboard helps an insurance company understand its policies, premiums and claims in one place. It shows how much premium is collected and how much coverage and claim amount is involved, so the company can see which policy types bring in the most premium, which age groups claim the most, and how many claims are approved, pending or rejected. It also shows how many policies are active or inactive, so the company can look into why policies lapse.

> The dataset used is a practice/sample dataset (`InsuranceData\_Dummy`), not real company data.

\---

## Dataset

|Detail|Info|
|-|-|
|Table|`InsuranceData\_Dummy`|
|Source|\[CSV / Excel file, confirm]|
|Records|101|
|Key fields|PolicyType, CustomerID, ClaimNumber, Gender, AgeGroup, PremiumAmount, CoverageAmount, ClaimAmount, ClaimStatus, Active/Inactive|

## Tools Used

* Power BI Desktop
* DAX \[keep only if you wrote DAX]
* Power Query (data cleaning) \[confirm]

\---

## Steps followed

* Step 1 : Loaded the insurance data into Power BI Desktop.
* Step 2 : Checked the data in Power Query editor for errors, blanks and wrong data types. \[confirm and describe what you found or fixed]
* Step 3 : Applied a theme and added a header text box with the company name, "PRISM INSURANCE PVT. LTD".
* Step 4 : Added three slicers for **Policy Type**, **Customer ID** and **Claim Number**, so users can filter the whole report.
* Step 5 : Added three card visuals for **Total Premium Amount**, **Total Coverage Amount** and **Total Claim Amount**.
* Step 6 : Added a multi-row card showing the number of customers by **Gender**.
* Step 7 : Added a ribbon chart, **Number of Claims by Claim Status**.
* Step 8 : Added a bar chart, **Premium Amount by Policy Type**.
* Step 9 : Added a line chart, **Claim Amount by Age Group**.
* Step 10 : Added a donut chart, **Active/Inactive Policies**.
* Step 11 : Added a matrix of **Coverage Amount by Claim Status and Policy Type**.
* Step 12 :Created a calculated column or measure.

```
  Approved Claims =
CALCULATE(

CALCULATE(
DISTINCTCOUNT(InsuranceData\_Dummy\[ClaimNumber]),
InsuranceData\_Dummy\[ClaimStatus] = "Approved"
)

Claim Approval Rate % = DIVIDE(\[Approved Claims], \[Total Claims]) \* 100

```


---
# Snapshot of Dashboard (Power BI Desktop)

![Insurance Dashboard](https://github.com/user-attachments/assets/9a86045f-ddaa-4d8d-9114-20cbbb14de2a)

https://github.com/user-attachments/assets/9a86045f-ddaa-4d8d-9114-20cbbb14de2a


---

# Insights

> Fill these in from your own dashboard. Write the exact numbers you see on your visuals.

### \[1] Totals
- Total Premium Amount = 1.43M
- Total Coverage Amount = 167M
- Total Claim Amount = 4.27M

### \[2] Policy Type
- Highest premium comes from Life Insurace \*\* 0.48M.
- Lowest premium comes from Home Insurace \*\* 0.29M.

### \[3] Claims
- Number of claims by status: \[Approved = 6, Pending = 10, Rejected = 7].
- The age group with the highest claim amount is Adult (25-60) Amount of (3.3M).

### \[4] Policies and Customers
- Active policies = \[67 %], inactive policies = \[33 %].
- Customers by gender: Male = \[54], Female = \[46].

### \[5] Recommendation
- An insurance company provides financial protection to customers against potential risks.

