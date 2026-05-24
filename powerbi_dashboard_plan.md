# Power BI Dashboard Plan for Vendor Performance

## Data source
Use the existing file: `vendor_sales_summary.csv`

Fields to use:
- VendorNumber
- VendorName
- Brand
- Description
- TotalPurchaseQuantity
- TotalPurchaseDollars
- TotalSalesQuantity
- TotalSalesPrice
- TotalSalesDollars
- TotalExciseTax
- FreightCost
- GrossProfit
- ProfitMargin
- StockTurnover
- SalesToPurchaseRatio

## Dashboard pages and layout

### Page 1: Executive Summary

- Top row: 4 KPI cards
  - `Total Sales` = `SUM('vendor_sales_summary'[TotalSalesDollars])`
  - `Total Gross Profit` = `SUM('vendor_sales_summary'[GrossProfit])`
  - `Average Profit Margin` = `AVERAGE('vendor_sales_summary'[ProfitMargin])`
  - `Average Stock Turnover` = `AVERAGE('vendor_sales_summary'[StockTurnover])`

- Filters panel (left or top)
  - Slicer: `VendorName`
  - Slicer: `Brand`
  - Slicer: `Description`

- Main visuals
  - Bar chart: `VendorName` on axis, `Total Sales` as value, color saturation by `ProfitMargin`
  - Clustered column chart: `Brand` on axis, `Total Gross Profit` as value
  - Scatter chart: `ProfitMargin` on X, `StockTurnover` on Y, bubble size `Total Sales`, legend `VendorName`
  - Table / matrix: `VendorName`, `Brand`, `TotalSalesDollars`, `GrossProfit`, `ProfitMargin`, `StockTurnover`
  - Card visuals for `Total Freight` and `Total Excise Tax`

### Page 2: Vendor Detail

- Filters panel
  - Slicer: `VendorName`
  - Slicer: `Brand`
  - Slicer: `Description`

- Detail visuals
  - Matrix visual with rows: `Description`, `Brand`; values: `TotalSalesDollars`, `TotalPurchaseDollars`, `GrossProfit`, `ProfitMargin`, `StockTurnover`
  - Bar chart: `Description` on axis, `GrossProfit` as value
  - Donut chart: breakdown of `TotalSalesDollars` by `Brand`
  - Card: `Sales to Purchase Ratio` = `AVERAGE('vendor_sales_summary'[SalesToPurchaseRatio])`

### Page 3: Cost and Efficiency

- Key measures
  - `Total Freight`
  - `Total Excise Tax`
  - `Average Sales to Purchase Ratio`

- Visuals
  - Stacked column chart: `VendorName` by `TotalSalesDollars` and `TotalPurchaseDollars`
  - Line chart or area chart: `ProfitMargin` trend by `VendorName` (if vendor count is small enough)
  - Scatter chart: `FreightCost` vs `GrossProfit`, size by `TotalSalesDollars`

## Recommended Power BI measures
Create these DAX measures after import:
- `Total Sales = SUM('vendor_sales_summary'[TotalSalesDollars])`
- `Total Profit = SUM('vendor_sales_summary'[GrossProfit])`
- `Average Profit Margin = AVERAGE('vendor_sales_summary'[ProfitMargin])`
- `Average Stock Turnover = AVERAGE('vendor_sales_summary'[StockTurnover])`
- `Total Freight = SUM('vendor_sales_summary'[FreightCost])`
- `Total Excise Tax = SUM('vendor_sales_summary'[TotalExciseTax])`
- `Sales to Purchase Ratio = AVERAGE('vendor_sales_summary'[SalesToPurchaseRatio])`
- `Average Sales to Purchase Ratio = [Sales to Purchase Ratio]`

## Build steps in Power BI Desktop
1. Open Power BI Desktop.
2. Click `Get data` → `Text/CSV` and select `vendor_sales_summary.csv`.
3. Load the data.
4. If needed, click `Transform Data` and ensure numeric fields are typed as `Decimal Number`.
5. Add slicers for `VendorName`, `Brand`, and `Description`.
6. Add KPI cards for the top measures.
7. Add the visuals listed above.
8. Use the matrix/table visual to let users drill into the best/worst vendors and brands.
9. Save the report as `Vendor Performance Dashboard.pbix`.

## Optional enhancement
If you want a more interactive report, add these:
- Drill-through page for a selected vendor with product-level details.
- Tooltip page showing `ProfitMargin`, `StockTurnover`, and `FreightCost`.
- Conditional formatting on the table by `ProfitMargin` or `GrossProfit`.

## Notes
The file `vendor_sales_summary.csv` already contains vendor-product-level summary data, so this is a strong starting point for an interactive Power BI dashboard.
