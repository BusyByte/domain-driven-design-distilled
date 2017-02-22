# Tactical Design with Aggregates

concepts are likely aggregates in your model

## Why used

value object

### What is an Entity?

entity has an identifier

aggregate is one or more entities where one is the aggregate root

### What is a Value Object?

has no identifier

compared using equivalence

### Broader Meaning of Transaction

modify and commit only one aggregate in one transaction

## Aggregate Rules of Thumb

- protect business invariants inside aggregate boundaries
- design small aggregates
- reference other aggregates by id only
- update other aggregates using eventual consistency

### Rule 1: Protect Business Invariants Inside Aggregate Boundaries

### Rule 2: Design Small Aggregates

single responsibility principle

### Rule 3: Reference Other Aggregates by Identity Only

### Rule 4: Update Other Aggregates Using Eventual Consistency

#### If Eventual Consistency Seems Scary

## Modeling Aggregates

Anemic Domain Model 
- getters and setters but no real business behavior
- technical rather than business focus during modeling

watch for leaking business logic into App Services above your domain model

not utilities / helpers

put Business logic in domain model

ADM will suffer from bugs

### What about Functional Programming?

Anemic Domain Model does not apply for FP because they normally are separated


Every Aggregate Root Entity must have a globally unique identity

Id's modeled as immutable value objects

Product aggregate modeled per Ubiquitous Language

Don't just make up composed parts

Harmony between Domain Experts and developers

### Choose Your Abstractions Carefully

do these drawbacks apply to FP because it aims to provide a higher level abstraction? (page 94)
  
### Right-Sizing Aggregates

start with large cluster Aggregates

- start small, model ever aggregate with just one entity which will service as aggregate root
- protect business invariants inside Aggregate boundaries and maintain consistency rules
- time for reactions based updates
  - immediate
  - within N seconds/minutes/hour/days
  - business experts respond with acceptable time frame (my experience is all DE want everything immediately consistent and right now) 
- if same time frame of `immediately` from above consider composing 
- for each of reacting `with N` from above use `update other aggregates using eventual consistency`

be careful the business doesn't insist every Aggregate is `immediate consistency`

discuss failure cases and memory concerns of large cluster aggregates

consider discussing the business process if it was ran by only means of paper systems to provide insights

### Testable Units

business specifications - scenario specification acceptance tests

tests kept in source control with bounded context

