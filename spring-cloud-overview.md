# Spring Cloud

Spring Cloud helps us **manage multiple microservices**.  
It reduces complexity and provides a **centralized system** for distributed applications.

----

## Why Do We Need It?
In the cloud, one service does not know where the other services are.  
That’s why we use **Service Discovery** tools such as **Netflix Eureka**.  
Spring Cloud provides ready-to-use implementations of `DiscoveryClient`.

------
## Key Features
- **Configuration Management** → Centralized configuration for all services
- **Service Discovery** → Services can find each other dynamically
- **Circuit Breakers** → Fault tolerance and resilience
- **Intelligent Routing** → Smart request routing between services
- **Micro-proxy** → Lightweight service communication proxy

---

## Analogy
Think of a **shopping mall**:  
- Each shop = a **microservice**  
- Information desk = **Eureka (Service Discovery)**  
- Mall rules board = **Config Server**  
- Entrance/security gates = **Gateway**  
- Alternative shop when one is closed = **Circuit Breaker**

---

## Diagram
![Spring Cloud Diagram](https://github.com/user-attachments/assets/01573d0c-c15b-4a47-b3af-262069260236)

