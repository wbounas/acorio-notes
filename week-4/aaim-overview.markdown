# AAIM Overview (Tom Sobczak)
Acorio Accelerated Implementation Methodology

1. *Initiate*
- Kickoff Meeting
- Methodology Overview
- High0level Planning

2. *Define*
- Workshops
- Harvest Requirements
- Guidance
- Adjustmnets
- Story Grooming

3. *Plan*
- Architecture
- Story Approval
- Sprint Planning
- Detailed Planning

4. *Build*
- Develop and Configure


**Initiate Phase**: Alignment
- Sales Handover to Delivery
- PM & EM Introductions to Client
- Internal Kickoff (PLT)
  - Internal team discusses the project
- Joint Kickoff (with client)
- Story Grooming
  - Ensuring that this is on the same page with the customer

_Define Phase_: Discover and uncover!
- Workshop Prep
- Workshop
  - Whatever we are doing in the SOW for the customer, this is what we focus on

**Define Phase** - _Workshop Preparation_
What to Expect
Activities
- Exchange of Information
- Review of any documentation you have
- Questions as documents are reviewed
- Identify the right players
  - Try to identify the right people *up front* so that they are in the right workshops
    from the beginning

Inputs (Client)
- Process Docs
- Process Workflows
- Requirements or use cases
- Process Charter
- Business Case or justification

Outputs (Acorio)
- Agenda
- Initial Questions
- Next Steps (2-3 weeks)

**Define Phase** - _Workshops_
What to expect
Activities
- Our process leadesr will guide you through the workshop process with questions that will branch as discovery ensues
- Walk through your current process
- Sketch out proposed process
- Shar eindustry practices
- Provide Demos
- We'll scribe and have a parking lot

Inputs
- Agenda
- Workshop decks
- Process Docs (Client)
- Existing Demos (Client)
- NOW Demos (Client)

Outputs
- Daily wrap-up
- Parking Lot items (All)
- Requirements Notes (Acorio)
- Workflows (Acorio)
- (Potential) User Stories (Acorio)

*NOTE*: Trying to do the workshops right before the build, so that everything is fresh


**Define Phase** - Story Writing
What to Expect
Activities
- Acrio BPC will write initial user stories
- Acorio BPC will write initial Acceptance Criteria
- Process owners should participate
- Process owners shold enhance and approve acceptance criteria

Inputs
- Any Process Docs (Client)
- Workshop output (All)
- Additional conversations (All)

Outputs
- Draft of User Stories (Acorio)
- Acceptance Criteria (Acorio)

**Define Phase** - _Story Grooming_
What to Expect
Activities
- Acorio will document the technical approach for each story
- Additional conversations/meetings to clarify behavior
- Guidance from Acorio on industry practices
- Improving and finalizing Acceptance Criteria
- Sizing of stories -- effort estimate to implement

Inputs
- Draft User Stories (Acorio)

Outputs
- Backlog of Stories
- Improved Acceptance Criteria (Client)

**Story Overview**
- Simple template to capture features and business value
- A story will contain acceptance criteria
- A story describes the functionality that will be built
- Stories will be placed in a backlog
- The high-values stories should be prioritized and developed first
- As the backlog will continue to grow, it's likely some stories will be addressed
  in a future release

**Story Overview: Best Practices**
- Stories kept in Client's Production environment (if client has PPM); otherwise 
  maintained in sub-prod environment
- Whichever application the story relates to will also be the Product or Theme on the story (ie. incident, problem, change)
- Short description summarizes the story (ie Short Description - Mandatory Fields)
- Do not assign a story to a Spring. The EM and Technical Team will do that!

If a story is incomplete, it is set to _draft_
- If a story needs more info from Client, the story is set to Draft and Block the 
  story with a _DETAILED_ description of what additional info is needed in the Blocked 
  Reason field
- Blcoked stories belonging to the customer wil be assigned to them in the tool
- Any relevent documents are attached to the story (workflows, screenshots, wireframes, layouts, etc.)
Acorio will be writing the initial acceptance criteria and the *Client PO* will finalize and approve during the Story Roadblock

`As a <role>, I want a <feature> so that <I get this business value>`

**Story Writing** - _Discover_
- Discovery sessions (Workshops) are used to build our initial product backlog
  - The output of the discovery sessions is a first draft of stories
- In some cases, these stories are summarized in a Req document
- Ongoing clarifications
- Stories may or may not be fully fleshed out after discover (A story is an ongoing, iterative process)

**Story Writing** - _Structure_
A good story description should identify:
- The role of the user in the system
- The need expressed by the user
- The benefit to the stake holders, the `business value`

**Stories should be told, not written**
- Stories are not lightweight requirements documents, but a starting point to a conversation
- No requirement can ever be captured perfectly in writing, and even if it were, it would 
  miss the benefits of a discussion between the business and delivery team that often leads 
  to questions, options, and ideas (standard or industry practice)
**Stories should focus on the perspective of the user**
- Be careful of the "generic user" and instead describe a user role that can guide a 
  discussion of how the functionality will be used

A well-written story should be able to stand on nit's own, small enough to 
understand, and test-able!
- A developer without prior experieence on the project should be able to go in 
  and implement a story

**Story Writing: Acceptance Criteria - Standard Practices**
Initial Acceptance criteria will be entered by the Acorio BPC
- This is the _most crucial part_ of the story

Roles - The Process Owner (PO)
- Someone must be the _single_ point of contact
- Work with BA's as *proxy* POs (so they can do their day-job)
- **Prioritize** every single story
- Helps getting stories to _complete_
- They _own_ the Stories and Acceptance Criteria and usually need to help _Unblock_ stories

**Planning**
Planning is **just-in-time**, **just-enough**, and done **frequently** to adjust to reality
- Release Planning, Sprint Planning, Daily _Huddle_, Sprint **Review**

**Sprinting**
- 2-week sprints eem to work the best
- Continuous testing during all sprints is _key_
- **Grooming** sessions to clarify and improve
- Technical sessions, Knowedge Transfer and _code_ review
- Sprint _review_
- If Knowledge Transfer sessions apply to your project, this should be happening during sprints


**Story Points**: "best estimate" of what it will take in hours to
- Work with the PO to groom and refine Acceptance Criteria
- Configure and/or build scripts
- Unit test the story
- Fix any story defects

Typically, if a story is **more than 8 hours**, this may be a sign this is an _Epic_, which needs to be further unpacked into multiple stories for independence and testing
- If a story is an out-of-box (OOB) feature of ServiceNow, the story would receive -1- point
- Acceptance Criteria will change as `Story Points` get more or less








