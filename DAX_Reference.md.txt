// ============================================
// 1. YoY Growth %
// ============================================
YoY Growth % = 
DIVIDE(
    CALCULATE([Total Sales], SAMEPERIODLASTYEAR(Dates[Date])) - [Total Sales],
    [Total Sales]
)

// ============================================
// 2. Running Total Sales
// ============================================
Running Total Sales = 
CALCULATE(
    [Total Sales],
    FILTER(ALL(Dates), Dates[Date] <= MAX(Dates[Date]))
)

// ============================================
// 3. Top N Products (Top 5)
// ============================================
Top 5 Sales = 
RANKX(ALL(Products[ProductName]), [Total Sales], , DESC)

// ============================================
// 4. Customer Retention Rate
// ============================================
// Assumes Dates[Year] is text like "FY2020"
Retention Rate =
DIVIDE(
    CALCULATE(
        DISTINCTCOUNT(Customer[Customer ID]),
        FILTER(
            ALL(Dates),
            VALUE(RIGHT(Dates[Year], 4)) = VALUE(RIGHT(MAX(Dates[Year]), 4)) - 1
        )
    ),
    DISTINCTCOUNT(Customer[Customer ID])
)

// ============================================
// 5. Contribution Margin %
// ============================================
Contribution Margin % = DIVIDE([Profit], [SalesAmount])

// ============================================
// 6. RLS Roles
// ============================================

// US Manager
[Country] = "United States"

// Europe Manager
[Country] IN {"France","Germany","Italy", ...}
