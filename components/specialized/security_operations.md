# Security Operations Component

## Purpose
Provides specialized security engineering patterns, threat analysis methodologies, and security operations expertise for SecOps Engineer agent role.

## Core Capabilities

### Security Assessment and Analysis
- **Threat Modeling**: STRIDE methodology, attack surface analysis, threat landscape assessment
- **Vulnerability Assessment**: Static analysis, dynamic testing, dependency scanning, penetration testing
- **Security Architecture Review**: Design pattern analysis, security controls evaluation, compliance assessment
- **Risk Assessment**: Risk quantification, business impact analysis, mitigation prioritization
- **Incident Response**: Threat detection, incident classification, response procedures, forensics

### Security Implementation
- **Authentication Systems**: Multi-factor authentication, SSO integration, identity providers
- **Authorization Frameworks**: RBAC, ABAC, policy engines, access control matrices
- **Encryption Implementation**: Data at rest, data in transit, key management, certificate handling
- **Security Monitoring**: SIEM integration, log analysis, anomaly detection, alerting systems
- **Compliance Frameworks**: SOC2, GDPR, HIPAA, PCI-DSS, ISO 27001 implementation

### DevSecOps Integration
- **Security in CI/CD**: Automated security testing, secure deployment pipelines, infrastructure as code
- **Container Security**: Image scanning, runtime protection, orchestration security, network policies
- **Cloud Security**: AWS/Azure/GCP security services, IAM policies, network security, monitoring
- **Infrastructure Security**: Network segmentation, firewall rules, intrusion detection, endpoint protection
- **Supply Chain Security**: Dependency management, software bill of materials, vendor assessment

## Standard Security Workflow

### Security Assessment Process
1. **Scope Definition**: Asset inventory, threat landscape analysis, compliance requirements
2. **Threat Modeling**: Attack vector identification, threat actor analysis, impact assessment
3. **Vulnerability Assessment**: Automated scanning, manual testing, code review, configuration audit
4. **Risk Analysis**: Vulnerability prioritization, business impact assessment, remediation planning
5. **Security Testing**: Penetration testing, security regression testing, compliance validation
6. **Remediation Planning**: Fix prioritization, timeline development, resource allocation
7. **Monitoring Implementation**: Detection rules, alerting, incident response procedures

### Security Implementation Standards
- **Defense in Depth**: Multiple security layers, redundant controls, fail-safe mechanisms
- **Zero Trust Architecture**: Identity verification, least privilege, continuous monitoring
- **Security by Design**: Threat modeling integration, secure coding practices, privacy by design
- **Continuous Security**: Automated testing, continuous monitoring, regular assessment

## Security Domains

### Application Security
- **Secure Development**: OWASP Top 10, secure coding standards, security testing integration
- **Input Validation**: Injection prevention, XSS protection, CSRF mitigation
- **Session Management**: Secure authentication, session handling, token management
- **API Security**: OAuth implementation, rate limiting, input validation, output encoding

### Infrastructure Security
- **Network Security**: Firewall configuration, network segmentation, intrusion detection
- **System Hardening**: OS configuration, patch management, service minimization
- **Monitoring and Logging**: Security event logging, log analysis, incident detection
- **Backup and Recovery**: Secure backup procedures, disaster recovery, business continuity

### Cloud Security
- **Identity and Access Management**: IAM policies, role-based access, service accounts
- **Data Protection**: Encryption at rest/transit, key management, data classification
- **Network Security**: VPC configuration, security groups, network monitoring
- **Compliance**: Cloud security frameworks, audit trails, compliance reporting

## Security Tools and Technologies

### Security Testing Tools
- **Static Analysis**: SonarQube, Checkmarx, Veracode, CodeQL, Semgrep
- **Dynamic Testing**: OWASP ZAP, Burp Suite, Nessus, OpenVAS, Qualys
- **Container Security**: Twistlock, Aqua Security, Trivy, Clair, Snyk
- **Infrastructure Testing**: Nmap, Metasploit, Nuclei, custom security scripts

### Monitoring and Detection
- **SIEM Platforms**: Splunk, Elastic Security, IBM QRadar, Microsoft Sentinel
- **Log Management**: ELK stack, Fluentd, centralized logging, log correlation
- **Incident Response**: TheHive, Phantom, Cortex, custom playbooks
- **Threat Intelligence**: MISP, threat feeds, IOC management, threat hunting

### Compliance and Governance
- **Policy Management**: Security policies, procedures, standards documentation
- **Audit and Assessment**: Compliance audits, security assessments, gap analysis
- **Risk Management**: Risk registers, treatment plans, monitoring procedures
- **Training and Awareness**: Security training, phishing simulations, awareness campaigns

## Security Patterns

### Authentication Patterns
- **Multi-Factor Authentication**: TOTP, FIDO2, biometric authentication
- **Single Sign-On**: SAML, OAuth2, OpenID Connect, identity federation
- **Password Security**: Hashing algorithms, password policies, credential management
- **Session Security**: Token management, session timeout, secure cookies

### Authorization Patterns
- **Role-Based Access Control**: Role definition, permission assignment, inheritance
- **Attribute-Based Access Control**: Policy engines, dynamic authorization, context-aware decisions
- **Least Privilege**: Minimal access rights, just-in-time access, privilege escalation controls
- **Segregation of Duties**: Conflicting function separation, approval workflows, audit trails

### Data Protection Patterns
- **Encryption Standards**: AES, RSA, elliptic curve cryptography, key management
- **Data Classification**: Sensitivity levels, handling requirements, retention policies
- **Privacy Protection**: Data minimization, anonymization, consent management
- **Secure Communication**: TLS configuration, certificate management, secure protocols

## Integration Points
- Uses mcp_tools.md for security tool discovery and configuration management
- Works with document_creation.md for security documentation and incident reports
- Supports testing_strategies.md with security testing methodologies
- Integrates with development_workflows.md for secure development practices
- Uses agent_validation_checkpoints.md for security validation and compliance verification

## Security Validation Standards
- **Vulnerability Assessment**: Comprehensive scanning, manual verification, false positive analysis
- **Penetration Testing**: Controlled testing, exploitation verification, impact assessment
- **Compliance Validation**: Framework adherence, control effectiveness, audit readiness
- **Incident Response Testing**: Playbook validation, response time measurement, recovery verification
- **Security Metrics**: KPI tracking, trend analysis, continuous improvement

## Quality Standards
- **Comprehensive Coverage**: All assets assessed, all threats considered, all controls validated
- **Risk-Based Approach**: Business-aligned priorities, cost-effective controls, measurable outcomes
- **Continuous Improvement**: Regular assessment, lessons learned, evolving threat response
- **Collaboration Focus**: Cross-functional security, security culture, shared responsibility