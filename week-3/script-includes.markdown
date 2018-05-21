# Script Includes (Jesse Nocon)




Typically server-side code

Takes a JavaScript Class

*API Name*: the name of the script include
- This is what you are going to call when referencing the script include
*Application*: Scope of the script include
*Accessible Form*

The most common extension is that of the *AbstractAjaxProcessor*
- This allows your script include to be called client side and will be included by default when selecting 'Client-callable'

Script includes are only loaded and only run when called as opposed to global business rules which are loaded with every interaction

Script includes can be made to be reusable blocks of functionality - try to design them with as _general use cases_ as possible so that the code can get reused
  - Group them by functionality

If all of your functionality for a process is grouped in a script include, you only will ever need to update that one script -- each function you reuse means less modification to numerous records
- Keeping your code DRY

*NOTE*: Because Workflows can be tedious to check out -- modify -- check in and workflow context always run on the version they were created under, Script Includes provide an easy way to make modifications

If you call script includes intead of housing the functionality inside a workflow:
  - You only need to update the script include, not check out the workflow and make modifications, then publish
  - Committing a script include with updated methods will affect

_What is AJAX?_
- AJAX is an acronym for Asynchronous JavaScript and XML
  - It is a set of web development techniques that is used to update a webpage WITHOUT requiring a full-page reload
- Within the context of SN, that means that you can call script includes from the client side
- AJAX is Asynchronous which means that client's webpage will not freeze while it retrieves data

*GlideAJAX*
- ServiceNow uses a Glide Class called GlideAJAX
- GlideAJAX does not have many methods - the basic structure of the AJAX call is primarily all you will use
- There is an additional method (.getXMLWait) that can be used but this will cause teh call to be synchronous -- locking the browser until the call is returned
- The basic GlideAJAX call will return one piece of information: a string, boolean, etc.

*Note*: When looking at ServiceNow documentation, check out _Global_, NOT /SCOPED/!!!






As an incident fufiller, I want a caller manager's email, name, and location in the worknotes, so that I can reach out to the caller's manager at any time.
