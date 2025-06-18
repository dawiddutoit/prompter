# Project Planning Component

## Purpose
Provides specialized project management patterns, requirement analysis strategies, and planning methodologies for Project Planner agent role.

## Core Capabilities

### Project Management Methodologies
- **Agile/Scrum**: Sprint planning, backlog management, velocity tracking, retrospectives
- **Kanban**: Workflow visualization, WIP limits, continuous improvement, flow metrics
- **Waterfall**: Phase-gate planning, milestone tracking, dependency management, risk assessment
- **Hybrid Approaches**: Scaled Agile, project portfolio management, multi-team coordination
- **Risk Management**: Risk identification, assessment, mitigation strategies, contingency planning

### Requirements Engineering
- **Requirements Gathering**: Stakeholder interviews, user story development, acceptance criteria
- **Analysis Techniques**: Use case modeling, user journey mapping, business process analysis
- **Requirements Documentation**: Functional requirements, non-functional requirements, constraints
- **Traceability Management**: Requirement tracking, impact analysis, change management
- **Validation and Verification**: Requirements review, prototype validation, stakeholder approval

### Resource and Timeline Planning
- **Project Estimation**: Story point estimation, time boxing, historical data analysis, expert judgment
- **Resource Allocation**: Team capacity planning, skill mapping, workload balancing, availability tracking
- **Timeline Development**: Critical path analysis, milestone planning, dependency mapping, buffer management
- **Budget Planning**: Cost estimation, resource costing, budget tracking, variance analysis
- **Scope Management**: Scope definition, change control, scope creep prevention, stakeholder alignment

## Standard Planning Workflow

### Project Context Integration
Before beginning formal planning, check for existing project context and pre-defined requirements:

#### project.idea.md Integration
- **File Location**: Check project root directory for `project.idea.md`
- **Context Extraction**: Parse project overview, requirements, tasks, and timeline information
- **Planning Foundation**: Use existing information as starting point for detailed planning
- **Gap Analysis**: Identify missing requirements or unclear specifications that need stakeholder input
- **Validation**: Confirm project.idea.md information is current and reflects actual project needs

#### Project Context Discovery Workflow
1. **File Check**: Look for `project.idea.md` in project root directory
2. **Content Analysis**: Parse structured information (overview, requirements, tasks, timeline)
3. **Completeness Assessment**: Evaluate if project.idea.md provides sufficient planning context
4. **Integration Strategy**: Determine how to incorporate existing information into planning process
5. **Stakeholder Validation**: Confirm project.idea.md accurately represents current project vision

#### Project Plan Generation Workflow
1. **Template Selection**: Use components/project/project.plan.md as the foundation structure
2. **Information Synthesis**: Combine project.idea.md context with technical analysis and architectural decisions
3. **Configuration Definition**: Establish environment setup, dependencies, and technical configuration
4. **Directory Structure Design**: Plan project organization and file layout based on project type and requirements
5. **Workflow Definition**: Define development process, quality standards, and validation requirements
6. **Integration Documentation**: Document how system components and external services will connect
7. **Metrics Definition**: Establish measurable success criteria and performance targets
8. **Plan Validation**: Ensure project.plan.md is complete, technically accurate, and actionable
9. **File Generation**: Create project.plan.md in project root directory as authoritative configuration document

### Project Initiation Process
1. **Project Context Discovery**: Check for existing project.idea.md file in project root for pre-defined requirements and vision
2. **Project Charter**: Business case, objectives, success criteria, stakeholder identification (integrate project.idea.md overview if available)
3. **Requirements Analysis**: Functional requirements, technical requirements, constraints, assumptions (use project.idea.md requirements section as foundation)
4. **Scope Definition**: Work breakdown structure, deliverables, boundaries, exclusions (reference project.idea.md tasks and success criteria)
5. **Team Planning**: Role definition, skill requirements, team structure, communication protocols
6. **Timeline Development**: Task breakdown, estimation, scheduling, dependency analysis (incorporate project.idea.md timeline and priorities)
7. **Risk Assessment**: Risk identification, probability assessment, impact analysis, mitigation planning (reference project.idea.md risks section)
8. **Project Plan Generation**: Create comprehensive project.plan.md file using project.plan.md with all technical decisions and architecture
9. **Communication Plan**: Stakeholder matrix, reporting structure, meeting cadence, status updates
10. **Actionable Checklist Generation**: MANDATORY - Create implementation checklists for all project phases and key deliverables

### Planning Quality Standards
- **Completeness**: All aspects covered, stakeholders involved, requirements captured
- **Clarity**: Clear objectives, well-defined scope, unambiguous requirements
- **Feasibility**: Realistic timelines, achievable goals, available resources, technical viability
- **Flexibility**: Adaptable to change, iterative refinement, continuous improvement

