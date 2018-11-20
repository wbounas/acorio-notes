go into the company record
- go into configuration items
- look at their express instance (possible they have other instances)
  - when that happens, we'll talk about it
- ensure that they are AT LEAST on Jakarta Patch 7 or higher
  - If Not: they should have a change already created (which would be on the record of their instance)
    - This is under `Tasks` related list
    - you can go and change the start date to 11pm at night local time
    - if there is no change existing, let Damien know that the customer is upgrading at this time,
      but they are on this patch, and there has been no change created yet
      - "Need to have it done by X time"


**FIRST TICKET**
- Reach out with initial template
- as soon as you do this, change the ETIU01 state to `In Progress`

Hopefully both meetings scheduled
credentials shared to us

Most of the time, 2nd meeting is not scheduled or creds not shared
- we then ask for these again

Once they've done that, we can share a `roadmap` through the ETIU01 ticket
- we go and update the short descriptions with the times on the schedule
- put local time tbd on ETIU01 as we do not know until the KO/GT
- mark in personal calendar the day of the prod upgrade and the end of the 5-day helpline



Then, depending on the time that the user was created we can do the DEV Upgrade
- with creds, we log in, go to users table, look up the remote.services user (in list view
  - created that day, we have to wait for the backup to finish, otherwise we can do our dev
    upgrade that day


it takes a little time for the dev upgrade, so typically the dev upgrade is done the day before
you do your dev validation

When doing the Dev Upgrade, (search express to enterprise conversion in filter navigator)
- Upon hitting submiton that form, creates the master change record for the customer

last step of the dev validation is to put the results in the work notes of ETIU01

THEN we can close ticket number one, bill the ticket (close complete)


**SECOND TICKET** ETIU02
- Set to work in progress
  - can't continue until actually hold the KO/GT
- Once the session is over, send follow up communications through additional comments
- Update short descriptions with roadmap times if they changed

Unless the customer finds something during their `Data Validation`, we
wait until the day of the prod upgrade to select `Schedule for Conversion`
- We do this on the master change record
- Upon hitting that button, a CTASK and Change Recorded are created under the master change ticket
  - You need to follow the guide for the `Change Record`
  - Close the CTASK after that
  - ALWAYS BE LOOKING THROUGH THE DOCUMENTATION WHEN PERFORMING THE PRODUCTION UPGRADE

Once you've gone into the master change and scheduled that upgrade, once it's scheduled
you can close ETIU03 and change ETIU04 to `In Progress`
- Before closing ETIU03, if you have not heard from the client in a while you can add
  additional communication through the HI Service Portal

First thing the morning after a production upgrade, change the status of ETIU05 to `In Progress`

Hold BP
- After completion, send follow up message
- Close ETIU04

After the 5th day, close ETIU05 and you are finished
