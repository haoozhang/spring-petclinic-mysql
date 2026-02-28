# Architecture Diagram

## Spring PetClinic MySQL - Application Architecture

```mermaid
graph TB
    subgraph Client
        Browser[Web Browser]
    end

    subgraph PresentationLayer["Presentation Layer (Spring MVC + Thymeleaf)"]
        WC[WelcomeController]
        OC[OwnerController]
        PC[PetController]
        VC[VisitController]
        VetC[VetController]
        CC[CrashController]
    end

    subgraph DataAccessLayer["Data Access Layer (Spring Data JPA)"]
        OR[OwnerRepository]
        VR[VetRepository]
    end

    subgraph DomainModel["Domain Model"]
        Owner[Owner]
        Pet[Pet / PetType]
        Visit[Visit]
        Vet[Vet / Specialty]
    end

    subgraph Infrastructure["Infrastructure"]
        Cache[Caffeine Cache]
        Actuator[Spring Boot Actuator]
        Validation[Bean Validation]
    end

    subgraph DataStorage["Data Storage"]
        MySQL[(MySQL Database)]
        H2[(H2 In-Memory DB)]
    end

    subgraph AzureCloud["Azure Cloud"]
        AzureJDBC[Azure Spring Cloud JDBC MySQL]
    end

    Browser -->|HTTP requests| PresentationLayer
    OC -->|CRUD operations| OR
    PC -->|CRUD operations| OR
    VC -->|CRUD operations| OR
    VetC -->|read| VR
    OR -->|manages| Owner
    OR -->|manages| Pet
    OR -->|manages| Visit
    VR -->|manages| Vet
    OR -->|cached via| Cache
    VR -->|cached via| Cache
    DataAccessLayer -->|JPA/Hibernate| MySQL
    DataAccessLayer -->|JPA/Hibernate| H2
    MySQL -->|managed connection| AzureJDBC
    PresentationLayer -->|monitoring| Actuator
    PresentationLayer -->|input validation| Validation
```

## Technology Stack

| Layer | Technology |
|-------|-----------|
| Framework | Spring Boot 3.3.2 |
| Language | Java 17 |
| Web | Spring MVC, Thymeleaf |
| Data Access | Spring Data JPA, Hibernate |
| Database (prod) | MySQL (via Azure Spring Cloud JDBC 5.16.0) |
| Database (dev) | H2 In-Memory |
| Caching | Caffeine, javax.cache |
| Monitoring | Spring Boot Actuator |
| Frontend | Bootstrap 5.3.3, Font Awesome 4.7.0 (Webjars) |
| Validation | Jakarta Bean Validation |
| Build | Maven |
