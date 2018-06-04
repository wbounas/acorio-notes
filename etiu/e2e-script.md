# Express to Enterprise Upgrade Script
## Express To ITSM Upgrade // Paired with ETIU Services Kick-off 2017 v3.0 Slide Deck


### Introduction + Set Up (Slide #1)
**Can you see my screen?**
**Will there be anyone else joining this call?**

"Is it alright that I record this, for future training purposes?"

We are now recording.


### Agenda (Slide #2)
Today what we'll be doing is going through an hour long presentation that will walk you
through what the upgrade process is, how it works, and give you some information about
your upgraded instance and what it looks like under the hood.
- Review the upgrade roadmap today, to make sure we are on the same page in terms of the schedule

For the second half of this session, we already have your enterprise developer instance generated and
upgraded, so for the second half of this call i'll have you:
- Take over and share your screen, and we'll:
- Jump into your developer instance to take a look at some of the key new features now available to
you with Enterprise


### Who Are We (Slide #3)
My name is Will, and I am part of a team of other `Remote Services Professionals` that work across
the country.
**If there is anything I am unable to answer for you, our team should be able to get the answer for you.**
((There are some things that do lie outside the scope of the `Remote Services Department` and really more in
the hands of your `Sales Rep`. We will work with you as much as possible to get in contact with them, but))

Sometimes really the _quickest way_ to get that information from your `Sales Rep` is for you actually to
get in contact with them yourself.

**My goal here is really twofold:**
1. To make sure you are upgraded in a technically sound manner. We begin this process with a technical
validation that has been done on your developer instance, and we'll get more into how that plays into
the whole upgrade process in a moment.
**-and then-**
2. As we upgrade you, our goal is that you're feeling confident and secure with your new instance!
   Having some knowledge about what is there and available to you now, but also where you can go to
   get more knowledge, or more assistance with your training.

### Review Slide #4

### Critical Success Factors (Slide #5)
**There are a few more points I'd like to make as we continue here:**
- Your participation is a critical part of the success of this process. We have a timeline, but we
  are really working together here to achieve that timeline. And sticking to that timeline really depends on
  your participation as much as mine.
- If you are working with a Service Partner, we want to reach out to them to ensure
  they have the information they need.

_Are you working with a Service Partner?_
If **YES:**
If **NO:**

////////////////////////////////////////////////
Aja's Experience (Optional)
The shift from Express to Enterprise.. Once you're onto Enterprise, if you continue to use the instance
the same way, you'll see a lot more available to you. You can choose to not use the Enterprise features
and only use the Express features. I do not recommend it, as you'll find the Enterprise features can
make your life a whole lot easier, but that is an option. If you are looking to take advantage of some
of the more compex Enterprise features (or even just shifting to them), I recommend getting some
support early on in your joruney, as I see clients that have that support are more successful long term.

They also save money, time, and energy down the road, the reason for that being because Enterprise has
so many moving pieces, there being so much we can now do with incorporating scripting, since there are
now so many options you may be moving forward in a direction that you really don't want to be going long
term, and could need to be un-done. Doesn't necessarily have to be a Service Partner or Remote Admin
hours, it could be going to a local ServiceNow meetup group, or even taking the time to do some of
the training (some is free, some do have a cost), reading documentation. As long as you recognize that
in Express, while you could jump in and make configurations without worrying too much long term, with
Enterprise we want to think carefully about what we are doing and how we set things up.
////////////////////////////////////////////////

### How does this all work? (Slide #6)
You have currently your `Express Production Instance`. What we've already done is:
- Spun up a new _Express Instance_
- Cloned your `Express Production Instance` (your _current live instance_) down to that new
  `Express Instance`, so that we have a **copy**, and then
- We performed the upgrade process on that cloned, copied `Express Instance`.

That is seperate from your `Production Instance`, so there has been no **business impact**. That
`cloned instance`, where we performed the _upgrade process_, that is now your **Enterprise Development
Instance,** sometimes referred to as your _Sub-Production (or sub-prod) Instance_. But that is your
**Developer (or Dev) Instance**, and it is now on `Enterprise`.

