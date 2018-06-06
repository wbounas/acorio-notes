# ServiceNow Fundamentals - Jakarta
## Module 01: User Interface and Navigation
## Section 1.1: ServiceNow Overview

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

### What is ServiceNow?
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



### What is the ServiceNow Instance?
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


![Key Platform UI Components](/images/ui-components.png)

### Key Platform UI Components
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
