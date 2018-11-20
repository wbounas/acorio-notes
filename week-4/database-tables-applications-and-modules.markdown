# Database Tables, Applications, and Modules (Andrew Easterling)
/An overview of how data is stored in ServiceNow/

Everything in ServiceNow is Data on a Table!
- Specifically, it's a MySQL database
- ServiceNow provides an API to abstract away SQL, no need to write queries

The database contains tables, tables contain records, and records hold fields

*Table Name* = Found in URL (ie [sys_db_object])
- Automatically populated based on the table label, and a prefix as follows:
  -- In a scoped application, the name is prefixed with a namespace identifier to indicated that it is part of an application
  -- For a table in the global application, the name is prefixed with the string `u_`
  -- You CANNOT modify the prefix; however, you can modify the rest of the table name
    -- The name can contain only lowercase, alphanumeric ASCII characters and underscores (_)

*Label* - Found at top of the list view of the table (plain English)

*Extending Tables*
Why Extend a Table?
- Extending a base table incorporates all the functionality of the original table -- including fields and scripts -- into the new table
- Administrators and application developers can only extend tables during table creation
- Administrators and application developers typically extend tables to create a set of related records that share information

*Key Parent Tables in ServiceNow*
/Task[task]/
- Stores records that represent work
- Extended by Incident, Problem, Change Request, and others
- Task and all tables that extend it have access to SLA's, Approval Rules, and Defining Assignment Rules

If you extend the Task table, you get the abilities of the Task table

Base Configuration Table [cmdb]
- [cmdb] is the core CMDB table
- Extended by Core Configuration Item [cmdb_ci] and CI Relationship [cmdb_rel_ci]
- [cmdb] is also extended to tables like Server [cmdb_ci_server] which is in turn extended to tables like UNIX Server [cmdb_ci_unix_server]


The Tables... table (aka [sys_db_object])
'Best table in ServiceNow' - Sean Duhaime

- This is every table in your ServiceNow instance, all stored on this master `meta-table`

Schema = Map of the relationships that a table has to any other tables in ServiceNow

Dictionary Table [sys_dictionary]
- Contains metadata on every table, and every column in every table

Tables & Columns (in System Definition application within the filter navigator)

Application (ie Incident, Problem, Change)
- Applications are a collection of filesand data that deliver a service and manage business processes
- Incident, Problem, and Change are all examples of applications
- Apps are more than just tables
  -- Can include: 
     - Tables
     - UI Elements 
     - Application Files
     - Integrations

Table Relationships
One-to-Many -- Within a table, a field can hold a reference to a record on aother table
  - Reference Fields
  - Glide List
  - Document ID Fields
Many-to-Many -- Two tables can be related in a bi-directional relationship so that the related records are visible from both tables in a related list
  - EX: Softare Vendors can sell multiple Products and Products can be sold to multple vendors
Extentions -- A table can extend another table
  - It has it's unique fields plus all the fields the extended table has
Database Views -- Two tables can be joined virtually using the Database Views Plugin to allow for reporting on data that might be stored in more than one table




