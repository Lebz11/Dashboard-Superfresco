# Key DAX Measures

The dashboard includes several DAX measures to enhance analytical insights.

## Return Metrics
- **Total Returns**: `COUNTROWS(Devoluciones)`
- **Return Rate**: `DIVIDE([Total Returns], [Total Transactions])`
- **Average Return Value**: `AVERAGEX(Devoluciones, Devoluciones[ReturnAmount])`

## Time Intelligence
- **YTD Returns**: `TOTALYTD([Total Returns], Calendario[Date])`
- **Monthly Trend**: Uses `FORMAT(Calendario[Date], "MMM YYYY")`

## Geography
- **Returns by Region**: Uses `RELATED(Tiendas[Region])`
- **Store Ranking**: `RANKX(ALL(Tiendas), [Total Returns])`

## Product
- **Top Returned Products**: Based on volume and value.
- **Return % by Category**: DAX for category-level return rate.
