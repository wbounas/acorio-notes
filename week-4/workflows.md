# Workflows (Garrison Bell)

## **Workflows**
A visual represenation of a process within ServiceNow -- consisting of activities and transitions

Workflows can check multiple conditions, and take different branches based on those conditions
- You can create notifications within the workflows

**Glossary**
Tabs: You can have more than one /Workflow/ open at a time
Tools: Buttons that help you manipulate the data within a workflow
Canvas: Shows all activities and pathways
Palette: Showing in plain text the workflow and all of its parts
Rollback: Allows you to go back to previous activity in the workflow
Transition Path: Lines that connect workflow activities
Service Catalog: Where you order things in your organization's ServiceNow instance
Workflow Activity: a step in the process, such as a task or a notification
Processing Path: Paths leading from one out put of an activity to another activity,
		 such as from 'Approved'

We tell our fulfillers the status of the project using `Stage` and `State`

Approvals will be SKIPPED if the user does not exist
- Double Check that the user exists when creating stages
- If it's a 2-stage approval process, you can skip over the first one and validate
  that there were 2 separate approvals

There are a few ways to change the Task Value inside of Workflow /Activity/

You can also add variables to re-use some data from elsewhere that might be useful on this form

*Variables*: You can create variables to use within the workflow so that certain
	     specific items can be adjusted based on the situation
- Only add 1 question!

Almost always being assigned to a group, but could be assigned to an indiviual
- NOTE: It is NOT considered best practice to assign activities to specific people,
	if they were to leave the organization from example

You can create workflow templates to re-use existing code

Typically, if a workflow is associated with a *single* Catalog Item, it is named the same
- NOTE: check previous naming conventions, as clients may have already established one
- Probably want to associate only one workflow per item, but you can create _sub-flows_,
  where you include an additional workflow inside of another workflow

A good tip is to create a 'Generic Workflow' that could be used in many different instances

*Stage* = End User sees
*State* = System uses to work off of

Instead of creating Notifications within our Workflow, we instead create _*events*_
- You can sort by `Updated` so that you can see the most recent events you've created
