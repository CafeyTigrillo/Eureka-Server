# **Eureka Server - Microservices for Online Store**

## **What is Eureka Server?**

**Eureka Server** is a service discovery server, part of the **Spring Cloud** ecosystem, used in microservices architectures. In a microservices system, each service can be running on different instances or even on different servers. Eureka Server helps by allowing services to discover each other dynamically.

Eureka Server acts as a "registry" where all registered services can be discovered by other services via a REST API. This improves the scalability and resilience of the architecture by allowing services to communicate with each other without the need to know static addresses.

## **Why is it useful in our project?**

In our **Online Store** project (which includes microservices like order service, product service, payment service, and more), **Eureka Server** acts as a central hub for service registration and discovery. This allows our microservices to find each other easily, even as they scale up or down based on demand.

- **Dynamic Service Discovery**: Services register themselves with Eureka when they start and unregister when they stop. Other services can then dynamically discover the location of these services.
  
- **Scalability**: As we add more instances of any service, Eureka will keep track of them, enabling horizontal scaling.
  
- **Fault Tolerance**: If a service goes down or becomes unreachable, Eureka allows other services to avoid that instance and continue functioning with available ones.

## **How does it work?**

1. **Service Registration**: Each microservice (such as order service, payment service, etc.) registers itself with Eureka Server when it starts. It includes information like its hostname and port number.
   
2. **Service Discovery**: Other microservices query Eureka Server to discover the available instances of a service before making a call.

3. **Heartbeat**: Services regularly send "heartbeat" signals to Eureka to let it know that they are still active. If Eureka does not receive a heartbeat within a specified timeout, it considers the service as unavailable and removes it from the registry.

## **Integration in Our Project**

- The **Eureka Server** is a critical part of our **microservices-based architecture**. It enables seamless communication and scaling between the following services:
    - **Order Service**
    - **Payment Service**
    - **Product Service**
    - **Inventory Service**
    - **And more...**

- Eureka simplifies the integration of new services and promotes a **flexible, resilient**, and **scalable** architecture for our online store.