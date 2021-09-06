*[Dax Guide](https://dax.guide/)*

COMBINEVALUES(delimiter, expression, expression[, expression]…) [syntax](https://docs.microsoft.com/en-us/dax/combinevalues-function-dax)


CONCATENATE(text1, text2) [syntax](https://docs.microsoft.com/en-us/dax/concatenate-function-dax)

COUNTA(column) [syntax](https://docs.microsoft.com/en-us/dax/counta-function-dax)
- counts the number of cells in a column that are not empty

DATESBETWEEN
```Sales PYTD =
VAR startyear = 
    STARTOFYEAR (PREVIOUSYEAR ('DATE'[DATE]))
VAR enddate =
    LASTDATE(Sales[Date) -365])
Return
    Calcuate(
        (Sales[Sales]),
        DatesBetween('Calendar'[date],startyear, endyear)

```

DATESINPERIOD(Calendar[Date], MAX (Calendar[Date]), 10, DAY)

HasOneValue
```
IF(
 HASONEVALUE('Salesperson (Performance)'[Salesperson]),
 SUM(Targets[TargetAmount])
 )
 ```

ISINSCOPE() function is used to test whether the region column is the level in a hierarchy


[isFiltered](https://dax.guide/isfiltered/)  
ISFILTERED ( TableNameOrColumnName )                 
TRUE when ColumnName is being filtered directly, or when any column of TableName is being filtered directly  
```
ISFILTERED ( Product[Color] )
```

LASTNONBLANK(column,expression)  [syntax](https://docs.microsoft.com/en-us/dax/lastnonblank-function-dax)
- Returns the last value in the column, column, filtered by the current context, where the expression is not blank

KEEPFILTERS(expression)
- for CALCULATION, default behavior is to keep override the filters mentioned in the parameter
- KeepFilters works like 'and' to add extra filter to the same column

[Outliers =](https://docs.microsoft.com/en-us/learn/modules/perform-analytics-power-bi/3-visuals)
```
CALCULATE (
    [Order Qty],
    FILTER (
        VALUES ( Product[Product Name] ),
        COUNTROWS ( FILTER ( Sales, [Order Qty] = [Min Qty] ) )  0
    )
)
```

[PARALLELPERIOD](https://dax.guide/parallelperiod/)
Returns a parallel period of dates by the given set of dates and a specified interval.

previous row or value:
```rowNum = 
Var preRow =
    TOPN(
        1,
        FILTER(
            MaitreD,
            MaitreD[RESTAURANT_ID] = EARLIER(MaitreD[RESTAURANT_ID]) && EARLIER(MaitreD[INVOICE_ID]) = MaitreD[INVOICE_ID]
        ),
        MaitreD[INVOICE_ID],
        DESC
    )
Var preValue = MAXX(preRow,[INVOICE_ID])
Return preValue
```

[RANKX](https://dax.guide/rankx/)
```
RANKX(ALL(Customers), SUMX(RELATEDTABLE(Sales), [Sales_amount]))
```
- default sorting: 0/false/desc -- descending
```
RANKX(ALL(Products), SUMX(RELATEDTABLE(InternetSales), [SalesAmount]))
```

[RELATED(column)  ](https://docs.microsoft.com/en-us/dax/related-function-dax)
Returns a related value from another table

[RELATEDTABLE(tableName)  ](https://docs.microsoft.com/en-us/dax/relatedtable-function-dax)
Evaluates a table expression in a context modified by the given filters
- The RELATEDTETABLE function changes the context in which the data is filtered, and evaluates the *expression* in the new context that you specify.
- This function is a shortcut for CALCULATETABLE function with no logical expression.

[SWITCH(expression, value, result[, value, result]…[, else])](https://docs.microsoft.com/en-us/dax/switch-function-dax)


[TOPN(n_value, table, orderBy_expression, [order[, orderBy_expression, [order]]…]) ](https://docs.microsoft.com/en-us/dax/topn-function-dax)
```EVALUATE
    TOPN (
        3,
        ADDCOLUMNS (
            VALUES ( 'Product'[Product Name] ),
            "@Sales Amount", [Sales Amount]
        ),
        [@Sales Amount],
        DESC
    )
```

[VALUES(TableNameOrColumnName)](https://docs.microsoft.com/en-us/dax/values-function-dax)
A column from which unique values are to be returned, or a table from which rows are to be returned

