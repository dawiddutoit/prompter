# Architecture Patterns Component

## Purpose
Provides standardized architectural design patterns, decision-making frameworks, and system design methodologies for the Architect agent role.

## Core Capabilities

### Architecture Decision Records (ADR)
- **Structure**: Problem, Options, Decision, Consequences
- **Numbering**: Sequential ADR numbering (ADR-001, ADR-002, etc.)
- **Status**: Proposed → Accepted → Superseded
- **Cross-references**: Link related ADRs and implementation impacts

### System Design Framework
- **Context Analysis**: Business requirements, constraints, stakeholders
- **Quality Attributes**: Performance, security, scalability, maintainability
- **Architecture Views**: Logical, physical, development, process views
- **Trade-off Analysis**: Cost/benefit evaluation for design decisions

### Design Pattern Application
- **Enterprise Patterns**: Layered architecture, microservices, event-driven
- **Integration Patterns**: API design, data flow, service boundaries
- **Scalability Patterns**: Load balancing, caching, data partitioning
- **Security Patterns**: Authentication, authorization, data protection

## Standard Workflows

### Architecture Planning Process
1. **Requirements Analysis**: Gather functional and non-functional requirements
2. **Constraint Identification**: Technical, business, and regulatory constraints
3. **Design Exploration**: Generate multiple architectural options
4. **Trade-off Analysis**: Evaluate options against quality attributes
5. **Decision Documentation**: Create ADR with rationale and consequences
6. **Implementation Planning**: Define development phases and dependencies

### System Documentation Standards
- **High-level Overview**: System context and major components
- **Component Specifications**: Interface definitions, responsibilities, dependencies
- **Data Architecture**: Data models, flow patterns, storage strategies
- **Deployment Architecture**: Infrastructure, scaling, monitoring

## Integration Points
- Works with mcp_tools.md for discovering existing architecture documents
- Uses document_creation.md for standardized ADR and design document formats
- Supports developer.md agent with implementation-ready specifications
- Provides research targets for researcher.md agent validation

## Quality Standards
- **Traceability**: Requirements → Architecture → Implementation
- **Consistency**: Aligned patterns across system components
- **Completeness**: All major design decisions documented
- **Maintainability**: Clear evolution path and change impact analysis