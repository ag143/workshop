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