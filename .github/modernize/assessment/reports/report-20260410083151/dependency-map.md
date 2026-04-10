# Dependency Map

Spring PetClinic MySQL is a Spring Boot 3.3 application with 14 declared non-test external dependencies spanning web, persistence, caching, observability, and utility categories.

## Dependencies

```mermaid
flowchart LR
    App["spring-petclinic-mysql"]

    subgraph BOM["Parent BOM"]
        SpringBootBOM["Spring Boot 3.3.2"]
    end
    subgraph Web["Web Frameworks"]
        SpringWeb["Spring Boot Starter Web"]
        Thymeleaf["Spring Boot Starter Thymeleaf"]
        Bootstrap["Bootstrap v5.3.3"]
        FontAwesome["Font Awesome v4.7.0"]
    end
    subgraph DB["Database / ORM"]
        DataJPA["Spring Boot Starter Data JPA"]
        AzureMySQL["Azure Spring JDBC MySQL v5.16.0"]
        MySQLDriver["MySQL Connector/J"]
        H2["H2 Database (runtime)"]
    end
    subgraph Cache["Caching"]
        SpringCache["Spring Boot Starter Cache"]
        CacheAPI["javax.cache API"]
        Caffeine["Caffeine"]
    end
    subgraph Obs["Observability"]
        Actuator["Spring Boot Actuator"]
    end
    subgraph Util["Utilities"]
        Validation["Spring Boot Starter Validation"]
        JakartaBind["Jakarta XML Bind API"]
    end

    App -->|"bom"| BOM
    App -->|"web"| Web
    App -->|"persistence"| DB
    App -->|"caching"| Cache
    App -->|"observability"| Obs
    App -->|"utilities"| Util
    SpringBootBOM -.->|"manages"| Web
    SpringBootBOM -.->|"manages"| DB
    SpringBootBOM -.->|"manages"| Cache
    SpringBootBOM -.->|"manages"| Obs
    SpringBootBOM -.->|"manages"| Util
```