So what we want to do here is during the second half of this call is:
- Take a look in it and explore some of the new features.

But for the next two days, you'll be validating that _Developer Instance_, and I'll
talk a little more about what you're doing during that _validation process_, and then once your `validation` is
complete, we perform the **Production Upgrade** (the _Prod Upgrade_), and during this **Production Upgrade** (the upgrade
of your live, `Production Instance`), there **is a business impact**. Your instance is _unavailable for 2-4 hours_.

It says 2 hours on the slide, but I like to say 2-4 hours so that we have that buffer.
- Generally it is closer to 2, but just to stay safe we give all of our `Production Upgrades` a little
  more time as sometimes the upgrade can run over 2 hours. We begin that live `Production Upgrade` at
  11pm, and we do this local time to avoid taking the instance during normal business hours.

**May I ask what time zone you are located in?**
_EXAMPLE ANSWER_: Eastern. Ok.

So we could schedule that `Production Upgrade` (do not have to answer right this second,
I am still going to be giving you some more information on the _validation process_), but we could
schedule this for as soon as:
- **11pm Tuesday (_1 day after this call_)**, or if that's too soon, we could do:
- **11pm Wednesday**
  - We wouldn't want to push it too much further out than that.
  - Then, after that `Production Upgrade`, we have another meeting together,
    this one being our `Best Practice` session.
- To ensure the accuracy of your data we like to schedule this `Upgrade` between 24-48 hours after this call ends

**During our Best Practice session, we'll be talking about:**
- How you move configurations from your `Developer Instance` to your `Production Instance` using Update Sets.
  - Do you have any _resources_ already available to you to help you with the administration of your instance?
- To make sure we are getting the _most use_ out of these upcoming sessions, do you have a **system administrator**
  with _Enterprise Experience_ who will be taking over, or will it be an `Express Sys-Admin` who will be learning
  **Enterprise**?
- We want to do this soon as possible after the upgrade has been run.
  - Suggest the day after the upgrade, and then the day after
- Next 5 Days: Personal Upgrade Helpline Available
  - You'll have a helpline available to you 5 days pertaining to issues from the upgrade itself

**Today, we'll have your `Guided Tour`**

This is a high level introduction to some new key features available to you in your `Enterprise Instance`.
There are _a lot of topics_ on here, anything that we do not get to **cover today** we'll be able to review
during our _Best Practices_ session, but we'll take a look at:
#### Slide #10
- The Graphical Workflows
- Contextual Security
- SLA's
- We'll look at many of the key places in your new Enterprise instance where you can implement scripting.

Do you have any `development background` or `scripting` knowledge personally? (No worries if you do not!)
- You will _not_ be `scripting` most of the time, but that feature is available to you.
- It is not _very heavy scripting_, it is utilizing **JavaScript** and enables you to do _more_ than you
  could without scripting, but that being said there is `A LOT` that you can do _without_ scripting at all.

Something I've found is coming from `Express`, and having some _knowledge_ of scripting background
but not so much it's your _first instinct_ to put yourself into a scripting solution, actually positions
you in a good place!
- Because `Best Practice` is:
  - If you can do something with a _conditional drop down_
  - If you can do something through `configuration` rather than customized `scripting`,
    we want to take that approach first because it's going to be more cost-efficient for
    your `organization` in the long-run
- **It's faster too!**
  - Instead of reading another _developer's script_ and try to get into their `head` to see their real
    intentions for why they wrote their script the way they did, we can utilize the `configuration` options
    that `Enterprise` gives us that you are already familiar with in a lot of areas in `Express`, it's a
    little more _straightforward_ and _easier_ to pick up for someone else down the line.

For the `Best Practice Session`, we'll look at **Update Sets**.
- Are you familiar with **Update Sets** at all?
- We want to make sure that you are set up to pull your Update Sets from Dev to Prod, so there's some
  setup we'll do together.
- Same with `Cloning`, we'll show you how to request a system clone and ensure that you're setup to
  make that `request`
- And then we can talk about `Upgrades` in `Enterprise`, `Plugins`, any `other topics` that you'd like us
  to cover or any that you know off the top of your head that aren't listed here,
  just let me know ahead.
  - Update the ticket in HI and let me know!
