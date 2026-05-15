# Security Assessment Report

**Generated:** 2026-05-15T06:19:15.0000000Z

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 30 |
| CVE Vulnerabilities | 30 |
| CWE Vulnerabilities | 0 |
| Total Rules Assessed | 59 |
| Rules Passed | 59 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 30 |
| optional | 0 |
| potential | 0 |

## CVE Findings (Dependency Vulnerabilities)

### CVE-2025-24813: Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-24813](https://github.com/advisories/GHSA-83qj-6fr2-vhqg): Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.3)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.35)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, < 9.0.99)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 8.5.0, <= 8.5.100)

Recommended fix:
  - Upgrade to patched version(s): 10.1.35, 11.0.3, 9.0.99
[CVE-2025-24813](https://github.com/advisories/GHSA-83qj-6fr2-vhqg): Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.3)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.35)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, < 9.0.99)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 8.5.0, <= 8.5.100)

Recommended fix:
  - Upgrade to patched version(s): 10.1.35, 11.0.3, 9.0.99

### CVE-2026-29145: Apache Tomcat: CLIENT_CERT authentication does not fail as expected
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-29145](https://github.com/advisories/GHSA-95jq-rwvf-vjx4): Apache Tomcat: CLIENT_CERT authentication does not fail as expected

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.83, < 9.0.116)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M7, < 10.1.53)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.20)

Recommended fix:
  - Upgrade to patched version(s): 10.1.53, 11.0.20, 9.0.116
[CVE-2026-29145](https://github.com/advisories/GHSA-95jq-rwvf-vjx4): Apache Tomcat: CLIENT_CERT authentication does not fail as expected

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.83, < 9.0.116)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M7, < 10.1.53)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.20)

Recommended fix:
  - Upgrade to patched version(s): 10.1.53, 11.0.20, 9.0.116

