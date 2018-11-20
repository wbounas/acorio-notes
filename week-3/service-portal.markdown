# Basic Portal Development (CMC)
Focusing on low-code aspect of basic portal development
- Reflections on Customer Service and Web Design
- The user-friendly User Interface for inexperienced SN end-users

*NOTE*: Content Management System (CMS) is the /OLD/ version of the more modern Service Portal

## The Big Picture / How the Portal Fits In
- The _Service Portal_ provides an *alternative user experience* to the standard platform UI
- It is _easy to configure, customize, and textend_, similar to what users are used to in other consumer products

*NOTE*: Service Portal /WILL NOT/ have *feature parity* with the platform UI
- The goal is to have a very refined user experience, and it will take tie to rethink and redisgn what we have accumulated as features over the past decade in the platform
  - CORE Apps (Incident, Service Catalog, Knowledge, Approvals (lite))
  - Custom apps (OOB widgets handle mostly CORE Apps, might have to customize for custom task-types)
  - CMS to Service Portal (many clients are moving to Service Portal, as it provides a way more refined UX, not always a straight-forward conversion)
  - Portal was designed and built by ServiceNow LABS team: Web Designers + Developers

### Feature Disparity
Incident
  - End-user is _unable_ to resolve their own incidents OOB in Portal
  - Acorio has a widget for that
Service Catalog
  - End users are unable to cancel their own REQ/RITMs
My Ticket / Requesuts
  - Only able to see currently active tickets
  - Unable to see anything in the past
  - Unable to filter at all
Approvals
  - Requiring comments on rejection, etc.

_*2 Basic Personas for ServiceNow*_
1. Non-roled User (End User, Customer) PRIMARY PERSONA
  - END USER Service Catalog
  - 'Report Issues' in the Service Portal
  - All self-serive Knowledge access
2. Roled user (Fulfiller) NOT PRIMARY PORTAL PERSONA
  - ALL Service Catalog categories and items
  - 'Report Issues' in the Service Portal
  - Access Knowledge is default UI

### Best Practices for Useability & Meaningful Content
_All Content Should:_
- Reflect your organiation's *goals and user's needs*
- Understand how your *users think and speak* about a subject
- *Communicate* to people in a way that they understand
- Be *useful* by being purposeful in the content that you include, *omit the needless*
- Be *consistent* by following style guides, both for language and design, which helps people understand and learn
- Have your information be accessible by making sure that users can *find content* both internally and through navigation, SEO is key!
  - Users want to search!
- Help define the *requirements* for the overall site, since content hsould drive desig, structure, etc.


_*Glossary*_
Portal: Buzzword for "Site". You can have as many unique portals as you would like. The portal is a group of pages linked by page IDs
Themes: Define the look and feel of the whole portal but can be overridden by pretty much any other style configuration
Pages: Control where and how you store Portal content. Pages don't have a defined relationship to portal records, they just exist
Widgets: Almost everything in Service Portal is a widget. You can use HTML teplates, CSS, client scripts, server scripts, and any JavaScript dependencies to define what a widget does
Widget Instance: When you add a widget to a page using the Service Portal Designer, it creates a widget instance. A widget instance is a reference to a widget that ocntains a location, properties, and CSS specific to that instance
Taking Ownership: When you clone a widget, this means any changes you make to that widget, you are owning the changes you are making. Ensuring scalability and compatiblity in future versions of ServiceNow





Header and Footer are consistent on EVERY page of the Portal you are on
- That's why they are defined on the `Theme` form record





