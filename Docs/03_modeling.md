# Data Modeling in Power BI

The data model was designed using a star schema approach, with a central fact table and supporting dimension tables.

## Fact Table

**Devoluciones** acts as the main fact table:
- Contains transactional data for product returns.

## Dimension Tables

- **Clientes**: Customer demographics and membership.
- **Productos**: Product catalog with pricing and attributes.
- **Tiendas**: Physical store data and location.
- **Calendario**: Date dimension used for time-based analysis.

## Relationships

- One-to-many relationships were created between:
  - `Clientes` → `Devoluciones`
  - `Productos` → `Devoluciones`
  - `Tiendas` → `Devoluciones`
  - `Calendario` → `Devoluciones`

All relationships use single direction filtering for performance optimization.