### CVE-2026-40477: Improper restriction of the scope of accessible objects in Thymeleaf expressions
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-40477](https://github.com/advisories/GHSA-r4v4-5mwr-2fwr): Improper restriction of the scope of accessible objects in Thymeleaf expressions

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (declared at pom.xml; vulnerable range: <= 3.1.3.RELEASE)
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (declared at pom.xml; vulnerable range: <= 3.1.3.RELEASE)

Recommended fix:
  - Upgrade to patched version(s): 3.1.4.RELEASE
[CVE-2026-40477](https://github.com/advisories/GHSA-r4v4-5mwr-2fwr): Improper restriction of the scope of accessible objects in Thymeleaf expressions

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (declared at pom.xml; vulnerable range: <= 3.1.3.RELEASE)
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (declared at pom.xml; vulnerable range: <= 3.1.3.RELEASE)

Recommended fix:
  - Upgrade to patched version(s): 3.1.4.RELEASE

### CVE-2026-40478: Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-40478](https://github.com/advisories/GHSA-xjw8-8c5c-9r79): Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (declared at pom.xml; vulnerable range: <= 3.1.3.RELEASE)
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (declared at pom.xml; vulnerable range: <= 3.1.3.RELEASE)

Recommended fix:
  - Upgrade to patched version(s): 3.1.4.RELEASE
[CVE-2026-40478](https://github.com/advisories/GHSA-xjw8-8c5c-9r79): Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (declared at pom.xml; vulnerable range: <= 3.1.3.RELEASE)
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (declared at pom.xml; vulnerable range: <= 3.1.3.RELEASE)

Recommended fix:
  - Upgrade to patched version(s): 3.1.4.RELEASE

### CVE-2026-41901: Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-41901](https://github.com/advisories/GHSA-c9ph-gxww-7744): Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (declared at pom.xml; vulnerable range: <= 3.1.4.RELEASE)
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (declared at pom.xml; vulnerable range: <= 3.1.4.RELEASE)

Recommended fix:
  - Upgrade to patched version(s): 3.1.5.RELEASE
[CVE-2026-41901](https://github.com/advisories/GHSA-c9ph-gxww-7744): Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (declared at pom.xml; vulnerable range: <= 3.1.4.RELEASE)
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (declared at pom.xml; vulnerable range: <= 3.1.4.RELEASE)

Recommended fix:
  - Upgrade to patched version(s): 3.1.5.RELEASE

### CVE-2024-38816: Path traversal vulnerability in functional web frameworks
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2024-38816](https://github.com/advisories/GHSA-cx7f-g6mp-7hqm): Path traversal vulnerability in functional web frameworks

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc:6.1.11 (declared at pom.xml; vulnerable range: >= 6.1.0, < 6.1.13)
  - org.springframework:spring-webmvc:6.1.11 (declared at pom.xml; vulnerable range: >= 6.0.0, <= 6.0.23)
  - org.springframework:spring-webmvc:6.1.11 (declared at pom.xml; vulnerable range: >= 5.3.0, <= 5.3.39)

Recommended fix:
  - Upgrade to patched version(s): 6.1.13
[CVE-2024-38816](https://github.com/advisories/GHSA-cx7f-g6mp-7hqm): Path traversal vulnerability in functional web frameworks

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc:6.1.11 (declared at pom.xml; vulnerable range: >= 6.1.0, < 6.1.13)
  - org.springframework:spring-webmvc:6.1.11 (declared at pom.xml; vulnerable range: >= 6.0.0, <= 6.0.23)
  - org.springframework:spring-webmvc:6.1.11 (declared at pom.xml; vulnerable range: >= 5.3.0, <= 5.3.39)

Recommended fix:
  - Upgrade to patched version(s): 6.1.13

### CVE-2024-38819: Spring Framework Path Traversal vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2024-38819](https://github.com/advisories/GHSA-g5vr-rgqm-vf78): Spring Framework Path Traversal vulnerability

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc:6.1.11 (declared at pom.xml; vulnerable range: >= 6.1.0, < 6.1.14)
  - org.springframework:spring-webmvc:6.1.11 (declared at pom.xml; vulnerable range: <= 5.3.39)
  - org.springframework:spring-webmvc:6.1.11 (declared at pom.xml; vulnerable range: >= 6.0.0, <= 6.0.23)

Recommended fix:
  - Upgrade to patched version(s): 6.1.14
[CVE-2024-38819](https://github.com/advisories/GHSA-g5vr-rgqm-vf78): Spring Framework Path Traversal vulnerability

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc:6.1.11 (declared at pom.xml; vulnerable range: >= 6.1.0, < 6.1.14)
  - org.springframework:spring-webmvc:6.1.11 (declared at pom.xml; vulnerable range: <= 5.3.39)
  - org.springframework:spring-webmvc:6.1.11 (declared at pom.xml; vulnerable range: >= 6.0.0, <= 6.0.23)

Recommended fix:
  - Upgrade to patched version(s): 6.1.14

### CVE-2024-50379: Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2024-50379](https://github.com/advisories/GHSA-5j33-cvvr-w245): Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.2)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.34)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, < 9.0.98)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 8.5.0, <= 8.5.100)

Recommended fix:
  - Upgrade to patched version(s): 10.1.34, 11.0.2, 9.0.98
[CVE-2024-50379](https://github.com/advisories/GHSA-5j33-cvvr-w245): Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.2)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.34)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, < 9.0.98)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 8.5.0, <= 8.5.100)

Recommended fix:
  - Upgrade to patched version(s): 10.1.34, 11.0.2, 9.0.98

### CVE-2024-56337: Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2024-56337](https://github.com/advisories/GHSA-27hp-xhwr-wr2m): Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.2)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.34)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, < 9.0.98)

Recommended fix:
  - Upgrade to patched version(s): 10.1.34, 11.0.2, 9.0.98
[CVE-2024-56337](https://github.com/advisories/GHSA-27hp-xhwr-wr2m): Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.2)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.34)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, < 9.0.98)

Recommended fix:
  - Upgrade to patched version(s): 10.1.34, 11.0.2, 9.0.98

### CVE-2024-57699: Netplex Json-smart Uncontrolled Recursion vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2024-57699](https://github.com/advisories/GHSA-pq2g-wx69-c263): Netplex Json-smart Uncontrolled Recursion vulnerability

Severity: HIGH

Affected dependencies:
  - net.minidev:json-smart:2.5.1 (declared at pom.xml; vulnerable range: >= 2.5.0, < 2.5.2)

Recommended fix:
  - Upgrade to patched version(s): 2.5.2
[CVE-2024-57699](https://github.com/advisories/GHSA-pq2g-wx69-c263): Netplex Json-smart Uncontrolled Recursion vulnerability

Severity: HIGH

Affected dependencies:
  - net.minidev:json-smart:2.5.1 (declared at pom.xml; vulnerable range: >= 2.5.0, < 2.5.2)

Recommended fix:
  - Upgrade to patched version(s): 2.5.2

### CVE-2025-22235: Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-22235](https://github.com/advisories/GHSA-rc42-6c7j-7h5r): Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: <= 2.7.24.2)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.1.0, <= 3.1.15.2)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.2.0, <= 3.2.13.2)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.3.0, <= 3.3.10)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.4.0, <= 3.4.4)

Recommended fix:
  - Upgrade to patched version(s): 3.3.11, 3.4.5
[CVE-2025-22235](https://github.com/advisories/GHSA-rc42-6c7j-7h5r): Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: <= 2.7.24.2)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.1.0, <= 3.1.15.2)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.2.0, <= 3.2.13.2)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.3.0, <= 3.3.10)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.4.0, <= 3.4.4)

Recommended fix:
  - Upgrade to patched version(s): 3.3.11, 3.4.5

### CVE-2025-24970: SslHandler doesn't correctly validate packets which can lead to native crash when using native SSLEngine
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-24970](https://github.com/advisories/GHSA-4g8c-wm8x-jfhw): SslHandler doesn't correctly validate packets which can lead to native crash when using native SSLEngine

Severity: HIGH

Affected dependencies:
  - io.netty:netty-handler:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.1.91.Final, <= 4.1.117.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.118.Final
[CVE-2025-24970](https://github.com/advisories/GHSA-4g8c-wm8x-jfhw): SslHandler doesn't correctly validate packets which can lead to native crash when using native SSLEngine

Severity: HIGH

Affected dependencies:
  - io.netty:netty-handler:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.1.91.Final, <= 4.1.117.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.118.Final

### CVE-2025-41249: Spring Framework annotation detection mechanism may result in improper authorization
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-41249](https://github.com/advisories/GHSA-jmp9-x22r-554x): Spring Framework annotation detection mechanism may result in improper authorization

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-core:6.1.11 (declared at pom.xml; vulnerable range: >= 5.3.0, <= 5.3.44)
  - org.springframework:spring-core:6.1.11 (declared at pom.xml; vulnerable range: >= 6.0.0, <= 6.1.22)
  - org.springframework:spring-core:6.1.11 (declared at pom.xml; vulnerable range: >= 6.2.0, <= 6.2.10)

Recommended fix:
  - Upgrade to patched version(s): 6.2.11
[CVE-2025-41249](https://github.com/advisories/GHSA-jmp9-x22r-554x): Spring Framework annotation detection mechanism may result in improper authorization

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-core:6.1.11 (declared at pom.xml; vulnerable range: >= 5.3.0, <= 5.3.44)
  - org.springframework:spring-core:6.1.11 (declared at pom.xml; vulnerable range: >= 6.0.0, <= 6.1.22)
  - org.springframework:spring-core:6.1.11 (declared at pom.xml; vulnerable range: >= 6.2.0, <= 6.2.10)

Recommended fix:
  - Upgrade to patched version(s): 6.2.11

### CVE-2025-48988: Apache Tomcat - DoS in multipart upload
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-48988](https://github.com/advisories/GHSA-h3gc-qfqq-6h8f): Apache Tomcat - DoS in multipart upload

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, <= 11.0.7)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, <= 10.1.41)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, <= 9.0.105)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 8.5.0, <= 8.5.100)

Recommended fix:
  - Upgrade to patched version(s): 10.1.42, 11.0.8, 9.0.106
[CVE-2025-48988](https://github.com/advisories/GHSA-h3gc-qfqq-6h8f): Apache Tomcat - DoS in multipart upload

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, <= 11.0.7)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, <= 10.1.41)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, <= 9.0.105)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 8.5.0, <= 8.5.100)

Recommended fix:
  - Upgrade to patched version(s): 10.1.42, 11.0.8, 9.0.106

### CVE-2025-48989: Apache Tomcat Improper Resource Shutdown or Release vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-48989](https://github.com/advisories/GHSA-gqp3-2cvr-x8m3): Apache Tomcat Improper Resource Shutdown or Release vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.10)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.44)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, < 9.0.108)

Recommended fix:
  - Upgrade to patched version(s): 10.1.44, 11.0.10, 9.0.108
[CVE-2025-48989](https://github.com/advisories/GHSA-gqp3-2cvr-x8m3): Apache Tomcat Improper Resource Shutdown or Release vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.10)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.44)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, < 9.0.108)

Recommended fix:
  - Upgrade to patched version(s): 10.1.44, 11.0.10, 9.0.108

### CVE-2025-52520: Apache Tomcat Catalina is vulnerable to DoS attack through bypassing of size limits
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-52520](https://github.com/advisories/GHSA-wr62-c79q-cv37): Apache Tomcat Catalina is vulnerable to DoS attack through bypassing of size limits

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.9)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.43)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, < 9.0.107)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 8.5.0, <= 8.5.100)

Recommended fix:
  - Upgrade to patched version(s): 10.1.43, 11.0.9, 9.0.107
[CVE-2025-52520](https://github.com/advisories/GHSA-wr62-c79q-cv37): Apache Tomcat Catalina is vulnerable to DoS attack through bypassing of size limits

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.9)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.43)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, < 9.0.107)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 8.5.0, <= 8.5.100)