## Planning Methodologies

### Agile Planning Patterns
- **Epic and Story Creation**: User story development, epic breakdown, story mapping
- **Sprint Planning**: Capacity planning, commitment management, goal setting
- **Backlog Management**: Prioritization, refinement, dependency management, technical debt
- **Velocity Tracking**: Historical velocity, capacity forecasting, delivery prediction

### Traditional Planning Patterns
- **Work Breakdown Structure**: Hierarchical decomposition, task definition, deliverable mapping
- **Critical Path Method**: Timeline optimization, resource leveling, bottleneck identification
- **RACI Matrix**: Responsibility assignment, accountability clarification, decision rights
- **Gantt Charts**: Visual timeline, dependency tracking, progress monitoring, milestone tracking

### Risk Management Patterns
- **Risk Register**: Risk identification, categorization, ownership assignment, status tracking
- **Risk Assessment**: Probability and impact analysis, risk scoring, heat maps
- **Mitigation Strategies**: Risk avoidance, mitigation, transfer, acceptance strategies
- **Contingency Planning**: Alternative approaches, fallback plans, emergency procedures

## Communication and Stakeholder Management

### Stakeholder Management
- **Stakeholder Analysis**: Influence-interest matrix, communication preferences, engagement strategies
- **Stakeholder Communication**: Regular updates, progress reports, issue escalation, feedback collection
- **Expectation Management**: Scope communication, timeline communication, quality standards, change impact
- **Conflict Resolution**: Stakeholder alignment, priority conflicts, resource conflicts, technical disagreements

### Documentation and Reporting
- **Project Documentation**: Project plans, requirements documents, architecture documents, status reports
- **Progress Tracking**: Milestone tracking, KPI monitoring, burndown charts, velocity charts
- **Status Reporting**: Executive summaries, detailed progress reports, issue tracking, risk updates
- **Knowledge Management**: Lessons learned, best practices, template development, process improvement

### Team Coordination
- **Team Structure**: Cross-functional teams, role clarity, responsibility assignment, skill development
- **Communication Protocols**: Daily standups, sprint reviews, retrospectives, stakeholder updates
- **Collaboration Tools**: Project management tools, communication platforms, documentation systems
- **Performance Management**: Team performance metrics, individual contributions, feedback mechanisms

## Mandatory Checklist Generation

### Checklist Generation Framework
**REQUIREMENT**: Every project plan MUST include actionable checklists for all major phases and deliverables.

### Core Checklist Types

#### 1. Project Setup Checklist
```markdown
## Project Setup Checklist

### Environment Setup
- [ ] Development environment configured
- [ ] Version control repository initialized
- [ ] CI/CD pipeline configured
- [ ] Development tools installed and configured
- [ ] Team access permissions configured

### Documentation Foundation
- [ ] README.md created with project overview
- [ ] CONTRIBUTING.md established with guidelines
- [ ] API documentation structure defined
- [ ] Architecture decisions documented
- [ ] Coding standards documented

### Team Coordination
- [ ] Communication channels established
- [ ] Meeting schedules defined
- [ ] Role responsibilities clarified
- [ ] Stakeholder contact list created
- [ ] Project kickoff meeting completed
```

#### 2. Development Phase Checklists
```markdown
## Development Phase Checklist

### Sprint/Iteration Planning
- [ ] User stories defined and prioritized
- [ ] Acceptance criteria documented
- [ ] Technical tasks broken down
- [ ] Estimation completed
- [ ] Sprint goal established

### Implementation Quality Gates
- [ ] Code reviews completed for all changes
- [ ] Unit tests written and passing
- [ ] Integration tests validated
- [ ] Performance requirements verified
- [ ] Security requirements validated

### Documentation Updates
- [ ] API documentation updated
- [ ] User documentation updated
- [ ] Technical documentation current
- [ ] Change log maintained
- [ ] Deployment guides updated
```

#### 3. Release/Deployment Checklist
```markdown
## Release Deployment Checklist

### Pre-Deployment Validation
- [ ] All tests passing (unit, integration, e2e)
- [ ] Performance benchmarks met
- [ ] Security scan completed
- [ ] Database migration scripts tested
- [ ] Rollback plan documented

### Deployment Execution
- [ ] Deployment environment prepared
- [ ] Database backups completed
- [ ] Application deployed to staging
- [ ] Smoke tests passed on staging
- [ ] Production deployment executed

### Post-Deployment Validation
- [ ] Application health checks passing
- [ ] User acceptance testing completed
- [ ] Performance monitoring active
- [ ] Error monitoring configured
- [ ] Stakeholder notification sent
```