- **These sessions are recorded and are each 2 hours long.**
- **We want to do this soon as possible after the upgrade has been run.**
  - Suggest the day after the upgrade, and then the day after

We do have a suggested `Validation Checklist`, and this contains a _checklist of items_ to guide you through
the `Validation Process`. This may not all apply or be appropriate for you in your situation, and there may
be _additional things_ you'd like to validate as well.

### Scheduling the Upgrade Steps
Taking a look at our _schedule_, by the time we **complete our call** here it will be (**_2 HOURS PAST START_**), so
that will give you a `few more hours` in your day.
- We could schedule the `Production Upgrade` for Tuesday, 11pm Eastern Time (Kickoff is at 1pm Monday), or
- We could do Wednesday 11pm to give you the extra day to _validate_.
  - What do you think is the _most realistic_?
  - Then, we want to look for a time to schedule the `Best Practice` session.
    - Suggest the day after the upgrade, and then the day after
    - We want to have this done as soon as possible after the upgrade has been run


/////OPTIONAL/////

Because you have familiarity with Update Sets, not worried once on Prod with a sys-admin that has some
general SN background. Is there a particular day that works best for you?

//////////////////

### Customer Process Validation (Slide #9)
Let me jump into what's involved with the `Validation`.

This would be something that you'd begin with the close of our call today, and continue up until we
do the `Production Upgrade`.

I have performed _technical validation_ on your `Developer Instance` (which again,
is your **cloned Express Production Instance** that we have already upgraded to `Enterprise`), and we know that
whatever we see with the `Developer Instance` is what we are going to see with our `Production Instance` because
we are performing the same process.

We can be confident that if the `Developer Instance` is looking good technically,
the `Production Instance` will also. What we need to check now are things that _you_
really have the best knowledge about, which is your:
- **Core Data** and your
- **Business Processes**

**I am going to ask you to check different tables in your instance.**
- If you have any `custom tables`, that the data has _carried over properly_.
  - One way to check that is to verify that the number of records in your **Express Production
    Instance** table are the same as your new **Developer Instance** table.
- Checking the form itself for multiple tables
  - Making sure that the form looks the same as it does in `Express`.
  - One form in particular I'll ask you to pay attention to is `Incident`, and if you have any `custom tables`.
- There is your `Users` table, and you may see some extra `Demo` Users in your Developer instance.
  - You just want to ensure that there are _no fewer users_, and no `duplicates`
    in your **Developer Instance** that we're not seeing in `Express`.
- `Companies`, `Locations`, `Departments`, any new tables like that.
  - `Groups` and `Roles` are tables you will want to check.

Our goal here is to make sure that when we perform the `Production Upgrade`, your `fulfillers` and `end-users`
will _not_ be noticing any **difference**, and that everyone will be able to _do the work_ that they expect to do, with
everything being _where they expect it_.

With the `Roles table`, be aware that `OOB with Express` there are only _5 Roles total_, and we really only primarily
use 3 or 4 of them:
- ITIL
- ITIL Admin, and
- Knowledge Role

With `Enterprise`, I want to say there are about `72 roles OOB` and one area in particular is `Reporting`.
If you have any users who use Reporting, whether that is:
- `viewing reports`
- `creating reports`
- `editing reports`
**make sure that you impersonate those users** and ensure that _they have access_.

In `Enterprise`, there are a _number of roles_ that all together grant that `reporting
access` (_more granular control_), where as in `Express`, we only have the **ITIL Role** that is bundled into
the `Reporting Role`.

When carrying over your configuration from `Express` to `Enterprise`, it doesn't always know
how to properly interpret that **blanket ITIL access** to reporting in terms of the more `granular Enterprise Reporting
Role` options.
- If you see anything like that, let me know and we'll make sure that they get the `correct role` so
  they have the right access to the reporting needs they have.

Once you check that your **core data** is there _with integrity_, you want to:
- `Impersonate` different users
- Different roles
- Impersonate an `end-user`
  - Create an `incident`
  - Create a `request` or a `catalog item`.
