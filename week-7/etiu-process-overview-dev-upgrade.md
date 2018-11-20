# E2E Process Overview and Development Upgrade (Aja)

**When you're in the `Kickoff` itself, you're just reviewing the roadmap**
- It's already been outlined in `HI`
- We're not _asking_, we're reviewing
  - The client has already had the information for a while
  - If they had any questions about those dates, they should be entering
    that meeting with those questions

_BEFORE_ the kickoff, we want to make sure they responded and confirmed the
date and time of the Kickoff/Guided Tour call
- We are sharing the `Upgrade Roadmap` with them to review at least once
  before they get on the call with us
- Usually they don't understand all of this, but at least they were exposed to it
  once before the call

**All of this so far is through the _HI Service Portal_**
- The username/password for `remote.services` account is available for another
  person to see when they see the ticket
  - Be sure to let the client know that this is a temporary password, and it will
    be changed
  - Depending on the timeline, we can schedule the dev upgrade for the following day	to ensure that the temp password is captured on the backup

**IDEAL:** When the client is scheduling their upgrade (you are first reaching
       out to schedul the kickoff/guided tour), they also update the ticket
       in HI to provide the credentials
- Sometimes doing this 4, 5 days ahead so that we can go ahead and validate
  before the start of the initial call

**AJA's HI Icon Process**
- ETIU Tickets = Head Icon
- Master Change = Gear Icon

**Always pull up Damien's guide to the Upgrade**
- There are a lot of small details, easy to miss

First thing, open up Knowledge Article that contains our Upgrading from Express to Enterprise
- Want to ensure that we are looking at the most `current version` of the article
- If you haven't seen it before, read the guide top to bottom
- If you are familiar with it, we are ging to 'Creating the Master Change Request'

### Jesse's Upgrade Process Walkthrough
**Go to HI**
- Looking to run an E2E Upgrade
- We are currently pre-upgrade, started scheduling process
- Jesse likes to put the actual date on the ETIU tickets' `Short Description`
  - Ensure you are putting the proper _time zone_ on the ticket as well

**Self-Service Express to Enterprise Conversion module
  under `Self-Service` Application**
- Make sure you follow the `Create the Master Change Record` guide _EXACTLY_
- Look at instance name, ensure they are on the proper version

We tend to put '_dev_' on the end of their production instance name
- If the name is `unavailable`, the system will error out and will not let you
  input the name
  - You can use `dev`, `development`, there are other appropriate names
- Typically there is only one contract, if you see multiple you can reach out
  to Steven or Damien directly
  - We don't want contracts that say `App-Store` only, but other ones are
    usually good to go
- Want to ensure that the _instance record_ and the _application version_ are
  the same
- Click **SUBMIT**, and a `Standard Change` has been committed
  - First thing: **Create a _favorite_ for this**
  - _EX:_ `Chatters Master Change`

**Preferred Data Center Region**: ALWAYS _North America_
**Need Encrypted Drive**: ALWAYS _Unselected_
  - In a year and a half, Aja has never asked about an `Encrypted Drive`

- Enter `Main Point of Contact`
  - Sometimes is auto-populated, you just want to ensure that it's the proper person
- Add Ricky U. and Damien B. to the `ITIL Watch List`
- Set proper dates
- Just want to `Update` the changes, not close it
  - Important that you _Favorited_ the master change, as `Updating` will navigate
    you away from the record
- Before _finishing_ the sub-production upgrade, you need to ensure
  that the `CTASK` (in related list) is closed
  - By marking that `CTASK` closed, it kicks off our upgrade process

**You might find that in the HI Portal, things could be slow**
- Just be patient, and things will be ready shortly

When in DOUBT, follow the KB article!
- Otherwise, reach out to one of your fellow consultants in Remote Services


**Technical Validation**
Documentation provided by ServiceNow
- This documentation is _not complete_
  - Just a `starter resource`

We have our _own documents_ about the `Techincal Validation`, where the first
`7 steps` are from the original, and then _builds off them_
- Adds a lot to what ServiceNow has, catches the client up

## DON'T PANIC
If the client walks away from the Upgrade Process thinking about `errors`,
`bugs`, or something else they can point to in the future, they've lost confidence
- $100k+ instance that they've invested in, they now have _shaken confidence_
- They will start to _question EVERYTHING_
  - "My instance is flawed"
  - This will make it difficult to troubleshoot, or for the client to take proper
    care of their instance

**BOOST THEIR CONFIDENCE**: "We have already run a techincal validation on
			     your instance, and everything looks good!"

**Express SLA's run on a separate table than Enterprise SLA's**
- When we activate the Service Level Mgmt Plugin, the module that clients
  used to use to view their SLA's is replaced with an `Express SLAs` module
  - We actually create this `module` for the customer
- Many customers have metrics associated with their `Express SLAs`, so this is
  _very important_ to many clients


**SLA: Agreement between the Service Provider and the Customer**
- Saying that an Incident or Order will be fufilled in a certian amount of time

**At Acorio, with ServiceNow we have an SLA for responding to HI tickets**
- We have a 2-day SLA for OSP work
- We have a 1-day SLA for E2E work

This is why it's important that we have to respond, gotta make this happen because
we have that 1-day SLA
- If you can get it done today, get it done today!
  - You _do not know_ what will be on your plate tomorrow, or even from
    3 hours from now

**Optional Update Set:** something Aja set up for a client
- Not mandatory, but _welcome to experiment_ with it
- Nice for the client to have, something to give them for explaining how
  to switch from `Express to Enterprise SLA's`

While validating, pay _special attention_ to the URL to ensure that are you working
with the proper one
- The URL will have to change for the `Development` environment
