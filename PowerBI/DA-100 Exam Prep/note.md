(https://mtygroup.udemy.com/course/microsoft-power-bi-certification-da-100-exam-prep)
# notes:
- possible to add tile of 'web content'. ie, there are some video online, we can add this video as a tile to dashboad
- In order to confirm region is populated for every author, you need to use the column profile tool to understand the distribution for the region column. Additionally, the default Power Query profile is only done on the first 1,000 rows. You need to enable column profiling based on the entire dataset to see all 2,500 authors.
- *Deployment pipelines* allow you to manage the lifecycle of your organizations content
- Writing a SQL statement to filter the rows prior to loading is the only option that will minimize data load time.
- You need to create a visual that compares revenue and cost over time. What type of visual should you use?
    - Line charts are used to visualize change over time
- The web content tile allows you to add and customize any HTML content, like websites. Web content tiles preserve the functionality of the page so you can access other videos on the site. The video tile only allows you to post a single video
- Using parameters allows you to easily switch between different tables and schemas in a data source or database
- Contributors can update reports in a workspace and update an app. However, they cannot add other users to a workspace
- Members can assign member roles and below
- Azure Blob storage queries don't support query folding and therefore cannot take advantage of incremental refresh
- Combining the data using merge will cut down on the use of functions like RELATED and RELATEDTABLE that return a related value from another table
- You create multiple dashboards in Power BI Service and need to make sure users can see which dashboards contain Personally Identifiable Information (PII). What should you use?
    - Senstitivity labels (Sensitivity labels provide a simple way for users to classify content in Power BI Service)
- Line charts, with a single line, have a forecasting analytics option that can be enabled
- Splitting out the time component from the date helps reduce the model size
- Decomposition trees allow you to perform **exploratory** and **root cause** analysis
- When a user is assigned to multiple roles, the RLS filters become additive and create a union between the filters
- **The 50th percentile is also known as the median or middle value**
- The key influencers visual shows the most important factors based on the fields provided
- **Impact analysis** provides you the tools to understand how making changes to a dataset will impact downstream reports and dashboards
- **bin**: You can set the bin size for numerical and time fields in Power BI Desktop. You can make bins for calculated columns, but not for measures. Use binning to right-size the data that Power BI Desktop displays.

# error notes:
- Your company has a data model for its sales data. The sales data has a column named Date. You want to view the data by week. What action should you take to quickly view sales data by week?
    - Create a new group on the Date column and set the Group type to **Bin**.
    - [Reference:] (https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-grouping-and-binning)
    - [Topic 5, Deploy and Maintain Deliverables] (https://www.mssqltips.com/sqlservertip/4720/binning-and-grouping-data-with-power-bi/ https://community.powerbi.com/t5/Desktop/Adding-week-to-date-hierarchy/m-p/427762 )
- Contributors can create, edit, and delete content in a workspace and publish reports to the workspace
- In order to transform the visual and make it useful for analysis we need to promote the headers first, then unpivot all columns except for the "Measure" column. After the unpivot, we'll need to rename the column attribute column to year and then update the datatype.
- if the file name or location changes, you will need to change the source via the Data Source Settings
- When would you use a tool from the Transform tab over the Add Column tab
    - When you want to overwrite the values of existing columns
- which two blocks make up the M code that runs your query?
    - let & in
- filter flow
    - by default, the filter direction will point from the "one" side of the relationship to the "many" side
    - When you filter a table, the filter context is passed along to all related "downstream"
    - Filters cannot flow "upstream" (against the direction of the arrow)
- Which of the following functions allows you to calculate running totals?
    - DATESINPERIOD
- In what field do measures typically "live" in a visual?
    - 'Value' field of a visual
- Before creating the data model, you’re reviewing the data in the Sales table to check for possible negative values. What action should you take in the Query Editor?
    - Select Column Profile, then select the trasations column. -- the 'profile' has 'min' and 'max' etc.
- You need to create relationships in the data model based on the VP of Inventory Management’s requirements. How should you create the relationships?
    - Create an additional date table named Stock_Date and create 1:* relationship from Calendar[date_id] to Sales[date_id], and a 1:* relationship from Stock_Date[date_id] to Sales[stock_date_id]
    - because the key word 'independantly' for filter
- You need to provide access to your team of analysts, how should you configure their access?
    - Power BI permission: **Viewer Role**
    - Permission for **dataset: build**
    - requierment: Analysts on your team are assigned to different regions, and should only be able to see data from that specific region when building
    - key: to apply RLS, only *viewer* role is possible
- You plan to create a relationship between the Calendar table and the Projections table but need to calculate the first day of each month in the Calendar table first. Keeping performance best practices in mind, which type of calculation and which formula should you use?
    - Calculation type: M code custom column
    - Formula: =Table.AddColumn(#"Inserted Start of Quarter", "Start of Month", each Date.StartOfMonth([Date]), type date)
    - **try to do work in DB query**
- You need to create a DAX measure that allows users to see forecasted sales at the appropriate level of granularity. How should you complete the following DAX measure?
    - Forcasted Sales =
    ` **IF** (
        NOT (
            **ISFILTERED**('Calendar'[Date])
        ),
        SUM('Projection'[Forecasted_Sales])
    )
    `
- You have marketing data contained in the tables shown below that's at the daily level. The Search data table contains 3 years of data with approximately 20 million records per month. You need to create a year-over-year visual to show the count of impressions by day, campaign name, and ad name that minimizes the data model size. What two things should you do
    - In order to minimize the data model size and build out a year-over-year visual, you first need to reduce the size of the dataset before loading it. Using the **group by** function in the Query Editor is the best approach here. Next, in order to create a visual, you need to **create relationships** between the tables. 
- You've built a line chart that shows revenue by month. Your manager has asked you to show mean monthly revenue on the chart. You need to add the value in a way that considers users adding other filters and involve minimal effort. What do you do?
    - Adding an average line from the analytics pane is the only option that satisfies both requirements of considering other users adding filters and involving minimal effort. You could create a DAX measure to calculate the average but it accomplishes the same thing as an average line from the analytics pane and requires more effort
- The three steps that need to happen in order to transform a JSON file to a usable data are first convert the list to a table, second expand the columns, and third set the column data types
    - It's JSON, there is no header row (which exists in CSV file)
- Your company uses Active Directory security groups to manage access. You have sales managers assigned to four different regions and each manager can only see their sales in Power BI Service. You need to ensure that when a manager changes to a different region, they can see the correct sales data. What should you do?
    - Assign the manager to the correct Active Directory Group.
    - Using Active Directory group, you no longer need to maintain lists of individual users
- You have Power BI report that is published to your company's public website. You want the report on the website to update automatically when the data is refreshed. What should you do in the Power BI service
    - Publish the report to the we, In the website, use the embeded code URL.
    - [ref](https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-publish-to-web)
- Your company has a Power BI workspace with several shared dashboards. You need to provide a user named user1@company.com with the permissions to edit and publish dashboards. What should you do?
    - Modify the Access settings of the dashboards (share and allow edit)
    - access to workspace will not affect dashboard access

# source
Dataset: useable format of data source
## type
1. csv -- changed Delimiter during Transform Preview
1. Json
1. PBDIS
1. Ms Dataverse
1. SSAS
1. sharepoint
    1. structure
        - Sharepoint(site) : filing cabinet
        - document library: drawer
        - folders and files

    1. connect to sharepoint
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

### **Large dataset storage format**
    used for datasets over the 0GB refresh limit in Sevice
- available for Premium & Embedded capacities and Premium Per User
**STeps to enable**:
1. configure **incremental refresh**, if you expect your ds will become larger and progressively consume more memory
1. Publish the model as a **dataset** to Power BI Sevice
1. In PBI service, go to Dataset > Settings > **Large dataset storage forma**, click the lider to turn "on", and then "apply"
1. refresh the ds to load **historical data** based on the incremental refresh policy

# transform
1. unpivot and pivot to transform a table into correct format (section 6, 43)

# M language (power query editor)
1. formula: = Function Name (Previous Step, Function Arguments)
1. LET block -- define all the variables
1. IN blcok -- specify the final output of all variables in the query
1. variable name
    + individual steps to take
    + match the individual steps in the Applied Steps pane
1. functions category
    1. Table = Table.SelectRows(#"Reordered Columns", each([Quantity_Sold]=2))
    1. List
    1. Text
    1. Date
1. parameter
    - create paramenter: home -> Manage Parameters.
    - use: Applied Steps -> Source -> File path -> choose 'Parameter' from the dropdown list -> select <para name> from the next dropdown
## notes:
- The **fixed decimal** number data type stores values with **full precision**, and so requires more storage space that decimal number. It’s important to use the fixed decimal number type for financial values, or rates (like exchange rates).

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

## = USERPRINCIPALNAME()
returns the user's name as their email address (i.e., aaron@mavendemo.com)
User Principal Name (**UPN**) looks like an email address, but echnically it's a combination of three items:
1. Person's **username** (i.e., aaronp)
1. "**@**" symbol
1. Company **domain** (i.e., maven inspectional services)

## Azure Groups
Azure Active Directory **security groups** allow you to manage an entire group of users instead of a list of individual users.
benefits:
- used to manage member and computer access to shared resources for a group of users
- create specific security policies (permission levels) for different groups of users
- allows you to set permissions for all members of a group at once
- great for managing user access when people join and leave teams

## subscriptions
- Creating subscriptions requires a Pro or PPU license (self & others)
- Add email, subject and an optional message
- Set frequency & time (montly, weekly, daily, hourly)
- Schedule the start and end dates.

## sharing
- reports, dashboards, apps
- max recipients is 100 at a time (500 total)
- share with more than 100 recipients, split into multiple sends or use groups
- **pro license** or access to **premium capacity** in order to view

## user permissions
- viewer, contributer, member, admin
- principle: **Lease Prvilege**, not to over permission

# deployment
## Pipelines
1.Create a  pipeline -> 2.Assign workspace -> 3.Develop and test your content, Share with your users
Devleopment -> Test -Production


## incremental refresh
- **Fster refresh times** -- used with large ds to decrease processing times
- **more reliable** -- Decreases the time connections are made to external sources
- **Reduced Resource Usage** -- Easier on the internal resources of your computer (i.e., memory)
steps
1. Set **RangeStart & RangeEnd** parameter from the Query Editor in PBI desktop (recommend: use  **Date/Time** column)
1. Apply ** RangeStart & RangeENd parameters to a date column using a *Custom Filter* from the filter options
1. Define the incremental refresh policy on the dataset (right-click dataset)

## Endorsement
- None
- Promoted: ready to distribute the dataflow to coworkers
- Certified
to flag content that's ready for others to use
- Ay content owner or member with write permissions can endorse content
- It's possible to endorse **datasets, dataflows, reports,** and **apps**

## Sensitivity Labels
- Pro or Premium per user license
- **Belong to a security group that has permission to apply sensitivity labels**
- Sensitivity labels must be enabled for your organization
- Subscribe to Azure Information Protection


# term
**Dataverse**: a cloud-based storage options for your organizations's data that you can connect to business applications like Power Apps, Power Automate, and Power Virtual Agents.
