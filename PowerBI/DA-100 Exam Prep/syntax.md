*[Dax Guide](https://dax.guide/)*


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
    )`

[isFiltered](https://dax.guide/isfiltered/)
Returns true when there are direct filters on the specified column.
`ISFILTERED ( Product[Color] )`