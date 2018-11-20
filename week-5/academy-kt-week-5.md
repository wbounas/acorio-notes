# Knowledge Transfer Week 5

### Resolving Update Set Conflicts when Updating an Instance (ex. Helsinki to Jakarta)
Most of the time, you will want to `skip` and keep a customer's customized

**Notifications**
- Add company header / footer
- We do NOT want to mess with their modifications

**2 Main Reasons to Revert**
1. Application changes drastically
  - ServiceNow OOB _now_ does what you originally wanted OOB
  - EX: ServicePortal (massive customization, then SN comes out with it OOB)
  - EX: Change Management is another example of this
2. Cleaning Up Update Sets
  - Sometimes when changing things you touch records by accident
  - Even if you briefly touch a record (add a space to short\_description),
    it is recorded in an update set
    - Here, you want to _revert back_ so that those records are untouched
      when importing a new update set

Most of the time, probably want to _skip_

**When upgrading environment, there is no real `generic knowledge` to know what to do**
- You're going to need to know _what the client needs_
- Always try to have someone there that _understands their instance_
  - That way, you have someone to ask if this is the way they want it
  - It is easier here to resolve conflicts, and determine what the client wants to
    keep or remove

**Form Fields: Visible vs Display**
- IF you set Display to False in a Client Script, but a UI Policy sets Visible to True, it won't work
  - Display is the actual HTML attribute, setting to false removes the element from the form
  - Setting Visible to False means that the field is still on the form (in HTML), but it is not
    human visible from the default form view

**Separate the functionality of your Catalog Items as much as possible**
- Enables greater long-term supportability and maintainability
- Allows future developers to more easily decipher what is happening in the system

UI Policies
- Look out for `Nested Containers`
  - It is typically a _Bad Practice_ to enforce UI Policies on Containers


### Workflows
If there is a switch at the beginning of your workflow, chances are there should be _different items_

**Event-Based Notification**
If you create a notification that is not based off an event, when you look for the
notification in the events list you will not find it
  - Cannot search for it
Copy/Pasted Messages
- When you want to make edits to these notifications, you have to check out the workflow and re-save
  - If you used `Create an Event`, all you'll have to do is update the `Notification` record

