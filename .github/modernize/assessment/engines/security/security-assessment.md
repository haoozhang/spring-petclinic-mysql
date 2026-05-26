# Security Assessment Report
**Generated:** 2026-05-26T03:57:01.0000000Z
## Summary
| Metric | Count |
|--------|-------|
| Total Findings | 10 |
| CVE Vulnerabilities | 7 |
| CWE Vulnerabilities | 3 |
| Total Rules Assessed | 59 |
| Rules Passed | 56 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 7 |
| optional | 3 |
| potential | 0 |

## CVE Findings (Dependency Vulnerabilities)

### CVE-2025-24813: Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:54

[CVE-2025-24813](https://github.com/advisories/GHSA-83qj-6fr2-vhqg): Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:54)

Recommended fix:
  - Upgrade affected dependencies to vendor-patched versions

### CVE-2026-40477: Improper restriction of the scope of accessible objects in Thymeleaf expressions
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:62

[CVE-2026-40477](https://github.com/advisories/GHSA-r4v4-5mwr-2fwr): Improper restriction of the scope of accessible objects in Thymeleaf expressions

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at pom.xml:62)
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at pom.xml:62)

Recommended fix:
  - Upgrade affected dependencies to vendor-patched versions

### CVE-2026-40478: Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:62

[CVE-2026-40478](https://github.com/advisories/GHSA-xjw8-8c5c-9r79): Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at pom.xml:62)
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at pom.xml:62)

Recommended fix:
  - Upgrade affected dependencies to vendor-patched versions

### CVE-2026-41293: Apache Tomcat - HTTP/2 request headers not validated
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:54

[CVE-2026-41293](https://github.com/advisories/GHSA-r29c-68gh-xp6x): Apache Tomcat - HTTP/2 request headers not validated

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:54)

Recommended fix:
  - Upgrade affected dependencies to vendor-patched versions

### CVE-2026-41901: Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:62

[CVE-2026-41901](https://github.com/advisories/GHSA-c9ph-gxww-7744): Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at pom.xml:62)
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at pom.xml:62)

Recommended fix:
  - Upgrade affected dependencies to vendor-patched versions

### CVE-2026-43512: Apache Tomcat - Digest authenticator will authenticate any unknown user
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:54

[CVE-2026-43512](https://github.com/advisories/GHSA-h6fc-48rj-7qqh): Apache Tomcat - Digest authenticator will authenticate any unknown user

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:54)

Recommended fix:
  - Upgrade affected dependencies to vendor-patched versions

### CVE-2026-43515: Apache Tomcat - Security constraints not correctly applied
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:54

[CVE-2026-43515](https://github.com/advisories/GHSA-5m62-pw8w-7w9f): Apache Tomcat - Security constraints not correctly applied

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:54)

Recommended fix:
  - Upgrade affected dependencies to vendor-patched versions

## CWE Findings (Code-Level Vulnerabilities)

### CWE-259: Use of Hard-coded Password
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** src/main/resources/db/mysql/user.sql

Hard-coded database password literal 'petclinic' appears in src/main/resources/db/mysql/user.sql:7 in the SQL statement `IDENTIFIED BY 'petclinic'`, indicating a static password embedded in project resources.

### CWE-732: Incorrect Permission Assignment for Critical Resource
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** src/main/resources/db/mysql/user.sql

Broad permission assignment is present in src/main/resources/db/mysql/user.sql:7 with `GRANT ALL PRIVILEGES ON petclinic.* TO 'petclinic'@'%'`, granting full privileges from any host for the database account.

### CWE-798: Use of Hard-coded Credentials
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** src/main/resources/db/mysql/user.sql

Hard-coded database credentials are embedded in src/main/resources/db/mysql/user.sql:7 (`'petclinic'` username and `'petclinic'` password) inside the grant statement used to provision DB access.
