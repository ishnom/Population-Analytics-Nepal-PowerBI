# DAX Measures and Calculations

## Measures
- **Total population of country**
  - `SUM(census[Total population])`

- **Total Household**
  - `SUM(census[Total household number])`

- **Total Families sum**
  - `SUM(census[Total family number])`

- **Avg household size**
  - `DIVIDE([Total population of country],[Total Household],0)`

- **Avg family Size**
  - `DIVIDE([Total population of country],[Total Familes sum],0)`

- **Total Female in Country**
  - `SUM(census[Total Female])`

- **Total male in country**
  - `SUM(census[Total Male])`

## Calculated Table
### District Population
```
SUMMARIZE(
    census,
    census[District],
    "Total Population", SUM(census[Total Population]),
    "Female Population", SUM(census[Total Female])
)
```
