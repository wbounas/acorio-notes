# Best Practice Shadowing Notes (Max Dore)
## `Medical Solutions` Best Practices Session 06/11/18

**Customer Question:** _Are we driving?_

**Answer:** Like last session, you'll be logging on. We'll be using dev as well as prod, but we'll
            be diving into some of the features that come with enterprise
- This session is typically shorter, they have _less material_, but it's more _important_



## Overall Goal Today
**Creating and retrieving update sets**
- See how `system clones` work
  - How to create a `system clone`
- `Upgrades` and `Releases`
- Touch on `plugins`
  - Their _benefits_ and
  - Best _practices_

**When you are ready, go ahead and share your screen**
- We'll start with the `development instance` today

----------------------
## IF THEY HAVE `SSO`:
Put the link to the `dev instance` in the `WebEx` chat
- So they can just easily navigate to their `Dev Environment`

`We will be using the remote services user that we used last time`
- **Do you still have the credentials?**
  - _I can provide if necessary_

----------------------


## Update Sets: Development Environment
We'll go over the _basics_ of `creating` and `retrieving` __**update sets**__
in the beginning of this session

Go ahead and type `Update Set` in the `Filter Navigator`
- We're going to go to the `Local Update Sets`

### _"So, what is an update set?"_
An `Update Set` is how we capture groups of `customizations` and move them from one `instance` to another
- Always from `development` to `production`
- There is a `set of processes` when moving these **update sets**
  - There are things that they **DO** and **DON'T** capture
  - They **DO** capture any `configurations` or `customizations`
    - Such as:
      - List Views
      - Changes to Forms
      - UI policies
      - Biz rules
  - They **DO NOT** capture:
    - `Scheduled Jobs`
    - `Reports`
    - `Data` (like _incident records_, _problem records_)
    - The reason being that we don't want _test records_ (like `incidents`) being pushed up to prod
      - like a safety net so you don't see those test records in prod

What we have in front of us is the **default record**
- You _NEVER_ want to delete this
- All the `customizations` you don't want in an **update set**, you'll have here
  - They will remain _untouched_

**Today we are:**
1. Creating an `update set`
2. Creating a `customization`
3. Complete the update set
4. Move it to production and finally,
5. See the change reflected in your `production environment!`
  - When you were on `Express`, you only had the `1 instance`, where you had to
    do all `development` and `testing`
    - A lot of risk involved with this
  - Now, with `2 instances`, you can _test and develop here_, and **move over** after
    you are confident there will be _no issues_

### Update Set Naming Convention
**We highly encourage that you come up with a naming convention**
Typically, we see: Date_name_application/module you're working with

`EX:` **6-11-2018_alicia_notifications**
- This is because the `configuration` we'll make, we're changing a __specific module__
  and __application__ in your `Prod Instance`
- There are **3 state fields**
  - When an `Update Set` is being worked on, it is considered `In Progress`
  - **ONLY** When you are ready to move to `Prod`, you change this to `Complete`
- When you are in `Prod`, you go and click __retrieve__
  - Any ompleted update sets would be retrieved
- When that is **done**, you would go and change this to `Ignored`
  - This way, the update set will not show up any more
- You have the __parent__ and __release date__
  - This is _really for you_, if you are building out a feature,
    if you have **multiple update sets** that are related to each other
    - You can have `update sets` that are related each other, you can have
      a link between update sets
  - **Release Date** is when you you have an idea in mind about when to bring
    these `Update Sets` into `Production`


Need to Research what is allowed and not allowed (characters that we can use)

# **~11/12 minutes in**

**Short Description:** You want to be descriptive as possible
- `Description` is not really for you to re-read and know, but more so for someone
  else in the future for them to see what the update set was for
  - They will know exactly what's going on in the update set

- click `Submit`
you can see the update set was created

Need to change two things about the UI
- Click gear in the top RH corner
  - Go to the `theme` tab
  - You'll want to choose a different theme, so that your prod and dev instances look different,
    and you don't get confused which environment you are working in
    - you can always change this later
  - Go to the `developer` tab
    - Choose to `Show Update Set Picker in Header`
      - This adds a drop-down to the top banner, where you can select _which update set_ you are working in
        - Go ahead and select the new one
        - At this point, and changes to configuration you make will be recorded in this update set

