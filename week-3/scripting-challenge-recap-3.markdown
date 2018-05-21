# Scripting Challenge Week #3 Recap

*(Create a related list of the parents subtasks)*
ServiceNow automaticaly creates a `Related List` when there is a 1-to-Many relationship established

There are some cases where you need to define your *OWN* Related List

_Syntax_
table -> field on the current record 

EX: Incident -> Caller
- This means that the `Related List` will hold all of the `Incident` records where the `Caller` field is associated with the current record (that you are adding this `Related List` to)

EX: Incident -> Parent
- This means that the `Related List` will hold all of the `Incident` records where the `Parent` record is the current record whose form that the `Related List` is on


*_Andrew E.'s Challenge_*
use GlideAjax to send your sys_id to script include
script include queries user table for that user
check to see if that user has a dept head
then will return a bool to see if you have access to the submit button


*2 Different Ways to get Information from a Server*
1. GlideAJAX
  - You want ^this^ if you do _not_ have access to their form
2. onDisplay BR
  - When you click "show me this form"
  - onDisplay BR will run, and will send some data (which you can add to the scratchpad)

