# Security Assessment Report

**Generated:** 2026-04-10T08:33:20Z

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 1 |
| CVE Vulnerabilities | 1 |
| CWE Vulnerabilities | 0 |
| Total Rules Assessed | 59 |
| Rules Passed | 59 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 1 |
| optional | 0 |
| potential | 0 |

## CVE Findings (Dependency Vulnerabilities)

### CVE-2026-22733: Spring Boot has an Authentication Bypass under Actuator CloudFoundry endpoints
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:43

[CVE-2026-22733](https://github.com/advisories/GHSA-mgvc-8q2h-5pgc): Spring Boot has an Authentication Bypass under Actuator CloudFoundry endpoints

Severity: MANDATORY (High — CVSS 8.2)

Spring Boot applications with Actuator can be vulnerable to an "Authentication Bypass" vulnerability when an application endpoint that requires authentication is declared under the path used by the CloudFoundry Actuator endpoints. This issue affects Spring Security: from 3.3.0 through 3.3.17.

Affected dependencies:
  - org.springframework.boot:spring-boot-starter-actuator:3.3.2 (declared at pom.xml:43) — vulnerable range: >= 3.0.0, <= 3.3.13

Recommended fix:
  - Upgrade Spring Boot parent to 3.4.x or 3.5.x series and update spring-boot-starter-actuator accordingly (no patched version available in the 3.3.x line)

## CWE Findings (Code-Level Vulnerabilities)

No CWE vulnerabilities were detected. All 59 CWE rules across 6 categories passed.
