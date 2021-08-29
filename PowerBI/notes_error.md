*wrong book*
# 1.Microsoft Power Query
tacked bar chart that the axis shows all the individual dates
- Create a new table that has columns for the date, year, week, and day.
- (incorrect)From the Format Pane of the Chart set the type of the X-Axis to Categorical.

Your company has a data model for its sales data. The sales data has a column named Date. You want to view the data by week. What action should you take to quickly view sales data by week?
- Create a new group on the Date column and set the Group type to **Bin**.
- [Reference:] (https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-grouping-and-binning)
- [Topic 5, Deploy and Maintain Deliverables] (https://www.mssqltips.com/sqlservertip/4720/binning-and-grouping-data-with-power-bi/ https://community.powerbi.com/t5/Desktop/Adding-week-to-date-hierarchy/m-p/427762 )


# 2. Data visualization


# 3.Pulbishing and Sharing data

report Sales_1 connects to a Microsoft SQL Server database by using DirectQuery connection. After you have published the Sales_1 report to the Power BI service, the visualizations don't work.
How can you solve the issue
- Install the on-premises data gateway and configure a data source.
- need an on-premises data gateway between on-premises data (data that isn't in the cloud) and several Microsoft cloud services, such as Power BI Service
- there is no data loaded into dataset, so DirectQuery send queries to source peiodically

You want to embed a company video hosted on the Company YouTube channel into the dashboard
- To the dashboard, add a tile that uses a video content source.
- (incorrect) To the dashboard, add a tile that uses a Web content source.

You have a Microsoft Excel spreadsheet that contains a table named Sales. You want to add the Sales table to a Power BI dashboard as a tile. How should you configure the tile?
- From Excel, publish the workbook to the Power BI service.
- In PBI service, 'Get Data' from 'Local Files' or 'OneDrive for Business', the execl will be imported as dataset and dashboard tile (new dashbaord of the same name as excel name)

a table named 'Enrollments' stored on a Microsoft Excel spreadsheet. You want to add the Enrollments table to a Power BI dashboard as a tile.
- From the Power BI tab in Excel, pin the table.
- Excel has 'pin' to PBI addon for files saved in **OneDrive for business**. (Highlight the cells that you'd like to pin to a dashboard, then click on button 'pin')
- [Pin a range of cells to a dashboard] https://docs.microsoft.com/en-us/power-bi/create-reports/service-dashboard-pin-tile-from-excel




#####

Contributors can create, edit, and delete content in a workspace and publish reports to the workspace

In order to transform the visual and make it useful for analysis we need to promote the headers first, then unpivot all columns except for the "Measure" column. After the unpivot, we'll need to rename the column attribute column to year and then update the datatype.

if the file name or location changes, you will need to change the source via the Data Source Settings

When would you use a tool from the Transform tab over the Add Column tab
- When you want to overwrite the values of existing columns

which two blocks make up the M code that runs your query?
- let & in

filter flow
- by default, the filter direction will point from the "one" side of the relationship to the "many" side
- When you filter a table, the filter context is passed along to all related "downstream"
- Filters cannot flow "upstream" (against the direction of the arrow)

Which of the following functions allows you to calculate running totals?
- DATESINPERIOD

In what field do measures typically "live" in a visual?
- 'Value' field of a visual

Before creating the data model, you’re reviewing the data in the Sales table to check for possible negative values. What action should you take in the Query Editor?
- Select Column Profile, then select the trasations column. -
    the 'profile' has 'min' and 'max' etc.

You need to create relationships in the data model based on the VP of Inventory Management’s requirements. How should you create the relationships?
- Create an additional date table named Stock_Date and create 1:* relationship from Calendar[date_id] to Sales[date_id], and a 1:* relationship from Stock_Date[date_id] to Sales[stock_date_id]
- because the key word 'independantly' for filter

You need to provide access to your team of analysts, how should you configure their access?
- Power BI permission: **Viewer Role**
- Permission for **dataset: build**
- requierment: Analysts on your team are assigned to different regions, and should only be able to see data from that specific region when building
- key: to apply RLS, only *viewer* role is possible

You plan to create a relationship between the Calendar table and the Projections table but need to calculate the first day of each month in the Calendar table first. Keeping performance best practices in mind, which type of calculation and which formula should you use?
- Calculation type: M code custom column
- Formula: =Table.AddColumn(#"Inserted Start of Quarter", "Start of Month", each Date.StartOfMonth([Date]), type date)
- **try to do work in DB query**

You need to create a DAX measure that allows users to see forecasted sales at the appropriate level of granularity. How should you complete the following DAX measure?
- Forcasted Sales =
    ` **IF** (
        NOT (
            **ISFILTERED**('Calendar'[Date])
        ),
        SUM('Projection'[Forecasted_Sales])
    )
    `

You have marketing data contained in the tables shown below that's at the daily level. The Search data table contains 3 years of data with approximately 20 million records per month. You need to create a year-over-year visual to show the count of impressions by day, campaign name, and ad name that minimizes the data model size. What two things should you do
- In order to minimize the data model size and build out a year-over-year visual, you first need to reduce the size of the dataset before loading it. Using the **group by** function in the Query Editor is the best approach here. Next, in order to create a visual, you need to **create relationships** between the tables. 

You've built a line chart that shows revenue by month. Your manager has asked you to show mean monthly revenue on the chart. You need to add the value in a way that considers users adding other filters and involve minimal effort. What do you do?
- Adding an average line from the analytics pane is the only option that satisfies both requirements of considering other users adding filters and involving minimal effort. You could create a DAX measure to calculate the average but it accomplishes the same thing as an average line from the analytics pane and requires more effort

The three steps that need to happen in order to transform a JSON file to a usable data are first convert the list to a table, second expand the columns, and third set the column data types
- It's JSON, there is no header row (which exists in CSV file)

Your company uses Active Directory security groups to manage access. You have sales managers assigned to four different regions and each manager can only see their sales in Power BI Service. You need to ensure that when a manager changes to a different region, they can see the correct sales data. What should you do?
- Assign the manager to the correct Active Directory Group.
- Using Active Directory group, you no longer need to maintain lists of individual users

You have Power BI report that is published to your company's public website. You want the report on the website to update automatically when the data is refreshed. What should you do in the Power BI service
- Publish the report to the workspace, In the website, use the embeded code URL.
- [ref](https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-publish-to-web)
- When you use Publish to web, anyone on the Internet can view your published report or visual. Viewing requires no authentication. It includes viewing detail-level data that your reports aggregate

Your company has a Power BI workspace with several shared dashboards. You need to provide a user named user1@company.com with the permissions to edit and publish dashboards. What should you do?
- Modify the Access settings of the dashboards (share and allow edit)

Which two types of visualizations can be used in the balance sheet reports to meet the reporting goals? Each correct answer presents part of the solution. NOTE: Each correct selection is worth one point.
 -  A line chart that shows balances by quarter filtered to account categories that are long-term liabilities.
 -  A **ribbon** chart that shows balances by quarter and accounts in the legend. (ribbon chart is similar as Stacked Column Chart)

You download and install Visual Studio on the computer that has Power BI Desktop installed. Does this action allow you to use Microsoft R scripts in your visualization?
- No, it does not.
- download and install Microsoft R Open on the computer that has Power BI Desktop installed

replace the non-numeric values in the CustomerID column with the number 0
- From Query Editor, select the CustomerID column and click Replace Values. Then enter null in the Value To Find dialog box and 0 in the Replace With dialog box.

You want to provide users with a sample of questions that they can ask when using Q&A. What should you do
- In PowerBI Settings, configure **datasets** [Create featured questions for Power BI Q&A] (https://docs.microsoft.com/en-us/power-bi/create-reports/service-q-and-a-create-featured-questions)

RANKX(ALL(Customers), SUMX(RELATEDTABLE(Sales), [Sales_amount]))
- yes, it does

You want to create a report that displays the count of products sold by each salesperson. What should you do before you can create the report
- For each relationship, change the Cross filter direction to Both.

You want to compare the year-to-date sales with the previous year for the same time period. Which DAX function should you use
- **SAMEPERIODLASTYEAR**

The Sales role filters sales transaction data by the sales person. Each sales person must see only the data from their office
- Use the Test as role option to view data as the Sales role.

Which two visualizations can you embed into the website?
- Visualizations that use datasets stored in Microsoft OneDrive for Business
- Custom visualizations
- [limitations](https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-publish-to-web#limitations)

You open the **properties of the dataset**s and modify the **Q&A and Cortana** settings. Does this action allow users to find data by using natural language queries?
- Yes, it does

You open the properties of the datasets and modify the Q&A and Cortana settings. Does this action allow users to find data by using natural language queries?
- No, it does not

You need to filter all the visualizations in the report except the KPI visualization. Which two actions should you perform?
- **Edit the interactions of the KPI visualization**
- Edit the interactions of the slicer that is on the same page as the KPI visualization

Your company has a Microsoft Excel file that stores purchase data. The Excel file has a date and time column named Date_Time. The Date_Time column contains data in the format: 2020-08-13 13:46:83 . You want to use a built-in date hierarchy to analyze the purchase data by the date. How should you prepare the data in the Date_Time column
- D. Add a new column by example that starts with 2020-08-13. Set the data type of the new column to Date.

Present ad impression counts for the day, campaign, and Site_name
- A. Group the impressions by Ad_id, Site_name, and Impression_date. Aggregate by using the CountRows function.
- D. Create a calculated table that contains Ad_id, Site_name, and Impression_date.

Your company has training videos that are published to Microsoft **Stream**. You need to surface the videos directly in a Microsoft Power BI dashboard.  Which type of tile should you add?
- Custom Streaming Data

The users require insights on the completeness of the data and the value distributions
- **Create a blank query as a datasource**
- Specify query -Table.Profile(# "SalesDetail"), then close and apply
- Create a visual on a report page using fields from the new table

You are modeling data by using Microsoft Power BI. Part of the data model is a large Microsoft SQL Server table named Order that has more than 100 million records.  During the development process, you need to import a sample of the data from the Order table.  Solution: From Power Query Editor, you import the table and then add a filter step to the query.  Does this meet the goal?
- No
- Do it in "source" step

You need to update the query to reference the parameter instead of multiple hard-coded copies of the location within each query definition.  Solution: In the Power Query M code, you replace references to the Excel file with DataSourceExcel.  Does this meet the goal?
- Yes
- "DataSourceExcel" is the parameter

You need to ensure that the users can get a useful result for "subscriber count" by using Q&A
- Add a synonym of "subscriber" to the Customer table.

1.The number of customers invoiced in each state last month; 2.The average invoice amount per customer in each postal code; You need to define the relationship from the Customers table to the Invoice table. The solution must optimize query performance.
- One to Many (cust to inv), Single

Multiple RLS
- combine (= 'or')

The Products table is related to the ProductCategory table through the ProductCategoryID column. You need to ensure that you can analyze sales by product category
- Many to One (product to category), Single

You plan to have a menu page that will show all the business questions. You need to ensure that users can click each business question and be directed to the page where the question is answered. The solution must ensure that the menu page will work when deployed to any workspace
- Create a button for each business question and set the action type to Bookmark.

Plus, you want to count sales by Date and Store
- Use the Group by function in Power Query, aggregating sales by DateKey and StoreKey using Count Rows as operation.

Consider a new table named SchoolYearDate which has the same columns schema as the Date table. You want to create a report that shows the total Enrollments by SchoolYearDate and Calendar Month
- Append SchoolYearDate into the Date table.

Which function let you optimize the query for Courses before creating the relationship
- Table.Distinct

to set-up a new ID Column to map the product catalog and you want to be sure that there are not duplicates. How can you meet the goal?
- Select a Product Table Column and click Remove Duplicates.
- Add an Index Column to Products Table.

You are analyzing the Customer Sales monthly report and you notice that the Churn Rate metric is strangely increased. You want to understand which variables may affect this result. Which solutions can help you to explore the possible causes in Power BI Desktop?
- Use the Key influencer visual
- Decomposition tree visual

Your workspace contains 10 dashboards. You want to allow users to find data by using natural language queries. What should you do to meet the goal?
- From the properties of **datasets**, modify the Q&A settings ('turn on Q&A to ask natural language questions about your data')

to customize the chart's tooltip in order to show images and custom visualizations
- **Create a new report page and set it as Tooltip**

You notice that the Line Values doesn't' match the correspondent Y-axis Values and it is set on the top of the chart by default as shown in the picture
- Set to Auto the Y-axis 'start' and 'end' settings.

to set the drill down in the chart to display CourseName by year, by week, and day
    -From the Format Pane of the Chart set the type of the Y-Axis to Categorical.

Gauge visualization
- Value: Total Enrollments this Year; Max: Total Enrollments last Year; Target: Total Enrollments Last Year

the Enrollments amount value appears as the count of Enrollments amount instead of the sum of Enrollments amount for each region.
- Change the Data Type of Enrollments amount column to Whole Number.
- 'count' means the type was 'text'

You plan to create a custom visualization for Power BI. What do you install first?
- **Node.js**

You publish the Enrollments_BI project to Power BI Service and plan to share it with your colleagues: how could you share it? N.B. Your colleagues must be able to use the Drill Down feature.Solution: You create a dashboard and pin the Bar Chart visualization to it, then share the dashboard with your team.Does this solution meet the goal?
- no
- Drill Down feature is not currently available for dashboards experience.

Share **Dashboard with external users**
- Enable external sharing in the Tenant Settings from the PowerBI admin portal

The App will be available to all Organization users. You need to be sure that all the PowerBI users will have access to the App
- Ask the PowerBI admin for enabling permission to install the app automatically to all users.

embed a company video hosted on the Company YouTube channel into the dashboard
- To the dashboard*, add a tile that uses a **Web content** source.

option ''Allow users to build new content using the underlying dataset'' from the report settings. What will happen to the underlying dataset?
- You haven't made a copy of the dataset. The dataset still resides in its original location.
- Row-level security restrictions on the dataset are in effect.

The report retrieves data from an Azure SQL Database. How can you ensure that users of your organization will see the current data when they access the report on the Power BI Service
- In the Power BI service's Settings page, select the Datasets tab, choose the dataset that uses DirectQuery, and select Edit credentials.
- *existed* report, to be updated

share the dashboard with external guest users giving them editing and manage content permissions.
- Add guest users to Azure Active Directory.
- (incorrect)Enable the Share content with 'external users' feature from the Power BI admin portal.

add one of your videos to a tile in the Subscritions&Views dashboard.
- video
- (incorrect) Custom streaming data

Publish to web is supported for the vast majority of data sources and reports in the Power BI service. **Limitations**:
- Reports using row-level security(**RLS**).
- Reports using any **Live Connection** data source, including Analysis Services Tabular hosted on-premises, Analysis Services Multidimensional, and Azure Analysis Services.
- Reports using a **shared dataset** that is stored in a **different workspace** from the report.
- Shared and **certified** datasets.
- **Reports shared** to you directly or through an app.
- Reports in a workspace in which you are**n't an edit member**.
- *"R" and Python* visuals aren't currently supported in Publish to web reports.
- Exporting data from visuals in a report that **has been published** to the web.
- **ArcGIS Maps** for Power BI visuals.
- *Q&A* for Power BI visuals.
- Reports containing **report-level DAX measures**.
- **Single sign-on data query models**.
- Secure **confidential or proprietary** information.
- *The automatic authentication capability provided with the Embed option doesn't work with the Power BI JavaScript API. For the Power BI JavaScript API, use the user owns data approach to embedding.*
- Admins can **block public internet access**, as described in Private links for accessing Power BI. In that case, the Publish to Web option is grayed out for your tenant in the Power BI admin portal.

files importation' limitation
- Dataset size limit - 1-GB
- Distinct values in a column - When caching data in a Power BI dataset (sometimes called 'Import' mode), there is a 1,999,999,997 limit on the number of distinct values that can be stored in a column.
- Row limit - When using DirectQuery, Power BI imposes a limit on the query results that are sent to your underlying data source. If the query sent to the data source returns more than one million rows, you see an error and the query fails. Your underlying data can still contain more than one million rows. You're unlikely to run into this limit as most reports aggregate the data into smaller sets of results.
- Column limit - The maximum number of columns allowed in a dataset, across all tables in the dataset, is 16,000 columns


When data is exported from Power BI to Excel, PowerPoint, or PDF files, Power BI automatically applies a sensitivity label on the exported file and protects it according to the label's file encryption settings. 

Your organization owns a consistent number of dashboards on Power BI. Your goal is to ensure that when users browse the list of the available dashboard, they can see the ones that contain Personal Identifiable Information. Which function best fit your needs
- [Microsoft Information Protection sensitivity labels.](https://docs.microsoft.com/en-us/power-bi/admin/service-security-sensitivity-label-overview) -- can be applied in both Power BI Desktop and the Power BI service
- (incorrect) Row Level Security.

A Microsoft Excel Workbook, which contains several Power View sheets, is stored on Microsoft One Drive for Business. You want to replicate the Power View sheets as reports in the Power BI Service
- From Excel, click Publish to Power BI and then click Export.
- Get the data from Microsoft OneDrive for Business, and then click Import.

# 4.Administration settings in Microsoft PowerBI
Your Organization plan to get Power BI Premium. Which parameters will influence the subscription pricing
- Number of **cores**

three types of visualizations that will work in PowerBI Report Server
- Funnel charts
- Custom Visual
- Bubble maps
+ not supported: R and Python Visual

Your organization has subscripted a Microsoft Office 365 license. In order to ensure that all users can have access to the PowerBI Service:
- From Microsoft Azure PowerShell, run the Set-MsolCompanySettings cmdlet.
- (incorrect) From Power BI Admin portal, modify the Tenant settings.

Your Organization asks to ensure that all the Power BI users who create the region sales reports will be **aware of the availability of a high-quality data source**. On behalf of Power BI Admin, how can you achieve this task
- From the Tenant Settings of Power BI, enable the certification section, then select users or groups who can certify datasets.
- (incorrect) Create a new app workspace that contains only the high-quality dataset and add all the organization users as members of the workspace.

Your company follows a security protocol about data management for which information can't be provided over the Internet.
You need to plan a solution to ensure that the company will be compliant with the security policy also when using Power BI Service.
What should you include in your recommendation?
- Power BI report Server. ExpressRoute is an Azure service that lets you create private connections between Microsoft datacenters and infrastructure that's on your premises or in a colocation facility
- (incorrect) Power BI report Server.

Your organization uses Power BI Premium for BI reporting activities. Sometimes, the BI team share Power BI contents with customers whitout a Power BI PRO license.
Which activities are allowed with a Power BI *free license*
- Access a published **Power BI app**

You need to use Power BI Embedded to distribute reports into a Web application. You want that reports display live data.
Which of the following datasources meet the goal?
-  Azure SQL Database.
- Azure Synapse Analytics.
- You can achieve the goal by using Microsoft Azure SQL Database or Azure Synapse and DirectQuery Connection mode.
- [limitation of publish to web](https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-publish-to-web)

three operations that developers can achieve by using the API
- **Create a dataset**
- Add rows to a dataset
- Refresh and imported dataset
- [Power BI API](https://docs.microsoft.com/en-us/power-bi/developer/automation/overview-of-power-bi-rest-api)
- (incorrect) Retrieve rows from a dataset

You have distributed an app from a workspace to a group of users, giving them Build and Share Permissions. Later, you decide to remove access to the app for some users.
You want to be sure that Build and Share Permissions will be also removed.
- You need to manage datasets permissions to remove build and share permissions.
- grant when give access of dashboard to users, but remove from deeper level

# 5.DAX
create a measure to rank the courses based on their total enrollment amount
- RANKX(ALL(Courses), SUMX(RELATEDTABLE(Enrollments), [Enrollments_amount]))
- RANK.EQ, return the rank number from a list
- there is no 'rank'


create a chart that displays total Enrollments[Total Paid] by Course[Name]
- Create a relationship between the Enrollments table and the Courses table.
- Create a relationship between the Enrollments table and the Courses table. Then, to the Enrollments table, add a column that uses the RELATED('Courses'[Name]) DAX formula.

compare the year-to-date sales with the previous year for the same time period
- DATEADD (get the same dates of last year)
- SAMEPERIODLASTYEAR
- (Incorrect) PREVIOUSYEAR -- whole year

add a date table named Date, containing the following columns: date, year, month
- CALENDAR, YEAR, MONTH     -- pass in start and end date
- (incorrect) CALENDARAUTO -- check existed dates and generate.

# Data Modeling
The active relationship is on Enrollments[EnrollmentDate]. You plan to create measures to count both the number of Enrollments by [AttendanceDate] and the Enrollments by [StartingDate].
N.B. You can't meet the goal by duplicating data or loading additional data.
Solution: You should create a calculated table, then you create a measure that uses the new table. Does this solution resolve the issue?
- No (because of duplicated data)

You plan to create measures to count both the number of Enrollments by [AttendanceDate] and the Enrollments by [StartingDate].
N.B. You can't meet the goal by duplicating data or loading additional data.
Solution: You create measures that use the following functions: CALCULATE, COUNT, and **FILTER** DAX function.
Does this solution resolve the issue?
- Yes.(filter('Enrollments', 'Enrollments'[StartingDate]='Date'[Date]))
- Another way: USERELATIONSHIP

create a calculated column that shows the day's difference between the order reception and the order shipping
- DATEDIFF

You want to analyze the Badging trend by the Starting Time column and use a built-in date hierarchy. What should you do
- Create a column by example that starts with 2021-01-10, then set the data type of the new column to Date. (built-in hierachy. CALENDAR/AUTO is not built-in)














[**Comparing Power BI Report Server and the Power BI service**](https://docs.microsoft.com/en-us/power-bi/report-server/compare-report-server-service)
