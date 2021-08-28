*[Dax Guide](https://dax.guide/)*

[COMBINEVALUES(<delimiter>, <expression>, <expression>[, <expression>]…)](https://docs.microsoft.com/en-us/dax/combinevalues-function-dax)


[CONCATENATE(<text1>, <text2>)](https://docs.microsoft.com/en-us/dax/concatenate-function-dax)


DATESBETWEEN
`Sales PYTD =
VAR startyear = 
    STARTOFYEAR (PREVIOUSYEAR ('DATE'[DATE]))
VAR enddate =
    LASTDATE(Sales[Date) -365])
Return
    Calcuate(
        (Sales[Sales]),
        DatesBetween('Calendar'[date],startyear, endyear)

`

[isFiltered](https://dax.guide/isfiltered/)
Returns true when there are direct filters on the specified column.
`ISFILTERED ( Product[Color] )`

[PARALLELPERIOD](https://dax.guide/parallelperiod/)
Returns a parallel period of dates by the given set of dates and a specified interval.

previous row or value:
`rowNum = 
Var preRow =
    TOPN(
        1,
        FILTER(
            MaitreD,
            MaitreD[RESTAURANT_ID] = EARLIER(MaitreD[RESTAURANT_ID]) && EARLIER(MaitreD[INVOICE_ID]) <MaitreD[INVOICE_ID]
        ),
        MaitreD[INVOICE_ID],
        DESC
    )
Var preValue = MAXX(preRow,[INVOICE_ID])
Return preValue
`

[RANKX](https://dax.guide/rankx/)
`RANKX(ALL(Customers), SUMX(RELATEDTABLE(Sales), [Sales_amount]))`
- default sorting: 0/false/desc -- descending
`RANKX(ALL(Products), SUMX(RELATEDTABLE(InternetSales), [SalesAmount]))`

[RELATED(<column>)  ](https://docs.microsoft.com/en-us/dax/related-function-dax)
Returns a related value from another table

[RELATEDTABLE(<tableName>)  ](https://docs.microsoft.com/en-us/dax/relatedtable-function-dax)
Evaluates a table expression in a context modified by the given filters
- The RELATEDTETABLE function changes the context in which the data is filtered, and evaluates the *expression* in the new context that you specify.
- This function is a shortcut for CALCULATETABLE function with no logical expression.


[TOPN(<n_value>, <table>, <orderBy_expression>, [<order>[, <orderBy_expression>, [<order>]]…]) ](https://docs.microsoft.com/en-us/dax/topn-function-dax)
`EVALUATE
    TOPN (
        3,
        ADDCOLUMNS (
            VALUES ( 'Product'[Product Name] ),
            "@Sales Amount", [Sales Amount]
        ),
        [@Sales Amount],
        DESC
    )
`
