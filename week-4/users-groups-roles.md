# Users, Group Administration, and Maintenance (Max Dore)

**What is a User?**
- One record, on the table `[sys_user]`
- Holds data about an individual

**Multiple Ways to Create a User**
- Local Database (on the instance)
- Multifactor: like local, but a passcode is sent to user's mobile device 

**Most companies have an Active Directory**
- Source of information for Users
- Separate from ServiceNow
- These clients connect Active Directory to Service Now using LDAP

**Groups**
Single record stored in the `[sys_user_group]` table, which serves to be a collection 
of users who share a common purpose
- A container of users (people)
- IE Departments

**Roles**
A role is a persona record in `[sys_user_role]` table, which can be assigned to either a user or group
- A role is also /hierarchical/ and can contain other roles
  -- When someone is granted the parent roe, they are also granted any child role
- Roles grant permissions to applications and other parts of ServiceNow, as well as 
  to assign security controls


**Avoid assigning roles to specific users**
- Assign Roles to Groups, and assign users to specific Groups
- When a user gets removed from a group, the roles that they inherited from their group will be revoked

**Clients should NEVER delete users**
- Make them inactive
_OR_
- Put them into a category that is `unused` or `retired`


**PROVIDED ROLES**
- _System Admin_: Access to Everything
- _Specialized Admin_: Admin rights, but only to specific sections (ex. just HR)
  - Some companies do this with respect to the sensitivity of the data
- _ITIL Fulfiller_: people who do incident handling, problem handling, changesi
  - Fulfill ITIL activites associated with the ITIL workflow
- _Requestor (Employee Self-Service, or ESS)_: Have no associated roles, but can submit requests and manage their own requests, access public pages, take surveys
- _Approvers_: Can say yes or no



In ServiceNow Enterprise, there are OOB roles that most likely a role that already exists




