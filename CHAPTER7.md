# Acceleration and Management Tools

time

deliver on time

## Event Storming

rapid design technique with both Domain Experts and developers

focus on business and business process and not nouns and data

ditch UML

use sticky notes

maybe use [Draw IO](https://www.draw.io/) over a hangout?

- everyone gets a pad of sticky notes and contributes to the Ubiquitous Language
- focus on events and business process rather than classes and database
- visual
- fast and cheap
- breakthroughs in understanding
- everybody learns something
- identify problems and get on same page
- big picture and design level modelling
- can have multiple sessions across multiple days eg 2 hours per day

things you will need
- right people (Domain experts and developers) in same room (hangouts?)
- open mind free of judgment, try not to be too correct too soon
- lots of different color stickies, square, extra sticky
- black marker pen per person
- wide wall where can model, table, or floor
- roll of paper

steps
1) Storm out the business process by creating a series of Domain Events on sticky notes. 
The most popular color to use for Domain Events is orange.
  - create domain events first emphasize on business process not data and structure
  - write name of event on sticky (past tense)
  - place stickies in order of time left to right, worry about the `when` part later
  - parallel can be represented vertical space
  - problem spots label with purple/red and text
  - outcome of event is `Process` which needs run
    - lilac sticky and line with arrow head from event to process
    
keep around, next day add missing concepts or throw out superficial ones

2) create commands that cause each event
  - light blue sticky
  - place left of event so they are in pairs
  - user role that performs action on yellow sticky
  - commands can cause `Process` to be run
    - lilac sticky and line with arrow head from command to process
  - move left to right in time
  - address discovery of new events
  - command can cause multiple events

3) Associate the Entity/Aggregate on which the Command is executed and 
that produces the Domain Event outcome
  - don't use word Aggregate, use Entity or Data
    - pale yellow sticky for Aggregates
  - place behind and above command/event pair
  - repeat aggregates, don't reorganize and group by aggregate, focus on business process
  - address new Domain Events; can break big aggregate into managed `Process` (lilac)
  
overlap of event storming and event sourcing
  
4) Draw boundary lines and arrows to show flow
  - boundaries found under
    - departmental divisions
    - conflicting definition of same term
    - concept important but not part of core domain
  - solid lines for `Bounded Contexts` and dashed lines for `Subdomains`
    - can use pink stickies to denote bounded context before drawing lines
  - draw lines with arrowheads between bounded contexts to show direction of events flowing 
  between bounded contexts

5) Identify views user need to carry out their actions and import roles of various users
  - UI View - green sticky
  - User Role - bright yellow sticky 

probably should make sure nobody is color blind? 
otherwise a lot of meaning is lost, maybe write a stereotype on the sticky eg `<<command>>`
   
steps 4 and 5 are extras
  
### Other Tools
  
avoid ceremony  
  
`Specification by Example` book by Gojko Adzic
  
`Impact Mapping` also defined by Gojko Adzic to make sure it's a core domain
  
`User Story Mapping` by Jeff Patton to focus on core domain and features should be investing in
 
## Managing DDD on an Agile Project
    
### First Things First
    
hire good people

### Use SWOT Analysis

- strengths
- weaknesses
- opportunities
- threats

quadrant with stickies in each

plan what to do about them

### Modeling Spikes and Modeling Debt

modeling spike early in project - timeboxed

expect modeling spike every iteration

retrospective create task to update model based on what you learned and add to Kanban queue

### Identifying Tasks and Estimating Effort

estimate based on type

Easy, Moderate, Complex (analogous to Tee-shirt sizes Small, Medium, Large )

#### A Comment on Accuracy

20% accuracy on long term estimates

much better on short term estimates


## Timeboxed Modeling

don't make board too complex

combine Commands and Events for a single Aggregate into a single Task

### How to Implement

Concrete Scenarios and Event Storming

- quick event storming
- partner with Domain Expert to refine concrete scenario(s)
- create a concrete set of acceptance tests
- create components which allow tests/specs to execute until do what Domain Expert expects
- iteration will cause you to consider other scenarios, 
create additional tests/specifications, 
and refine existing and create new components

### Interacting with Domain Experts

include Domain Experts
- when Event Storming
- discussion and creation of model scenarios
- review tests and verify model correctness
- refine the Ubiquitous Language and its Aggregate names, Commands, and Domain Events