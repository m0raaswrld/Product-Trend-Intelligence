// ============================================
// PowerBI Practical Exam – [Your Name]
// ============================================

// ============================================
// 1. Overview
// ============================================
// A data-driven sales performance dashboard built using the AdventureWorks dataset
// to uncover profit drivers, market trends, and customer behavior.

// ============================================
// 2. Dataset & Preparation
// ============================================
// Source: AdventureWorksDW2020
// Fact table: Sales (10,000+ rows)
// Dimensions: Products, Customers, Dates, Geography
// Cleaning steps:
// - Removed data before 2018
// - Handled nulls
// - Removed duplicates
// - Categorized sales

// ============================================
// 3. Methodology
// ============================================
// - Power Query for ETL
// - Star schema model with optimized relationships
// - DAX for advanced KPIs (YoY Growth, Running Total, CLV)
// - Interactive visuals with drill-through, bookmarks, and sync slicers

// ============================================
// 4. Key Insights
// ============================================
// - Electronics contributed 40% of sales, but only 25% of total profit — pricing optimization potential
// - 60% of customers are concentrated in 3 states — geographic expansion opportunity
// - High-value customers (> $10k/year) showed 8% YoY growth; low-value customers declining

// ============================================
// 5. Challenges & Solutions
// ============================================
// Challenge: Misaligned date formats
// Solution: Standardized via Power Query transformations
// 
// Challenge: Category hierarchy gaps
// Solution: Filled missing subcategories via reference table
// 
// Challenge: Performance with large joins
// Solution: Replaced calculated columns with measures

// ============================================
// 6. Assumptions & Limitations
// ============================================
// - Forecast assumes linear growth
// - Profit margin based on current cost — no variable cost modeling

// ============================================
// 7. Deliverables
// ============================================
// - .pbix file: PowerBI_Practical_Exam_YourName.pbix
// - PDF Export: Sales_Report.pdf
// - Power BI Service Link: https://app.powerbi.com/view?r=example
// - Screenshots:
//   - Sales Overview: ./screenshots/sales_overview.png
//   - Product Analysis: ./screenshots/product_analysis.png

