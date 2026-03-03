# Architecture Diagram

Spring PetClinic MySQL is a Spring Boot web application that manages pet clinic data using a MySQL backend, with Thymeleaf-based UI, Spring Data JPA for persistence, and Spring Cloud Azure for cloud-native MySQL connectivity.

## Application Architecture

```mermaid
flowchart TB
    subgraph Client["Client Layer"]
        Browser["Web Browser"]
    end

    subgraph Presentation["Presentation Layer (Spring MVC + Thymeleaf)"]
        WelcomeCtrl["WelcomeController"]
        OwnerCtrl["OwnerController"]
        PetCtrl["PetController"]
        VisitCtrl["VisitController"]
        VetCtrl["VetController"]
        CrashCtrl["CrashController"]
    end

    subgraph Business["Business Layer"]
        PetValidator["PetValidator"]
        PetTypeFormatter["PetTypeFormatter"]
        CacheConfig["CacheConfiguration (Caffeine)"]
    end

    subgraph DataAccess["Data Access Layer (Spring Data JPA)"]
        OwnerRepo["OwnerRepository"]
        VetRepo["VetRepository"]
    end

    subgraph DataStore["Data Storage"]
        MySQL["MySQL Database\n(spring-cloud-azure-starter-jdbc-mysql)"]
        H2["H2 In-Memory DB\n(test/dev)"]
        Cache["Caffeine Cache"]
    end

    subgraph Monitoring["Observability"]
        Actuator["Spring Boot Actuator\n(health, metrics, info)"]
    end

    Browser -- "HTTP requests" --> Presentation
    Presentation --> Business
    Business --> DataAccess
    DataAccess -- "JPA/Hibernate" --> MySQL
    DataAccess -- "JPA/Hibernate" --> H2
    Business --> Cache
    Presentation --> Actuator
```
