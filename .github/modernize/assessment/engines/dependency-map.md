# Dependency Map

Spring PetClinic (MySQL) declares 13 production dependencies managed via Spring Boot 3.3.2 parent BOM, covering web, persistence, caching, observability, and UI layers.

## Dependencies

```mermaid
flowchart LR
    App["spring-petclinic-mysql v3.3.0"]
    BOM["spring-boot-starter-parent v3.3.2"]

    subgraph Web["Web Frameworks"]
        SpringWeb["Spring Boot Web"]
        Validation["Spring Boot Validation"]
        Thymeleaf["Spring Boot Thymeleaf"]
    end
    subgraph DB["Database / ORM"]
        JPA["Spring Boot Data JPA"]
        MySQL["mysql-connector-j (runtime)"]
        H2["H2 Database (runtime)"]
        AzureJDBC["Azure Spring Cloud JDBC MySQL v5.16.0"]
    end
    subgraph Cache["Caching"]
        SpringCache["Spring Boot Cache"]
        Caffeine["Caffeine"]
        CacheAPI["javax.cache API"]
    end
    subgraph Obs["Observability"]
        Actuator["Spring Boot Actuator"]
    end
    subgraph UI["UI Assets"]
        Bootstrap["Bootstrap v5.3.3"]
        FontAwesome["Font Awesome v4.7.0"]
    end
    subgraph Util["Utilities"]
        JakartaBind["Jakarta XML Bind API"]
    end

    BOM -.->|"manages versions"| App
    App -->|"web"| Web
    App -->|"persistence"| DB
    App -->|"caching"| Cache
    App -->|"observability"| Obs
    App -->|"ui assets"| UI
    App -->|"utilities"| Util
```
