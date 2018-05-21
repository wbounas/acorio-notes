**Update Sets** (Delonte Bess)

Update Sets: the more common of the two primary methods of moving customizations from one instance to another
- Essentially a container

They are comprised of a /container record/ on the Update Set table `[sys_update_set]` 
and /customizations/ on the Customer Update table `[sys_update_xml.list]`
- *Update Sets* aremanaged in the System Update Sets application

*The Default Update Set* (DO NOT DELETE OR EXPORT)
The Default update set is the update set in which any changes not captured in ahoter update set are placed
- It is NOT best practice to perform any work in a default update set

What is Tracked in Update Sets?
**CAPTURED:**
- Scripts
- Form Configuration
- List Configuration
- Tables
- Reports
- Views
- Workflows
- System Properties
**NOT CAPTURED:**
- New Data Records
- New Configuration Items
- Modified Data Records
- Modified Configuration Items
- Schedules / Scheduled Jobs
- Users
- Groups
- Personalizations

*NOTE:* 10 - 20 Changes per Update Set is a Best Practice

*NOTE:* Any field with a `u` in front of it is a customized field


