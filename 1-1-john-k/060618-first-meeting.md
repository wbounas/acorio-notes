# First 1:1 Meeting with John Kanthak

**Script Includes**
- Why we use them
  - Keep code DRY
  - Re-usable
- Most common tools in the belt
- Not something you're gonna be doing soon, but when you
  - Not a day will go by that you're _not_ using one

This is NOT something you need to know now

**if I can absorb it, anyone can**

Up til about 3 years ago, we had

**ESS (old style portal)**
- you could write client scripts
  - query database, fetch records

Overnight, you were no longer able to do that, had to switch to
_script include_

`Script Include:` chunk of code that runs on the server,
but is callable from the browser using AJAX

**Can send back a lot of different stuff!**
- array
- string
- more!

Uses a callback function to parse it back out

Most of the time, you want script includes to be `client callable`, which
allows you to call the script include from the browser

`.get()` is a shortcut query method
- only designed to get one record
  - does .next() implicitly


- A glide record object CAN BE a single record, or a collection of records
  from a database table (depending on what it returns)

Always use `.toString();` to convert a field value, JUST IN CASE
- **make it MORE of a string**

**Note:** ensure that the `UI Type` is _always_ set to **All**

`Control:` the value of the `field` on a form, not the value that field contains
`isLoading:` makes sure that the system doesn't interpret the browser action as a `change`
`sysparm_name:` name of the method from your script include that you want to use

then you can pass in data from the client script into your script include

Reference Qualifier for reference fields
- Does NOT query entire database
- Can leverage script includes
  - Example: only return sys_id's for the records I want

`.getUser()` returns entire User Object
`.hasRole()` returns boolean if that user has the role or not

anytime you instantiate a variable using GlideRecord, prefix with `grSomething`

using `gs.log()` to match the count of records if you're doing a big query

**Homework:**
client comes to me
will, here's what I want:

- got the incident form
- you see how when you click on priority, it opens a new tab, takes you to sn docs, etc
- we'd rather impact and urgency labels to be turned into links, when you click on them
  they go to knowledge articles in our knowledge base that explain what impact and urgency are
- what does impact 1 really mean in our organization
  - definitions for each impact

turn labels into links, takes you to published knowledge article in a new tab

ping the #acorio-certification channel for a study guide for the CSA exam
