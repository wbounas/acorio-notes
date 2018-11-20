# AAVI: E2E Training: Training Process, Resources, & Success Strategies (Aja)

**Sometimes we get clients that are SNOW-knowledgable, but sometimes not**
- There are some clients where you can "skip" certain sections because they already
  know what's there

**Fail on your mock kick-off, so you know where to study!**
- You can make use of reference material on the call
  - There are `transcripts` that you can reference
  - The material is all there
  - You can supplement this material with things like `Evernote`
  - These are found on /box/
    - Location:

## Mock Kickoffs
Getting your Feet Wet in front of Everybody

**What is E2E?**
- Express to Enterprise Conversion
- You may need to communicate to clients:
  - This product was built with the intention to upgrade to Enterprise
    - There are differences *under the hood*
    - These are there to `preserve` the Express instance
  - It will _grow with you_, no need to `rip and replace`

If you are making any major changes, make it `clear` to everyone that this
is *NOT OOB*
- Not having worked with Express, it might be beneficial to bring this up when
  speaking with clients

**No plugins available in Express**
- What you see is what you've got!
- Table list views = _reduced_
- Related Lists/Actions on a form = _reduced_
- _NOTE_: Be wary of giving end-users on Express `access` to ACL's
  - You're doing all your configuration in a sub-prod instance (sandbox)
  - This means you're doing your configuration live in `Prod`
- Enterprise allows for `scripting` (one of the big new features!)

**Ask clients if they have a development background**
- Clients with a development background will be thrilled to have a `developer` instance
- For clients who do *NOT* have a dev background, the concept of doing testing in a
  sub-prod instance is completely alien (un-necessary caution and work)

**UI Policies are Restricted in Express**
- Very basic, none of the extra actions are available to us (even as Admin!)
  - Cannot edit certain forms, such as UI Policy (you can do this in Enterprise)
- There are RITM stages, but we do _not_ have control over what they say

**Execution Plan**
- Don't have the option to add a `workflow` in Express
- Execution Plans are available in Enterprise, but they are very limited
  - Most go for Workflows at that stage
- Uses things such as `Approval Rules`, which are qualifiers for an approval to go through

**If users try to Google `ServiceNow`, most docs are for Enterprise**
- Most users will not be able to tell the differences, and will get lost pretty quickly
- SNOW is moving towards a product where there is much more documentation, which is good!

Service Portal is **NOT** Available in _EXPRESS_
- This is usually a BIG pull for clients
  - Something to upsell when converting!

### There is `Knowledge`, `Discovery`, `CMDB Light`
### Also `REST`, `LDAP/SSO/OKTA/Azure`,
### In `Express`, you can only have **1** set of SLA's running against a table

**NO SCRIPTING IN EXPRESS**
- Andrew W. found a bunch of places, but they might be hard to find (scheduled reporting,
  sometimes in the `Condition Building`)
  - This is a little funky, not necessary "Best Practice"
  - Though, this should not affect Enterprise instances
- Whenever an Academy member was working with a client, we always told clients that
  we are moving away from OOB behavior, therefore possibly losing maintainability,
  update-ability
  - If you modify an `OOB UI Policy` (for example), you should really `disable` the original,
    make a _copy_, and then modify the copy (as its based off of OOB)

**There are no local variable sets**
- You will have to create the same variable _over and over again_

**Express**: highly standardized solution, ready to be rapidly deployed, with minimum
	     configuration and customization

**During an upgrade, their instance will be off for 2-4 hours (some buffer time)**
- If you say `2 hours`, some clients will be _up_ at that hour, checking their instance
  - You do not want to be in that position!!
- It could run a little bit long!

**Main Enterprise Platform Features**
- Workflow
- Security
- SLA (Service Level management plugin)
- Business rules
- Client Scripts
- UI Policies
- UI Actions
- Script Include
- Other relevant enterprise plugins

#### Some clients don't want to go into certain sections (scripting, for example)
- Some may want the details, because they have the background
  - Take a **temperature gauge** for a _successful guided tour_!
- _Update Set_ and _Cloning_ are 2 features that the client should have explained to them
  from the beginning
  - This will save their business time and money! $$$

## Final Product: ITSM Enterprise
- Express running on Enterprise
  - Express SLAs running
  - Service Catalog running on Express execution plans, notifications, & approval rules
    - No variable sets
    - Express order guides (if any)
    - Carried over as it runs in Express
  - ACLs configured for Express
  - Self-service via ESS and ITIL homepages
  - Express layout of forms
  - Most plugins inactive, same as in Express
  - Express roles, "reinterpreted" in Enterprise


# In _box_, there are 2 folders
- ServiceNow Resources
  - Upgrade Guide
  - Kickoff Powerpoint
- Overview of Condensed Acorio Process

