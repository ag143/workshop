
**Data preparation** is the process of profiling, cleaning, and transforming your data to get it ready to model and visualize

Parts of PowerBI:
1. Power BI Desktop
2. Power BI service (online SaaS)
3. Power BI Apps (mobile)

**dashboard** is a collection of reports in a single page, from which users can go to full reports

**Stepped layout** in format of report, to show hierarchy in different columns



===========================================================

# Notes:
+ only one Active Relation between tables
+ Append will not remove duplicates
+ 'Active' relationship will propagate filters between tables in the direction of 'Arrow Head'
+ calculated columns are stored in .pbix file, but calculated measures are not (calculated on demand)
+ Mark as Date Table
+ [multiple filter conditions](https://www.sqlbi.com/articles/specifying-multiple-filter-conditions-in-calculate/)
+ [**semi-additive calculation/measure**](https://www.sqlbi.com/articles/semi-additive-measures-in-dax/)
    In situations where you don't want the standard evaluation behavior in Power BI, you can use the CALCULATE and/or USERELATIONSHIP functions. However, more circumstances exist where you don't want the standard behavior. One of those situations is when you have a semi-additive problem to resolve. Standard measures are simple concepts, where they might use the SUM, AVERAGE, MIN, and MAX functions. Thus far, you've been using SUM for the Total Sales measure.

    Occasionally, summing a measure doesn't make sense, such as when you are performing inventory counts in a warehouse. For example, if on Monday, you have 100 mountain bikes, and on Tuesday you have 125 mountain bikes, you wouldn't want to add those together to indicate that you had 225 mountain bikes between those two days. In this circumstance, if you want to know your stock levels for March, you would need to tell Power BI not to add the measure but instead take the last value for the month of March and assign it to any visual.

    You can use the CALCULATE function to complete this action, along with the LastDate function, as shown in the following example:

    >Last Inventory Count =
    >CALCULATE (
    >    SUM ( 'Warehouse'[Inventory Count] ),
    >    LASTDATE ( 'Date'[Date] ))

    This approach will stop the SUM from crossing all dates. Instead, you will only use the SUM function on the last date of the time period, thus effectively creating a semi-additive measure.

+ [Direct Query](https://community.powerbi.com/t5/Desktop/direct-query-vs-import/m-p/112212)
    just bring in schema of table
    Generally, it's up to date (live), but [Scheduled cach refresh](https://powerbi.microsoft.com/fr-fr/blog/announcing-custom-cache-refresh-schedules-in-the-power-bi-service/) is required.

## Report Navigation
- move between pages
- use buttons, bookmarks, or conditional formatting

## Model Optimization
+ Variable
+ Performance Analyzer
+ Review performance results
+ Analyze query plan
+ Reduce Cardinality
+ Implement Table Granularity
+ [data reduction](https://docs.microsoft.com/en-ca/power-bi/guidance/import-modeling-data-reduction#group-by-and-summarize)


## links
[report template](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-templates)
[different Cardinatily meanings in modeling and query](https://stackoverflow.com/questions/10621077/what-is-cardinality-in-databases)

============================================================
# Formula

+ Variables  
    can be useful for simplifying the formula logic, and more efficient when an expression needs to be evaluated multiple times within the formula (which will be the case for the YoY growth logic). Variables are declared by a unique name, and the measure expression must then be output after the RETURN keyword.

+ Calculate(expression, filterContext)  
    most used.    
    a powerful function used to manipulate the filter context. The first argument takes an expression or a measure (a measure is just a named expression). Subsequent arguments allow modifying the filter context.
+ RemoveFilters()  
    removes active filters. It can take either no arguments, or a table, a column, or multiple columns as its argument.
+ CalendarAuto(M)  
    M: last month number of a year, default is 12
+ [HasOneValue()](https://docs.microsoft.com/en-us/dax/hasonevalue-function-dax)
+ UseRelationship
+ LastDate()
+ [TOTALYTD()](https://docs.microsoft.com/en-us/dax/totalytd-function-dax)
    evaluates an expression—in this case the sum of the Sales column—over a given date column. The date column must belong to a date table marked as a date table, as was done in the Create DAX Calculations in Power BI Desktop, Part 1 lab.

    The function can also take a third optional argument representing the last date of a year. The absence of this date means that December 31 is the last date of the year. For Adventure Works, June in the last month of their year, and so “6-30” is used.

    The TOTALYTD() function performs filter manipulation, specifically time filter manipulation. For example, to compute YTD sales for September 2017 (the third month of the fiscal year), all filters on the Date table are removed and replaced with a new filter of dates commencing at the beginning of the year (July 1, 2017) and extending through to the last date of the in-context date period (September 30, 2017).

    Note that many Time Intelligence functions are available in DAX to support common time filter manipulations.

+ [All()](https://docs.microsoft.com/en-us/dax/all-function-dax)
    Returns all the rows in a table, or all the values in a column, ignoring any filters that might have been applied.
    >LastBalanceDate = CALCULATE ( MAX ( Balances[Date] ), ALL ( Balances[Name] ) )

+ [Evaluate()](https://dax.guide/st/evaluate/)

+ [Row()](https://docs.microsoft.com/en-us/dax/row-function-dax)  
    Returns a table with a **single** row containing values that result from the expressions given to each column.


============================================================
# Shortkey
+ *shift+enter* : carriage return in DAX editor