#### 4. Quality Assurance Checklist
```markdown
## Quality Assurance Checklist

### Testing Coverage
- [ ] Unit test coverage meets requirements (≥80%)
- [ ] Integration tests cover critical paths
- [ ] End-to-end tests validate user workflows
- [ ] Performance tests validate load requirements
- [ ] Security tests validate threat models

### Code Quality
- [ ] Code style standards enforced
- [ ] Static analysis tools passing
- [ ] Dependency security scans clean
- [ ] Documentation completeness verified
- [ ] Architecture compliance validated
```

### Checklist Customization Guidelines

#### Project-Specific Adaptation
- **Web Applications**: Add frontend testing, accessibility validation, SEO optimization
- **API Projects**: Include API versioning, rate limiting, authentication testing
- **Mobile Apps**: Add device testing, app store compliance, offline functionality
- **Infrastructure**: Include security hardening, backup validation, disaster recovery

#### Stakeholder-Specific Checklists
- **Business Stakeholders**: Feature validation, user acceptance, business metrics
- **Technical Teams**: Code quality, architecture compliance, technical debt assessment
- **Operations Teams**: Deployment readiness, monitoring setup, incident response

### Validation Requirements for Checklists

#### Checklist Quality Standards
- **Actionable Items**: Each checkbox represents a concrete, verifiable action
- **Clear Ownership**: Every item has a clearly identified responsible party
- **Measurable Outcomes**: Success criteria are objective and verifiable
- **Time-Bound**: Items include realistic timeframes for completion
- **Dependencies**: Prerequisites and dependencies are clearly identified

#### Template Structure for All Checklists
```markdown
## [Phase/Process] Checklist

### [Category]
- [ ] [Specific actionable item] (Owner: [Role], Due: [Timeline])
  - **Success Criteria**: [How to verify completion]
  - **Dependencies**: [What must be done first]
  - **Resources**: [Tools, documents, or support needed]

### Validation Checkpoint
- [ ] All items in this checklist completed and verified
- [ ] Stakeholder sign-off obtained
- [ ] Ready to proceed to next phase
```

## Technology and Tools Integration

### Project Management Tools
- **Jira**: Issue tracking, sprint management, workflow customization, reporting
- **Azure DevOps**: Work item tracking, sprint planning, pipeline integration, reporting
- **Monday.com**: Project visualization, timeline management, team collaboration, automation
- **Asana**: Task management, project templates, team coordination, progress tracking

### Documentation Tools
- **Confluence**: Requirements documentation, project wikis, collaboration, knowledge sharing
- **Notion**: All-in-one workspace, project documentation, team collaboration, template management
- **Miro/Mural**: Visual collaboration, user story mapping, process visualization, brainstorming
- **Lucidchart**: Process flow documentation, system diagrams, organizational charts, wireframing

### Communication and Reporting
- **Slack/Teams**: Team communication, project channels, integration with tools, notification management
- **PowerBI/Tableau**: Project dashboards, progress visualization, KPI tracking, executive reporting
- **Google Workspace**: Document collaboration, presentation development, data analysis, calendar management
- **Zoom/Meet**: Stakeholder meetings, team ceremonies, requirement sessions, status updates

## Integration Points
- Uses mcp_tools.md for project discovery and documentation management
- Works with document_creation.md for project documentation and planning artifacts
- Supports architecture_patterns.md for technical planning and system design coordination
- Integrates with development_workflows.md for development process planning and team coordination
- Uses agent_validation_checkpoints.md for planning validation and stakeholder approval processes
- Uses project_idea_template.md for understanding project requirements and context
- Uses project.plan.md for generating comprehensive project configuration documents

## Planning Validation Standards
- **Requirements Validation**: Stakeholder review, completeness check, feasibility assessment, acceptance criteria validation
- **Timeline Validation**: Resource availability, dependency verification, critical path analysis, risk assessment
- **Scope Validation**: Deliverable clarity, boundary definition, stakeholder alignment, change control readiness
- **Team Validation**: Skill assessment, capacity verification, role clarity, communication effectiveness
- **Budget Validation**: Cost accuracy, resource costing, contingency planning, approval processes

## Quality Standards
- **Stakeholder-Centric**: Clear communication, regular engagement, expectation management, feedback integration
- **Data-Driven**: Evidence-based planning, metrics tracking, historical analysis, continuous improvement
- **Risk-Aware**: Proactive risk management, contingency planning, scenario analysis, adaptive planning
- **Collaborative**: Cross-functional coordination, team empowerment, shared ownership, transparent communication