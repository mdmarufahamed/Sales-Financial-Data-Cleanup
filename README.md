The Dataset: 
This dataset contains sales transaction records with client names, payments, revenue, and profit.

The Problems I Found:
Inconsistent Client Names: e.g., AMAZON.COM, INC. (XNAS:AMZN) vs. amazon.com, inc.
Inconsistent Contact Names: e.g., Bill SmITH, KEN Singh (needed capitalization fix).
Combined "Department_Region" Column: Needed to be split into two separate columns for better analysis.
Missing Payment Methods: Blank cells.
Missing Revenue Data: Which breaks the Profit Margin formula.
Remove Duplicates

My Cleaning Process:
Standardization: Used PROPER, LOWER, or UPPER functions to fix text cases.
Text-to-Columns: Used the _ delimiter to split the Department/Region column.
Handling Missing Data: Flagged missing Payment and Revenue values as "NA" to make the gaps explicit.
Robust Formulas: Changed the Profit Margin formula to =IFERROR(Profit/Revenue,"NA") to avoid division-by-zero errors from missing revenue.

The Outcome: 
A clean, analysis-ready table where you could easily filter by region, calculate average profit by department, etc.
