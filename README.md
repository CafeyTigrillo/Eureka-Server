# 🌟 Eureka Service Registry Server

## Overview
This project implements a Eureka Server instance, which acts as a service registry and discovery server in a microservices architecture. Built with Spring Boot and Spring Cloud Netflix Eureka, this server allows microservices to register themselves and discover other services without hardcoding hostname and port.

## ✨ Features
- Service Registration and Discovery
- Self-preservation mode
- Dashboard UI for monitoring registered services
- High availability ready
- Spring Boot integration

## 🛠 Technologies
- Java
- Spring Boot
- Spring Cloud Netflix Eureka Server
- Maven/Gradle (build tool)

## 🚀 Quick Start

### Prerequisites
- Java 17 or higher
- Maven 3.6+ or Gradle 7+

### Configuration
Add the following to your `application.properties` or `application.yml`:

```yaml
server:
  port: 8761

eureka:
  client:
    registerWithEureka: false
    fetchRegistry: false
  server:
    waitTimeInMsWhenSyncEmpty: 0
```

### Running the Application
1. Clone the repository
2. Navigate to the project directory
3. Run the application:
   ```bash
   ./mvnw spring-boot:run
   ```
   or with Gradle:
   ```bash
   ./gradlew bootRun
   ```
4. Access the Eureka Dashboard at: `http://localhost:8761`

## 🔍 Project Structure
```
eureka_sv/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── mipagina/
│   │   │           └── eureka_sv/
│   │   │               └── EurekaSvApplication.java
│   │   └── resources/
│   │       └── application.properties
└── pom.xml
```

## 📝 Usage
To register a client with this Eureka server:

1. Add the Eureka Client dependency to your microservice:
```xml
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-netflix-eureka-client</artifactId>
</dependency>
```

2. Configure the client application:
```yaml
eureka:
  client:
    serviceUrl:
      defaultZone: http://localhost:8761/eureka/
```

## 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

## ✨ Acknowledgments
- Spring Cloud Netflix team
- Spring Boot team
- Netflix Eureka team
