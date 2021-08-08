(https://mtygroup.udemy.com/course/microsoft-power-bi-certification-da-100-exam-prep)
# error notes:
- if the file name or location changes, you will need to change the source via the Data Source Settings

# source type
## csv
- changed Delimiter during Transform Preview
## Json
## PBDIS
## Ms Dataverse
## SSAS
## sharepoint:
### structure
- Sharepoint(site) : filing cabinet
- document library: drawer
- folders and files

### connect to sharepoint
1. **Enter** the site root URL https://...sharepoint.com/sites/PBIExample(teamGroupName)    --https://mtygroup.sharepoint.com/sites/mtybiproject
1. **Combine & transform** the data
1. **filter** folder path to correct document library

## storage modes
+ Import: Tables stored in-memory within PBI. In import storage mode, tables are stored in-memory, whereas in DirectQuery tables are connected directly to the source. Dual storage mode allows tables to come from in-memory data or by an on-demand query to the data source.
+ DirectQuery: not data stored.
    - Dataset is too large to be stored in-memory
    - Source data change frequently & reports must show the most recent data
    - company policy states data can only be accessed from the original source
+ Dual: _same query constraint as DirectQuery_

### SSAS Tabular
when publish SSAA Tabular (live connection) data model to Power BI Service, Data Gateway must be used in order for this to be possible (due to Live Connection)

# transform
- unpivot and pivot to transform a table into correct format (section 6, 43)

# M language (power query editor)
## LET block
+ define all the variables
## IN blcok
specify the final output of all variables in the query
## variable name
+ individual steps to take
+ match the individual steps in the Applied Steps pane
## functions category
-- formula: = Function Name (Previous Step, Function Arguments)
### 1. Table
- = Table.SelectRows(#"Reordered Columns", each([Quantity_Sold]=2))
### 2. List
### 3. Text
### 4. Date
## parameter
- create paramenter: home -> Manage Parameters.
- use: Applied Steps -> Source -> File path -> choose 'Parameter' from the dropdown list -> select <para name> from the next dropdown

# date model
relations based on common columns/keys.
A well-designed model is **critical** and ideally should:
- Use a start schema with **one-to-many** (1:*) relations
- Contain relationships with **one-way** filters (*vs.bidirectional*)
- Contain tables that each serve a specific purpose, including data(fact) tables and **lookup** (dim) tables
- Only include the data you need for analysis *(no redundant or unnecessary records or files)*
- Split out individual data and time components from **DateTime** fields


## relationship
accessed by Das Function:
- Related
- RelatedTable
- UseRelationship (inactive only). *The USERELATIONSHIP function allows you to determine which relationship to use between to tables, including inactive relationships.*
- ...

# DAX calculation
the formula language that drives Power BI. Used for:
1. Calculated columns
    - refer to entire tables or columns (no 'A1-style' reference like Excel)
    - generate values for each row, which are visible within tables in the Data view
    - They understan row context; they're great for defining properties based on information in each row, but generally useless for aggregation (SUM, COUNT, etc)
    - increase the sizoe of your data model
1. Measures -- DAX formulas used to generate new calculated values, which aggregate data that can then be visualized.
    - *use [] to quick access existed measure, and measure name is bracketed by []*
    - *cannot directly operate on column*, either use a measure or result of Dax function (resulting in a measure). ie [new measure] = [measure1] - [measure2], or  [new] = [measure1] - sum(table[col])

    - refer to entire tables or columns (no 'A1-style' or 'grid' reference like Excel)
    - aren't visible within tables; they can only be "seen' within a visualization like a chart or matrix (similar to a calculated field in an Excel pivot)
    - evaluated based on **filter context**, which means they recalculate when the fields or filters around them change (like when new row or column labels are pulled into a matrix or when new filters are applied to a report)
    - used to aggregate data

## Quick Measures
pre-built formula templates that allow you to drag and drop fields rather than write DAX from scratch
- helpful for defining complex measures (ie: weighted average, rolling average, variance per category, sales from new customers or time intelligence formulas)


## common DAX Function Categories
+ Math & Stats -- basic aggreagation functions as well as "iterators" evaluated at the row-level
    - Common: Sum, Average, Max/Min,...
    - Iterator Functions -- allow to loop throug the same calculation on *each row of a table*, and then apply some sort of aggregation to the results (Sum, Max, etc.): Sumx, Averagex, Rankx, Countx, ...; allowing to add an expression as part of the function parameters
+ Logical -- return info about valuesbased on a give **conditional expression**: If, IfError, And, Or, Not, **Switch**, True, False
+ Text -- manipulate text strings or control formats for dates, times or numbers
+ Filter: Calculate, Filter, All, AllExcept, Related(*join*), RelatedTable, Distinct, Values, Earlier/Earliest, HasOneValue, HasOneFilter, IsFiltered, UseRelationship, TopN
    - **Lookup** functions: based on related tables
    - **filterring** functions: for dynamic calculations
+ Date & Time
    - basic **date & time** functions
    - advance **time intelligence** operations

## DAX Syntax
- Calculated columns don't always use functions, but measures do (otherwise, it will give error)

## Dax Function
+ StartOfYear(<date>)
+ StartOfQuarter(<date>)
+ startOfMonth(<date>)
+ month(<date>) -- get month number
+ date(<year>,<month>,<day>) -- ie date(2021,07,01) -> 2021-07-01
+ format(<date>, "<formatString>") -- ie format('2021-07-01',"mmm") -> "Jul"; format('2021-12-01',"mmmm") -> "December"
+ Divide(<Numerator>,<Denominator>,[AlteranteResult]) -- [AlternateResult] is optional parameter to specify a result in case of divide by zero, **default** is **0**
+ **Calculate()** = Calculate(Expression, *[Filter1],[Filter2],...*) 
    - CALCULATE **modifiies** and **overrules** any competing filter context!
    - **modifiers** are used to alter the way CALCULATE creates filter context, and are added as *filter* arguments within a CALCULATION function
    - Modifiers are typically used to change filter context, access inactive table relationships, or change the way filters propagate *(i.e. one-way to bidirectional)*
        + Modify **Filters**: All, AllSelected, AllNoBlankRow,AllExcept,KeepFilters, RemoveFilters
        + use **Relationships**: UseRelationship
        * Change **Filter Propagation**: CrossFilter
    - *[Fiter] set* accept both **Boolean & table** functions (individually or at the same time), but all fitler arguments are automatically converted into a table
    - when you understand that tables can be added in his filter, it kind of opens up a whole new world of possiblilities'
+ = UseRelationship(ColName1,ColName2). Can only be used in funcitons which accept a filter parameter (Calculate, TotalYTD, etc.)
+ = All(Table or ColumnName, *[colName1],[colName2],...)* -- remove all filters, for a talbe or some columns in the same table
+ = Fitler(Table, FilterExpression) -- *iterator* function,  to add new filter context, can handle more complex filter expressions than CALCULATE, but can impede the performance. Try to use Calculate to achieve the same result
+ = TopN(N_Value, TableName, *[OrderBy Expression],[order])
+ = Summarize(table, col_group, aggregation_name, col_toAggregate)
+ **Time Intelligence** functions
    - Performance To-Date = Calculate([measure], DATESYTD(Calendar[Date])), use **DATESQTD** for Quarters or **DATESMTD** for Months
    - Previous Period = CALCULATE([Measure], DATEADD(Calendar[Date],-1,MONTH)), select an interval(DA,mONTH,QUARTER,or YEAR) and the # of intervals to compare
    - Running Total = CALCULATE([Measure], DATESINPERIOD(cALENDAR[Date],MAX(Calendar[Date]),-10,DAY))
    - DATESBETWEEN, return a list of dates

# visuals
## Edit Interatraction.
- filter
- highlight (not fitler, but just hightlight the categories that filtered out in ohter visuals)
## Drill-through filters
    allow users to jump to different report pages (like bookmarks)， while simulataneously filtering based on the specific item selected
## Slicers
Limitation:
- cannot drill down non-hierachical fields
- cannot supp visual level filters
- cannot be pinned to a dashboard individually (but can be pined as part of a **live page** -- pined report)

## charts
### Scatter charts
- show patterns in large sets of data
- show linear & non-linear trends
- cluster analysis
- outlier identifications
### line charts
- Show changes in values over time
- add multiple lines to compare trends between series (categrories)
### Clustered column charts
- show distribution of data points
- comparisons across categories

## filter
1. Visual level
1. Page level
1. report level
1. Drill level

Filter settings include **Basic**, **Advanced***(text/value)*, and **Top N** options

## AI visuals
1. Key Influencers
    - drop down box -- value or metric under investigation
    - Left pane -- Visual that show a list of the top key influencers
    - Right pane -- Column chart display all values for the key influencer **theme** selected in the left pane
    - Average line -- shows the percentage of other thems that increase or decrease the etric under investigation

1. Decomposition tree
    - allows you to perform exploratory analysis by successively breaking down a measure across multiple dimensions
    - great choice to perform a **root cause analysis** or **ad hoc exploration**

# deliverables
## Scheduled refresh
    - 8 refresh a day (pro)

# Row Level Security
1. Static roles -- filtered views for specific audiences (territory managers, dep leads, execs, etc.)
    - not the sames as bookmarks or pre-filtered views; roles **filter data out of your model** and limit what audience can access. No option to unfilter/unhide the filtered rows.
    - static rows must first be confiured in PBI desktop and tehn applied in Power BI service
    - for **multiple roles**, the acces will be **combined**
    - **View as roles** to test RLS
1. Dynamic RLS -- define filtered views for a specific list of uses with the DAX functions **USERNAME** or **USERPRINCIPLNAME**
    - rquire adding an additional table into your data model
    - dynamic roles must first be confiured in Power BI Desktop and then applied in Power BI Service

## =Username()
returns the domain and user's unername in the format of domain-name\user-name
1. Person's **username** (i.e., aaronp)
1. Company **domain** (i.e., mavencyles)
1. **USERNAME** returns (i.e., mavencycles\aaronp)

# term
**Dataverse**: a cloud-based storage options for your organizations's data that you can connect to business applications like Power Apps, Power Automate, and Power Virtual Agents.


# mistake
+ When would you use a tool from the Transform tab over the Add Column tab
    - When you want to overwrite the values of existing columns
+ which two blocks make up the M code that runs your query?
    - let & in
+ filter flow
    - by default, the filter direction will point from the "one" side of the relationship to the "many" side
    - When you filter a table, the filter context is passed along to all related "downstream"
    - Filters cannot flow "upstream" (against the direction of the arrow)
+ Which of the following functions allows you to calculate running totals?
    - DATESINPERIOD
+ In what field do measures typically "live" in a visual?
    - 'Value' field of a visual