*notes*:
# Prepare the Data
# Model the Data
# Visualize the Data
# Deploy and Maintain Deliverables



# Microsoft Power Query
Pyton to show visual:
- You should add the following command to the script: pyplot.show();

customize the report with both the corporate colors of your organization and a set of custom icons.
- Configure a **JSON** file and then import it in Power BI Desktop as Custom Theme.

to create a custom visualization for Power BI. What do you install first?
- **Node.js**

You are configuring a Gauge Chart. Where do you set the Goal?
- **Format** settings -- to switch *target* on.

# Prepare the Data
[NoSql database connection](https://docs.microsoft.com/en-us/learn/modules/get-data/4-nosql-database)
- db URL
- Account Key (Az Portal > Primary Key > Read-only keys)
- You can specify the Azure Cosmos DB account endpoint URL that you want to get the data from (you can get the URL from the Keys blade of your Azure portal)

[Azure Analysis Services](https://docs.microsoft.com/en-us/learn/modules/get-data/7-azure-analysis-services)
Azure Analysis Services is an Azure product that allows you to ingest data from multiple data sources, build relationships between the data, and creates calculations on the data. The calculations are built using data analysis expressions (DAX). Azure Analysis Services is similar to the data modeling and storage technology in Power BI
- Authenticate to the server.
- Pick the cube (database) you want to use.
- Select which tables you need.
- Analysis Services cubes have calculations already in the cube, which will be discussed in more detail later. 
- If you don’t need an entire table, you can query the data directly. Instead of using Transact-SQL (T-SQL) to query the data, like you would in SQL Server, you can use multi-dimensional expressions (MDX) or data analysis expressions (DAX).

[Query folding](https://docs.microsoft.com/en-us/learn/modules/get-data/8-performance-issues)
- More efficiency in data refreshes and incremental refreshes
- Automatic compatibility with DirectQuery and Dual storage modes

[Query diagnostics](https://docs.microsoft.com/en-us/learn/modules/get-data/8-performance-issues)

optimize performance
- Process as much data as possible in the original data source
- Use native SQL queries. When using DirectQuery for SQL databases, such as the case for our scenario, make sure that you are not pulling data from stored procedures or common table expressions (CTEs)
- Separate date and time, if bound together

## Clean, transform, and load data in Power BI
[unpivot](https://docs.microsoft.com/en-us/learn/modules/clean-data-power-bi/2-shape-data)


# Model the Data
[Flatten parent-child hierarchy](https://docs.microsoft.com/en-us/learn/modules/design-model-power-bi/4-dimensions)
```Path = PATH(Employee[Employee ID], Employee[Manager ID])```
- Path(Id_columnName, Paren_columnName)
- Level 1 = PATHITEM(Employee[Path],1)
- Level 2 = PATHITEM(Employee[Path],2)
- Level 3 = PATHITEM(Employee[Path],3)

Role-playing dimensions
- like date table can have 2 roles (order time, ship time)

[Behavior of DirectQuery connections, and limitation; Customize the Query reduction options](https://docs.microsoft.com/en-us/learn/modules/optimize-model-power-bi/5-directquery-models)



# Visualize the Data

[tooltips to display graphical information](https://docs.microsoft.com/en-us/learn/modules/visuals-power-bi/4-format)
- new page > Page Size > Tooltip (slider) > ON

If you decide to use an R or Python visual, and you want to refresh the data in Power BI service, you'll need to use a personal gateway

[Set the navigation destination](https://docs.microsoft.com/en-us/learn/modules/data-driven-story-power-bi/4-report-navigation)
use conditional formatting to set the navigation destination based on the output of a measure
- create a single column table (M)
- Button (type: Page navigation)
- Format condition:
    - Format by: Field value
    - Based on Field: First Select a destination
    - Summarization: First

[Cross-report drillthrough](https://docs.microsoft.com/en-us/learn/modules/data-driven-story-power-bi/6-advanced-interactions)
- both data models must contain the fields that you want to pass
- names of those fields, and the names of the tables that they belong to, must be identical

[rea-time dashbaord](https://docs.microsoft.com/en-us/learn/modules/create-dashboards-power-bi/6-configure-real-time-dashboard)
Add tile:
- MEDIA
    - Web content
    - Image
    - Text box
    - Video
- REAL-TIME DATA
    - Custom Streaming Data

[Data Classification](https://docs.microsoft.com/en-us/learn/modules/create-dashboards-power-bi/7-configure-data-classification)
custom data classification settings are added into the Power BI system. Data classification is done by an administrator
- high impact
- medium impact
- low impact
the dashboard will follow the default data rules or the rules that you have established under **Tenant** settings.
The classfication mark will be shown in title bar (HIGH)

[mobile view](https://docs.microsoft.com/en-us/learn/modules/create-dashboards-power-bi/8-set-mobile-view)
[mobile view - Dashboard](https://docs.microsoft.com/en-us/learn/modules/create-dashboards-power-bi/8-set-mobile-view)
- a new grid has been added to this view so that you can orient your visuals with more ease and overlay visuals on top of each other.
- This feature can be useful if you want to insert a visual on top of an image.

[Parameters in DAX Measures](https://www.sqlbi.com/articles/parameters-in-dax-measures/)


# Data analysis in Power BI
[set up the bin group](https://docs.microsoft.com/en-us/learn/modules/perform-analytics-power-bi/2-statistical-summary)

[group](https://docs.microsoft.com/en-us/learn/modules/perform-analytics-power-bi/4-group-data)
shade 'new' group in differen color
- create a group
- edit a group (right click the group field either in Legend or Fields)

[Analyze feature](https://docs.microsoft.com/en-us/learn/modules/perform-analytics-power-bi/7-analyze-feature)
This feature does not work if you have non-numeric filters applied to your visual and/or if you have measure filters applied.

[Apply insights](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-insights-find-where-different)
right-click on any data point: Analyze > Find where this distribution is different

[Quick Insigts](https://docs.microsoft.com/en-us/learn/modules/perform-analytics-power-bi/9-quick-insights)
PBI service > Datasets > ...> Quick Insigts

[AI insigts](https://docs.microsoft.com/en-us/learn/modules/perform-analytics-power-bi/10-ai-insights)
PBI Desktop > Power query > Add Columns > AI Insights (must turn the function on: File > Options and Settinsg > Options > Globle > Preview features > AI Insights function browser)

[Q&A setup](https://docs.microsoft.com/en-us/learn/modules/ai-visuals-power-bi/2-visual)

[AI splits](https://docs.microsoft.com/en-us/learn/modules/ai-visuals-power-bi/6-check)
AI splits work by considering all available fields and determining which one to drill into to get the highest/lowest value of the measure that is being analyzed. 

# Manage workspaces and datasets in Power BI
## Create and manage workspaces in Power BI
Create Workspace
- In the Advanced drop-down menu, you can create a Contact list of users who will receive notifications if issues with the workspace occur
- You can also add this workspace to a specific OneDrive and then choose whether this workspace will be a part of a dedicated capacity or not. Dedicated capacities are Power BI Premium features that ensure that your workspace will have its own computational resources as opposed to sharing resources with other users

An **app** is a published, read-only window into your data for mass distribution and viewing

Navigation:
- change the order in which the content is oriented
- change the name of the content, change the link, and then add it to a specific section on the navigation pane
- add content that is external to Power BI through a link. This external content can also be included within the content area. For example, a YouTube video or PowerPoint slide deck has to be an embed URL, not the raw URL

## Manage workspaces and datasets in Power BI
metric reports
- Admin, Member, or Contributor
- Workspace > reports/dashboards > ... > View usage metrics report

[deployment pipelines](https://docs.microsoft.com/en-us/learn/modules/create-manage-workspaces-power-bi/4-development-lifecycle-strategy)
- Premium
- PBI service - left Ribon/menu - Deploment pipelines
- Only workspaces that are assigned to a Premium capacity will appear
- At every stage, you have the option to publish the associated workspace as an app by selecting Publish app
- In 'Deployment pipelines', there is settings for each env, where parameters can be changed

[Lineage view](https://docs.microsoft.com/en-us/learn/modules/create-manage-workspaces-power-bi/5-troubleshoot-data)
- Admin, Member or Contributor
- Pro

[Data Protection](https://docs.microsoft.com/en-us/learn/modules/create-manage-workspaces-power-bi/6-data-protection)
- sensitivity labels to label dashboards, reports, datasets, and dataflows by using the same taxonomy that is used to classify and protect files in Microsoft 365
- Add more protection measures such as encryption and watermarks when you are exporting the data.
- Microsoft Cloud App Security to monitor and investigate activities in Power BI

[Sensitivity labels](https://docs.microsoft.com/en-us/learn/modules/create-manage-workspaces-power-bi/6-data-protection)
-specify which data can be exported. These labels are configured externally to Power BI, and Power BI allows you to quickly use them in your reports and dashboards
- go to Microsoft 365 Security Center to define your own labels
- Data that is exported to Microsoft Excel, Microsoft PowerPoint, and PDF files will have sensitivity labels enforced
- if you didn't have established permissions, you would be denied access to see the data

## Manage datasets in Power BI 
parameter:
- use parameter to filter column
    - the **datatype** for bother must be the **same**
- [function](https://docs.microsoft.com/en-us/learn/modules/manage-datasets-power-bi/2-report-parameters)
    - 'Create Function' convert a Query into a function (with parameters to pass in)
- [Create Parameter using query](https://guyinacube.com/2019/02/20/populate-a-power-bi-parameter-list-using-a-query/)
    - convert a table (single column) to a list (in the Ribbon)
    - right select a column from a table, then 'add as a query', remove duplicates


[incremental refresh settings](https://docs.microsoft.com/en-us/learn/modules/manage-datasets-power-bi/6-incremental-refresh)
*RangeStart*, *RangeEnd*

[Manage and promote datasets](https://docs.microsoft.com/en-us/learn/modules/manage-datasets-power-bi/7-manage-datasets)
two ways to **endorse** your datasets
- **Promotion** - Promote your datasets when they're ready for broad usage. Power BI Admins have permissions to promote datasets.
    - You can only promote a dataset if you're a Power BI admin user or the owner of that dataset.
- **Certification** - Request certification for a promoted dataset from an admin user that is defined in the Dataset Certification tenant admin setting. This certification adds another layer of security for your datasets. Certification can be a highly selective process, so only the truly reliable and authoritative datasets are used across the organization.
    - can only certify a dataset if you've been listed as a user in the tenant settings

[Query caching](https://docs.microsoft.com/en-us/learn/modules/manage-datasets-power-bi/9-query-caching)
a local caching feature that maintains results on a user and report basis. This service is only available to users with Power BI Premium or Power BI Embedded
- Improvement of the performance of reports, dashboards, and dashboard tiles by reducing loading time and increasing query speed; this notion is especially true for datasets that are not refreshed often and are accessed frequently.  
- It respects bookmarks and default filters, so even if you enable query caching, any bookmarks that you have created still exist. 
- Cached query results are specific to the user. 
- All security labels are followed.   
- It reduces the load on your dedicated capacity because query caching allows for usage of dedicated capacity and not on the dataset.
PBI service > dataset > setting > Query Caching

## Implement row-level security
[Add members to Role](https://docs.microsoft.com/en-us/learn/modules/row-level-security-power-bi/2-static-method)
- you can add Microsoft Azure Active Directory (Azure AD) users and security groups to the security role
- If members are not added to the role, but they have access to the report, RLS will not apply to them
- Test as role (both in PBI Service and Desktop)


---
---

In order to confirm region is populated for every author, you need to use the column profile tool to understand the distribution for the region column. Additionally, the default Power Query profile is only done on the first 1,000 rows. You need to enable column profiling based on the entire dataset to see all 2,500 authors.

*Deployment pipelines* allow you to manage the lifecycle of your organizations content

Writing a SQL statement to filter the rows prior to loading is the only option that will minimize data load time.

You need to create a visual that compares revenue and cost over time. What type of visual should you use?
- Line charts are used to visualize change over time

The web content tile allows you to add and customize any HTML content, like websites. Web content tiles preserve the functionality of the page so you can access other videos on the site. The video tile only allows you to post a single video

Using parameters allows you to easily switch between different tables and schemas in a data source or database

Contributors can update reports in a workspace and update an app. However, they cannot add other users to a workspace

Members can assign member roles and below

Azure Blob storage queries don't support query folding and therefore cannot take advantage of incremental refresh

Combining the data using merge will cut down on the use of functions like RELATED and RELATEDTABLE that return a related value from another table

You create multiple dashboards in Power BI Service and need to make sure users can see which dashboards contain Personally Identifiable Information (PII). What should you use?
- Senstitivity labels (Sensitivity labels provide a simple way for users to classify content in Power BI Service)

Line charts, with a single line, have a forecasting analytics option that can be enabled

Splitting out the time component from the date helps reduce the model size

Decomposition trees allow you to perform **exploratory** and **root cause** analysis

When a user is assigned to multiple roles, the RLS filters become additive and create a union between the filters

**The 50th percentile is also known as the median or middle value**

The key influencers visual shows the most important factors based on the fields provided

**Impact analysis** provides you the tools to understand how making changes to a dataset will impact downstream reports and dashboards

**bin**(equal-sized groups): You can set the bin size for numerical and time fields in Power BI Desktop. You can make bins for calculated columns, but not for measures. Use binning to right-size the data that Power BI Desktop displays.

**build** permission to dataset. For shared dataset, it is possible to grant 'build (report)' permission to recipients

You need to provide a user with the ability to add members to a workspace. The solution must use the principle of least privilege.Which role should you assign to the user?
- **Member** (Add **members** or others with lower permissions.)

you have several reports and dashboards in a workspace. You need to grant all organizational users read access to a dashboard and several reports. Solution: You enable included in app for all assets. Does this meet the goal?
- No
- correct: 1, publish app. 2, grant access to certain groups.

You need to create a visualization that shows the relationship between Unit Price and Quantity Ordered. The solution must highlight orders that have a similar unit price and ordered quantity
- A Scattered plot of Quantity Ordered and Unit Price by item, Automatically find clusters

three columns: 
City 
Total Sales 
Occupation You need to create a key influencers visualization as 
- Total Sales, Occupation, City (analyzer, legend, influencer)

The indicator color for Total Sales will be based on % Growth to Last Year
- Background Color, Rules

You need to view the employees by region as quickly as possible. What should you do
- Create a new group on the state column and set the Group type to List

You have a Power BI tenant. You have reports that use financial datasets and are exported as PDF files. You need to ensure that the reports are encrypted. What should you implement?
- **Sensitivity labels**

The report uses data from a Microsoft SQL Server Analysis Services (SSAS) cube located on your company's internal network. You plan to publish the report to the Power BI Service.
- An On-premises data gateway

You have several reports and dashboards in a workspace. You need to grant all organizational users read access to a dashboard and several reports. Solution: You assign all the users the Viewer role to the workspace. Does this meet the goal
- No

Manage users that have access to the **app workspace**
- In the Microsoft 365, select **Members**
- (Workspace > ... > Members > (outlook.office365.com/..) > members/Add members)

You want to know which Teacher is responsible for which course
- Inner Join

when using Pivot feature, take care of the 'Aggregate Value Function'
- if you want to preserve duplicated values, you do not have to select the Sum option. (Don't Aggregate)

import **50 Microsoft Excel** files to Power BI Desktop
- Add a folder data source and use the Combine Files command

ColumnA presents several values starting with space;
ColumnB contains several non-printable characters.
- ColumnA: TRIM 
    ColumnB: CLEAN

In the Power Querry editor, select the text column you want to shape and then right click on them. This menu will appear:
- Transform > Trim/Clean/Length/...

split datatime before importing to power bi
- In order to improve our Power BI model performances, it is really important to work at the data source level. Among the different techniques available to optimize the modeling experience, there is the split between the date and time if they come from a single combined column

to replace null values with the data from the previous row
- command: Fill, and then Down

From the **Extract** menu, click Text After Delimiter
- Fist/Last Characters, Range, Text before/after delimiter, Text Between Delimiters

data model presents a huge list of queries that make it difficult to organize the transformation steps
- create a group of queries to classify the data-transformations

parameter
- M: Advance Query Editor > replace text by [varName] (the varName looks like Pythons)

 know which reports present a critical usage
- Request to the Power BI admin enabling usage metrics for content creators.

When you publish a Power BI Desktop file with a live connection to a tabular model to your Power BI site, an on-premises data gateway must be installed and configured by an administrator

standardize the creation and the sharing of Power BI content among the company units
- Deploy **pipelines tool**

Your organization plan to use the Power BI Service to get several visualizations from data stored in a custom application. The developers ask for pushing data into the Power BI Service from the custom app. How can you ensure this task
- Go to dev.powerbi.com/apps and **register an application**.

embed a report into the Microsoft SharePoint site
- *Publish* the report to the Power BI service - Obtain an *embed link* for SharePoint - Add a **webpart** to a page.

RLS can't restrict access to the layout of the report. With Apps, users can interact with the app content but can't modify it.

A Power BI user in your organization has published a report to the Web. The report contained sensitive data. What can you do to prevent the reports from being published on the Web?
- From the Power BI Admin portal, disable the Publish to web setting.

# 4.Administration settings in Microsoft PowerBI
*Static roles* allow you to define filtered views for specific audiences ( territory managers, department leads, execs, etc. etc.) using simple DAX statements
- This is not the same as bookmarks or pre filtered views; roles **filter data out of your model** and limit what audiences can access
- Static roles must first be configured in Power BI Desktop and then applied in Power BI Service


manage the members that have access to the app workspace
- From the Office 365 Admin center, click Groups.

refresh of the underlying data source, incremental
refresh only works with a Date/Time column

Your organization has a Microsoft SharePoint Online site named Enrollments where can access over 1000 users. After you have created a report in an app workspace on Power BI Service, you embed the report into a page on the Enrollments site by using the Power BI web part. You must ensure that all over the 1,000 users can view the report from the Enrollments Sharepoint site
- Configure the app workspace for **Premium capacity**. [premium](https://docs.microsoft.com/en-us/power-bi/admin/service-premium-what-is)
- becasue it's embeded code, the users will jump to access the report in PBI, so it's required to scale up PBI performance.

You need to create a Power BI app workspace that will be accessible by 10,000 users. The dashboard contains sensitive data and you want that it will be updated every 1 hour. What should you do
- Configure the app worksapce for Premium capacity
- pro has a limit of 8 refresh daily

create a Machine Learning Model
- Get Power BI Premium - Create a Dataflow for the historical data - Add a Machine Learning Model.

Your customer owns a custom BI App based on PowerBI Embedded technology. He requests to scale up the capacity available for his custom BI App.
What do you need to change?
- **Pricing tier** from Azure Portal.

embed a report from the app workspace into a line-of-business application by using Power BI Embedded and APIs REST.
Which information should you provide to the application developers
- The application token and the report URL

add a specific user named User_01 as a member to a workspace
- Add-PowerBIWorkspaceUser - Scope Organization -/subscription ID/ -UserEmail Address user@data.com - AccessRight membe

# 5.Microsoft DAX language
create a goal for the number of sales made in the current year and set it as 10% higher than the number of sales made in the previous year
- GOAL = Calculate(Count('Sales'[SalesID]), PreviousYear('Date'[Date]))* 1.10

create a bar chart visualization to show the count of course enrollments by year that have an Enrollments Amount greater than 1,000.
- Larger enrollments = Calculate(Filter('FactcourseEnrollments','FactCourseEnrollments'[EnrollmentsAmount]>1000))

pivot and show the weekd day scheduled
- Schedule Checkbox = IF(COUNTROWS(Appointments)>0, UNICAHR(9635),"")

you have a Power BI model for sales data. You create a measure to calculate the year-to-date sales. You need to compare the year-to-date sales with the previous year for the same time period
- to filter out the dates for calculation

a measure to rank total sales by product
- RANKX(ALL('Product_Sales'), [SalesAmount],,DESC, **Dense**)
- DENSE will give consecutive numbers

You need to create a relationship between the Monthly Drop out table (month id) and Date[Date ID]
- In the Monthly Drop Out table, create a new calculated column named Date_ID that uses the ddmmyyyy format.
- *(incorrect)* In the Date table, create a new calculated column named Month_ID that uses the yyyydd format. (there wll be duplicates of MonthId in date table, which cannot used as keys)

create a chart that displays total Enrollments[Total Paid] by Course[Name]. Before creating the visualization, you need to modify the model
- Create a relationship between the Enrollments table and the Courses table.
- Create a relationship between the Enrollments table and the Courses table. Then, to the Enrollments table, add a column that uses the RELATED('Courses'[Name]) DAX formula.
- *(incorrect)* To the Enrollments table, add a measure that uses the COUNTA('Enrollments'[Enrollment ID]) DAX formula.
- : The first thing to do to create a visualization that combines two different tables is creating a relationship between them; otherwise, the visualization will not work:



# 6.Data Modeling
By default, Power BI automatically creates a
hidden date table for any table that
contains a Date or DateTime column on the one side of a relationship

Develop a template app (when create a workspace)
- Template apps are developed for sharing outside your organization.
- A template app workspace will be created for developing and releasing the app.
1. Create a dataflow using define new tables
1. Create a dataflow using linked tables.reference an existing table, defined in another dataflow, in a **read-only** fashion
1. Create a dataflow using a computed table() reference a linked table and perform operations on top of it in a write-only fashion. To convert a linked table into a computed table, you can either create a new query from a merge operation, or if you want to edit or transform the table, create a reference or duplicate of the table
1. Create a dataflow using a CDM (common data model) folder

---

[difference between Dataset and Dataflow](https://senturus.com/blog/what-is-the-difference-between-power-bi-dataflows-an-datasets/)

A **dataflow** is used to organize and persist self-service data. Behind the scenes, Power BI is using an Azure Data Lake for data storage of the source data and meta data. Data can be cleaned and transformed as part of the dataflow.

Data is then mapped to a standard, extensible schema called the Common Data Model for clearer presentation to end users. Data from multiple sources can be combined in the Data Lake to present a unified data structure to the report developer.

A **dataset** is a pointer to your data source, typically including a subset of the data in the data source. When used with dataflows, the dataset is pointing at the managed Azure Data Lake and including some or all of the data in the data lake. The dimensions and measures of the data lake that are needed in the current report can be pulled into a specific dataset at the proper grain for speed and efficiency. For example, a retailer may wish to have a dataset containing transaction level product mix (which would be large) and another dataset containing summarized daily sales and discounts (which would be small).

Report developers can then select the proper, minimal dataset when building a report. Multiple datasets can leverage the same underlying data in the managed Azure Data Lake at similar or different grains.

Once published, datasets can be shared between workspaces to other users and groups. To further clarify the quality of a dataset, an organization can certify datasets to indicate to analysts the quality of the data they’re using.

---

[Dataset connectivity with the XMLA endpoint](https://docs.microsoft.com/en-us/power-bi/admin/service-premium-connect-tools)
- The user account or app identity that the client application uses to access a dataset must have a valid Premium Per User (PPU) license unless the dataset resides on a Premium capacity

[object-level security](https://powerbi.microsoft.com/en-us/blog/object-level-security-ols-now-available-for-public-preview-in-power-bi-premium/)
- it not only hides tables and columns, but also secures them
- A user without permissions cannot access secured metadata objects via DAX or any other method
- even cache is secured
- object-level security is defined within model roles. Currently OLS definitions are not created natively in Power BI Desktop, but external tools such as Tabular Editor can set OLS rules on Power BI Desktop datasets or through the XMLA endpoint in the service using TMSL or TOM


[Creating a dataflow](https://docs.microsoft.com/en-us/power-bi/transform-model/dataflows/dataflows-create)
Creating a dataflow from a CDM folder allows you to reference an table that has been written by another application in the Common Data Model (CDM) format. You are prompted to provide the complete path to the CDM format file stored in ADLS Gen 2
- Create a dataflow using define new tables
- Create a dataflow using linked tables (read only)
- Create a dataflow using a computed table (can write)
- Create a dataflow using import/export


[what-if parameters](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-what-if)

The first operation you can do in order to optimize the data loading performances is removing unnecessary columns and rows.

[Apply the Assume Referential Integrity](https://docs.microsoft.com/en-us/power-bi/connect-data/desktop-assume-referential-integrity)
- it increase query efficiency
- only available when using **DirectQuery**
- use **INNER JOIN** statements rather than OUTER JOIN
- Data in the From column in the relationship is never Null or blank
- For each value in the From column, there is a corresponding value in the To column.

create measures to count both the number of Enrollments by [AttendanceDate] and the Enrollments by [StartingDate]
Solution: You create measures that use the following functions: CALCULATE, COUNT, and FILTER DAX function.
- YES
- CALCULATE(COUNT(Table[Column]), FILTER(Table, NOT(ISBLANK(Table[Column))))
- the question is to CountRows of different columns.

You plan to import in Power BI Desktop a set of tables from a Microsoft SQL Server.
The Database Engineer created a single view in Microsoft SQL Server that joined the fact and dimension tables in the underlying query as you need to reduce your effort in Power BI modeling data. Does this solution work?
- NO
- You need to model data in Power BI Desktop when using the import data connection mode. In this case, the Developer doesn't reduce your effort.

# [compare groups](https://docs.microsoft.com/en-us/microsoft-365/admin/create-groups/compare-groups?view=o365-worldwide)
- **Microsoft 365 groups** are used for collaboration between users, both inside and outside your company. They include collaboration services such as SharePoint and Planner.
- **Distribution groups** are used for sending email notifications to a group of people.
- **Security groups** are used for granting access to resources such as SharePoint sites.
- **Mail-enabled** security groups are used for granting access to resources such as SharePoint, and emailing notifications to those users.
- **Shared mailboxes** are used when multiple people need access to the same mailbox, such as a company information or support email address.



