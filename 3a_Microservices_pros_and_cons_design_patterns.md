### Introduction - Part 1

- This is part 3 of the video series on high-level design
- Previous 2 videos already covered
- This part covers:
    - Monolithic vs microservices
    - Covering important microservices patterns
    - Says this topic can lead to around 15 questions in interviews

### Disadvantages of Monolithic Architecture

- Tight Coupling
    - Changing one line can impact other components
    - Need to test/deploy entire application for one change
- Difficult to scale
    - If one component needs scaling, entire application needs to be scaled
- Expensive deployments and rollbacks
    - Entire application needs redeployment for a small change
- Large codebase
    - Everything in a single application
    - Codebase grows large over time
    - Difficult to make changes, understand impact

### Why Microservices?

- To overcome monolithic disadvantages
- Split large application into small services

### Advantages of Microservices

- Better separation of concerns
- Loose coupling between services
- Independent deployment of services
- Easy to scale out specific services
- Faster release cycles

### Disadvantages of Microservices

- Proper service boundaries/decomposition is challenging
- Inter-service communication is complex
    - Monitoring calls across services
    - Handling failures
- Distributed transaction management is difficult
    - Across multiple databases

### Microservices Design Phases

- Decomposition patterns
- Database patterns
- Communication patterns
- Integration patterns
- Deployment patterns
- Cross-cutting concerns like monitoring, logging

### Decomposition Patterns

- By business capability
    - Split based on business functions like order mgmt, inventory, etc
- By subdomain - Domain Driven Design (DDD)
    - Split large domains into multiple services
        - E.g. splitting payment domain
