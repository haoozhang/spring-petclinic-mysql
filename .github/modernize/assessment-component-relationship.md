# Component Relationship Diagram

## Spring PetClinic MySQL - Component Relationships

```mermaid
graph TD
    subgraph Startup["Startup and Configuration"]
        App["PetClinicApplication\n(main)"]
        Hints["PetClinicRuntimeHints\n(RuntimeHintsRegistrar)"]
        CacheConf["CacheConfiguration\n(Configuration)"]
    end

    subgraph PresentationLayer["Presentation Layer (Controllers)"]
        WC["WelcomeController\nGET /"]
        OC["OwnerController\nGET/POST /owners/**"]
        PC["PetController\nGET/POST /owners/{id}/pets/**"]
        VC["VisitController\nGET/POST /owners/{id}/pets/{id}/visits/**"]
        VetC["VetController\nGET /vets, /vets.html"]
        CC["CrashController\nGET /oups"]
    end

    subgraph DataAccessLayer["Data Access Layer (Repositories)"]
        OR["OwnerRepository\n(JpaRepository)"]
        VR["VetRepository\n(JpaRepository)"]
    end

    subgraph DomainModel["Domain Model (Entities)"]
        subgraph OwnerDomain["Owner Domain"]
            Owner["Owner\n(Entity)"]
            Pet["Pet\n(Entity)"]
            PetType["PetType\n(Entity)"]
            Visit["Visit\n(Entity)"]
        end
        subgraph VetDomain["Vet Domain"]
            Vet["Vet\n(Entity)"]
            Specialty["Specialty\n(Entity)"]
            Vets["Vets\n(XML wrapper)"]
        end
        subgraph BaseModel["Base Model"]
            BaseEntity["BaseEntity"]
            NamedEntity["NamedEntity"]
            Person["Person"]
        end
    end

    subgraph Support["Support Components"]
        PTF["PetTypeFormatter\n(Formatter)"]
        PV["PetValidator\n(Validator)"]
    end

    App -->|starts| PresentationLayer
    App -->|starts| DataAccessLayer
    App -->|registers| Hints

    CacheConf -->|configures Caffeine cache for| VR

    OC -->|constructor inject| OR
    PC -->|constructor inject| OR
    VC -->|constructor inject| OR
    VetC -->|constructor inject| VR

    PTF -->|constructor inject| OR

    PC -->|uses| PTF
    PC -->|uses| PV

    OR -->|persists| Owner
    OR -->|persists| Pet
    OR -->|persists| Visit
    OR -->|reads| PetType

    VR -->|persists| Vet

    Owner -->|has many| Pet
    Owner -->|has many| Visit
    Pet -->|has one| PetType
    Pet -->|has many| Visit
    Vet -->|has many| Specialty
    Vets -->|wraps list of| Vet

    Owner -->|extends| Person
    Vet -->|extends| Person
    Person -->|extends| NamedEntity
    Pet -->|extends| NamedEntity
    PetType -->|extends| NamedEntity
    Specialty -->|extends| NamedEntity
    Visit -->|extends| BaseEntity
    NamedEntity -->|extends| BaseEntity
```

## Component Inventory

| Component | Type | Package | Dependencies |
|-----------|------|---------|--------------|
| PetClinicApplication | Main | petclinic | - |
| PetClinicRuntimeHints | RuntimeHintsRegistrar | petclinic | - |
| CacheConfiguration | Configuration | system | VetRepository (via cache manager) |
| WelcomeController | Controller | system | - |
| CrashController | Controller | system | - |
| OwnerController | Controller | owner | OwnerRepository |
| PetController | Controller | owner | OwnerRepository, PetTypeFormatter, PetValidator |
| VisitController | Controller | owner | OwnerRepository |
| VetController | Controller | vet | VetRepository |
| OwnerRepository | Repository | owner | Owner, Pet, PetType, Visit (JPA entities) |
| VetRepository | Repository | vet | Vet, Specialty (JPA entities) |
| PetTypeFormatter | Formatter | owner | OwnerRepository |
| PetValidator | Validator | owner | - |
| Owner | Entity | owner | Pet, Visit |
| Pet | Entity | owner | PetType, Visit |
| PetType | Entity | owner | - |
| Visit | Entity | owner | - |
| Vet | Entity | vet | Specialty |
| Specialty | Entity | vet | - |
| Vets | XML Wrapper | vet | Vet |
| BaseEntity | Base Model | model | - |
| NamedEntity | Base Model | model | BaseEntity |
| Person | Base Model | model | NamedEntity |
