# Security Assessment Report

**Generated:** 2026-06-01T09:23:23.0000000Z

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 8 |
| CVE Vulnerabilities | 7 |
| CWE Vulnerabilities | 1 |
| Total Rules Assessed | 59 |
| Rules Passed | 58 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 7 |
| potential | 1 |

## CVE Findings (Dependency Vulnerabilities)

### CVE-2026-43512: Apache Tomcat - Digest authenticator will authenticate any unknown user
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-43512](https://github.com/advisories/GHSA-h6fc-48rj-7qqh): Apache Tomcat - Digest authenticator will authenticate any unknown user

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml:55) → patch: 9.0.118

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.118 or later

### CVE-2026-43515: Apache Tomcat - Security constraints not correctly applied
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-43515](https://github.com/advisories/GHSA-5m62-pw8w-7w9f): Apache Tomcat - Security constraints not correctly applied

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml:55) → patch: 9.0.118

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.118 or later

### CVE-2026-41293: Apache Tomcat - HTTP/2 request headers not validated
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-41293](https://github.com/advisories/GHSA-r29c-68gh-xp6x): Apache Tomcat - HTTP/2 request headers not validated

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml:55) → patch: 9.0.118

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.118 or later

### CVE-2025-24813: Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-24813](https://github.com/advisories/GHSA-83qj-6fr2-vhqg): Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml:55) → patch: 11.0.3

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 11.0.3 or later

### CVE-2026-41901: Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:63

[CVE-2026-41901](https://github.com/advisories/GHSA-c9ph-gxww-7744): Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (declared at pom.xml:63) → patch: 3.1.5.RELEASE
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (declared at pom.xml:63) → patch: 3.1.5.RELEASE

Recommended fix:
  - Upgrade org.thymeleaf:thymeleaf to 3.1.5.RELEASE or later
  - Upgrade org.thymeleaf:thymeleaf-spring6 to 3.1.5.RELEASE or later

### CVE-2026-40478: Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:63

[CVE-2026-40478](https://github.com/advisories/GHSA-xjw8-8c5c-9r79): Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (declared at pom.xml:63) → patch: 3.1.4.RELEASE
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (declared at pom.xml:63) → patch: 3.1.4.RELEASE

Recommended fix:
  - Upgrade org.thymeleaf:thymeleaf to 3.1.4.RELEASE or later
  - Upgrade org.thymeleaf:thymeleaf-spring6 to 3.1.4.RELEASE or later

### CVE-2026-40477: Improper restriction of the scope of accessible objects in Thymeleaf expressions
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:63

[CVE-2026-40477](https://github.com/advisories/GHSA-r4v4-5mwr-2fwr): Improper restriction of the scope of accessible objects in Thymeleaf expressions

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (declared at pom.xml:63) → patch: 3.1.4.RELEASE
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (declared at pom.xml:63) → patch: 3.1.4.RELEASE

Recommended fix:
  - Upgrade org.thymeleaf:thymeleaf to 3.1.4.RELEASE or later
  - Upgrade org.thymeleaf:thymeleaf-spring6 to 3.1.4.RELEASE or later

## CWE Findings (Code-Level Vulnerabilities)

### CWE-778: Insufficient Logging
- **Category:** Credentials & Secrets
- **Severity:** potential
- **Story Points:** 3
- **Files:** src/main/java/org/springframework/samples/petclinic/owner/OwnerController.java, src/main/java/org/springframework/samples/petclinic/owner/PetController.java, src/main/java/org/springframework/samples/petclinic/owner/VisitController.java

The application controllers (OwnerController, PetController, VisitController) perform data-modifying operations (create, update) without any security event logging. No logger is declared or used in any of the main application controllers or service classes. Security-critical operations such as creating or updating owner/pet records, and adding visits are not logged, making audit trails and security incident detection impossible.