In the filter navigator, we can go to where we want to add something
- Type in `Application Menu` (select **Application Menus** module)
- Get rid of the breadcrumbs by clicking `All`
- In the `Title` field, we'll type in **System Notification**
- Click in there, and change `Active` to _true_ by checking it, and select `Update` (top RH corner)

**Now you want to go back to the update set to ensure that was recorded properly**
- __Best way__ to do it is to go through the `top RH gear` again, and there is a `Blue I` for the update set
  - That goes right _into the record_
  - Scroll down, we'll be able to see the `update` that we just added (__date and time__)
  - You can click into the **particular update**, and we can see the `code` that will then be _injected_
    into the `production environment` (**HUMOR:** good thing we don't have to type it all out)
- One thing to note: If you scroll to the **bottom**, you can see that the change made was __very small__
  - In this case, because this change was **very small**, say that you made the
    change in the wrong update set
    - With the `Update Set` field, you can change which `update set` these changes are _attributed to_
      - With a __more complicated change__, Best Practice is considered to revert all changes, ensure you
        are in the **proper update set**, and **re-write your changes** in the `correct update set`
        - This is the best way to _guarantee_ that it will all work

# **17 minutes in**

Click back arrow to go back to our `Update Set`
- Change the state of the update set to `Complete`

**Now we are done**
- Made our change
- Update set is closed
- [x] Now we will log into the `Production Instance` (using your `SSO login` if applicable)
----------------------

## Update Sets: Production Environment
Type `Update Set` in the filter navigator
- This time, we'll choose `Update Sources`
  - What we are doing is a one-time setup, establishing the link between your `Production`
    and `Development`
  - Here, click on `New`

`Name:` **`CompanyNameDev`** (<-- template)
- You see the lock box next to URL
  - Click that and copy the URL of the `Development Environment` from
    `https://` all the way to `.com`
- For `username`, you'll put in `remote.services`
- For `password`, you'll put in the _password for that user_
  - **If Applicable:** Once you have `SSO` set up, you can come back here
    and update these __credentials__ accordingly
- For `short description`, you can put in "Development Environment"
- Then we can click `Test Connection`
  - Using this, you can __test your credentials__ to ensure that you can log in

Now we have the link between the two, and you can click on the blue `Retrieve Completed Update Sets`
- This is **very quick** because it is a __small update set__
- If there were any `collisions`, you would be alerted to what the collision is all about
  - This time, you can just click `close`
- Scroll to the bottom to the second tab (`Retrieve Update Set`), and
  you can go into your retrieved update set
  - Important to note here that the `System Notification` is **not yet reflected** in `Production`
    - It's not until you click `commit update set` that those changes are actually reflected
      - Currently still _only in the `Update Set`_
    - If you were to have any `collisions`, you would _have_ to fix those before you could
      commit any changes
    - Then you just want to triple check that those changes were reflected in `Production`
      - Type in `notifications` in the system navigator, and you can see that the change was reflected
    - **Congratulations, first update set!**
      - Any questions???

In Summary, Update Sets are really `moving configurations` from `Development` to `Production`

----------------------

## System Clones
`Purpose:` your `Production` and `Development Environments` are close as possible to each other
- that way, when you move update sets you will not expect much (if any) `merge conflicts` because the
  environments are **so close** to each other
- **Best Practice** is to have a regular schedule for cloning, based on how often you
  are using the `Development Environment`
  - Just make sure to `clone` before making any _development changes_ so that you can be sure
    that you are **developing** and **testing** as if you were working in `Production`
**Any Questions on that Concept?**

One thing people do (We'll hop onto the `Dev Environment` for a second)
- Top `LH`, to the left of the logo, some admins change that to the date of the `last clone`
  that they were working with
 iHRdtype `basic configuration` to the filter navigation, you want the bottom
  one `ui16` and change the value of the `Page Header` field

Type in `system clone` into the filter nav
- First one, `Request Clone`
- Every time you _request a clone_, it goes through `this process`
- `Target instance:` we click the search icon to the right, and we create a
                    login (using `Dev URL`, and remote services login)

For anyone creating clones in the future, they can go in and `add their credentials`
- **They will need to**
  - When submitting a `system clone`, you will be asked again for _credentials_
    and they will have to **match up**

We can now go back into Production (on System Clone Record)

# **26 minutes in**

Let's talk about these 3 `check-marks`
`Exclude Audit` - Exclusive to `Dev Environment`, so that logs don't get overwritten
- You can override these, you have the option
`Exclude Large Data` - might want this, SNOW considers anything larger than 12KB as a large attachment
  - Typically, _any word doc_ is bigger than that
  - Unchecked means a slower process, if you know attachments are larger you want unchecked
`Preserve Theme:` we want this checked so the themes we _just changed_ stay different
  - If you have it unchecked, it will be the same again
`Date and Time:` You have to schedule this clone **at least 4 hours out**
  - EX: If you want it done on Monday at Midnight, you need to schedule before 8pm
  - Schedule for when clone is to take place
`Email upon Completion:` Alerts you via email upon completion of the clone

**Once you hit submit, __which we will not do today__, it will ask for those credentials**


**Any questions?**
- Just want to ensure we have the basics covered

Currently, this would bring everything over to your `Development Instance`
A way to be granular with what is brought over and what is included:
**2 modules to your left**
1. Exclude tables
2. Preserve data

# **29 Minutes In**
With these, you can determine which `tables` are not brought over, and which _data is preserved_
`EX:` You can have HR Data in `Prod` you don't want moved into `Development`, you can
      choose those things here

----------------------

**Those are really the 2 big topics for us today**
1. Update Sets
2. System Clones

----------------------

## Upgrades and Releases
The next topic is about upgrading and releases

**36 minutes in**
in **Express**, `Upgrades` were done FOR YOU
in **Enterprise**, you'll have to go into the `HI Portal` and request any `Upgrades`
- If you'd like, I can show you how to do that
  - Log into the `HI Portal`
  - Go to the left, under `instances`
    - `Manage Instances`
      - You can see your `two instances`, _if upgrades are available_, tells you
        what `version` you're currently on
      - If you click on `Action`, you'll see `Upgrade Instance`
        - Here you're given some __great documentation__ (`Upgrade`, `Release Notes`, `Planning Checklist`)
        - `ServiceNow` makes it as __easy as possible__ for that _transition_
- `Upgrades` are all about new features, while `Patches` support the existing functionality by


Later this year, there will be the `London` release
- It is suggested that you stay within `1 or 2` of the latest release
  - The reason being there is the most `up to date` _documentation_ and _support_ with the most
    __recent upgrades__


There are emails that are sent out about updates, not sure exactly who in your company will
be receiving those emails, but in here you will see all of that documentation
- You can also visit this page to see if there are currently any updates available for your instance



One thing I need to touch upon is Plugins, and we'll go back to the dev environment for that

**Plugins, there are a few things to know**
- Once activated, they cannot be deactivated
  - It's important to know exactly which one you want to work with, what you need, before activating
  - Please check with your sales rep, as some plugins are free, some are not
    - Good idea just to make sure you know what you're getting into

Do you have a case where someone else has gone in and activated random stuff and purhcased something accidently?
`ANSWER:` if you activate all of them, it will dramatically slow down your instance, but
I myself have not heard of someone turning one on before knowing the cost prior to activating it
- Hopefully, partly because it's because we let them know to check in
- We are not trying to trick you into activating plugins
- That part of the cost is not revealed to us, that information is really with the Sales Rep
  as they would have the most up to date information
  - You would just put a ticket into the HI Service Portal
  - If me and my team had that information, we would share that with you

Last thing to mention, I'll double check the date here to make sure you have the right information
- You have until ________ to utilize the 5th ticket
  - If you notice anything in the upgrade with a bug, or something you missed, my team will be able to help
    out
  - After that date, you'd still write a ticket in the HI Service Portal, and another team would be able
    to help you out


Hope you are feeling more and more confident with the Enterprise platform

we can ive you back some of your time today (especially if it's the end of the day)



Making sure you have dates right for prod upgrade (time zone especially)


