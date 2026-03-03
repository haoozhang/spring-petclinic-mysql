# Component Relationship Diagram

Spring PetClinic MySQL internal component structure and interactions, showing how controllers, repositories, entities, and supporting components are related.

## Component Relationships

```mermaid
flowchart TD
    subgraph Presentation["Presentation Layer (Spring MVC Controllers)"]
        WelcomeCtrl["WelcomeController\nGET /"]
        OwnerCtrl["OwnerController\nGET/POST /owners/**"]
        PetCtrl["PetController\nGET/POST /owners/ownerId/pets/**"]
        VisitCtrl["VisitController\nGET/POST /owners/ownerId/pets/petId/visits/**"]
        VetCtrl["VetController\nGET /vets, /vets.html"]
        CrashCtrl["CrashController\nGET /oups"]
    end

    subgraph Business["Business Components"]
        PetValidator["PetValidator\n(Spring Validator)"]
        PetTypeFormatter["PetTypeFormatter\n(Spring Formatter)"]
        CacheConfig["CacheConfiguration\n(Caffeine Cache)"]
    end

    subgraph DataAccess["Data Access Layer (Spring Data JPA Repositories)"]
        OwnerRepo["OwnerRepository\nfindByLastName, findById\nfindPetTypes, save"]
        VetRepo["VetRepository\nfindAll (paginated)"]
    end

    subgraph Entities["Domain Entities (JPA)"]
        Owner["Owner extends Person\nid, address, city, telephone\nPets collection"]
        Pet["Pet extends NamedEntity\nbirthDate, type, visits"]
        Visit["Visit extends BaseEntity\ndate, description"]
        PetType["PetType extends NamedEntity\nname"]
        Vet["Vet extends Person\nspecialties collection"]
        Specialty["Specialty extends NamedEntity\nname"]
        Person["Person extends NamedEntity\nfirstName, lastName"]
        NamedEntity["NamedEntity extends BaseEntity\nname"]
        BaseEntity["BaseEntity\nid"]
    end

    subgraph Infrastructure["Infrastructure"]
        PetClinicApp["PetClinicApplication\n(Spring Boot entry point)"]
        RuntimeHints["PetClinicRuntimeHints\n(GraalVM hints)"]
        MySQL[("MySQL Database")]
        Cache[("Caffeine Cache")]
    end

    OwnerCtrl -- "injects / queries" --> OwnerRepo
    PetCtrl -- "injects / queries" --> OwnerRepo
    PetCtrl -- "validates with" --> PetValidator
    VisitCtrl -- "injects / queries" --> OwnerRepo
    VetCtrl -- "injects / queries" --> VetRepo
    PetTypeFormatter -- "loads pet types via" --> OwnerRepo

    OwnerRepo -- "manages" --> Owner
    OwnerRepo -- "manages" --> Pet
    OwnerRepo -- "manages" --> Visit
    OwnerRepo -- "manages" --> PetType
    VetRepo -- "manages" --> Vet
    VetRepo -- "manages" --> Specialty

    Owner -- "has many" --> Pet
    Pet -- "has type" --> PetType
    Pet -- "has many" --> Visit
    Vet -- "has many" --> Specialty
    Owner --> Person
    Vet --> Person
    Person --> NamedEntity
    Pet --> NamedEntity
    PetType --> NamedEntity
    Specialty --> NamedEntity
    NamedEntity --> BaseEntity

    OwnerRepo -- "persists via JPA" --> MySQL
    VetRepo -- "persists via JPA" --> MySQL
    CacheConfig -- "caches vet list" --> Cache
    VetCtrl -- "cached response" --> CacheConfig
```
