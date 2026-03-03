# Component Relationship Diagram

This diagram shows the internal component structure and interactions within the Spring PetClinic MySQL application, organized by architectural layer.

## Component Relationships

```mermaid
flowchart TD
    subgraph Presentation["Presentation Layer - Controllers"]
        WelcomeCtrl["WelcomeController\nGET /"]
        OwnerCtrl["OwnerController\nGET/POST /owners"]
        PetCtrl["PetController\nGET/POST /owners/id/pets"]
        VisitCtrl["VisitController\nGET/POST /owners/id/pets/id/visits"]
        VetCtrl["VetController\nGET /vets"]
        CrashCtrl["CrashController\nGET /oups"]
    end

    subgraph BusinessLogic["Business Logic Layer - Services and Utilities"]
        PetValidator["PetValidator\nvalidates Pet form input"]
        PetTypeFormatter["PetTypeFormatter\nformats PetType for forms"]
        CacheConfig["CacheConfiguration\nconfigures Caffeine cache"]
    end

    subgraph DataAccess["Data Access Layer - Repositories"]
        OwnerRepo["OwnerRepository\nSpring Data JPA"]
        VetRepo["VetRepository\nSpring Data JPA - cached"]
    end

    subgraph Domain["Domain Model - Entities"]
        Owner["Owner\nextends Person"]
        Pet["Pet\nextends NamedEntity"]
        PetType["PetType\nextends NamedEntity"]
        Visit["Visit"]
        Vet["Vet\nextends Person"]
        Specialty["Specialty\nextends NamedEntity"]
        Person["Person\nextends BaseEntity"]
        NamedEntity["NamedEntity\nextends BaseEntity"]
        BaseEntity["BaseEntity\nid field"]
    end

    subgraph Config["Application Configuration"]
        AppMain["PetClinicApplication\nSpring Boot entry point"]
        RuntimeHints["PetClinicRuntimeHints\nGraalVM native hints"]
    end

    %% Controller to Repository relationships
    OwnerCtrl -->|"findByLastName, findById"| OwnerRepo
    PetCtrl -->|"findById, save"| OwnerRepo
    VisitCtrl -->|"findById, save"| OwnerRepo
    VetCtrl -->|"findAll"| VetRepo

    %% Controller to Utility relationships
    PetCtrl -->|"validate"| PetValidator
    PetCtrl -->|"format PetType"| PetTypeFormatter
    PetTypeFormatter -->|"findPetTypes"| OwnerRepo

    %% Repository to Domain relationships
    OwnerRepo -->|"manages"| Owner
    VetRepo -->|"manages"| Vet

    %% Domain entity inheritance
    Owner -->|"extends"| Person
    Vet -->|"extends"| Person
    Person -->|"extends"| BaseEntity
    Pet -->|"extends"| NamedEntity
    PetType -->|"extends"| NamedEntity
    Specialty -->|"extends"| NamedEntity
    NamedEntity -->|"extends"| BaseEntity

    %% Domain entity relationships
    Owner -->|"has many"| Pet
    Pet -->|"has one"| PetType
    Pet -->|"has many"| Visit
    Vet -->|"has many"| Specialty

    %% Cache config
    CacheConfig -->|"caches vets"| VetRepo

    %% App startup
    AppMain -->|"bootstraps"| RuntimeHints
```
