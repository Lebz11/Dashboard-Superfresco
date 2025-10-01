# Power Query Transformations

This section describes the data transformation steps applied to the source files using Power Query in Power BI.

## Common Steps

Most CSV files went through the following basic steps:
- Removed extra headers or blank rows.
- Changed data types to ensure consistency (e.g., dates, numbers).
- Renamed columns for clarity.
- Applied filters to remove null or invalid values.

## Individual File Transformations

### 1. Calendario.csv
- Generated a continuous date table from `2027-01-01` to `2028-09-09`.
- Added calculated columns: Year, Month, Quarter, Day of Week.

### 2. Clientes.csv
- Split full names into First Name and Last Name.
- Cleaned membership ID and ensured uniqueness.
- Filtered out inactive or test customer records.

### 3. Devoluciones.csv
- Removed duplicate records.
- Added a flag for returns with high value.
- Merged with `Clientes.csv` for demographic analysis.

### 4. Productos.csv
- Cleaned product names and removed discontinued items.
- Parsed pricing data into separate columns: Base Price, Discount, Final Price.
- Mapped categories to broader product groups.

### 5. Tiendas.csv
- Converted location coordinates to a readable format.
- Created a derived column for store region/grouping.