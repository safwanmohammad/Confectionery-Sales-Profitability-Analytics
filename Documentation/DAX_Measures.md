# DAX Measures

## Total Sales

```DAX
Total Sales = SUM('06_Clean_Sales'[Sales])
```

## Total Units

```DAX
Total Units = SUM('06_Clean_Sales'[Units])
```

## Total Records

```DAX
Total Records = COUNTROWS('06_Clean_Sales')
```

## Total Products

```DAX
Total Products = DISTINCTCOUNT('06_Clean_Sales'[Product ID])
```

## Total Gross Profit

```DAX
Total Gross Profit = SUM('06_Clean_Sales'[Gross Profit])
```

## Total Cost

```DAX
Total Cost = SUM('06_Clean_Sales'[Cost])
```

## Top Region

```DAX
Top Region =
CONCATENATEX(
    TOPN(
        1,
        ALL('06_Clean_Sales'[Region]),
        [Total Sales],
        DESC
    ),
    '06_Clean_Sales'[Region]
)
```

## Sales Records

```DAX
Sales Records = COUNTROWS('06_Clean_Sales')
```

## Gross Margin

```DAX
Gross Margin = [Total Gross Profit] / [Total Sales]
```

## Avg Sales Per Record

```DAX
Avg Sales Per Record = DIVIDE([Total Sales],[Total Records],0)
```

## Avg Sales Per Product

```DAX
Avg Sales Per Product = DIVIDE([Total Sales],[Total Products])
```

## Avg Gross Profit per Record

```DAX
Avg Gross Profit per Record = DIVIDE([Total Gross Profit],[Total Records],0)
```

## Avg Gross Profit / Product

```DAX
Avg Gross Profit / Product = DIVIDE([Total Gross Profit],[Total Products])
```

## Avg Gross Margin

```DAX
Avg Gross Margin = DIVIDE([Total Gross Profit],[Total Sales])
```

## Avg Cost Per Record

```DAX
Avg Cost Per Record = DIVIDE([Total Cost],[Total Records],0)
```
