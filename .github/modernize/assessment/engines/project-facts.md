# Project Facts

## Container Engine

| Field | Value |
|-------|-------|
| **Status** | Not Applicable |
| **Finding** | No container engine configuration found. The project has no Dockerfile, Containerfile, or docker-compose.yml. Docker is implied indirectly through test-scoped dependencies (spring-boot-docker-compose, spring-boot-testcontainers) but no production container engine is configured. |
| **Confidence** | High |
| **Evidence** | No Dockerfile or Containerfile found; no docker-compose.yml found; no CI/CD workflow files found; pom.xml includes spring-boot-docker-compose (test scope) and spring-boot-testcontainers (test scope) |
| **Values** | No container engine configured for production; Docker implied for test environment via spring-boot-docker-compose |

## Base Image

| Field | Value |
|-------|-------|
| **Status** | Not Applicable |
| **Finding** | No Dockerfile or Containerfile found in the repository. No base image is configured. |
| **Confidence** | High |
| **Evidence** | No Dockerfile found; no Containerfile found; no docker-compose.yml found; no Kubernetes manifests found |
| **Values** | No base image configured |

## Image Size

| Field | Value |
|-------|-------|
| **Status** | Not Applicable |
| **Finding** | No Dockerfile or Containerfile found in the repository. Container image size cannot be estimated as the application is not yet containerized. |
| **Confidence** | High |
| **Evidence** | No Dockerfile found; no Containerfile found; no container build configuration exists |
| **Values** | No container image configured |

## Summary

This Spring Boot 3.3 application (`spring-petclinic-mysql`) is **not yet containerized**. No Dockerfile, Containerfile, docker-compose.yml, or CI/CD pipeline configuration was found. The project relies on Docker only indirectly through test-scoped dependencies (`spring-boot-docker-compose`, `spring-boot-testcontainers`). To deploy to Azure Container Apps or AKS, a Dockerfile and container build pipeline will need to be created.