- If you have any order guides, create a request with those.
  - If using order guides doesn't make any sense to you, no worries.
- Then, walk through the entire process:
  - For Example, impersonate a `Fufiller` and take all the actions a `Fufiller`
    would, all the way until the **closure** of an incident or request.
  - When closed, ensure that the `end-user's` view of that form versus the `Fufiller`'s view,
    - That everyone has the correct access and can see the _proper fields_ on those forms
      based on their **level of access**

Also want to make sure you validate `Notifications`.
- Any notifications that are hanging during the `Upgrade Process` will wait in a queue,
  and then go one-by-one when the `Upgrade Process` is complete
  - This ensures that your system does not crash upon starting the `Enterprise Instance`


By default, `Notifications` are turned off in your `Developer Instance`. That's not the case with your `Production
Instance`, but with your `Developer Instance` they are _actually turned off_.

I will include some _instructions_ about this, and there is some information included in this Kickoff as well,
on how to turn on those `email properties` so you can validate both:
- `Inbound` and
- `Outbound Notifications`, whichever you were using in the past.
  - If you weren't using notifications previously, _no need to validate_!

## Any Questions?
### Switch to Slide #10

Do you have an `LDAP integration`, or `Okta`, `SSO`?

Ok, great.

With your `Developer Instance`, we've generated a `new URL`, and as of right now you do not have an **Okta**
set up for that new URL.
- So, we'll have to use `local credentials` to do your _validation_
- **IF HELP NEEDED**: If you need help setting this up, it is a little out of scope for this upgrade process, but
  I'm more than happy to provide you some documentation on getting it set up!

/////OPTIONAL/////

I recommend doing that during your `Support Week`, we have Day 1 `Kickoff and Guided Tour`.
You complete your `validation` on Day 2, wait until your `Production Instance` has been upgraded before setting
up any **Okta** logins for your `Developer Instance` because it's not going to be something that tells us any
information setting it up.
- It is not helpful in terms of validation, but I can understand wanting to get it setup, and
  it be best to do that while you can leverage the support you'll have for those _first five days_
  after you have upgraded.

//////////////////

For your `Production Instance`, there is **no URL change**, so **Okta** is already setup for that `Production URL` and
there will be no change there
- It will continue to function as it has been.

We ask of course during this upgrade process, until we have that `Best Practices` sesssion,
please be sure that whether its in the `Developer Instance` or `Production Instance` that there is
no _actual configuration_ being done. We want to stay away from _configuration_ during this time.
You'll be still creating records, capturing data, and performing your validations on the `Developer Instance`,
but we ask in both instances that we do not actually do any `Development` work during this process.

**Any questions so far?**

/////OPTIONAL/////

Because you have familiarity with Update Sets, not worried once on Prod with a sys-admin that has some
general SN background. Is there a particular day that works best for you?

//////////////////

### Future Sys-Admins (Slides #12 + #13)
These next 2 slides will be talking about some of the _differences_ between an instance that is upgraded
from `Express to Enterprise`, and one that is freshly spun out of the box as an `Enterprise Instance`.
- _Functionality wise_, they have all the same functionality, the purpose of these slides is just to:
  - View the entire `Express to Enterprise` Upgrade Process
  - To enable the carryover of your `Express` functionality, configuration, and data
    - And do it in a way that is `smooth` and `non-destructive` to your `end-users` and `fufillers`,
    - To show that we have _some differences_ under the hood.
- This is something that, if you're working with a ServiceNow developer that may have _years of experience_
  with the `Enterprise` platform, but sometimes the _more experience_ that a ServiceNow Developer may have
  with `Enterprise`, the less experience they have with `Express`, so it's important to share this information
  with them so they're not confused or surprised when they look at your upgraded instances and see these
  differences under the hood.

**What are those differences?**

First and foremost, for your `end-users` and `fufillers` they are going to experience the same functionality.
It will take a **VERY** observant `end-user` or `fufiller` to really notice that there's been
a difference.
#### Slides #14 and #15 highlight the visual differences
- To show you _what I mean_, here's a snapshot of `Admin View` in an `Express Instance`, and here's the same
  instance after it's been `Upgraded to Enterprise`.
- Someone who is **super observant** may notice that the size of the logo and banner are slightly smaller
  in `Enterprise`, and there is `slightly different shadowing` on the tiles in the dashboard.
- Again, there wil be _very little visual difference_ between the two instances.

As a `System Admin`, you'll see once we're in your `instance` that there are a lot of _differences_ in your new
`instance`.
1. You'll see there are way more options, more applications, available to you in `Enterprise` versus
   what was available in `Express`. Don't feel overwhelmed as that is a common feeling,
   you are not expected to know every single application inside and out.
  - ((There are very, very few ServiceNow developers that know all these applications at an expert level.))

### Plugins (Slide #13)
To get into _little more detail_ on what those differences are, one of them is that there are a number of `Plugins`.

Are you familiar with the concept of `Plugins`?
- You may have seen them before
  - They are pretty quick and easy ways activate a whole set of features
  - Some plugins are free, and some do have a cost associated with them.
- Once _activated_, they cannot be **deactivated**.
- With a freshly spun up instance, there are a number of plugins that are _activated by default_.
  - However, _in your particular case_, because we are upgrading your `Express Instance` to `Enterprise`,
    there are going to be a _number of plugins_ that would have been activated in a freshly
    spun up instance that are not _currently_ activated.
  - They're there, you can activate them if you ever want to, but _by default_ they are de-activated.

There is a list of _these Plugins_ in this `Upgrade Guide`, which I also included when I reached out to you
via the HI Service Portal.
- I strongly recommend that you take a look and read through this upgrade guide
  - It has a lot of helpful information in there, including this _list of plugins_ (about 30) that
    will be inactive _in your instance by default_.
  - We also strongly recommend that you activate these plugins one by one, instead of all at once,
    so you can kind of see what the `differences` are and **ensure** your instance will function the
    way you intend it to
- Of course, if you're working with a Service Partner, they may be comfortable doing it differently,
  but our recommendation is activating these new plugins one-by-one, and only as-needed.

## Any questions?

Again, once plugins are `active`, they cannot be _de-activated_.
- The upgrade guide shows which plugins will have a fee associated with them.
  - If you have any doubt about costs associated with plugins, please reach out to your `Sales Rep`,
    as they will have that information for you most accurate and sooner than anyone else.
- Sometimes if there is a `fee` associated with a plugin, you may have already paid that fee as a
  part of a bundle or something else, you just want to **_confirm_** that again with your `Sales Rep`.

Some other differences are that some modules will retain their `Express` name, rather than adopt
their `Enterprise` name.
**Example**:
- In `Express`, we have the module `Catalog Items` under our `Service Catalog Application`
- In Enterprise, the module `Catalog Items` is by default called `Maintain Items`, but in
  your _upgraded instance_ the naming **does NOT change**.
  - This may confuse a `system admin` who does not have prior exprience with `Express` instances,
    but they still should be able to find many of the modules pretty quickly.

_Another difference_ is **ACLs**
- How we control _access_ to certain areas of the `instance`
  - Whether it be `fields` and the `data` contained inside of those fields
  - Or even entire `tables`
- Those **ACLs** in your instance will look a little different than from a freshly-spun-up `Enterprise` instance,
  again we want to retain that `Express` experience so that your `fufillers` and `end-users` have as smooth
  of a transition to `Enterprise` as possible.
- Likewise, we're carrying over _Express_ features and those continue to be what your instance runs on,
  instead of just jumping straight into `Enterprise`, as there is some setup required, which we'll be
  touching on later today.

Your instance will still be running on **Execution Plans** and **Approval Rules**, which are unique to `Express`
(at least Approval Rules are)
- But now you have that option
  - When you are at a _pace_ that is appropriate for you (no pressure from a particular timeline),
    you can start shutting down _Execution Plans_ and _Approval Rules_ and start shifting over to _Workflows_ instead.

**Do you currently have items in your Service Catalog, and are you currently using a Service Catalog at all?**

yes.

**Ok, that's probably somnething you'll want to take a look at with your `Service Partner`.**
- Especially because sometimes in `Express` where it makes sense to create what's called a
  `Record Producer`, it's not necessarily the case in `Enterprise`.
  - You'll want to have the _review with them_, where they can come in and say "Oh, well you might be
    better off with an _Order Guide_" for example, depending on the situation.
- Revisiting what your original business goals were can be very helpful, there are so many limitations
  that `Express` imposes upon us whether that's through the `Service Catalog` or the `Change Form`
  (that's another big area), and we often _compromise_ on our `requirements` to make it work,
  so now is a _great opportunity_ to _revisit_ these things!
- With your Service Partner or just yourself too, to ensure whatever you're **building out** will give you the
  full functionality available to you with the `Enterprise` platform and set you up for _long-term success_
  down the road.

### Slide #16 for `Express to ITSM Upgrade Guide` Link
We also have some _documentation_ too provided by `ServiceNow` where they cover the _Express to ITSM Upgrade_
through this guide here, so I do recommend that you take a look at this and share this with your
`Service Partner` (if you end up utilizing one).

**Do you have any questions on anything that we've covered so far?**

**We're almost done with this portion of the presentation!**

### Contacting Remote Services ()
Some basic info here:
- The Remote Services Department is open _Monday through Friday_, 9-5
- 9-5 can get a little blurry working across _multiple time zones_, but the idea being that we are
  working 8 hours a day.
  - If it's a _really urgent emergency_, there is the _HI Service Portal_, there is the **request
    escalation button** on your ticket, but by and large there may be a little time between when you
    reach out to us and when we're able to respond.
  - I am aware of what `stage` you're at in the process, and knowing that you're entering the
    `Validation Process`, I am going to be keeping a _closer eye_ on your ticket than I would be otherwise.

Please be sure if you're `reaching out to me` to get in contact, that it's either through the _HI Service Portal_
or by replying to one of the notifications generated from the tickets within the _HI Service Portal_.
- If you try to reach me by _email_, it most likely will _NOT be successful_ unfortunately as I
  am constantly receiving a lot of automated emails and things easily get lost in there versus
  when I go into `HI` and am actively monitoring the tickets myself.
- The _other reason_ is because we want these tickets to have as many conversations on them
  as possible as a record of truth, which can then be referred to later on
  - In the case down the road you create an `Incident` and that `Incident` is in some way tied to
    your upgrade, there are records of everything that had happened throughout that upgrade process.

**Any questions?**

You may have seen a `Change Record` that was created.
- Again, don't reach out to me on that **Change Record** as I won't see it.
- Likewise, be sure if possible to _reach out to me first_ if you run into anything unexpected
  during the `validation process`
  - It could just be `a knowledge transfer` issue, it could be something very simple like ensuring the _proper
    role_ is granted to a `user`, or it could be something more complex that requires an
    incident to be created.
  - If that's the case, I would go ahead and create that `incident` for you.
  - That way, I _personally_ can assure that it's getting the proper attention for being an `Upgraded Incident`
    that it should have.

If at any point you feel in any way `confused`, `uncomfortable`, anything less than `100% Satisfied or
Comfortable`, **please let me know**.
- I am more than happy to:
  - Adjust my _approach_
  - Hop on a _quick call_
  - Change how I'm doing things to ensure that you know what is going on and are on the same page with me.
- If for _any reason_ that you're not comfortable reaching out to me, you can always reach out to my manager
  `Juliet Acuff @ servicenow.com`, I would just ask that you copy remoteservices@servicenow.com on that
  communication as well

We do have a _customer feedback program_.
- You should get a survey a few weeks after your upgrade process has been complete, and we do like
  to hear good news as much as room for improvement!
  - I point that out because _sometimes_ there are calls to `change things`, and if we hear things where
    customers _like how we approach a certain aspect_ of the process, sometimes those comments are
    just as `valuable` as when we do need to go ahead and change something.

**Any questions on anything we've covered so far in this presentation?**
- Go over scheduling again, when they will be offline.

For this next portion, I am going to stop sharing my screen, and turn it over to you.
- I will be sending you your `Dev Instance URL` in the meeting's chat, and I ask that you navigate to
  that URL and share your screen so we can begin the second portion of our call today.
