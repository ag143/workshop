AFTERDELIMITER
```
Text.AFTERDELIMITER([product_SKU], "x", {0, RELATIVEPOSITION.FromEnd})
```
-contains only string after "x"

highest spending customers  
``` Top 100 Customers = TOPN(100, SUMMARIZE(FactTrans,FactTrans[Customer ID], "Sales", SUM(FactTrans[Sale])))```

List.Dates(#date(2011,05,31), 365*10, #duration(1,0,0,0))


Text.replace
- replace first 6 letter of column [SSN]
```Text.Replace([SSN], Text.Start([SSN],6), "xxx-xx")```

[Table.ReplaceValue(table as table, oldValue as any, newValue as any, replacer as function, columnsToSearch as list)](https://docs.microsoft.com/en-us/powerquery-m/table-replacevalue)

remove any columns that have a suffix of sourceid.
```removeSources = Table.RemoveColumns(rawData, List.Select(Table.ColumnNames(rawData),each Text.EndsWith(_,"sourceid")))```

show percentile for selected data
```Product Category % of total 2 = 
    DIVIDE([Total Sales]),
        CALCULATE([Total Sales],
            ALLSELECTED(
                Product[ProductCategoryName]
            )
        )
    )
```

Revenue Last 50 Transactions= 
```
CALCULATE(
    SUM(Transactions[Amount]),
    TOPN(50, Transactions, Transactions[TransactionDate]),
    desc
)
```
