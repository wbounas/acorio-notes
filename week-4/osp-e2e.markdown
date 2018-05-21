# OSP and E2E (Juliet Acuff)

**Outsourced Service Partner** (really provider) (OSP)
- Investors/Analysts needs a certain percentage of revenue to come from software 
  sales, NOT services to support that
- Software companies are very aware of this
  - This is why ServiceNow has this type of program, to appease the businsess analysts

_Professional Services_: more like projects
- Net-new implemenetations, etc.
- SNOW sometimes reaches out for help

_Remote Services_: blocks of time for support
- EX: 30 hours to use within the next year
- Similar to Acorio's AVA program

There are _2 partners_ that do Remote Services work for ServiceNow
1. DXC (previously Fruition)
2. Acorio


Remote Admin Services

Express Services
- Package of hours for the Express or Enterprise product

This has evolved over time
- Now we have E2E Conversions
- There are some balances of hours


ServiceNow is currently moving _all_ clients to Enterprise from Express
- That means that there will be no more Express Serivces
  - To Acorio, this means all that is left is `E2E` and `Remote Admin Services`

**HI as in `Hello!`**

HI is the tool that SNOW uses to track and bill for Remote Services / OSP work
- You should know that `HI` is bigger (for clients)
  - Even though it is in the application

- Within ServiceNow, this is their `Help Desk System`
- They also created a home-grown application within HI to run _Remote Services_
  - They utilize the SNOW functionality



## E2E: Express to Enterprise AAVI (Aja)
We are taking an `Express Instance` and transforming it into something _much_ more powerful!

#### What is Express?
- Simplified, single instace "junior" version of SNOW for small organizations with minimal to no development or scripting knowledge and/or very tight budgets
- Temporary means for IT departments to mae a case for SNOW Enterprise
**NOTE**: There will be clients who are not in this category
- The purpose of `Express` was to grow-into Enterprise for smaller-scale organizations
- `Express` can grow with you, no need to "rip-and-replace"!


There are **NO** Update Sets in Express
- Many clients only have 1 instance in Express any way
  - But this is important to understand, as the client might not realize the value of Update Sets because
    they have not yet needed to implment them in their SNOW Journey

Enterprise is _a lot_ of money to upgrade to
- There has to be confidence that this is the right step for this business
  - We have to continue to build up this confidence
    - We need to have a _smooth_ conversion and upgrade, that is **technically sound**

**Express History Timeline**
2014: Pay to Upgrade
2017: Acorio begins helping out
Sept - Nov 2017: Early adopters can volunteer to upgrade early (no fee)
Jan 2018 On: Required upgrades begin
??: Forced upgrades (all instances upgraded)

##### Typical Workflow for E2E Conversion:
1. Live `Express Instance` (w/ no Update Sets or XML import capabilities)
  - This is cloned down to a fresh **sub-prod Express instance**
2. This _sub-prod_ instance is upgraded to an Enterprise DEV instance (w/ a new URL)
-- ServiceNow (Acorio) performs technical validation --
3. **ServiceNow go ahead** for client validation to begin
4. **Client validates** data integrity & business logic/processes are all set in **DEV**
5. Live `Express Instance` is upgraded to a **live PROD instance**
  - Live instsance is **_offline 2 - 4 hours_** during PROD conversion

[linkhere][https://cl.ly/2D3p372W1z0b/Image%202018-05-16%20at%203.21.30%20PM.png]



