# Security Assessment Report

**Generated:** 2026-05-26T03:29:05.429005+00:00

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 7 |
| CVE Vulnerabilities | 7 |
| CWE Vulnerabilities | 0 |
| Total Rules Assessed | 59 |
| Rules Passed | 59 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 7 |
| optional | 0 |
| potential | 0 |

## CVE Findings (Dependency Vulnerabilities)

### CVE-2026-43512: Apache Tomcat - Digest authenticator will authenticate any unknown user
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-43512](https://github.com/advisories/GHSA-h6fc-48rj-7qqh): Apache Tomcat - Digest authenticator will authenticate any unknown user

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: < 9.0.118, first patched: no patch available
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: >= 10.1.0-M1, < 10.1.55, first patched: no patch available
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: >= 11.0.0-M1, < 11.0.22, first patched: no patch available

Recommended fix:
  - Upgrade affected dependencies to the first patched version or later as noted above

### CVE-2026-43515: Apache Tomcat - Security constraints not correctly applied
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-43515](https://github.com/advisories/GHSA-5m62-pw8w-7w9f): Apache Tomcat - Security constraints not correctly applied

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: < 9.0.118, first patched: no patch available
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: >= 10.1.0-M1, < 10.1.55, first patched: no patch available
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: >= 11.0.0-M1, < 11.0.22, first patched: no patch available

Recommended fix:
  - Upgrade affected dependencies to the first patched version or later as noted above

### CVE-2026-41293: Apache Tomcat - HTTP/2 request headers not validated
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-41293](https://github.com/advisories/GHSA-r29c-68gh-xp6x): Apache Tomcat - HTTP/2 request headers not validated

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: < 9.0.118, first patched: no patch available
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: >= 10.1.0-M1, < 10.1.55, first patched: no patch available
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: >= 11.0.0-M1, < 11.0.22, first patched: no patch available

Recommended fix:
  - Upgrade affected dependencies to the first patched version or later as noted above

### CVE-2025-24813: Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-24813](https://github.com/advisories/GHSA-83qj-6fr2-vhqg): Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: >= 11.0.0-M1, < 11.0.3, first patched: no patch available
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: >= 10.1.0-M1, < 10.1.35, first patched: no patch available
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: >= 9.0.0.M1, < 9.0.99, first patched: no patch available
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml), vulnerable range: >= 8.5.0, <= 8.5.100, first patched: no patch available

Recommended fix:
  - Upgrade affected dependencies to the first patched version or later as noted above

### CVE-2026-41901: Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-41901](https://github.com/advisories/GHSA-c9ph-gxww-7744): Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (declared at pom.xml), vulnerable range: <= 3.1.4.RELEASE, first patched: no patch available
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (declared at pom.xml), vulnerable range: <= 3.1.4.RELEASE, first patched: no patch available

Recommended fix:
  - Upgrade affected dependencies to the first patched version or later as noted above

### CVE-2026-40478: Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-40478](https://github.com/advisories/GHSA-xjw8-8c5c-9r79): Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (declared at pom.xml), vulnerable range: <= 3.1.3.RELEASE, first patched: no patch available
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (declared at pom.xml), vulnerable range: <= 3.1.3.RELEASE, first patched: no patch available

Recommended fix:
  - Upgrade affected dependencies to the first patched version or later as noted above

### CVE-2026-40477: Improper restriction of the scope of accessible objects in Thymeleaf expressions
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-40477](https://github.com/advisories/GHSA-r4v4-5mwr-2fwr): Improper restriction of the scope of accessible objects in Thymeleaf expressions

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (declared at pom.xml), vulnerable range: <= 3.1.3.RELEASE, first patched: no patch available
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (declared at pom.xml), vulnerable range: <= 3.1.3.RELEASE, first patched: no patch available

Recommended fix:
  - Upgrade affected dependencies to the first patched version or later as noted above


## CWE Findings (Code-Level Vulnerabilities)