Recommended fix:
  - Upgrade to patched version(s): 10.1.43, 11.0.9, 9.0.107

### CVE-2025-53506: Apache Tomcat Coyote vulnerable to Denial of Service via excessive HTTP/2 streams
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-53506](https://github.com/advisories/GHSA-25xr-qj8w-c4vf): Apache Tomcat Coyote vulnerable to Denial of Service via excessive HTTP/2 streams

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 8.5.0, <= 8.5.100)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, < 9.0.107)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.43)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.9)

Recommended fix:
  - Upgrade to patched version(s): 10.1.43, 11.0.9, 9.0.107
[CVE-2025-53506](https://github.com/advisories/GHSA-25xr-qj8w-c4vf): Apache Tomcat Coyote vulnerable to Denial of Service via excessive HTTP/2 streams

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 8.5.0, <= 8.5.100)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0.M1, < 9.0.107)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.43)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.9)

Recommended fix:
  - Upgrade to patched version(s): 10.1.43, 11.0.9, 9.0.107

### CVE-2025-55163: Netty affected by MadeYouReset HTTP/2 DDoS vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-55163](https://github.com/advisories/GHSA-prj3-ccx8-p6x4): Netty affected by MadeYouReset HTTP/2 DDoS vulnerability

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http2:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, <= 4.2.3.Final)
  - io.netty:netty-codec-http2:4.1.111.Final (declared at pom.xml; vulnerable range: <= 4.1.123.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.124.Final, 4.2.4.Final
[CVE-2025-55163](https://github.com/advisories/GHSA-prj3-ccx8-p6x4): Netty affected by MadeYouReset HTTP/2 DDoS vulnerability

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http2:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, <= 4.2.3.Final)
  - io.netty:netty-codec-http2:4.1.111.Final (declared at pom.xml; vulnerable range: <= 4.1.123.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.124.Final, 4.2.4.Final

### CVE-2025-55752: Apache Tomcat Vulnerable to Relative Path Traversal
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-55752](https://github.com/advisories/GHSA-wmwf-9ccg-fff5): Apache Tomcat Vulnerable to Relative Path Traversal

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.11)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.45)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0-M11, < 9.0.109)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 8.5.6, <= 8.5.100)

