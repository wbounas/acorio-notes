# Scripting Challenge Week #5 (Andrew W.)

## Workflows
__Stages__: important for Workflows
Show your users where in the lifecycle your progress is

On an __Approval Step__, you definitely need to have a stage
On a __Catalog Task__, you definitely need to have a stage

Table table = [sy\_db\_object]
When it comes to Workflow Stages, you cannot jump back a stage
- Typically, clients understand that `Approval` means it's set in stone
  - You cannot "disapprove" an already-approved RITM

**OOB, Approvals are handled at the Request Stage**
- Best Practice is to add Approvals to the RITM form
  - Typically, it is under `State`

Sometimes, there are instances where you need 5 approvals to get something approved
- You need to explicitly `define` the state of your ticket to `Approved` in your Workflow


**Workflow Best Practice: _DO NOT USE NOTIFICATIONS**
- Notification Activity in Workflows
  - You are linking a notification to a workflow
    - If someone wants to edit the notification, they would try to search the [notification] table,
      and never find it
    - The admin would have to search through the workflows, and find it (roundabout way)
    - The better way to go about this is using an _`Event`_
    - The workflow will _not_ be held up waiting for the event to fire, rather the event
      will be pushed to the `Event Queue` and the workflow will move on
      - Events named will typically utilize `dots`
      - These are created in the `Event Registry`

**Events are always going to start with the table name**
- After the first dot, it's a little inconsistent what the rest of the name
  is referencing

**Sometimes, clients do not understand anything about SNOW, even if it's implemented**
- You can have clients that have ServiceNow departments that share a Sys-Admin,
  but that does _not_ necessarily mean that they understand what they are doing
  on the platform

There is no visibility into the stages of `Incident Tasks`

On the `Workflow Editor`, the location of the **mouse** determines where the `Core Module`
is placed inside of the workflow


**First step to adding workflows to a table that doesn't have them?**
1. Create a UI Action to "Show Workflow"
  - Otherwise, it will be _very_ hard to debug


**Not Best Practice to use timers in Workflows**
- SLA Timers OOB are good

__NOTE__: Turnstyles are something that previous Academy's do _not_ use that often
