# Tactical Design with Domain Events

domain event - record of some business-significant occurrence in a bounded context

causual consistence - one operation causes another

example conversation - correctly ordered

sequence metadata on event

wait for prior event

ignore latent event (dismissible)

## Designing, Implementing, and Using Domain Events

capture event time

name domain event after Ubiquitous Language

should name past tense to indicated statement of past occurrence

event is result of a corresponding command eg ProductCreated event results from CreateProduct command
 
created event has all fields on command

domain event can be enriched

don't put too much information into event that it loses it's meaning

time triggered events like end of day end of fixcal year can be events not triggered by commands but by some concrete timer

eg MarketsClosed event and not just `4 pm event`

command different from event as command can be rejected

## Event Sourcing

persisting all domain events that have occured for an aggregate instance as record about what changed about that aggregate instance

don't persist whole state

event store is append only - high throughput, low latency, high scalability

### Performance Conscious

caching in memory and snapshots, see IDDD and Reactive Messaging Patterns with the Actor Model
 

stores record of everything happened
 
 