Recommended fix:
  - Upgrade to patched version(s): 10.1.45, 11.0.11, 9.0.109
[CVE-2025-55752](https://github.com/advisories/GHSA-wmwf-9ccg-fff5): Apache Tomcat Vulnerable to Relative Path Traversal

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.11)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.45)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.0-M11, < 9.0.109)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 8.5.6, <= 8.5.100)

Recommended fix:
  - Upgrade to patched version(s): 10.1.45, 11.0.11, 9.0.109

### CVE-2026-22733: Spring Boot has an Authentication Bypass under Actuator CloudFoundry endpoints
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:43

[CVE-2026-22733](https://github.com/advisories/GHSA-mgvc-8q2h-5pgc): Spring Boot has an Authentication Bypass under Actuator CloudFoundry endpoints

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot-starter-actuator:3.3.2 (declared at pom.xml:43; vulnerable range: >= 4.0.0-M1, < 4.0.4)
  - org.springframework.boot:spring-boot-starter-actuator:3.3.2 (declared at pom.xml:43; vulnerable range: >= 3.5.0, < 3.5.12)
  - org.springframework.boot:spring-boot-starter-actuator:3.3.2 (declared at pom.xml:43; vulnerable range: >= 3.4.0, <= 3.4.13)
  - org.springframework.boot:spring-boot-starter-actuator:3.3.2 (declared at pom.xml:43; vulnerable range: >= 3.0.0, <= 3.3.13)
  - org.springframework.boot:spring-boot-starter-actuator:3.3.2 (declared at pom.xml:43; vulnerable range: <= 2.7.18)

Recommended fix:
  - Upgrade to patched version(s): 3.5.12, 4.0.4
[CVE-2026-22733](https://github.com/advisories/GHSA-mgvc-8q2h-5pgc): Spring Boot has an Authentication Bypass under Actuator CloudFoundry endpoints

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot-starter-actuator:3.3.2 (declared at pom.xml:43; vulnerable range: >= 4.0.0-M1, < 4.0.4)
  - org.springframework.boot:spring-boot-starter-actuator:3.3.2 (declared at pom.xml:43; vulnerable range: >= 3.5.0, < 3.5.12)
  - org.springframework.boot:spring-boot-starter-actuator:3.3.2 (declared at pom.xml:43; vulnerable range: >= 3.4.0, <= 3.4.13)
  - org.springframework.boot:spring-boot-starter-actuator:3.3.2 (declared at pom.xml:43; vulnerable range: >= 3.0.0, <= 3.3.13)
  - org.springframework.boot:spring-boot-starter-actuator:3.3.2 (declared at pom.xml:43; vulnerable range: <= 2.7.18)

Recommended fix:
  - Upgrade to patched version(s): 3.5.12, 4.0.4

### CVE-2026-24734: Apache Tomcat has an Improper Input Validation vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-24734](https://github.com/advisories/GHSA-mgp5-rv84-w37q): Apache Tomcat has an Improper Input Validation vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.18)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M7, < 10.1.52)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.83, < 9.0.115)

Recommended fix:
  - Upgrade to patched version(s): 10.1.52, 11.0.18, 9.0.115
[CVE-2026-24734](https://github.com/advisories/GHSA-mgp5-rv84-w37q): Apache Tomcat has an Improper Input Validation vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.18)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M7, < 10.1.52)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.83, < 9.0.115)

Recommended fix:
  - Upgrade to patched version(s): 10.1.52, 11.0.18, 9.0.115

### CVE-2026-33870: Netty: HTTP Request Smuggling via Chunked Extension Quoted-String Parsing
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-33870](https://github.com/advisories/GHSA-pwqr-wmgm-9rr8): Netty: HTTP Request Smuggling via Chunked Extension Quoted-String Parsing

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (declared at pom.xml; vulnerable range: < 4.1.132.Final)
  - io.netty:netty-codec-http:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, < 4.2.10.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.132.Final, 4.2.10.Final
[CVE-2026-33870](https://github.com/advisories/GHSA-pwqr-wmgm-9rr8): Netty: HTTP Request Smuggling via Chunked Extension Quoted-String Parsing

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (declared at pom.xml; vulnerable range: < 4.1.132.Final)
  - io.netty:netty-codec-http:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, < 4.2.10.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.132.Final, 4.2.10.Final

### CVE-2026-33871: Netty HTTP/2 CONTINUATION Frame Flood DoS via Zero-Byte Frame Bypass
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-33871](https://github.com/advisories/GHSA-w9fj-cfpg-grvv): Netty HTTP/2 CONTINUATION Frame Flood DoS via Zero-Byte Frame Bypass

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http2:4.1.111.Final (declared at pom.xml; vulnerable range: < 4.1.132.Final)
  - io.netty:netty-codec-http2:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, < 4.2.10.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.132.Final, 4.2.11.Final
[CVE-2026-33871](https://github.com/advisories/GHSA-w9fj-cfpg-grvv): Netty HTTP/2 CONTINUATION Frame Flood DoS via Zero-Byte Frame Bypass

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http2:4.1.111.Final (declared at pom.xml; vulnerable range: < 4.1.132.Final)
  - io.netty:netty-codec-http2:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, < 4.2.10.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.132.Final, 4.2.11.Final

### CVE-2026-34483: Apache Tomcat has an Improper Encoding or Escaping of Output vulnerability in the JsonAccessLogValve
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-34483](https://github.com/advisories/GHSA-rv64-5gf8-9qq8): Apache Tomcat has an Improper Encoding or Escaping of Output vulnerability in the JsonAccessLogValve

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.40, < 9.0.116)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.54)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.21)

Recommended fix:
  - Upgrade to patched version(s): 10.1.54, 11.0.21, 9.0.116
[CVE-2026-34483](https://github.com/advisories/GHSA-rv64-5gf8-9qq8): Apache Tomcat has an Improper Encoding or Escaping of Output vulnerability in the JsonAccessLogValve

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.40, < 9.0.116)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.54)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.21)

