
**Data preparation** is the process of profiling, cleaning, and transforming your data to get it ready to model and visualize

Parts of PowerBI:
1. Power BI Desktop
2. Power BI service (online SaaS)
3. Power BI Apps (mobile)

**dashboard** is a collection of reports in a single page, from which users can go to full reports

**Stepped layout** in format, to show hierarchy in different columns



===========================================================

# Notes:
+ only one Active Relation between tables
+ Append will not remove duplicates
+ 'Active' relationship will propagate filters between tables
+ calculated columns are stored in .pbix file, but calculated measures are not
+ Mark as Date Table
+ [**semi-additive calculation**](https://www.sqlbi.com/articles/semi-additive-measures-in-dax/)
+ [multiple filter conditions](https://www.sqlbi.com/articles/specifying-multiple-filter-conditions-in-calculate/)
+ **Semi-additive Measures**  
In situations where you don't want the standard evaluation behavior in Power BI, you can use the CALCULATE and/or USERELATIONSHIP functions. However, more circumstances exist where you don't want the standard behavior. One of those situations is when you have a semi-additive problem to resolve. Standard measures are simple concepts, where they might use the SUM, AVERAGE, MIN, and MAX functions. Thus far, you've been using SUM for the Total Sales measure.

Occasionally, summing a measure doesn't make sense, such as when you are performing inventory counts in a warehouse. For example, if on Monday, you have 100 mountain bikes, and on Tuesday you have 125 mountain bikes, you wouldn't want to add those together to indicate that you had 225 mountain bikes between those two days. In this circumstance, if you want to know your stock levels for March, you would need to tell Power BI not to add the measure but instead take the last value for the month of March and assign it to any visual.

You can use the CALCULATE function to complete this action, along with the LastDate function, as shown in the following example:

>Last Inventory Count =
>CALCULATE (
>    SUM ( 'Warehouse'[Inventory Count] ),
>    LASTDATE ( 'Date'[Date] ))

This approach will stop the SUM from crossing all dates. Instead, you will only use the SUM function on the last date of the time period, thus effectively creating a semi-additive measure.



============================================================
# formula
+ Calculate(expression, filterContext)  
    most used. To manipulate filter context  
    a powerful function used to manipulate the filter context. The first argument takes an expression or a measure (a measure is just a named expression). Subsequent arguments allow modifying the filter context.
+ RemoveFilters()  
    removes active filters. It can take either no arguments, or a table, a column, or multiple columns as its argument.
+ CalendarAuto(M)  
    M: last number of a year, default is 12
+ [HasOneValue()](https://docs.microsoft.com/en-us/dax/hasonevalue-function-dax)
+ UseRelationship
+ LastDate()
+ TOTALYTD()  
    evaluates an expression—in this case the sum of the Sales column—over a given date column. The date column must belong to a date table marked as a date table, as was done in the Create DAX Calculations in Power BI Desktop, Part 1 lab.

    The function can also take a third optional argument representing the last date of a year. The absence of this date means that December 31 is the last date of the year. For Adventure Works, June in the last month of their year, and so “6-30” is used.

    The TOTALYTD() function performs filter manipulation, specifically time filter manipulation. For example, to compute YTD sales for September 2017 (the third month of the fiscal year), all filters on the Date table are removed and replaced with a new filter of dates commencing at the beginning of the year (July 1, 2017) and extending through to the last date of the in-context date period (September 30, 2017).

    Note that many Time Intelligence functions are available in DAX to support common time filter manipulations.

+ Variables  
    can be useful for simplifying the formula logic, and more efficient when an expression needs to be evaluated multiple times within the formula (which will be the case for the YoY growth logic). Variables are declared by a unique name, and the measure expression must then be output after the RETURN keyword.


============================================================
# shortkey
+ *shift+enter* : carriage return in DAX editor