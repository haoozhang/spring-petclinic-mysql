# Project Facts Report

**Project**: spring-petclinic-mysql  
**Generated**: 2026-04-09  
**Fact Skills Executed**: 36

---

## Summary

Spring PetClinic MySQL is a Spring Boot 3.3.2 web application (version 3.3.0-SNAPSHOT) running on Java 17. It follows a layered MVC monolith architecture, uses server-side Thymeleaf rendering, and connects to MySQL as its primary data store (with H2 for development). The application has no containerization, no orchestration, and no security configuration. It is ready for cloud migration with minor adjustments.

---

## Application Identity

| Fact | Value | Confidence |
|------|-------|------------|
| **Application Name** | `spring-petclinic-mysql` (groupId: `org.springframework.samples`) | High |
| **Version** | `3.3.0-SNAPSHOT` (development/pre-release) | High |
| **Application Type** | Web Application (Thymeleaf MVC) + limited REST API (`/vets` JSON endpoint) | High |
| **Architecture Pattern** | Layered Monolith with MVC pattern | High |
| **Application Port** | `8080` (Spring Boot default; no explicit `server.port` set) | Medium |

---

## Runtime & Technology Stack

| Fact | Value | Confidence |
|------|-------|------------|
| **Runtime Environment** | Java 17 (JVM) | High |
| **Framework** | Spring Boot 3.3.2 (Spring MVC, Spring Data JPA, Thymeleaf) | High |
| **Servlet Container** | Embedded Apache Tomcat 10.1.x (Servlet API 6.0 / Jakarta EE 10) | High |
| **Operating System** | Cross-platform JVM; Linux recommended for production | Medium |
| **Build Tool** | Apache Maven (spring-boot-maven-plugin) | High |
| **XML Configs** | None — pure annotation-based Spring Boot configuration | High |
| **Embedded Language Usage** | None — pure Java implementation | High |

---

## Dependencies

| Fact | Value | Confidence |
|------|-------|------------|
| **Language Dependencies** | 15 non-test dependencies (pom.xml); managed via Spring Boot BOM 3.3.2 | High |
| **External Services** | MySQL (primary database); Azure Database for MySQL (cloud managed variant) | High |
| **External Dependencies** | MySQL only; no Redis, LDAP, S3, Kafka, RabbitMQ | High |
| **Testing Framework** | JUnit 5 (Jupiter), Spring Boot Test, Mockito, Testcontainers (MySQL), AssertJ | High |

**Key dependencies:**
- `spring-boot-starter-web` — Spring MVC
- `spring-boot-starter-data-jpa` — Hibernate/JPA
- `spring-boot-starter-thymeleaf` — Server-side HTML rendering
- `spring-cloud-azure-starter-jdbc-mysql:5.16.0` — Azure MySQL integration
- `mysql-connector-j` — MySQL JDBC driver (runtime)
- `h2` — In-memory database (dev/test)
- `caffeine` + `spring-boot-starter-cache` — In-process caching
- `spring-boot-starter-actuator` — Health/metrics endpoints

---

## Configuration & Profiles

| Fact | Value | Confidence |
|------|-------|------------|
| **Profile Settings** | 2 profiles: `default` (H2/MySQL config) + `mysql` (real MySQL via env vars) | High |
| **Environment Variables** | 5 MySQL env vars: `MYSQL_HOST`, `MYSQL_PORT`, `MYSQL_DATABASE`, `MYSQL_USERNAME`, `MYSQL_PASSWORD` | High |
| **Communication Protocols** | HTTP only (Spring MVC GET/POST endpoints + Actuator) | High |

---

## Containerization & Orchestration

| Fact | Value | Confidence |
|------|-------|------------|
| **Container Engine** | Not configured (no Dockerfile/Containerfile) | High |
| **Base Image** | Not applicable | High |
| **Image Size** | Not applicable | High |
| **Image Layers** | Not applicable | High |
| **Multi-stage Build** | Not applicable | High |
| **Container Version** | Not applicable | High |
| **Volume Mounts** | Not applicable | High |
| **Orchestration Tool** | Not configured | High |
| **Service Definition** | Not configured (no docker-compose or K8s manifests) | High |
| **Resource Limits** | Not configured | High |
| **Network Settings** | Not configured | High |
| **System Packages** | Not applicable | High |

---

## Observability & Operations

| Fact | Value | Confidence |
|------|-------|------------|
| **Health Checks** | Spring Boot Actuator `/actuator/health` available; no container-level probe configured | High |
| **Startup Instrumentation** | Default Spring Boot Logback logging; Spring Boot Actuator for metrics; no APM agent | High |

---

## Security

| Fact | Value | Confidence |
|------|-------|------------|
| **Security Implementation** | **None** — no Spring Security, no HTTPS/TLS, no authentication/authorization; all Actuator endpoints publicly exposed | High |

---

## Data & Compliance

| Fact | Value | Confidence |
|------|-------|------------|
| **Data Classification** | **PII** — owner names, addresses, cities, telephone numbers stored in MySQL | High |
| **Compliance Requirements** | No explicit compliance requirements detected | Medium |
| **Licensing Information** | Apache License 2.0 (declared in pom.xml); no LICENSE file in repo root | Medium |

---

## Key Findings for Cloud Migration

1. **No containerization** — Dockerfile and container configuration must be created before cloud deployment.
2. **No security** — Spring Security with authentication/authorization should be added before production deployment.
3. **PII data** — Owner personal data (name, address, phone) requires appropriate data protection measures.
4. **Azure-ready** — `spring-cloud-azure-starter-jdbc-mysql:5.16.0` already included for Azure Database for MySQL integration.
5. **Health endpoint available** — `/actuator/health` is ready to be wired into container liveness/readiness probes.
6. **MYSQL_PASSWORD defaults to empty** — Should be enforced as required before production.
7. **No test files** — Test infrastructure dependencies exist but no test source files are present in `src/test/java`.

---

## AppCAT Assessment

Assessment report generated: `.github/modernize/assessment/reports/report-20260409041719/report.json`

The AppCAT analysis was run against this Java 17 / Spring Boot 3.3.2 project to identify Azure migration issues and readiness.