Recommended fix:
  - Upgrade to patched version(s): 10.1.54, 11.0.21, 9.0.116

### CVE-2026-34487: Apache Tomcat vulnerable to Insertion of Sensitive Information into Log File
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-34487](https://github.com/advisories/GHSA-x4m4-345f-5h5g): Apache Tomcat vulnerable to Insertion of Sensitive Information into Log File

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.13, < 9.0.117)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.54)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.21)

Recommended fix:
  - Upgrade to patched version(s): 10.1.54, 11.0.21, 9.0.117
[CVE-2026-34487](https://github.com/advisories/GHSA-x4m4-345f-5h5g): Apache Tomcat vulnerable to Insertion of Sensitive Information into Log File

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 9.0.13, < 9.0.117)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 10.1.0-M1, < 10.1.54)
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (declared at pom.xml; vulnerable range: >= 11.0.0-M1, < 11.0.21)

Recommended fix:
  - Upgrade to patched version(s): 10.1.54, 11.0.21, 9.0.117

### CVE-2026-40973: Spring Boot accepts predictable temp directory without ownership verification
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-40973](https://github.com/advisories/GHSA-wwpq-f5c3-7hvx): Spring Boot accepts predictable temp directory without ownership verification

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 4.0.0, < 4.0.6)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.5.0, < 3.5.14)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.4.0, <= 3.4.15)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.3.0, <= 3.3.18)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: <= 2.7.32)

