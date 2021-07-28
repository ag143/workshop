(https://mtygroup.udemy.com/course/microsoft-power-bi-certification-da-100-exam-prep)
# section4 Data Prep
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
2. **Combine & transform** the data
3. **filter** folder path to correct document library

### storage modes
+ Import: Tables stored in-memory within PBI
+ DirectQuery: not data stored.
    - Dataset is too large to be stored in-memory
    - Source data change frequently & reports must show the most recent data
    - company policy states data can only be accessed from the original source
+ Dual: _same query constraint as DirectQuery_