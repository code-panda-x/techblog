# What is SOA


### What is SOA
Service Oriented Architecture:

Distributed system architecture where all components are designed to be services

eg. Cloud solutions are based on SOA

### Key attributes
- Services over components
- Interoperability & Cross platform
- Loose coupling & Distributed
- Abstraction against complexity

### SOA Components
Services: Pieces of software that are autonomous, self-contained and accessible
- Automic services: well-defined and **independent**
- Composite: fusion of two or more automic services
- Types: frontend, integration, business, public enterprise, infrastructure

ESB: Enterprise bus (backbone of a SOA system)
- Providing connectivity
- Data transformation
- Routing
- Security 

SDR: Service description repository: for service consumer to use services


Service consumer:
- Internal: Use ESB to send request and receive responses from services
- External: Use SDR to call the service

API:
- Single entry point for all clients
- Translate requests and route them to apropriate service

![soa.png](/images/soa.png)

### SOA principles
- Standard Service Contracts
- Interoperability
- Composability
- Abstraction
- Discoverability
- Statelessness

### Pros & Cons
Pros:
- Reusability
- Maintainability
- Scalability & Availability
- Platform independence

Cons:
- Complex service management
- Increased overhead

