# Orders Sales Target Analysis | Power BI

## Project Overview

This project analyzes order sales performance against sales targets using **Microsoft Power BI**. The report is designed to help stakeholders compare actual sales with target values, monitor performance over time, and identify categories or segments that may require attention.

The project demonstrates core Power BI skills, including data modeling, DAX measures, time-based analysis, KPI cards, and matrix visualizations.

## Business Objectives

- Compare actual sales with sales targets.
- Analyze sales and target performance by category and month.
- Monitor year-to-date (YTD) sales performance.
- Present total sales and sales target KPIs for quick comparison.
- Display the minimum sales target by segment.
- Make it easier to identify performance gaps and areas for improvement.

## Tools and Technologies

- **Microsoft Power BI Desktop** — report development and visualization
- **DAX (Data Analysis Expressions)** — measures and calculations
- **Power Query** — data preparation and transformation, where applicable
- **GitHub** — project documentation and portfolio presentation

## Dashboard Features

### 1. Sales Performance Matrix
A matrix view compares actual sales with sales targets across categories and months. This helps users explore how performance changes over time and which categories are meeting or missing their targets.

### 2. Total Sales and Sales Target KPI Cards
KPI cards display total sales alongside the sales target, providing a quick high-level comparison.

### 3. Year-to-Date (YTD) Sales Analysis
YTD calculations help track cumulative sales from the beginning of the year through the selected reporting date. This supports progress monitoring during the year.

### 4. Minimum Target by Segment
A multi-row card displays the minimum sales target for each segment, making it easier to compare target levels across segments.

### 5. Interactive Analysis
Power BI filters and slicers, where included in the report, allow users to explore the data by available categories, months, or segments.

## Example DAX Measures

> Measure names and table/column names may differ depending on the model. Adjust these examples to match the fields in your PBIX file.

### Total Sales

```DAX
Total Sales =
SUM('Orders'[Sales])
```

### Total Sales Target

```DAX
Total Sales Target =
SUM('Sales target'[Sales target])
```

### Minimum Target

```DAX
Minimum Target =
MIN('Sales target'[Sales target])
```

Use **Minimum Target** in a visual grouped by Segment to show the minimum target for each segment. Confirm that the target table's relationships and filter context are configured correctly so the measure returns the intended result.

### Year-to-Date Sales

If the model contains a properly configured date table related to the sales date, a YTD measure can follow this pattern:

```DAX
Sales YTD =
TOTALYTD(
    [Total Sales],
    'Date'[Date]
)
```

Replace `'Date'[Date]` with the date column in your model. A dedicated, continuous date table is recommended for reliable time-intelligence calculations.

## Business Questions

This report is designed to help answer questions such as:

- How do actual sales compare with targets?
- Which categories perform better or worse across months?
- How are sales progressing year to date?
- What are the total sales and target values for the selected period?
- How do minimum targets vary across segments?

## Key Insights

Use the completed report to document evidence-based findings. Examples of useful insights to investigate:

- Categories and months where actual sales exceed the target.
- Categories and months with the largest shortfall against target.
- Changes in cumulative YTD sales over the reporting period.
- Differences in minimum targets across segments.

**Note:** Add the actual findings and figures from your report here before publishing. Do not present these examples as confirmed results unless they are supported by the data.

## Business Recommendations

Recommendations should follow the results shown in the report. Potential actions to consider include:

- Review categories and months with recurring target shortfalls.
- Investigate factors behind strong-performing categories and consider replicating effective practices.
- Monitor YTD progress regularly so that gaps can be addressed earlier.
- Review target-setting approaches across segments to ensure comparisons are meaningful.

Tailor these recommendations to the verified insights from your report.

## How to View the Project

1. Download `Orders_Sales_Target_Analysis.pbix` from this repository.
2. Open the file using **Microsoft Power BI Desktop**.
3. Interact with the report visuals and use any available slicers or filters to explore performance.

## Repository Structure

```text
Orders-Sales-Target-Analysis/
├── Orders_Sales_Target_Analysis.pbix
└── README.md
```

## Skills Demonstrated

- Business performance analysis
- KPI reporting and dashboard design
- DAX measures and aggregations
- Year-to-date analysis
- Matrix and card visualizations
- Sales-versus-target comparison
- Data storytelling and business recommendations

## Future Improvements

- Add a sales achievement percentage KPI.
- Add a variance measure showing the difference between actual sales and target.
- Use conditional formatting to highlight target achievement and shortfalls.
- Add trend charts and drill-through pages for deeper analysis.
- Publish verified screenshots of the dashboard in this repository.

## Author

**Your Name**  
Aspiring Data Analyst | Power BI | Excel | Data Visualization

Connect with me on [LinkedIn](YOUR_LINKEDIN_URL) and explore more projects on [GitHub](YOUR_GITHUB_URL).

---

*This project was created for learning and portfolio development. All findings and recommendations should be validated against the report data before being used for business decisions.*
