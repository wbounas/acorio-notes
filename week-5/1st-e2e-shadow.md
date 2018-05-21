# 1st Express-2-Enterprise Conversion Shadow (Oxford w/ Aja)

**Look through their original `Express` instance, and look for custom things**
These could include:
  - Custom Tables
  - Custom Groups
  - Custom Roles

If there is *OKTA/LDAP* integration, it is suggested that we _wait_ until
the Prod instance has been upgrade
  - This will not hold up any of the upgrade
  - It is beneficial to set this up when there is support available

We ask during the upgrade process, there is _no_ configuration happening on the
`Production` instance

## Visual differences between `Upgraded Instance` and `OOTB ITSM`
**Several ITSM feature (plugins) are _inactive_ by default as compared**
**to a fresh `ITSM instance` (eg Service Portal)**
  - This will be evident in the application navigator as some modules will not be
    visible until coresponding plugins are activated
  - Full list of inactive plugins is provided in the Upgrade Guide
  - We advise customers to activate these plugins incrementally and evaluate them
    on the sub-prod instance, before enabling them in production
- Some modules will keep their Express name, rather than adopting the OOTB ITSM name
  (eg `Catalog Items` vs `Maintain Items`, under Catalog Definitions)
- Some ACLs affecting requestor and fulfillers are disabled in order to retain an
  Express-like experience for these users
- Express features still exist and function but customers are encouraged to _discontinue_
  their use and take advantage of more powerful options offered by ServiceNow ITSM
  (eg Execution Plans and Approval Rules -> Workflows)

## Contacting Remote Services
Remote Services Requests can be accessed via `HI Service Portal` under the
Remote Services application
  - These requests have the prefix RS (eg RS0012345)
- **All communication with Remote Services MUST be done on a Remote Services Request**
  - Updates can also be made by replying to the HI notification
    (contains `internal@servicenow.com`)
  - Request provides one source of truth: "If it isn't in HI it doesn't exist."
- **_DO NOT_** create INTs or update the Upgrade CHS Request these are not monitored
  by Remote Services and will delay your response time
  - DO NOT contact your consultant via external email

**Writing JavaScript in the ServiceNow Environment (Enterprise)**
- There are _so_ many ways to implement something in ServiceNow, it is worthwhile
  to ensure we are taking our time to create functionality that will last for the
  long haul

# New Stuff Learned

**Branch** = `Department`-like entity in `Knowledge`
- Similar to a category, but in the `Knowledge` application

**NOTE**: `Workflow Activities` can be used to _Set Values_ in a form
- We want customers to move away from `Execution Plans` and into `Graphical Workflows`
  - This will enable them to leverage the full-features of `ServiceNow Enterprise`
    Workflows application

Using an **update set**, you'll want to remove or duplicate and modify demo
data that you plan on using
- This is for most efficiency

**SLA (aja's)**: Anything that's agreed by in your organization
- EX: IT dept has an SLA to resolve this P2 within this time span

**OLA (aja's)**: Operational Level Agreement (between different operational depts)
- Marketing has OLA to complete this task within a certain time period

**Underpinning Contract**: similar to SLA's, but with 3rd-party vendor

We need to look at **metrics**, any graphics that might be associated with Express SLA's
- When we are switching over, it is important to know those graphs or metrics have
  updated properly

**SLA's**
**Retroactive Start**: An incident comes in, initially a P3, maybe a day into the lifespan
		       it's discovered it's actually a P1, and we change priority
- So, now the SLA will start at the opening of the Incident, not when the priority was changed
  - You can actually select what to `Set Start to:` (Approval set, etc...)
- If **not** selected, the SLA timer will begin when the priority changes and meets the SLA conditions


**ACLs** are something you want to be cautious about modifying
**Contextual Security**: (ACL's are in Express as of 'Jakarta')
  - They allow access to tables, data on tables, etc.
- They are contextual: if you deactivate 1 ACL, it might not be super straightforward impact
  - The other ACLs will then take in that space!
  - You might restrict the wrong users access
  - You might enable access to the wrong users
- If you need to make modifications to your ACLs, you want to reach out to your
  Service Partner so that you make the best possible choices for the long-term
- Sys-Admin has the `security admin` role, which allows them to modify ACL records

"If this is early on in your journey, I recommend that you rely on your SerivceNow Experts
to ensure that the work and changes you are making will work for you in the long run" - Aja (basically)


