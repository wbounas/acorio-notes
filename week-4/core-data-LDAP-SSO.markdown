# Core Data - Active Directory, LDAP, and Authentication (Brianne Gallagher)

**Active Directory**
Acorio has 150 employees
Lockheed Martin has 100,000+ employees
- You need to get this user data into ServiceNow so that you can access it and do your job within the same platform

`side_door.do`
- this can be disabled in a `sys_prop`
- Allows you to login w/o using the SSO page

//== can also use `login.do` ==//
- this _cannot_ be disabled in `sys_prop`

Typically, ServiceNow is **NOT** the _Source of Truth_ for user information
- **Active Directory** is!!!
  - This is not a 2-way street
    - If a client utilizes Active Directory, 9/10 clients update information in AD, and that is reflected in SNOW
    - Usually, clients are not updating user data in ServiceNow and reflecting those changes in their AD

In ServiceNow, you can check `LDAP Servers` to see if there are any active connections (with green dot)
- This can give clues to you as a developer if their SNOW instance is pulling information from somewhere else

**Integration** - It is very common for clients to want to integrate ServiceNow with other applications
- 2 Applications sending data back and forth to each other
- Examples of this are SSO Integrations, AD Integrations, etc.
- As a dev, you always want to know where the data is coming from, what tables they're feeding in SerivceNow

Instances can be `bonded` (similar to sync), where if you update a record in *Instance A*, it will be 
reflected the same in *Instance B*

_**Glossary**_
_AD_ = Active Directory
_LDAP_ = Lightweight Directory Access Protocol
_SSO_ = Single Sign On
  - Used for Authentication in ServiceNow
_SAML_ = Security Assertion Markup Language
  - The common protocol used in SSO
  - Used to communicate between SNOW and IDP (Identity Provider, which provides authentication for SNOW)
Data Population (putting data into the system) vs. Authentication (having the ability to do so)
  - Usually handled in different manners


**Active Directory** _(Domain Services)_
- "Active Directory Domain Services (AD DS)" is the cornerstone of every *Windows domain* network
- It stores information about memebrs of the domain, including devices and users, verifies their 
  credentials and defines their access rights
- The server (or the cluster of servers) running this service is called a _domain controller_
  - A domain controller is contacted when a user logs into a device, accesses another device across the network
- Used primarily for **users**, **groups**, and **locations**


_**LDAP Key Terms**_
Active Directory / directory of users = database for user, group, and location information for many clients
Distinguised Name (DN) = Unique Identifier for any object in AD (like a filepath pointing to a specific object)
  - Similar to a `sys_id` in SNOW, but is more like a filepath or location versus a string value
Relative Distinguished Name (RDN) = Relative to another location
  - Similar to a `Relative URL`, where you don't specify the entire path because context will 
    tell you where it is located "OU" - organizational unit = Groups for users in AD
  - 1 layer in the heirarchy 
  - A client _needs_ to know what is in each one of their OU's
  - In an LDAP setup, you might need to specify each OU that you will be pulling users from
  - You will **NOT KNOW** where a client's users are coming from!
LDAP - Lightweight Directory Access Protocol = Protocol that connects AD with SNOW
ServiceNow key terms:
  - Data Source = the source of data that you are importing into SNOW
  - Import Set = captures the data in a staging table
  - Transform Map = transforms the data from staging table to the target table

**How to get information from AD into ServiceNow**
Need an understanding of:
- Import Sets
- Transform Maps
- Scheduled Loads = Scheduling of when Data will come into ServiceNow from LDAP
  - Depends on the client, have seen every ~4 hours or so
  - Also not when the majority of users are on the instance, as it might slow down performance

When creating an Excel template for `importing` data, you can choose to *ONLY* import the fields on your
personal list view by not choosing `all fields` for that particular table

**Import Set Table** - Staging Table for Importing Data
Data Source (table) --> Import Set Table --> Transform Data (Table Transform Map)--> SNOW Table

- Naming is **key!**
  - Prefix staging tables with `IMP`, or staging so that it is *obvious* that this table
    is not for perm. data storage
  - There are automatic scripts that clean up these tables and can potentially delete data on there!
  - Also, a user w/o the type of table in their view could mistake the table for a `normal` SNOW table

You can also manipulate the data coming in using **Transform Scripts**
- It's all about knowing the data coming in, and how you want the data to come out


**Coalesce Value**: checks the value of a particular field, and only allow 1 record with a particular value (no dupes)
- This is my identifier for records going into this table
- Only 1 user per user ID 
- Common on LDAP imports to Coalesce on `user_id`
- What is *not* going to change for a user, but at the same time *uniquely identify* them apart from other users

Bradford Shelly has done `Litmos` sessions on LDAP imports
[https://acorio.litmos.com/course/1030862?r=False&ts=636619207519857581]

**LDAP Email Template for Client [acorio.NOW search for it!!]**

LDAP OU Definitions: some are created automatically for you
- Might have to go in and create more, depending on the complexity of the organization

Cheat Sheet on AD Attributes [here][http://www.kouti.com/tables/userattributes.htm]

LDAP Browse: You can `peer into` AD objects if you have a proper filter and RDN
- Using this, you can `troubleshoot` data BEFORE it came into the SNOW environment
  - If a client claims they are missing data, this is a good way to check if it was there in the first place!

LDAP Integration Notes
- The integration uses a _read-only connection_ that never writes to the LDAP directory
  - The integration only queries for information and then updates its internal database accordingly
By default, the SNOW system **does not delete** any entries after they dissappear from LDAP

- If you see _truncated data_, there is probably an issue with your import set
  - Check if there are any limitations on the fields (EX: max character length of 40)


## SSO
People do not typically use LDAP for Authentication (but you can)
- That would be set in LDAP properties

Most Common Setup for Clients
- LDAP feed (just for getting data into the system)
- For Authentication, they are setting up an SSO connection


_Activating Plugins_
- Say you have to do SSO setup
  - Have to activate plugins
    - That plugin activation is **NOT** captured in the `Update Set`
    - Step 1. Activate Plugins
    - Step 2. Import Update Set

//== **Glossary** ==//
_Okta_ = Identity Provider (IDP) primarily used for managing user access to applications across the organization
  - Special relationship with ServiceNow, had a huge booth at Knowledge 2018
  - Can be used to manage users (similar to AD), but is typically not used in this way
  - You can set up MFA (Multi-Factor Authentication) with ServiceNow, but typically MFA is set up with an IDP
  - If your client are asking you `detailed questions` about their IDP or Okta, get someone else in the room 
    as that is not really your role or responsiblity in the relationship with a client
_X509 Certificate_ = Certifies that the IDP is a valid source
  - This is **required**
_Identity Provider (IDP)_ = The thing doing the authenticating (Azure, Okta)
_Service Provider (SP)_ = The application the user is looking to access to (in our case, ServiceNow)
_metadata_ = `machine readable` data that SNOW needs about an IDP 
_User Provisioning_ = Creates a user in SNOW if there isn't a corresponding one from your IdP
- This could potentially be bad
  - Data is not as robust
  - Data could be duplicated




**The Gist**
You have an IdP and a Service Provider
- Handshake with metadata
- Those services can now be connected!






People to talk to about LDAP:
Any Architect
Damien Broccoli
