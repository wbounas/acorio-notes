# Scripting in ServiceNow (John Nolan)
/Basic Scripting Deck.pptx/

*Only script when necessary*
- If you can accomplish what you want with set business rules or condition builders, do this instead
  - This is for the future system administrators, not YOU
  - Future maintainability, update-ability
  - This _simpler_ you can make things for them, the easier things will be going forward

There are several common APIs (also referred to as Glide Classes) within the ServiceNow platform
- GlideForm (g_form): Used for client manipulation  
- GlideUser (g_user): Used to retrieve user information while working client-side
- GlideRecord: Used to create or query for records on tables
- GlideSystem (gs): Used to retrieve general information

Anywhere you work on a script in ServiceNow (other than background scripts) will be in the *Script Editor*

GlideRecord query is what you'll be doing the most of (Server Side)
- Primary tool for querying a table in ServiceNow
- It is also used for insterting and updating records

Standard Pattern
- Querying
- Insert
- Update

.addQuery() can take two different sets of parameters
- 2 parameters: a field and a value
  - This is equivalent to an IS query (only the exact value is returned)
- 3 parameters: a field, an operator, and a value
  - This extends the functionality to where you can say is (=), is not (!=), greater than (>), less than (<), and so forth

Adding orConditions to a GlideRecord can make it a _complicated_ script -- you need to define a new variable to house the 'or' portions as below
  - This is tricky, due to easy misunderstanding of a 20-line .addQuery() script
  - You can use _.addEncodedQuery()_ and copy a query built using the *Condition Builder* on a list view of a table, and throw that in as an argument

There are 2 other GlideRecord methods of note but should _onlybe used_ while debugging or testing your code

.getRowCount(): this will return the number of records that your GLideCrecord has retrieved
  - It must be used following .query()
.getEncodedQuery():


*GlideSystem*: an API that provides a way to gain access about the system and the current logged in user
  - Also the primary means of triggering an event
  - You can also use GlideSystem for date methods, such as gs.beginningOfNextWeek()
  - GlideSystem is available anywhere you can script serverside
    - It is not available on the client

gs.getUser() - will return a user object with common fields (username, email, department, manager, etc) - but WILL NOT return the full user record
gs.getUserID() - just returns the sys_id of the current user
gs.getUserName() - just returns the username of the current user
gs.hasRole('role') - checks if the user has the role and returns true or false
  - *NOTE*: This will return `true` if the user has either the role specified _OR_ the `admin` role

System Properties
.getProperty('property_name') is one of the most useful `gs` methods
  - This allows you to check a system property -- a value set that can be referred to anywhere in teh system

In scripts, you sometimes need to reference `sys_id` of records
- If you are going to re-use those `sys_id`'s in a number of scripts, the best practice is to create a *system property*
  - If you ever have to change the group, you only have to change the `sys_property` record, instead of all the scripts that you reference that particular group
  - If you find you are hard-coding `sys_id`'s in scripts, might be worth looking into creating a `sys_property` record

Background Scripts
- Be careful when using this tool to update records!


Notes on sysIDs
- A sysID (system id) is a field that is present on *every* recod in SN
  - It is a 32 character gloally unique identifier for the record
- SysIDs are not stored as strings (they are stored as objects)


*Business Rules*: Primary scripts running on the Server Side in ServiceNow
- Act on interactions between a user and teh database - before a form loads, when a user quries a table, or submits a record

_*4 Types of Business Rules*_
*Display* - This BR will run before a form is displayed. These are primarily used to pass information to the client scripts
  - Typically used to populate the table's `scratchpad` that can be referenced by client `scripts`
*Before* - This BR runs after form submission but before the record is inserted or updated in the database
  - Typically used to update anything on the current record you are looking at
  - The fufiller changes the `incident state` to resolved, then populate
*After* - This BR runs after the record has been inserted or updated in the database but before the form reloads
  - Typically updating records that are NOT the current record
*Async* - This BR runs after the record has been inserted or updated in the database (the form may reload before it is processed - it is placed in a queue)
  - Takes code in BR, throws it in a queue, and will run when the system has the proper bandwidth
  - You do NOT have access to the _previous_ object
  - Used more for `web-services` calls, versus an `After Business Rules`

You should *NOT* create Global `Business Rules` as they will slow your system down

Display Business Rules are primarily used for passing information to the client to be used in scripts there
- This is accomplished via the g_scratchpad object
  - g_Scratchpad is useful when you need to build cline tscripts that require server data that is not typically part of the record being displayed

After BR are primarily used to update recrods other than the current record
- This can mean updating a parent record (if a task is closed, move the parent's status along) or modifying a record refereneced on the for - even querying an unrelated record and modifyin

NEVER UPDATE THE CURRENT RECORD IN AN AFTER BUSINESS RULE
  - The record has already been touched in teh database and you can trigger all business rules to run again -- including this one!
  - It may cause an infinite loop!!!

*Query Business Rules*
`Query` BR's are not a 'when' (like before or after), but rather run on an action (like insert or update) - when a user queries a table
- The most common query 'when' is before and this is used in conjunction with ACL's
- If you have an ACL that only let's users see incidents in their department, users will be presented with `X records removed due to security constraints` message
- You can use query business rules to limit the search results through adding query conditions


Scripting in Workflows
- There are a number of places within workflows that you can script -- the most notable of which is Run Script, which will just be a script to run
- You can also run scripts in many 


Script Includes
- A script include is a piece of logic that runs on the server
- Keeps code DRY
- It is available everywhere in the system to be called -- both server side from any business rules, scheduled jobs, etc and client side from client scripts and UI policies
  - They are a developer's best option to make reusbale code within ServiceNow

_3 Different Types of Script Includes_
1. Basic/classless/OnDemand: this script include is simply a fucntion that matches the name of the `SI` record and can be called anywhere server side
2. Utils (Class): Creates a new class and can be called anywhere. It is a set of methods and properties`
3. Extending another Class: Script includes can extend other classes to ehance functionality. These can also be called anywhere
