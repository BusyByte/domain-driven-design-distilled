# Strategic Design with Context Mapping

context mapping - integrating with other bounded contexts

line between bounded contexts

different kinds - team and technical

## Kinds of Mappings

### Partnership

line thickness to indicate teams must synchronize

the thicker the line, the higher the commitment

not long term and must be remapped when advantage not there

### Shared Kernel

modeled by intersection of bounded contexts

share a common model

difficult to maintain

open communication between teams

### Customer Supplier

Supplier is upstream annotated U

Customer is downstream annotated D

supplier meets needs of customer

### Conformist

upstream team has no motivation to support down stream team

use upstream model as is

eg Amazon.com being an affiliate seller

### Anticorruption Layer

translation layer between the ubiquitous languages of each bounded context

isolates downstream model from upstream and translates

integration approach

should do this when possible to isolate from foreign concepts

### Open Host Service

set of services with API for ease of use

### Published Language

can read write shared language with confidence

eg XML Schema, JSON Schema, Protobuf, or Avro

### Separate Ways

implement own specialized UL because no existing UL provides fully what you need

### Big Ball of Mud

- A growing number of Aggregates cross-contaminate because of unwarranted connections and dependencies.
- Maintaining one part of the Big Ball of Mud causes ripples across the model, which leads to “whack-a-mole” issues.
- Only tribal knowledge and heroics

## Making Good Use of Context Mapping

- RPC
- RESTful
- Messaging

less favorable is file or database

database should be avoided

if needed use anti-corruption layer

### RPC with SOAP

latency, failure, coupling

### RESTful HTTP

Bounded Context that sports a REST interface should provide an Open Host Service and a Published Language

can fail still and have latency

don't provide the aggregate from the domain

provide what the clients need

### Messaging

removes temporal coupling

Idempotent Receiver

some latency

## An Example in Context Mapping

event might only have id and query data later





