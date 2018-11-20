# ServiceNow Fundamentals - Jakarta
## Module 01: User Interface and Navigation
## Section 1.1: ServiceNow Overview

![Section Summary](https://cl.ly/1W2j333F2S26/Image%202018-06-06%20at%203.20.52%20PM.png)

**Section Contents**
- What is ServiceNow?
- Cloud Infrastructure
- Multi-Instance Software Stack
- Key Platform UI Components
  - Content Frame
  - Banner Frame
  - Application Manager
- Mobile Access
- Product Documentation

## What is ServiceNow?
**ServiceNow** is a cloud-based platform deployed in a browser that contains
applications and data that can vary by instance and user, automating common
business processes

- A leader in _Enterprise Service Management_ (ESM)
- Provides `modern`, `easy-to-use`, `service management` in the **cloud**,
  allowing your organization to:
  - Automate manual _repetitive_ setup tasks
  - Manage your `core IT processes`
  - Standardize `Service Delivery`
  - Focus on your _core business_, not just ITSM infrastructure


**ServiceNow** provides all of this to users from a `configurable` _web-based_
interface, built on top of a _flexible_ table schema
- The `applications` you run on the `platform` use a **single system of record**,
  and a `common data model` to consolidate your organization's business processes.
- Provides a **Platform as a Service (PaaS)**, a cloud-based computing model that
  provides the infrastructure needed to:
  - Develop applications
  - Run applications
  - Manage applicaions


Another advantage to this `single system` is that you can leverage it to build
your own _custom applications_


It is _not limited_ to a specific department or function, but encompasses the
`entire enterprise`



## What is the ServiceNow Instance?
An **instance** is a `single implementation` of the **ServiceNow platform**
- Independent, changeable, and highly _configurable_
- _Not shared_ with other ServiceNow customers (`single-tenant`)
- Each `instance` has _applications_
- Each `instance` has _customer data_ that can be exchanged between `instances`
- `Upgrades` are made on `individual instances`


An instance is _located_ (**hosted**) in one of the **ServiceNow Data Centers**
around the world
- For a _very, very small percentage_ of our customers, an instance can be implemented
  **onsite** at the customer's location
- Each `ServiceNow instance` has a _unique URL_ that uses a format similar to:
  - EX: `https://<instance name>.service-now.com/`


**ServiceNow** utilizes an `advanced`, `multi-instance`, `single-tenant` architecture
as the _default offering_ for customers
- An `instance` features an **individually isolated database** containing:
  - Data
  - Applications
  - Customizations


The **ServiceNow `multi-instance` architecture**, organized in an `instance stack`,
provides these _distinct advantages:_
- The `multi-instance architecture` allows **ServiceNow** to perform actions on
  `individual customer instances` such as:
  - Performing an **upgrade** on a schedule that fits the _compliance requirements_
    and _needs_ of your `enterprise`
- `Data` is _truly isolated_ in their own databases
  - Making `Hardware` and `Software` maintenance on these unique `customer instances`
    far easier to perform
  - Issues can be resolved on a `customer-by-customer` basis


Each `customer organization` recieves **two instances of ServiceNow**
1. Production
2. Sub-Production

- They have the ability to obtain _additional **Sub-Production** instances_ to be
  used for:
  - User Acceptance Testing (UAT)
  - Review
  - Development
  - Quality Assurance (QA)


![Key Platform UI Components](https://raw.githubusercontent.com/wbounas/acorio-notes/master/book-notes/SNOW-Fundamentals-Jakarta-Ebook/images/module-01/ui-components.png)

## Key Platform UI Components
The User Interface (UI) is the main way to interact with `applications` and
`information` in a `ServiceNow instance`

**Notable Features:**
- Real-time form updates
- User Presence
- An Application Navigator designed with `tabs` for favorites and history
- Enhanced `activity streams`

The `ServiceNow UI` is divided into 3 areas:
1. **Banner Frame:** highlights important tools and settings that apply to your instance
2. **Application Navigator:** provides links to all `application menus` and `modules`,
			    based on your _permissions_
  - Based on your _assigned roles_
  - May be `expanded` or `collapsed`
3. **Content Frame:** display _information_ depending on where you navigate within the
   platform, such as:
  - Lists
  - Forms
  - Dashboards
  - Knowledge Bases
  - Service Catalogs


  **NOTE:** this also impacts how the `information` is _visually represented_
  **NOTE:** the **position** of these `compoents` on your screen may vary _depending_
	  on your _region_

## __Content Frame: Common Types of Interfaces__

![Content Frame: Common Types of Interfaces](https://cl.ly/2839273W0l1e/Image%202018-06-06%20at%2010.20.31%20AM.png)

- **Homepage:** when a user logs into an instance, the `default homepage` defined
  _for their role_ appears **unless** the user switched to another homepage, OR
  has _set a **dashboard**_ to appear

  **Homepages** consist of:
  - Navigational Elements
  - Functional Controls
  - Platform Information

All users with a role can use the **Add Content** link on the homepage to _customize_
the homepage and `display important changes` and `emergency information` to other
users

- **List:** view `data records` as a list
  - Display records from a `data table`
  - Allow you to edit the `record information` using the `List Editor` functionality

- **Form:** view `individual data records` as a **form**
  - Data is _typically entered_ into ServiceNow through `forms`

- **Dashboard:** enable you to display:
  - Multiple perfrmance Analytics
  - Reporting
  - Other `widgets` on a single screen

- **Map:** display **ServiceNow** data `graphically` on a Google map
  - Drill-down into a map to view `specific data points`

- **Timeline:** used to track `tasks` or `projects`

## __Banner Frame__
![Banner Frame](https://cl.ly/1B082s0b130Z/Image%202018-06-06%20at%201.02.41%20PM.png)
The `Banner Frame` runs across the top of every page and contains `global
navigation controls` and `several key functionalities and features:`
- Your logo in the top LH corner
  - Also navigates you back to your homepage
- Information about the `logged-in user:`
  - Click the down arrow to the right of the user name to
    view the user profile or log out
- Click the `magnifying glass` to expand the **Global Search toolbar** and use this
  to search across _all data_ in ServiceNow, such as:
  - A `keyword`
  - Record number
  - More!
- _Toggle_ the `Connect Sidebar`
  - Used to _communicate_ with other users in **real-time**
- Get _help_, including `Product Documentation` and new features
- _Personalize_ your settings


**NOTE:** with __additional rights__, a user may see `Impersonate User` and
`Elevate Roles` as additional options from the `User Menu`
- These features are _useful_ for testing and visibility

## Application Navigator
![Application Navigator](https://cl.ly/0D2p2X36190s/Image%202018-06-06%20at%201.20.30%20PM.png)

**Applications** are a group of `modules` (or _pages_) that provide `related
information and functionality` in an `instance`
- **Modules** can contain:
  - Links to a `new record`
  - Lists of records with varying filters applied
  - Special visual tools


**For example**: the `Incident` application contains modues for _creating_ and _viewing_
	     `incidents`, while the `Configuration` application contains modules for
	     _changing_ and _accessing_ **servers, databases,** and **networks**


## Application Navigator: _Filtering_
![Application Navigator: Filtering](https://cl.ly/0h0u3g0j4210/Image%202018-06-06%20at%201.32.56%20PM.png)

The **Application Navigator** provides access to `all applications` and the `modules`
they contain
- Enables users to _quickly_ find `information` and `services`

To view `all applications` within the _navigator_, ensure that **All Applications**
icon is selected at the **top LH** of the `navigator`

**TIP:** `double-click` the **All Applications** icon to `expand` and/or `collapse`
_all applications_
- Click any `application` to _expand_ or _collapse_ all of its `modules`

To quickly search throughout your `application navigator` to view a particular
_application_ or _module_, use the **Filter Navigator**
- The **Filter Navigator** is located at the _top_ of the **Application Navigator**

**As soon as you begin typing,** the _Application Navigator_ displays only
`applications` and/or `modules` matching your <keyword>
- If you type "Incident", you will view the `Incident` application and a list
  of _all_ its modules, as well as any modules containing the word "Incident"
  within other applications, such as **Service Desk > Incidents**


## Application Navigator: _Favorites_ and _History_
![Application Navigator: Favorites and History](https://cl.ly/010H0L291e2C/Image%202018-06-06%20at%202.07.02%20PM.png)

**Favorites:** includes `application menus` and `modules` whcih you may wish to
             access quickly and often
             - Will also display in the `Application Navigator` even when a filter
               is applied, so long as the `Favorite` _matches_ the `search term`

**Your History:** contains a scrolling list of your recent history within ServiceNow
- **Example:** will display `forms` you were filling out, `lists` you were
               searching on
- Simply click on an `item` to open any _recent activity_ in your `content frame`
  - Some `content types` are **not tracked**, including `UI Pages` and other
    non-standard interfaces

## Mobile Access
![Mobile Access](https://cl.ly/010H0L291e2C/Image%202018-06-06%20at%202.07.02%20PM.png)

In addition to accessing a `SN Instance` from a laptop or desktop computer,
`SN` also supports the following _technologies:_
- **Smartphone:** the _smartphone interface_ supports many of the `features` found in the
  standard `desktop/laptop browser interface`, incuding:
  - Lists
  - Forms
  - Favorite/Shortcut Management
  - Filtering
- There are _no **special configurations**_ needed for the `iPhone` or `Android`
  devices
  - The `smartphone interface` uses familiar, _industry-standard_ techniques
    for perforing most actions (`Responsive Design`)

- **Tablet:** The `SN Instance` automatically detects the tablet and _redirects_
  the user to the _desktop interface_

- **Apple Watch:** features include:
  - Notifications
  - Favorites
  - Record Monitoring
  - Chat Messaging
  - Dashboard Charts
  - Record Interaction via _Canned Responses_
  - Voice to Text (Siri)


**NOTE:** Depending on how you access `SN`, the **UI** and **features** may _vary_


## Documentation: Docs and Community
![Documentation: Docs and Community](https://cl.ly/261V1L3o3F1w/Image%202018-06-06%20at%202.27.00%20PM.png)

**docs.servicenow.com** is the `official documentation resource` for `ServiceNow`, with
_content_ provided by `ServiceNow`
- From _features_ to _functionality_ (and even _release notes_), this resource should
  have all of the information needed to get the **most** out of the platform


**community.servicenow.com** is _similar_ to the **Docs** website
- Provides useful information about the `ServiceNow platform`
  - **HOWEVER:** the `Community` really _excels_ by bringing together
    actual `ServiceNow` users to:
    - Collaborate
    - Share
    - Produce ideas, content, and answers to questions you may have
- Great resource to _learn from users_ with `real-life experience` on the platform!

