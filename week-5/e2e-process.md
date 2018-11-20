# Express 2 Enterprise Process (Aja)
_find call scripts in **box** by searching `Express to Enterprise Upgrades`_
- This is favorited currently by Will B.

**NOTE**: We are working for **ServiceNow** when working these E2E
- Unless the customer directly asks about your involvement in Acorio,
  we keep things `general` and we do _not_ typically try to endorse
  Acorio as a Service Partner
- We want to ensure that if the client _does_ have a Service Partner, we get
  them in the loop so they are on the same page with us as we do the
  conversion

**Glossary**
Kickoff: Overview of the Upgrade Process (from Acorio's perspective)
Guided Tour: Client driving, explaining to them each step as we go
Remote Admin Hours: Remote service hours purchased through ServiceNow
Service Partner: helps clients configure their instance
  - Acorio
  - Fruition
  - Free options (local ServiceNow meetup, use SNOW Community, blogs, free training)

**Need to know time zones!**
- We are a big team across the country
  - If there's something I can't answer for you directly on the call, I'll be able
    to leverage our team to get you the services we need
  - Our goal is _twofold_:
    1. Get you upgraded to Enterprise
    2. Make sure you're comfortable moving forward with Enterprise

**Will you be considering _remote admin hours_ (COMPLETELY NON SALES)?**
  - It might be something to consider to help you long term
  - If you don't have the bandwidth ,a service partner can help you fully leverage
    all of the benefits that Enterprise has to offer

It is _very important_ that the client understands that their participation is critical
to their success in a conversion process

Just because someone has extensive experience in Enterprise, does **not** mean that they
have experience converting Express to Enterprise

**Client To-Do's:**
- How do you plan to use the system after the conversion is over?
  - **NEVER** say that they _need_ support (contractual issues with ServiceNow)


**Upgrade Steps**
If an Express client has a sub-prod instance, we do _not_ worry about it
- They will be worried about it, but in this process the only instance we care
  about is their `Production` instance
- We take their `Prod Express` instance, and we clone it as an Express instance
- With the _brand new_ `Duplicate Express` instance, we upgrade the clone into
  ServiceNow ITSM (no business impact as we are not touching the `Prod Instance`)
- Once that conversion is complete, that Enterprise Instance is setup as a dev instance
  (dev prefixed in URL)
- We perform technical validation on this instance to ensure everything moved over properly
**Now, we have our Kickoff and Guided Tour**
- The customer performs validation of their development ITSM Enterprise instance
  - Make it *clear* to the customer that this is their _last chance_ to ensure that we
    are ready for their ITSM Enterprise Upgrade!
- Once the customer gives go-ahead, we upgrade their `Prod Express` instance to ServiceNow ITSM
- Talk about what happens in the Guided Tour and Best Practice Session

Check out the *Suggested Validation Checklist* to ensure that there is no `unexpected behavior`

**Customer Process Validation**
- Ensure core data is moved to the upgraded instance (eg Users, Companies, Groups, etc.)
- Validate forms and business logic/process flows are working in the upgraded instance
- Ensure users have right access based on their roles
- Validate email notifications are working as expected
  - By default email properties are turned **OFF**
- Do not begin implementation, the instance should be used only to validate
- If you are using LDAP certificates wil need to be re-uploaded, SSO will require
  configuration on your IdP to change endpoints (sub-production only)
  - All of these integrations (LDAP, SSO, Azure, Okta) have URL's that don't change
  - Things should continue working the way they have been
    - **NOTE**: LDAP configuration is something that is considered _outside the scope_
		of an E2E conversion, but you can tell the customer that you're more than
		happy to provide documentation or resources to help them set it up

**The Upgrade Process**
- Upgrade to latest patch
- Dev Upgrade
  - **NOTE**: Give yourself a day buffer _between_ the DEV upgrade and the
	      client validation
    - eg: If the DEV upgrade is on 1/15, the client validation will start on 1/17
- Tech Validation
- Client Validation 1/2 Full Days
- Kickoff & Guided Tour
- Prod Upgrade - date, time zone, 11pm, remind them offline 2-4 hours
  - Do not seem like we are super flexible for times
  - Prod upgrades only happen Sunday thru Thursday nights
    - We have to be in the office the following morning to support them,
      this is why we have that limitation
- Best Practice


Never want to leave the Kickoff Call w/o getting these dates from the client,
especially _Best Practice_
- Even if it's a placeholder, this will enable us to manage our resources and schedule for them
- For the `Prod Upgrade`, we don't really want to go further than 1-2 days
  - "For a `Prod Upgrade`, it typically takes 1-2 days. We can do the best practice day
    Thursday or Friday, whichever is best for you."
  - If there is a situation where they are being wiggly on dates, we say "Let me see if I can
    talk to my manager about this, but let's at least get something tentative down."



**People are going to start posting calls for us to listen to in Academy in Slack**
- Upgrade Recordings are available in _box_, but these are
