# Strategic Design with Bounded Contexts and the Ubiquitous Language

DDD is primarily about modeling a Ubiquitous Language in an explicitly Bounded Context

part of your `problem space`

`solution space`

Bounded Context is where a model is implemented

separate software artifacts for each Bounded Context

context maps in problem space

core domain

ubiquitous language

boxes modelled inside bounded context are concepts

bounded context part of strategic initiative is core domain

core domain distinguishes organization strategically

major line of business

bounded context - language boundaries

multiple teams should not work on a single bounded context

single team can work on 1 or more bounded contexts

team owns source code and database and define official interfaces bounded context must be used

`big ball of mud`

monolith

## Domain Experts and Business Drivers

- Underwriting - Policy
- Claims - Policy
- Inspections - Policy

meaning differs across different insurance business functions

bounded context scopes Policy class

is Policy in all three Contexts and not UnderwritingPolicy, Claims- Policy, or InspectionsPolicy

## Case Study

## Fundamental Design Strategy Needed

one cohesive, collaborative team: Domain Experts and software developers

### Product Owner or Domain Expert?

domain experts - focused on business concerns

product owner - managing and prioritizing backlog

could be same

make sure have true domain expert on team


### Focus on Business Complexity, Not Technical Complexity

reject any tendency to allow documents to rule over conversation

deeper insights about the Core Domain


## Challenge and Unify

scope out things

use ubiquitous language for concepts

collaborative context - discussion defined outside of bounded context

move other concepts not in core domain into other bounded contexts


## Developing a Ubiquitous Language

nouns are important but not only important thing

include only essential elements

### Accelerate Your Discovery

Event storming sessions

set of concrete examples - what components do

english sentences

name persona involved in each scenario

## Putting Scenarios to Work

Specification by example (aka Behavior Driven Development BDD)

```
Scenario:  The product owner commits a backlog item to a sprint
   Given a backlog item that is scheduled for release
   And the product owner of the backlog item
   And a sprint for commitment
   And a quorum of team approval for commitment
   When the product owner commits the backlog item to the sprint
   Then the backlog item is committed to the sprint
   And the backlog item committed event is created
```

can use unit tests although but not as readable

acceptance test kept in source code repo

## What about the long haul?

innovation does not end when maintenance begins

## Architecture

Input Adapter

Application Service

Domain Model

Output Adapter

### Technology-Free Domain Model

- Event-Driven Architecture
- CQRS
- Reactive and Actor Model
- REST
- SOA
- Micro-services
- Cloud computing

micro-service smaller than bounded context

each concept has own micro-service 

eg Product and Backlog Item would be separate micro-services