Recommended fix:
  - Upgrade to patched version(s): 3.5.14, 4.0.6
[CVE-2026-40973](https://github.com/advisories/GHSA-wwpq-f5c3-7hvx): Spring Boot accepts predictable temp directory without ownership verification

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 4.0.0, < 4.0.6)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.5.0, < 3.5.14)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.4.0, <= 3.4.15)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: >= 3.3.0, <= 3.3.18)
  - org.springframework.boot:spring-boot:3.3.2 (declared at pom.xml; vulnerable range: <= 2.7.32)

Recommended fix:
  - Upgrade to patched version(s): 3.5.14, 4.0.6

### CVE-2026-42579: Netty has a DNS Codec Input Validation Bypass (Encoder + Decoder)
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-42579](https://github.com/advisories/GHSA-cm33-6792-r9fm): Netty has a DNS Codec Input Validation Bypass (Encoder + Decoder)

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-dns:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, <= 4.2.12.Final)
  - io.netty:netty-codec-dns:4.1.111.Final (declared at pom.xml; vulnerable range: <= 4.1.132.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.133.Final, 4.2.13.Final
[CVE-2026-42579](https://github.com/advisories/GHSA-cm33-6792-r9fm): Netty has a DNS Codec Input Validation Bypass (Encoder + Decoder)

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-dns:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, <= 4.2.12.Final)
  - io.netty:netty-codec-dns:4.1.111.Final (declared at pom.xml; vulnerable range: <= 4.1.132.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.133.Final, 4.2.13.Final

### CVE-2026-42583: Netty Lz4FrameDecoder is vulnerable to resource exhaustion 
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-42583](https://github.com/advisories/GHSA-mj4r-2hfc-f8p6): Netty Lz4FrameDecoder is vulnerable to resource exhaustion 

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec:4.1.111.Final (declared at pom.xml; vulnerable range: <= 4.1.132.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.133.Final
[CVE-2026-42583](https://github.com/advisories/GHSA-mj4r-2hfc-f8p6): Netty Lz4FrameDecoder is vulnerable to resource exhaustion 

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec:4.1.111.Final (declared at pom.xml; vulnerable range: <= 4.1.132.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.133.Final

### CVE-2026-42584: Netty has HttpClientCodec response desynchronization
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-42584](https://github.com/advisories/GHSA-57rv-r2g8-2cj3): Netty has HttpClientCodec response desynchronization

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, <= 4.2.12.Final)
  - io.netty:netty-codec-http:4.1.111.Final (declared at pom.xml; vulnerable range: <= 4.1.132.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.133.Final, 4.2.13.Final
[CVE-2026-42584](https://github.com/advisories/GHSA-57rv-r2g8-2cj3): Netty has HttpClientCodec response desynchronization

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, <= 4.2.12.Final)
  - io.netty:netty-codec-http:4.1.111.Final (declared at pom.xml; vulnerable range: <= 4.1.132.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.133.Final, 4.2.13.Final

### CVE-2026-42587: Netty: HttpContentDecompressor maxAllocation bypass when Content-Encoding set to br/zstd/snappy leads to decompression bomb DoS
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-42587](https://github.com/advisories/GHSA-f6hv-jmp6-3vwv): Netty: HttpContentDecompressor maxAllocation bypass when Content-Encoding set to br/zstd/snappy leads to decompression bomb DoS

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, <= 4.2.12.Final)
  - io.netty:netty-codec-http2:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, <= 4.2.12.Final)
  - io.netty:netty-codec-http:4.1.111.Final (declared at pom.xml; vulnerable range: <= 4.1.132.Final)
  - io.netty:netty-codec-http2:4.1.111.Final (declared at pom.xml; vulnerable range: <= 4.1.132.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.133.Final, 4.2.13.Final
[CVE-2026-42587](https://github.com/advisories/GHSA-f6hv-jmp6-3vwv): Netty: HttpContentDecompressor maxAllocation bypass when Content-Encoding set to br/zstd/snappy leads to decompression bomb DoS

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, <= 4.2.12.Final)
  - io.netty:netty-codec-http2:4.1.111.Final (declared at pom.xml; vulnerable range: >= 4.2.0.Alpha1, <= 4.2.12.Final)
  - io.netty:netty-codec-http:4.1.111.Final (declared at pom.xml; vulnerable range: <= 4.1.132.Final)
  - io.netty:netty-codec-http2:4.1.111.Final (declared at pom.xml; vulnerable range: <= 4.1.132.Final)

Recommended fix:
  - Upgrade to patched version(s): 4.1.133.Final, 4.2.13.Final

## CWE Findings (Code-Level Vulnerabilities)

No CWE findings.
