# Project Facts

Consolidated application facts for **spring-petclinic-mysql** (Spring Boot 3.3 / Java 17), generated from automated analysis of the repository.

## Container Engine

| Field | Value |
|-------|-------|
| **Status** | Not Applicable |
| **Finding** | No Dockerfile, Containerfile, or docker-compose files found. The project includes `spring-boot-docker-compose` and `spring-boot-testcontainers` as test-scoped dependencies, indicating Docker is used indirectly for local development and testing but no production container configuration exists. |
| **Confidence** | High |
| **Values** | Docker (test/dev only via spring-boot-docker-compose and Testcontainers); No production container engine configured |

**Evidence:**
- No Dockerfile or Containerfile found in repository
- No docker-compose*.yml files found
- No .dockerignore file found
- No CI/CD workflow files found
- pom.xml includes spring-boot-docker-compose (test scope) and spring-boot-testcontainers (test scope)
- testcontainers:mysql dependency present for integration testing

---

## Base Image

| Field | Value |
|-------|-------|
| **Status** | Not Applicable |
| **Finding** | No Dockerfile or Containerfile found in the repository. The application has no container base image configured. The project uses spring-boot-docker-compose and Testcontainers as test-scoped dependencies, but these do not define a base image for the application itself. |
| **Confidence** | High |
| **Values** | No base image configured; No container registry in use; No OS base layer defined |

**Evidence:**
- No Dockerfile found in repository
- No Containerfile found in repository
- No docker-compose*.yml files found
- No Kubernetes manifests with image references found
- spring-boot-docker-compose is test-scoped only

---

*Generated: 2026-04-10T08:32:10Z*
