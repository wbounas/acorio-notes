# Listen to Guided Tour (Aja)

- Used to have longer process
- Meet with client for kickoff
- Do all scheduling there
- Hold a separate, 2hour meeting for the guided tour
- Depending on the client, if you spend more time in the GT portion scripting (or even
  getting to scripting), there are still many other things (workflow, SLA's) that you need
  to get to
- Aja spends about 30 minutes on the Graphical Workflow

**It will be helpful to have 2 hours worth of material (old-school Guided Tour)**
- Sometimes you can get through the material very quickly, and still have 2 hours
- If you can fill the 2 hours, you can bill for it!
  - Keep this information fresh

**Easy Things for Starting Off with Guided Tour**
Clone Request
Create a User

## Guided Tour with Hoopp (CMC)

`Account Rep` = `Sales Rep`

**Basic workflow setup**
Associated with a single record
When applied to single record: called `context`
- Active Contexts: currently running
- All Contexts: all workflows that have run previously or current

_Approvals_ are just one section of the workflow
**Versions are different versions of a workflow**
- Workflow Versions only show published workflows
  - As in, workflows that are completed and ready for use
  - We have the ability to checkout and make edits to an existing workflow
  - You are unable to make edits to a workflow until you checkout a workflow
**Checking out a workflow**
- This creates a new version of the `workflow`
  - You have the _published version_ (still running on any active contexts)
  - You also have the checked out version that you can modify and manipulate at any time

One nice thing about workflows in enterprise
Gives you some freedom in terms of the different logical conditions that you can set up
  - EX if the Article is Draft, publish it!
    - If anything else, don't publish it!

**Clicking `Advanced` allows for Scripting within the conditions**
- Not only can you check for values on the field itself, but you can query related records
  or anything in the database and specify based off that information if the condition is
  met or not
  - Can use `If` conditions
    - For true, `answer = 'yes'`
    - For false, `answer = 'no'`

You can call a workflow inside of another workflow
- _EX:_ If you use an Approval Workflow, but the same is used for other processes, you can
  re-use that Approval workflow in all of the request workflows it would be used for

A lot more liberating going, but at the same time also a lot more going on in the system
- Worthwhile to have a few people in the business take ownership of several processes,
  instead of relying on a singular person to understand it all
