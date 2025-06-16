# Quality Standards Component

## Purpose
Provides standardized quality assessment frameworks, review processes, and compliance standards for the Reviewer agent role.

## Core Capabilities

### Code Review Framework
- **Structural Quality**: Architecture adherence, design pattern compliance, modularity
- **Implementation Quality**: Code clarity, efficiency, error handling, security
- **Documentation Quality**: Code comments, API documentation, usage examples
- **Test Coverage**: Unit tests, integration tests, edge case handling

### Quality Assessment Criteria
- **Functionality**: Requirements compliance, feature completeness, edge case handling
- **Reliability**: Error handling, fault tolerance, recovery mechanisms
- **Performance**: Efficiency, scalability, resource utilization
- **Security**: Vulnerability assessment, access control, data protection
- **Maintainability**: Code clarity, documentation, extensibility

### Standards Compliance
- **Coding Standards**: Style guidelines, naming conventions, formatting rules
- **Architecture Standards**: Design patterns, layer separation, dependency management
- **Documentation Standards**: Completeness, accuracy, clarity, consistency
- **Process Standards**: Development workflow, testing procedures, deployment practices

## Standard Review Process

### Review Workflow
1. **Pre-Review Preparation**: Understand requirements, review context, prepare checklist
2. **Structural Assessment**: Architecture review, design pattern evaluation, dependency analysis
3. **Implementation Review**: Code quality, logic correctness, performance considerations
4. **Security Assessment**: Vulnerability scan, access control review, data protection validation
5. **Documentation Review**: Completeness, accuracy, usability assessment
6. **Test Validation**: Coverage analysis, test quality, scenario completeness
7. **Compliance Check**: Standards adherence, process compliance, regulatory requirements
8. **Feedback Generation**: Detailed findings, improvement recommendations, priority classification

### Quality Metrics
- **Code Quality Score**: Complexity, maintainability, test coverage metrics
- **Security Score**: Vulnerability count, risk assessment, compliance level
- **Documentation Score**: Completeness, clarity, accuracy assessment
- **Process Compliance**: Workflow adherence, standard compliance, best practice adoption

## Review Categories

### Critical Issues (Must Fix)
- **Security Vulnerabilities**: Data exposure, access control failures, injection risks
- **Functional Defects**: Requirements non-compliance, critical functionality failures
- **Architecture Violations**: Design pattern violations, dependency issues, scalability problems
- **Safety Issues**: Data corruption risks, system stability threats

### Major Issues (Should Fix)
- **Performance Problems**: Inefficient algorithms, resource waste, scalability concerns
- **Maintainability Issues**: Code complexity, documentation gaps, extensibility problems
- **Standards Violations**: Coding standard deviations, process non-compliance
- **Usability Problems**: Poor user experience, accessibility issues

### Minor Issues (Could Fix)
- **Style Inconsistencies**: Formatting variations, naming convention deviations
- **Documentation Improvements**: Clarity enhancements, example additions
- **Code Optimization**: Performance tuning opportunities, refactoring suggestions
- **Best Practice Adoption**: Modern pattern usage, tool utilization improvements

## Integration Points
- Uses mcp_tools.md for discovering code, documentation, and related review artifacts
- Works with document_creation.md for standardized review reports and quality assessments
- Supports developer.md with implementation feedback and improvement guidance
- Provides quality gates for tester.md validation processes

## Quality Standards
- **Objectivity**: Fact-based assessment, consistent criteria application, bias elimination
- **Completeness**: Comprehensive coverage, systematic evaluation, nothing overlooked
- **Actionability**: Clear improvement recommendations, priority guidance, implementation support
- **Continuous Improvement**: Process refinement, standard evolution, best practice integration