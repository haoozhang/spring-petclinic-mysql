# Project Facts Report

**Project**: spring-petclinic-mysql  
**Generated**: 2026-04-09  
**Assessment Engine**: AppCAT + LLM Fact Analysis

---

## Summary

Spring PetClinic MySQL is a Java 17 / Spring Boot 3.3.2 web application demonstrating a veterinary clinic management system. It is a layered monolith with MVC pattern, using embedded Apache Tomcat, Spring Data JPA with MySQL, Thymeleaf server-side rendering, and Caffeine in-memory caching. No containerization or orchestration is configured.

---

## Application Identity

| Fact | Value |
|------|-------|
| **Application Name** | `spring-petclinic-mysql` |
| **Group ID** | `org.springframework.samples` |
| **Version** | `3.3.0-SNAPSHOT` |
| **Application Type** | Web Application + REST API endpoint |
| **Architecture Pattern** | Layered Monolith with MVC |
| **License** | Apache License, Version 2.0 |

---

## Runtime & Technology Stack

| Fact | Value |
|------|-------|
| **Runtime** | Java 17 (JVM) |
| **Framework** | Spring Boot 3.3.2 |
| **Servlet Container** | Embedded Apache Tomcat 10.1.x (Servlet 6.0 / Jakarta EE 10) |
| **Web Layer** | Spring MVC + Thymeleaf |
| **Data Access** | Spring Data JPA / Hibernate |
| **Database (Production)** | MySQL (external, host/port via env vars) |
| **Database (Dev/Test)** | H2 in-memory |
| **Caching** | Caffeine (in-process) |
| **Build Tool** | Apache Maven |
| **Operating System** | Cross-platform JVM (Linux recommended for server) |

---

## Configuration & Profiles

| Fact | Value |
|------|-------|
| **Spring Profiles** | `mysql` (1 profile) |
| **Maven Profiles** | `css` (build-time Bootstrap CSS only) |
| **Config Files** | `application.properties` (default), `application-mysql.properties` (mysql profile) |
| **XML Configs** | None (pure annotation-based Spring Boot) |
| **Environment Variables** | 5 (MYSQL_HOST, MYSQL_PORT, MYSQL_DATABASE, MYSQL_USERNAME, MYSQL_PASSWORD) |

---

## Containerization & Deployment

| Fact | Value |
|------|-------|
| **Container Engine** | Not configured |
| **Base Image** | Not applicable (no Dockerfile) |
| **Image Size** | Not applicable |
| **Image Layers** | Not applicable |
| **Multi-stage Build** | Not applicable |
| **Container Version** | Not applicable |
| **Volume Mounts** | Not applicable |
| **Orchestration Tool** | Not configured |
| **Service Definition** | Not configured |
| **Resource Limits** | Not configured |
| **Network Settings** | Not configured |

---

## Application Networking

| Fact | Value |
|------|-------|
| **Application Port** | 8080 (Spring Boot default, HTTP) |
| **Communication Protocols** | HTTP/REST via Spring MVC |
| **REST Endpoints** | GET /, GET+POST /owners*, GET+POST /owners/{id}/pets*, GET+POST visits*, GET /vets (JSON), GET /vets.html |
| **Actuator Endpoints** | All exposed (`management.endpoints.web.exposure.include=*`) |

---

## External Services & Dependencies

| Fact | Value |
|------|-------|
| **External Services** | MySQL (primary), H2 (dev/test fallback) |
| **External Dependencies** | MySQL (1 true external system) |
| **Message Queues** | None |
| **Caches (External)** | None |
| **Authentication Services** | None |
| **Storage Services** | None |

---

## Security

| Fact | Value |
|------|-------|
| **Authentication** | None |
| **Authorization** | None |
| **Transport Security** | HTTP only (no HTTPS configured) |
| **Encryption** | None |
| **Input Validation** | Bean Validation API (@Valid) |
| **Secret Management** | Environment variables for DB credentials |
| **Notable Risk** | All actuator endpoints exposed without authentication |

---

## Observability & Instrumentation

| Fact | Value |
|------|-------|
| **Logging Framework** | Logback (Spring Boot default via SLF4J) |
| **Log Level** | INFO for `org.springframework` |
| **Telemetry / APM** | Spring Boot Actuator (metrics, health, info) |
| **AOP** | None |
| **Health Checks (App)** | `/actuator/health`, `/actuator/health/liveness`, `/actuator/health/readiness` |
| **Health Checks (Container)** | Not configured |

---

## Data

| Fact | Value |
|------|-------|
| **Data Classification** | PII (owner names, addresses, telephone); Internal (pet records, visit notes) |
| **Compliance Requirements** | None explicitly documented |
| **Database Schema** | 6 tables: `owners`, `pets`, `visits`, `vets`, `specialties`, `vet_specialties`, `types` |

---

## Testing

| Fact | Value |
|------|-------|
| **Testing Frameworks** | JUnit 5, Mockito, AssertJ (via spring-boot-starter-test), Testcontainers (MySQL) |
| **Test Files** | 0 (no `src/test` directory in repository) |
| **Code Coverage** | JaCoCo configured |
| **Embedded Language Usage** | None |

---

## Hardware Requirements

| Fact | Value |
|------|-------|
| **RAM (Estimated)** | ~512MB minimum, 1GB recommended |
| **CPU (Estimated)** | 1 core minimum |
| **Disk (Estimated)** | ~500MB for application JAR and logs |
| **Note** | No formal requirements documented; MySQL requires separate resources |

---

## Key Observations for Azure Migration

1. **No containerization** — Dockerfile and docker-compose must be created before cloud deployment.
2. **MySQL dependency** — Migrate to Azure Database for MySQL Flexible Server; `spring-cloud-azure-starter-jdbc-mysql:5.16.0` already supports Azure Managed Identity for passwordless auth.
3. **Actuator endpoints unprotected** — Add Spring Security before exposing to internet.
4. **No HTTPS** — TLS termination required at load balancer or application level.
5. **Single environment profile** — Production-grade profile with hardened settings recommended.
6. **PII data** — Owner personal data requires access controls and audit logging for GDPR compliance in production.
7. **No test suite** — Test source directory absent; test coverage tooling (JaCoCo) is configured but no tests to run.
