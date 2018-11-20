# Client Scripts and UI Policies

# UI Policies
## Basic Reasons for UI Policies
- make field mandatory
- make field read only (Obie: least used in experience)
- make a field invisible depending on context

*Reverse if False*
- Reverses the actions of the UI policy if undone

It is possible to have multipe views associated with a particular view (end-users, fufillers, admins)
- You can make global UI policies, or for a particular view
  - Most of the time you are creating _global_ UI Policies

*NOTE*: Use short description
- Short and concise
- Detailed enough so that someone that is NOT YOU can discern what is happening
  - What you are building is NOT necessarily going to be maintained by you

You can create a UI Policy for any field on a form using _*Conditional statements*_
As soon as the field value changes _in your view_, UI policies kick in
  - This is different from *Business Rules*, which act server-side and will not run until CRUD is run on a record

*True / False / Leave Alone*
- Leave Alone: This rule is not intended to manipulate that particular field name
  - Typically, this is what you are using


*Order Values*
- The higher the order value, the higher priority the system gives it


Typically, if you are trying to make a field manadatory, UI Policy is your BEST FRIEND

UI Policies are used mainly for individual field control and reactions, not for sending messages
- Sending messages would be a *Client Script* use-case

*Client Scripts*
- A client script is JS that is run on the clients browser

**onCellEdit():** Runs when a cell on a list changes value
**onChange():** Runs when a particular field changes value (most common for client sripts)
**onLoad():** Runs when a form is loaded
**onSubmit():** Runs when a form is submitted

Client Scripts === Messages
UI Policies === Controlling Fields

Obie Scripting Challenge:
- Maintain Auxiliary Variable in Invisible Field (for onChange)
- Make sure to clear this invisible field onLoad for future changes
  - Note: this is all dependent on use-case specific scenarios

