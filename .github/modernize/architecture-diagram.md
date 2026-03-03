# Architecture Diagram

This diagram illustrates the high-level architecture of the Spring PetClinic MySQL application, showing the application layers, key frameworks, data storage, and external integrations.

## Application Architecture

```mermaid
flowchart TD
    subgraph Client["Client Layer"]
        Browser["Web Browser"]
    end

    subgraph Presentation["Presentation Layer\n(Thymeleaf Templates + Bootstrap + Font Awesome)"]
        WelcomeCtrl["WelcomeController"]
        OwnerCtrl["OwnerController"]
        PetCtrl["PetController"]
        VisitCtrl["VisitController"]
        VetCtrl["VetController"]
    end

    subgraph Business["Business Logic Layer\n(Spring Boot 3.3 / Spring MVC / Bean Validation)"]
        OwnerSvc["Owner Management"]
        PetSvc["Pet Management"]
        VetSvc["Vet Management"]
        Cache["Caffeine Cache\n(JSR-107)"]
    end

    subgraph DataAccess["Data Access Layer\n(Spring Data JPA / Hibernate)"]
        OwnerRepo["OwnerRepository"]
        VetRepo["VetRepository"]
    end

    subgraph Storage["Data Storage"]
        MySQL["MySQL Database\n(Azure MySQL via spring-cloud-azure-starter-jdbc-mysql)"]
        H2["H2 In-Memory DB\n(local/test profile)"]
    end

    subgraph Observability["Observability"]
        Actuator["Spring Boot Actuator\n(Health, Metrics, Info)"]
    end

    Browser -->|HTTP requests| WelcomeCtrl
    Browser -->|HTTP requests| OwnerCtrl
    Browser -->|HTTP requests| PetCtrl
    Browser -->|HTTP requests| VisitCtrl
    Browser -->|HTTP requests| VetCtrl

    WelcomeCtrl --> Business
    OwnerCtrl --> OwnerSvc
    PetCtrl --> PetSvc
    VisitCtrl --> PetSvc
    VetCtrl --> VetSvc

    VetSvc --> Cache
    Cache --> VetRepo

    OwnerSvc --> OwnerRepo
    PetSvc --> OwnerRepo

    OwnerRepo --> MySQL
    VetRepo --> MySQL
    OwnerRepo -.->|test profile| H2
    VetRepo -.->|test profile| H2

    Browser -->|metrics/health| Actuator
```
