# Data Import and Export (Obie Kopchak)
Used to import all sorts of data
- Users (used to be done in Excel spreadsheets)

ServiceNow offers a much more robust platform to handle the myriad of complex data 
in today's corporate environment

Excel, CSV, XML, and more

Insert = Create a new record with a /new/ sys-id
Update = Check for any records with a matching sys-id, and replace applicable fields

You can create an Update Reference Template with Excel, ensuring that you are importing 
the proper fields with your data
**NOTE**: For 'TRUE' and 'FALSE' values, you *MUST* use the dropdown, as typing the 
plain-text will confuse the system and not give you the proper value

Table Transform Maps

You can use a 'temporary import table' when importing data as a `Staging Area`

XML is very helpful when using Update Sets
- Includes Sys-ID's and other data-points that is useful when you don't have full admin rights

When doing work for ServiceNow, make sure that you are marking that in the name 
of your update set or table transform
- This is so they know who is making the change
- NOTE: this is *particularly* important when doing OSP work for ServiceNow, as you DO NOT represent Acorio at that time
