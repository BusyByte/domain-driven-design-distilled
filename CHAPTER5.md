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

### Rule 2: Desing Small Aggregates

single responsibility principle

### Rule 3: Reference Other Aggregates by Identity Only

### Rule 4: Update Other Aggregates Using Eventual Consistency


