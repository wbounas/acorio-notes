*CMDB Lite* (Andrew Easterling)
An Introduction to the Configuration Management Database Inside and Outside of ServiceNow

CMDB - Configuration Management Database
- Configuration Management (CM) is an ITIL process that tracks all of the 
  individual Configuration Items (CI) in an IT system
  - The fundamental component of CM is the CM database (CMDB) which have the CI 
    information and is used to understand the CI relationships and track their 
    configuration and more
  - Contributing to lower cost and higher customer satisfaction

A configuraton item (CI) is an IT asset or a combination of IT assets that may depend 
on and/or have relationships with other IT processes
*ATTRIBUTES*
- /Technical/ - Data that describes the CI's capabilities which include software 
                version and model numbers, HW and manufacturere specifications and 
                other technical details like networking speeds and data storage size
- /Ownership/ - Part of financical asset management, ownership attriutes record purchase 
                date, warranty, location, and responsibile person for the CI
              - ID numbers like bar codes and type, like software, hardware, and documentation 
                are also ownership attributes
- /Relationship/ - The relationships between hardware items (eg. a printer), 
                   software (eg. drivers), and users (eg. Alice)

Everything inside a CMDB is either both, one or the other, or a mixture of both
Asset Management - /Financial/
Configuration Management - /Technical/

CI Classes (how you structure CMDB tables)
CMDB classifications are groups of CIs that share the same attributes and are stored in their own table
These classifications allow administrators to define the hierarchy of CIs within the CMDB

- The core Configuration Item [cmdb_ci] table, which stores the basic attributes of all the CIs
- The CI Relationship [cmdb_rel_ci] table defines all relationships between CIs
- The Configuration Item table is extended to other tables, such as Database [cmdb_ci_database] and Computer [cmdb_ci_computer]
  -- The Computer table is extended to the Server [cmdb_ci_server] table, and so on.

*Relationships* are one of the most important aspects of the CMDB
  - So we can understand how different things impact one another
  - This is key and critical to ITOM, ITSM, it really becomes the *brain* of the business

*/ITOM/ Concepts in an Initial Implementation/*
- The path is different for every new ServiceNow custoer, but many ServiceNow kickoffs will involve the following components

-- The MID Server is a server located WITHIN the client's internal network
  -- This device acts as a middleman between the SN cloud and the customer's network (required for most ITOM products)
-- Lightweight Directory Access Protocol (LDAP) is a protocol used to authenticate users and share information across an IT environment
  -- Active Directory is a product that uses LDP, frequently used as a source of User Data
-- A Service is a top-level business value that is provided through one or more Applications
  -- ServiceNow may be logged as an "IT Management Service" in a CMDB

How is the CMDB applied?
- Planning: strategy, policy, scope, objectives, roles and responsibilities
- Identification: selection, id, and labeling of all CI's
- Control: All CIs will be under Change Management (ITSM) control
- Mintoring: enables changes to CIs and tracking of their records through various statuses, eg ordered, received, under etst, live, under repair, etc.
- Verification: reviews and audits

*NOTE*: An incident usually comes from a change that didn't go correctly

cmdb_ci is the prefix for any CMDB table

ServiceNow CSA Participant Guide - Exam Prep Book (need to read!)
-- Come up with 1, 2, or 3 questions per page
-- Write down the page that the question came from
-- Get learned


