 ============================================

 PowerBI Practical Exam – [Mitchelle Moraa]

 ============================================

 ============================================

 1. Overview

 ============================================

  This project presents a data-driven sales performance dashboard developed using the AdventureWorksDW2020 dataset. The dashboard aims to uncover profit drivers, market trends, and customer behavior, providing actionable insights for decision-making. 
  Key objectives included identifying top-performing products, analyzing customer segments, and assessing geographic sales distribution to guide strategic growth.

 ============================================

 2. Dataset & Preparation

 ============================================

  Source: AdventureWorksDW2020
  Fact table: Sales , Products, Customers, Dates, Sales Territory
  Cleaning steps:
  - Removed data before 2018
  - Handled nulls
  - Removed duplicates
  - categorized sales by product line, subcategory, and region

   Power Query

 <p 
  <img src="Screenshots/PowerQueryScreenshot/Sales%20(3).png.jpg" width="300"/>
  <img src="Screenshots/PowerQueryScreenshot/Customer.png.jpg" width="300"/>
  <img src="Screenshots/PowerQueryScreenshot/Product%20(2).jpg" width="300"/>
 </p>


 ============================================

 3. Methodology

 ============================================

  - ETL: Power Query for data extraction, cleaning, and transformation
  - Data Model: Star schema design with optimized relationships between fact and dimension tables
  - KPI Calculations: Advanced measures in DAX including Year-over-Year (YoY) growth, Running Totals, and Customer Lifetime Value (CLV)
  
  ![Star Schema](Screenshots/ModelView/StarSchema1.jpg)

  ![Star Schema 2](Screenshots/ModelView/StarSchema2.jpg)

  ![Star Schema 3](Screenshots/ModelView/StarSchema3.jpg)


 Visualizations:

  - Interactive dashboards with drill-through capabilities
  - Bookmarks and synchronized slicers for cross-filtering
  - Bubble maps, bar charts, and line graphs to highlight trends

  VisualsGallery
 
 <p align="center">
  <img src="Screenshots/VisualsGallery/BarChartTop7Products.jpg" width="250" style="margin-right:15px"/>
  <img src="Screenshots/VisualsGallery/BubbleChart.jpg" width="250" style="margin-right:15px"/>
  <img src="Screenshots/VisualsGallery/DecompositionTree.jpg" width="250"/>
 </p>

 <p align="center">
  <img src="Screenshots/VisualsGallery/KPICard.jpg" width="250" style="margin-right:15px"/>
  <img src="Screenshots/VisualsGallery/LineChartOfTotalSalesByMonth.jpg" width="250" style="margin-right:15px"/>
  <img src="Screenshots/VisualsGallery/MapVisual.jpg" width="250"/>
 </p>

 <p align="center">
  <img src="Screenshots/VisualsGallery/PieChartTotalSalesByCategory.jpg" width="250" style="margin-right:15px"/>
  <img src="Screenshots/VisualsGallery/ProfitMarginGauge.jpg" width="250" style="margin-right:15px"/>
  <img src="Screenshots/VisualsGallery/ScatterPlot.jpg" width="250"/>
 </p>

 
  Report Pages

 ![Customer Insights](Screenshots/ReportPages/CustomerInsights.jpg)

 ![Product Analysis](Screenshots/ReportPages/ProductAnalysis.jpg)

 ![Sales Overview](Screenshots/ReportPages/SalesOverview.jpg)

 
  Dashboard

 <p align="center">
  <img src="Screenshots/DASHBOARD/001.jpg" width="300"/>
  <img src="Screenshots/DASHBOARD/002.jpg" width="300"/>
  <img src="Screenshots/DASHBOARD/003.jpg" width="300"/>
 </p>

  ## Row-Level Security (RLS)

 <p align="center">
  <img src="Screenshots/RLS/RLS.jpg" width="500"/>
 </p>



 ============================================

 4. Key Insights

 ============================================

   Electronics account for ~38% of total sales, but only ~25% of overall profit, suggesting opportunities for pricing or cost optimization.

   Bikes and Accessories, while smaller in sales volume (~15–20%), contribute disproportionately to profit (~30%), indicating high-margin opportunities.

   Products with low sales but high profit margins can be prioritized for targeted marketing.

   60% of customers are concentrated in just 3–4 states, highlighting potential for geographic expansion.

   High-value customers (annual purchases > $10k) represent ~8–10% of the customer base but generate ~35% of total revenue, this shows that targeting high-value customers is more effective than increasing low-value customer volume.

   Low-value customers show a slight decline (~3% YoY), signaling a need for retention strategies.

   Peak sales occur in Q4 (Nov–Dec) and mid-year (July–August).

   Discounts and promotions drive temporary spikes in revenue, but often reduce profit margins.

   Electronics are typically purchased in single-item orders, while Bikes and Accessories often include multiple items per order.

   Large-value orders with few items suggest premium product purchases

 ============================================

 5. Challenges & Solutions

 ============================================

 Challenge: Complex KPI calculations
 Solution: Used DAX time intelligence functions 

 Challenge: Category hierarchy gaps
 Solution: Filled missing subcategories via reference table

 Challenge: Performance with large fact table
 Solution: Replaced calculated columns with measures

 Challenge: Handling nulls in customer demographic data
 Solution: Imputed missing values with defaults or categorized as “Unknown” to maintain analysis integrity

 ============================================

 6. Assumptions & Limitations

 ============================================

  - Forecast assumes linear growth without advanced predictive modeling
  - Profit margin based on current cost no variable cost modeling
  - Customer Lifetime Value (CLV) assumes constant retention rate and does not account for churn or acquisition costs.


 ============================================

 7. Deliverables

 ============================================

  - .pbix file: PowerBI_Practical_Exam_MitchelleMoraa.pbix
  - PDF Export: Report.pdf/Product Trend.pdf
  - Power BI Service Link: https://app.powerbi.com/reportEmbed?reportId=62590844-c7f6-40d4-8678-385409d6d612&autoAuth=true&ctid=16d83ee6-254a-469d-a6cc-54e2ca2313e7
  - Screenshots