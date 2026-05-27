# Security Assessment Report

**Generated:** 2026-05-27T06:12:22.0000000Z

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 79 |
| CVE Vulnerabilities | 78 |
| CWE Vulnerabilities | 1 |
| Total Rules Assessed | 59 |
| Rules Passed | 58 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 38 |
| optional | 27 |
| potential | 14 |

## CVE Findings (Dependency Vulnerabilities)

### CVE-2024-12798: QOS.CH logback-core Expression Language Injection vulnerability
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:43

[CVE-2024-12798](https://github.com/advisories/GHSA-pr98-23f8-jwxv): QOS.CH logback-core Expression Language Injection vulnerability

Severity: MEDIUM

Affected dependencies:
  - ch.qos.logback:logback-core:1.5.6 (transitive, pulled by org.springframework.boot:spring-boot-starter-actuator at pom.xml:43)

Recommended fix:
  - 1.3.15

### CVE-2024-12801: QOS.CH logback-core Server-Side Request Forgery vulnerability
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:43

[CVE-2024-12801](https://github.com/advisories/GHSA-6v67-2wr5-gvf4): QOS.CH logback-core Server-Side Request Forgery vulnerability

Severity: LOW

Affected dependencies:
  - ch.qos.logback:logback-core:1.5.6 (transitive, pulled by org.springframework.boot:spring-boot-starter-actuator at pom.xml:43)

Recommended fix:
  - 1.3.15

### CVE-2024-25710: Apache Commons Compress: Denial of service caused by an infinite loop for a corrupted DUMP file
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:117

[CVE-2024-25710](https://github.com/advisories/GHSA-4g9r-vxhx-9pgx): Apache Commons Compress: Denial of service caused by an infinite loop for a corrupted DUMP file

Severity: MEDIUM

Affected dependencies:
  - org.apache.commons:commons-compress:1.24.0 (transitive, pulled by org.springframework.boot:spring-boot-testcontainers at pom.xml:117)

Recommended fix:
  - 1.26.0

### CVE-2024-26308: Apache Commons Compress: OutOfMemoryError unpacking broken Pack200 file
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:117

[CVE-2024-26308](https://github.com/advisories/GHSA-4265-ccf5-phj5): Apache Commons Compress: OutOfMemoryError unpacking broken Pack200 file

Severity: MEDIUM

Affected dependencies:
  - org.apache.commons:commons-compress:1.24.0 (transitive, pulled by org.springframework.boot:spring-boot-testcontainers at pom.xml:117)

Recommended fix:
  - 1.26.0

### CVE-2024-31573: XMLUnit for Java has Insecure Defaults when Processing XSLT Stylesheets
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:72

[CVE-2024-31573](https://github.com/advisories/GHSA-chfm-68vv-pvw5): XMLUnit for Java has Insecure Defaults when Processing XSLT Stylesheets

Severity: LOW

Affected dependencies:
  - org.xmlunit:xmlunit-core:2.9.1 (transitive, pulled by org.springframework.boot:spring-boot-starter-test at pom.xml:72)

Recommended fix:
  - 2.10.0

### CVE-2024-38809: Spring Framework DoS via conditional HTTP request
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2024-38809](https://github.com/advisories/GHSA-2rmj-mq67-h97g): Spring Framework DoS via conditional HTTP request

Severity: MEDIUM

Affected dependencies:
  - org.springframework:spring-web:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 5.3.38

### CVE-2024-38816: Path traversal vulnerability in functional web frameworks
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2024-38816](https://github.com/advisories/GHSA-cx7f-g6mp-7hqm): Path traversal vulnerability in functional web frameworks

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 6.1.13

### CVE-2024-38819: Spring Framework Path Traversal vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2024-38819](https://github.com/advisories/GHSA-g5vr-rgqm-vf78): Spring Framework Path Traversal vulnerability

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 6.1.14

### CVE-2024-38820: Spring Framework DataBinder Case Sensitive Match Exception
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:47, pom.xml:55

[CVE-2024-38820](https://github.com/advisories/GHSA-4gc7-5j7h-4qph): Spring Framework DataBinder Case Sensitive Match Exception

Severity: MEDIUM

Affected dependencies:
  - org.springframework:spring-context:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-cache at pom.xml:47)
  - org.springframework:spring-web:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 6.1.14

### CVE-2024-47535: Denial of Service attack on windows app using netty
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2024-47535](https://github.com/advisories/GHSA-xq3w-v528-46rv): Denial of Service attack on windows app using netty

Severity: MEDIUM

Affected dependencies:
  - io.netty:netty-common:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.115.Final

### CVE-2024-50379: Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2024-50379](https://github.com/advisories/GHSA-5j33-cvvr-w245): Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.34

### CVE-2024-56337: Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2024-56337](https://github.com/advisories/GHSA-27hp-xhwr-wr2m): Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.34

### CVE-2024-57699: Netplex Json-smart Uncontrolled Recursion vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:72

[CVE-2024-57699](https://github.com/advisories/GHSA-pq2g-wx69-c263): Netplex Json-smart Uncontrolled Recursion vulnerability

Severity: HIGH

Affected dependencies:
  - net.minidev:json-smart:2.5.1 (transitive, pulled by org.springframework.boot:spring-boot-starter-test at pom.xml:72)

Recommended fix:
  - 2.5.2

### CVE-2025-11226: QOS.CH logback-core is vulnerable to Arbitrary Code Execution through file processing
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:43

[CVE-2025-11226](https://github.com/advisories/GHSA-25qh-j22f-pwp8): QOS.CH logback-core is vulnerable to Arbitrary Code Execution through file processing

Severity: MEDIUM

Affected dependencies:
  - ch.qos.logback:logback-core:1.5.6 (transitive, pulled by org.springframework.boot:spring-boot-starter-actuator at pom.xml:43)

Recommended fix:
  - 1.3.16

### CVE-2025-22227: Reactor Netty HTTP is vulnerable to credential leaks during chained redirects
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2025-22227](https://github.com/advisories/GHSA-4q2v-9p7v-3v22): Reactor Netty HTTP is vulnerable to credential leaks during chained redirects

Severity: MEDIUM

Affected dependencies:
  - io.projectreactor.netty:reactor-netty-http:1.1.21 (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 1.2.8

### CVE-2025-22233: Spring Framework DataBinder Case Sensitive Match Exception
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:47

[CVE-2025-22233](https://github.com/advisories/GHSA-4wp7-92pw-q264): Spring Framework DataBinder Case Sensitive Match Exception

Severity: LOW

Affected dependencies:
  - org.springframework:spring-context:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-cache at pom.xml:47)

Recommended fix:
  - 6.1.20

### CVE-2025-22235: Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:112

[CVE-2025-22235](https://github.com/advisories/GHSA-rc42-6c7j-7h5r): Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot:3.3.2 (transitive, pulled by org.springframework.boot:spring-boot-devtools at pom.xml:112)

Recommended fix:
  - 3.3.11

### CVE-2025-24813: Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-24813](https://github.com/advisories/GHSA-83qj-6fr2-vhqg): Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.35

### CVE-2025-24970: SslHandler doesn't correctly validate packets which can lead to native crash when using native SSLEngine
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2025-24970](https://github.com/advisories/GHSA-4g8c-wm8x-jfhw): SslHandler doesn't correctly validate packets which can lead to native crash when using native SSLEngine

Severity: HIGH

Affected dependencies:
  - io.netty:netty-handler:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.118.Final

### CVE-2025-25193: Denial of Service attack on windows app using Netty
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2025-25193](https://github.com/advisories/GHSA-389x-839f-4rhx): Denial of Service attack on windows app using Netty

Severity: MEDIUM

Affected dependencies:
  - io.netty:netty-common:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.118.Final

### CVE-2025-31650: Apache Tomcat Denial of Service via invalid HTTP priority header
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-31650](https://github.com/advisories/GHSA-3p2h-wqq4-wf4h): Apache Tomcat Denial of Service via invalid HTTP priority header

Severity: MEDIUM

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.40

### CVE-2025-31651: Apache Tomcat Rewrite rule bypass
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-31651](https://github.com/advisories/GHSA-ff77-26x5-69cr): Apache Tomcat Rewrite rule bypass

Severity: LOW

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.40

### CVE-2025-41234: Spring Framework vulnerable to a reflected file download (RFD)
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-41234](https://github.com/advisories/GHSA-6r3c-xf4w-jxjm): Spring Framework vulnerable to a reflected file download (RFD)

Severity: MEDIUM

Affected dependencies:
  - org.springframework:spring-web:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 6.1.21

### CVE-2025-41242: Spring Framework MVC Applications Path Traversal Vulnerability
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-41242](https://github.com/advisories/GHSA-r936-gwx5-v52f): Spring Framework MVC Applications Path Traversal Vulnerability

Severity: MEDIUM

Affected dependencies:
  - org.springframework:spring-webmvc:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 6.2.10

### CVE-2025-41249: Spring Framework annotation detection mechanism may result in improper authorization
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:72

[CVE-2025-41249](https://github.com/advisories/GHSA-jmp9-x22r-554x): Spring Framework annotation detection mechanism may result in improper authorization

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-core:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-test at pom.xml:72)

Recommended fix:
  - 6.2.11

### CVE-2025-46701: Apache Tomcat - CGI security constraint bypass
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-46701](https://github.com/advisories/GHSA-h2fw-rfh5-95r3): Apache Tomcat - CGI security constraint bypass

Severity: LOW

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.41

### CVE-2025-48988: Apache Tomcat - DoS in multipart upload
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-48988](https://github.com/advisories/GHSA-h3gc-qfqq-6h8f): Apache Tomcat - DoS in multipart upload

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.42

### CVE-2025-48989: Apache Tomcat Improper Resource Shutdown or Release vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-48989](https://github.com/advisories/GHSA-gqp3-2cvr-x8m3): Apache Tomcat Improper Resource Shutdown or Release vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.44

### CVE-2025-49124: Apache Tomcat installer for Windows has an untrusted search path vulnerability
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-49124](https://github.com/advisories/GHSA-42wg-hm62-jcwg): Apache Tomcat installer for Windows has an untrusted search path vulnerability

Severity: MEDIUM

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.42

### CVE-2025-49125: Apache Tomcat - Security constraint bypass for pre/post-resources
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-49125](https://github.com/advisories/GHSA-wc4r-xq3c-5cf3): Apache Tomcat - Security constraint bypass for pre/post-resources

Severity: MEDIUM

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.42

### CVE-2025-52520: Apache Tomcat Catalina is vulnerable to DoS attack through bypassing of size limits
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-52520](https://github.com/advisories/GHSA-wr62-c79q-cv37): Apache Tomcat Catalina is vulnerable to DoS attack through bypassing of size limits

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.43

### CVE-2025-53506: Apache Tomcat Coyote vulnerable to Denial of Service via excessive HTTP/2 streams
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-53506](https://github.com/advisories/GHSA-25xr-qj8w-c4vf): Apache Tomcat Coyote vulnerable to Denial of Service via excessive HTTP/2 streams

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.43

### CVE-2025-53864: Nimbus JOSE + JWT is vulnerable to DoS attacks when processing deeply nested JSON
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2025-53864](https://github.com/advisories/GHSA-xwmg-2g98-w7v9): Nimbus JOSE + JWT is vulnerable to DoS attacks when processing deeply nested JSON

Severity: MEDIUM

Affected dependencies:
  - com.nimbusds:nimbus-jose-jwt:9.37.3 (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 10.0.2

### CVE-2025-55163: Netty affected by MadeYouReset HTTP/2 DDoS vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2025-55163](https://github.com/advisories/GHSA-prj3-ccx8-p6x4): Netty affected by MadeYouReset HTTP/2 DDoS vulnerability

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http2:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.124.Final

### CVE-2025-55752: Apache Tomcat Vulnerable to Relative Path Traversal
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-55752](https://github.com/advisories/GHSA-wmwf-9ccg-fff5): Apache Tomcat Vulnerable to Relative Path Traversal

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.45

### CVE-2025-55754: Apache Tomcat Vulnerable to Improper Neutralization of Escape, Meta, or Control Sequences
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-55754](https://github.com/advisories/GHSA-vfww-5hm6-hx2j): Apache Tomcat Vulnerable to Improper Neutralization of Escape, Meta, or Control Sequences

Severity: LOW

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.45

### CVE-2025-58056: Netty vulnerable to request smuggling due to incorrect parsing of chunk extensions
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2025-58056](https://github.com/advisories/GHSA-fghv-69vj-qj49): Netty vulnerable to request smuggling due to incorrect parsing of chunk extensions

Severity: LOW

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.125.Final

### CVE-2025-58057: Netty's decoders vulnerable to DoS via zip bomb style attack
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2025-58057](https://github.com/advisories/GHSA-3p8m-j85q-pgmj): Netty's decoders vulnerable to DoS via zip bomb style attack

Severity: MEDIUM

Affected dependencies:
  - io.netty:netty-codec:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.125.Final

### CVE-2025-61795: Apache Tomcat Vulnerable to Improper Resource Shutdown or Release
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-61795](https://github.com/advisories/GHSA-hgrr-935x-pq79): Apache Tomcat Vulnerable to Improper Resource Shutdown or Release

Severity: LOW

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.47

### CVE-2025-66614: Apache Tomcat - Client certificate verification bypass
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2025-66614](https://github.com/advisories/GHSA-fpj8-gq4v-p354): Apache Tomcat - Client certificate verification bypass

Severity: MEDIUM

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.50

### CVE-2025-67735: Netty has a CRLF Injection vulnerability in io.netty.handler.codec.http.HttpRequestEncoder
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2025-67735](https://github.com/advisories/GHSA-84h7-rjj3-6jx4): Netty has a CRLF Injection vulnerability in io.netty.handler.codec.http.HttpRequestEncoder

Severity: MEDIUM

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.129.Final

### CVE-2026-1225: Logback allows an attacker to instantiate classes already present on the class path
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:43

[CVE-2026-1225](https://github.com/advisories/GHSA-qqpg-mvqg-649v): Logback allows an attacker to instantiate classes already present on the class path

Severity: LOW

Affected dependencies:
  - ch.qos.logback:logback-core:1.5.6 (transitive, pulled by org.springframework.boot:spring-boot-starter-actuator at pom.xml:43)

Recommended fix:
  - 1.5.25

### CVE-2026-22733: Spring Boot has an Authentication Bypass under Actuator CloudFoundry endpoints
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:43

[CVE-2026-22733](https://github.com/advisories/GHSA-mgvc-8q2h-5pgc): Spring Boot has an Authentication Bypass under Actuator CloudFoundry endpoints

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot-starter-actuator:3.3.2 (declared at pom.xml:43)

Recommended fix:
  - 3.5.12

### CVE-2026-22735: Spring MVC and WebFlux has Server Sent Event stream corruption
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-22735](https://github.com/advisories/GHSA-6hcq-hmm3-jj3c): Spring MVC and WebFlux has Server Sent Event stream corruption

Severity: LOW

Affected dependencies:
  - org.springframework:spring-webmvc:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 6.2.17

### CVE-2026-22737: Spring Framework Improper Path Limitation with Script View Templates
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-22737](https://github.com/advisories/GHSA-4773-3jfm-qmx3): Spring Framework Improper Path Limitation with Script View Templates

Severity: MEDIUM

Affected dependencies:
  - org.springframework:spring-webmvc:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 6.2.17

### CVE-2026-22741: Spring MVC and WebFlux applications are vulnerable to cache poisoning when resolving static resources.
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-22741](https://github.com/advisories/GHSA-wg35-8jpf-2xv3): Spring MVC and WebFlux applications are vulnerable to cache poisoning when resolving static resources.

Severity: LOW

Affected dependencies:
  - org.springframework:spring-webmvc:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 6.2.18

### CVE-2026-22745: Spring MVC and WebFlux applications are vulnerable to Denial of Service attacks when resolving static resources
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-22745](https://github.com/advisories/GHSA-6p4f-wcwh-5vvm): Spring MVC and WebFlux applications are vulnerable to Denial of Service attacks when resolving static resources

Severity: MEDIUM

Affected dependencies:
  - org.springframework:spring-webmvc:6.1.11 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 6.2.18

### CVE-2026-24400: AssertJ has XML External Entity (XXE) vulnerability when parsing untrusted XML via isXmlEqualTo assertion
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:72

[CVE-2026-24400](https://github.com/advisories/GHSA-rqfh-9r24-8c9r): AssertJ has XML External Entity (XXE) vulnerability when parsing untrusted XML via isXmlEqualTo assertion

Severity: HIGH

Affected dependencies:
  - org.assertj:assertj-core:3.25.3 (transitive, pulled by org.springframework.boot:spring-boot-starter-test at pom.xml:72)

Recommended fix:
  - 3.27.7

### CVE-2026-24733: Apache Tomcat - Security constraint bypass with HTTP/0.9
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-24733](https://github.com/advisories/GHSA-qq5r-98hh-rxc9): Apache Tomcat - Security constraint bypass with HTTP/0.9

Severity: LOW

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.50

### CVE-2026-24734: Apache Tomcat has an Improper Input Validation vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-24734](https://github.com/advisories/GHSA-mgp5-rv84-w37q): Apache Tomcat has an Improper Input Validation vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.52

### CVE-2026-24880: Apache Tomcat has an HTTP Request/Response Smuggling vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-24880](https://github.com/advisories/GHSA-563x-q5rq-57qp): Apache Tomcat has an HTTP Request/Response Smuggling vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.52

### CVE-2026-25854: Apache Tomcat has an Open Redirect vulnerability
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-25854](https://github.com/advisories/GHSA-9m3c-qcxr-9x87): Apache Tomcat has an Open Redirect vulnerability

Severity: MEDIUM

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.53

### CVE-2026-33870: Netty: HTTP Request Smuggling via Chunked Extension Quoted-String Parsing
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-33870](https://github.com/advisories/GHSA-pwqr-wmgm-9rr8): Netty: HTTP Request Smuggling via Chunked Extension Quoted-String Parsing

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.132.Final

### CVE-2026-33871: Netty HTTP/2 CONTINUATION Frame Flood DoS via Zero-Byte Frame Bypass
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-33871](https://github.com/advisories/GHSA-w9fj-cfpg-grvv): Netty HTTP/2 CONTINUATION Frame Flood DoS via Zero-Byte Frame Bypass

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http2:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.132.Final

### CVE-2026-34483: Apache Tomcat has an Improper Encoding or Escaping of Output vulnerability in the JsonAccessLogValve
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-34483](https://github.com/advisories/GHSA-rv64-5gf8-9qq8): Apache Tomcat has an Improper Encoding or Escaping of Output vulnerability in the JsonAccessLogValve

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.54

### CVE-2026-34487: Apache Tomcat vulnerable to Insertion of Sensitive Information into Log File
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-34487](https://github.com/advisories/GHSA-x4m4-345f-5h5g): Apache Tomcat vulnerable to Insertion of Sensitive Information into Log File

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.54

### CVE-2026-40477: Improper restriction of the scope of accessible objects in Thymeleaf expressions
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:63

[CVE-2026-40477](https://github.com/advisories/GHSA-r4v4-5mwr-2fwr): Improper restriction of the scope of accessible objects in Thymeleaf expressions

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at pom.xml:63)
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at pom.xml:63)

Recommended fix:
  - 3.1.4.RELEASE

### CVE-2026-40478: Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:63

[CVE-2026-40478](https://github.com/advisories/GHSA-xjw8-8c5c-9r79): Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at pom.xml:63)
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at pom.xml:63)

Recommended fix:
  - 3.1.4.RELEASE

### CVE-2026-40972: Spring Boot DevTools remote secret comparison is vulnerable to timing attacks
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:112

[CVE-2026-40972](https://github.com/advisories/GHSA-56v8-86gj-66jp): Spring Boot DevTools remote secret comparison is vulnerable to timing attacks

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot-devtools:3.3.2 (declared at pom.xml:112)

Recommended fix:
  - 3.5.14

### CVE-2026-40973: Spring Boot accepts predictable temp directory without ownership verification
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:112

[CVE-2026-40973](https://github.com/advisories/GHSA-wwpq-f5c3-7hvx): Spring Boot accepts predictable temp directory without ownership verification

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot:3.3.2 (transitive, pulled by org.springframework.boot:spring-boot-devtools at pom.xml:112)

Recommended fix:
  - 3.5.14

### CVE-2026-41284: Apache Tomcat: Unbounded read in WebDAV LOCK and  PROPFIND handling
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-41284](https://github.com/advisories/GHSA-gx5v-xp9w-j4cg): Apache Tomcat: Unbounded read in WebDAV LOCK and  PROPFIND handling

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.55

### CVE-2026-41293: Apache Tomcat - HTTP/2 request headers not validated
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-41293](https://github.com/advisories/GHSA-r29c-68gh-xp6x): Apache Tomcat - HTTP/2 request headers not validated

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.55

### CVE-2026-41417: Netty: Start-Line Injection in DefaultHttpRequest.setUri() Allows HTTP Request Smuggling and RTSP Request Injection
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-41417](https://github.com/advisories/GHSA-v8h7-rr48-vmmv): Netty: Start-Line Injection in DefaultHttpRequest.setUri() Allows HTTP Request Smuggling and RTSP Request Injection

Severity: MEDIUM

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.133.Final

### CVE-2026-41901: Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:63

[CVE-2026-41901](https://github.com/advisories/GHSA-c9ph-gxww-7744): Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.1.2.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at pom.xml:63)
  - org.thymeleaf:thymeleaf-spring6:3.1.2.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at pom.xml:63)

Recommended fix:
  - 3.1.5.RELEASE

### CVE-2026-42498: Apache Tomcat - WebSocket authentication header exposure
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-42498](https://github.com/advisories/GHSA-fv25-8xcx-gqjc): Apache Tomcat - WebSocket authentication header exposure

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.55

### CVE-2026-42578: Netty has HTTP Header Injection via HttpProxyHandler Disabled Validation (Incomplete Fix CVE-2025-67735)
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-42578](https://github.com/advisories/GHSA-45q3-82m4-75jr): Netty has HTTP Header Injection via HttpProxyHandler Disabled Validation (Incomplete Fix CVE-2025-67735)

Severity: LOW

Affected dependencies:
  - io.netty:netty-handler-proxy:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.133.Final

### CVE-2026-42579: Netty has a DNS Codec Input Validation Bypass (Encoder + Decoder)
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-42579](https://github.com/advisories/GHSA-cm33-6792-r9fm): Netty has a DNS Codec Input Validation Bypass (Encoder + Decoder)

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-dns:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.133.Final

### CVE-2026-42580: Netty vulnerable to HTTP Request Smuggling due to incorrect chunk size parsing
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-42580](https://github.com/advisories/GHSA-m4cv-j2px-7723): Netty vulnerable to HTTP Request Smuggling due to incorrect chunk size parsing

Severity: MEDIUM

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.133.Final

### CVE-2026-42581: Netty HTTP/1.0 TE+CL Coexistence Bypasses Smuggling Sanitization
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-42581](https://github.com/advisories/GHSA-xxqh-mfjm-7mv9): Netty HTTP/1.0 TE+CL Coexistence Bypasses Smuggling Sanitization

Severity: MEDIUM

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.133.Final

### CVE-2026-42583: Netty Lz4FrameDecoder is vulnerable to resource exhaustion 
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-42583](https://github.com/advisories/GHSA-mj4r-2hfc-f8p6): Netty Lz4FrameDecoder is vulnerable to resource exhaustion 

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.133.Final

### CVE-2026-42584: Netty has HttpClientCodec response desynchronization
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-42584](https://github.com/advisories/GHSA-57rv-r2g8-2cj3): Netty has HttpClientCodec response desynchronization

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.133.Final

### CVE-2026-42585: Netty vulnerable to HTTP Request Smuggling due to malformed Transfer-Encoding
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-42585](https://github.com/advisories/GHSA-38f8-5428-x5cv): Netty vulnerable to HTTP Request Smuggling due to malformed Transfer-Encoding

Severity: MEDIUM

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.133.Final

### CVE-2026-42587: Netty: HttpContentDecompressor maxAllocation bypass when Content-Encoding set to br/zstd/snappy leads to decompression bomb DoS
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-42587](https://github.com/advisories/GHSA-f6hv-jmp6-3vwv): Netty: HttpContentDecompressor maxAllocation bypass when Content-Encoding set to br/zstd/snappy leads to decompression bomb DoS

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)
  - io.netty:netty-codec-http2:4.1.111.Final (transitive, pulled by com.azure.spring:spring-cloud-azure-starter-jdbc-mysql at pom.xml:67)

Recommended fix:
  - 4.1.133.Final

### CVE-2026-43512: Apache Tomcat - Digest authenticator will authenticate any unknown user
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-43512](https://github.com/advisories/GHSA-h6fc-48rj-7qqh): Apache Tomcat - Digest authenticator will authenticate any unknown user

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.55

### CVE-2026-43513: Apache Tomcat: LockOutRealm treats user names as case-sensitive
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-43513](https://github.com/advisories/GHSA-5mp6-jrq3-r938): Apache Tomcat: LockOutRealm treats user names as case-sensitive

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.55

### CVE-2026-43514: Apache Tomcat - AJP secret compared in non-constant time
- **Severity:** potential
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-43514](https://github.com/advisories/GHSA-9m89-8frq-c98c): Apache Tomcat - AJP secret compared in non-constant time

Severity: LOW

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.55

### CVE-2026-43515: Apache Tomcat - Security constraints not correctly applied
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:55

[CVE-2026-43515](https://github.com/advisories/GHSA-5m62-pw8w-7w9f): Apache Tomcat - Security constraints not correctly applied

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:10.1.26 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at pom.xml:55)

Recommended fix:
  - 10.1.55

### GHSA-72hv-8253-57qq: jackson-core: Number Length Constraint Bypass in Async Parser Leads to Potential DoS Condition
- **Severity:** optional
- **Story Points:** 1
- **Files:** pom.xml:122

[GHSA-72hv-8253-57qq](https://github.com/advisories/GHSA-72hv-8253-57qq): jackson-core: Number Length Constraint Bypass in Async Parser Leads to Potential DoS Condition

Severity: MEDIUM

Affected dependencies:
  - com.fasterxml.jackson.core:jackson-core:2.17.2 (transitive, pulled by org.springframework.boot:spring-boot-docker-compose at pom.xml:122)

Recommended fix:
  - 2.18.6

## CWE Findings (Code-Level Vulnerabilities)

### CWE-732: Incorrect Permission Assignment for Critical Resource
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** src/main/resources/application.properties:17, pom.xml:43

The application exposes all Spring Boot actuator management endpoints over HTTP via `management.endpoints.web.exposure.include=*` in `src/main/resources/application.properties:17` while including the actuator module in `pom.xml:43`. In this codebase there is no Spring Security dependency or other access-control configuration protecting those endpoints, so sensitive operational resources are configured to be readable by unintended actors.
