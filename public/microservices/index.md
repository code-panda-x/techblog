# Microservices vs Monolith


## MicroService

- Take every app function and put it in its own service
- Runs in its own container
- Communicate via APIs

But if each microservice is implemented in different languages/environment, how do we deploy?
Deployment: Use **Docker !** Put each microservice into containers

### Pros
- Flexibility (each microservice can be built in different languages/technologies)
- Less risk in change
- Independent scaling
- Faster release cycles

## Monolith
- Server-side systme based on single application 

### Pros
- Good for small team
- Less complex
- Less duplication
- Run fast


### Cons
- Highly dependent (single point of failure)
- Language/Framework
- Growth
- Scaling issue
- Complex deployment

## Spring Boot

### Goal
- Enable quickly built applications
- Provide common non-functional features

### Not
- Spring boot does **NOT** generate code
- Spring boot is **NOT** an application server or a web server

### Features
Quick starter projects with auto configuration
- Web (Login, spring mvc)
- JPA (DB)

## start.spring.io starter apps/dependencies
- Spring Web
  - @RestController
    - `@GetMapping` handles REST API
  - MVC
- Spring Boot Actuator 
  - Monitor and manage application
- Spring Boot DevTools
  - Provide fast app restarts, livereload

## Spring vs Spring Boot vs Spring MVC
### Spring Framework
- Dependency Injection: Takes care of defining beans, dependencies, how to bind components
### Spring MVC
- Web applications
### Spring Boot
- Autoconfig

---
// 143

Questions:
What is spring boot/cloud?
Distirbuted system regarding microservice
load balancer what does it do?
what is maven

$$$$$$$$$$
Draw a overall blueprint of each model
Why use these techs
$$$$$$$$$$

Keyword
- Distributed system
- Maven
- Java Spring Boot?
  Dependencies:
  - Spring Boot Devtools
  - Spring Boot Actuator
  - Spring Web(REST, MVC)
  - Config Client (Connect to spring cloud config)
- REST
- H2 DB, SQL with JPA (Currency from / to, exchange rate)
- Build routes with Eureka naming server and redirect all requests thru Spring cloud gateway (Assigen different ports to different server)
- Circuit Breaker framwork: Resilience4j (fallback methods if ms is down)
- Zipkin as a distributed tracing server (as a container) connected to all ms ( to trace requests accross ms) // 174
  - What if distributed tracing server is down? Use Rabbit MQ
- Google Cloud Kubernetes

