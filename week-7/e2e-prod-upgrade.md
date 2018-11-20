# Express to Enterprise Production Upgrade (Aja D.)

The clone is based off a 24-hour backup
- Need to ensure that the password is accurate, as the backup will only
  have those credentials

**Dev Upgrade:** 6-12 hours (maybe even more)

**Technical Validation:** post results to work notes

Wait until Kickoff and Guided Tour to let them know the results of our tech validation
- We provide them instructions for their `client process validation`
- Remind them of any updates to the RoadMp
  - Prod Upgrade date and time

**Client Process Validation:** 1-2 days (2 days MAX)
- Can be done in a day (if client wants, go for it!)
- Shorter is better, 2 days should be _plenty of time_

Send a client a quick email during the **Process Validation**, and remind them of the
`Prod Upgrade` date and time
- Also want to remind them there is a _business impact_ of 2-4 hours

Once client validation is complete, we can then schedule the Prod upgrade
- Once scheduled, then we want to _close_ ticket number `ETIU03`
  - As soon as it's scheduled, we _close that ticket_
- Once an upgrade is scheduled, you _cannot cancel_
  - You want to try to block out your time on your calendar early on,
    but **wait** until the client validation has completed

Then, need to open the Support Week ticket
- Let client know

### **Jesse made a video about `Production Upgrades`**
- This is stored locally on this machine
- Should probably move it to a singular repository of `E2E` videos
- Can _currently be found_ in /Downloads/

**Production Upgrade List**
- On `Master Change Request`, there is a button in the top RH corner
  for _Schedule Conversion_
- Important: Check the timezone!
  - You can throw in a "Timezone Check" in the `Work Notes` and that would
    verify using the top RH corner `Time Stamp`, and just compare that
    `Time Stamp` to the clock on your computer

**Want to be careful with planned start and end dates**
- These fields have failed silently in the past
  - Have improved in the past, but still need to be **careful**
  - Try to get it right the _FIRST TIME_
- If you have to make adjustments, let Aja know ASAP

`Planned End Date` is going to be 3 hours after the `Planned Start Date`
- The `Planned Start Date` is based off what we've agreed on with the client
  for the `Production Upgrade` on the _roadmap_
  - Just ensure that you have the local **Date and Time**

Then, you will see a _freshly generated_ `CTASK`
- "Please provide the planned start date and end date" is in the short description
  - Once this `CTASK` is closed, we are _flipping the switch_
- **NOTE:** be careful, because this can also _silently fail_ on you

## Just triple check everything!! :)

Changing the state to `Closed Complete`
- Even though the prod upgrade hasn't happened yet, we change the ETIU03
  ticket state to this
  - Could wait until the next morning, but either _just before_ or _just after_, you want
    to open the `Support Week Ticket`

1-2 Days after, we tend to do the `Best Practices` session
- If client cancels/no shows, or wants to do the BP session two weeks later, we
  **CANNOT** do that
  - Needs to be during the _support week_
- Not `super strict` about it, we can reschedule 6 business days later (don't really want to)
- This is here to _protect you_ in case they keep pushing it off
- We **don't** want clients to miss this
  - Billable hours for us
  - Best interest for our clients to learn more about their new platform

**Sometimes you run into a client that does NOT need the BP session**
- Experienced SN Developer
- Already doing 1:1's with a Service Partner
- In **this case**, we check in with Damien, and if we need to skip, we can skip
  - We just let them know it's super important information
  - Need to have after _Prod Upgrade_ because its key and vital information
    for maintaining and caring for the health of your new Enterprise Instance

At `acorio`, `billable work` always takes precendence over `non-billable work`

Also, try tracking in Projector .5 hour here, 1 hour here

Once the BP session is complete, you can close that ticket
- Immediatly after scheduling Prod Upgrade, we close ETIU03, and open ETIU04
  - Change `Best Practice` to `Work in Progress`
- Opened `Support Week` ticket after scheduling Prod Upgrade

**Note: if you change the date on a ticket, make sure to update the `Short Description`**

If your client has questions that may take longer than an .5 or 1 hour, we can try to
troubleshoot any issues they may have, but at that point we should:
- Work with the client to create an incident
  - This will enable us to leverage the SNOW Support Team

They may be interested in `Remote Admin` hours

**Surveys**
SN collects survey responses to measure our growth
- Can see your own scores in HI
- Similar to how we have CSAT scores for `Engagements` with clients @ acorio

**In each of the ETIU tickets, there is a short description where we have dates**
- Kickoff date
- Dev upgrade date
- Prod upgrade date
- BP date
- Support Week date

**SNOW wants us to do this, but we were already doing them**
- They decided that it's also helpful for SN
- Helpful for Aja to ensure we are staying on track
  - She can see that you have 3 tickets open without a Prod Upgrade open, etc..
  - This helps her out in scheduling
- If anyone else takes over the ticket, this is also helpful

