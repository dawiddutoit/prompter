# Prompter Workflow Guide

## Complete Project Development Workflow

This guide shows you how to use Prompter's agents throughout your entire project lifecycle.

## Phase 1: Project Setup

### 1.1 Initialize Your Project
```bash
# Choose the template that matches your project type
.claude/commands/initializer.md --template web_app --name "my-project"

# Available templates:
# --template web_app      # Frontend + Backend web application
# --template api_service  # Backend API service
# --template slack_app    # Slack bot/integration
# --template enterprise   # Full enterprise stack with security
```

**What this creates:**
- Complete project directory structure
- Git repository with initial commit
- Project configuration for agent selection
- README with clear next steps

### 1.2 Select Your Development Team
```bash
.claude/commands/agent_selector.md --interactive
```

**What this does:**
- Reads your project configuration
- Recommends agents based on project type
- Allows customization of agent selection
- Generates specialized agents with project context

### 1.3 Verify Setup
After agent selection, you should have:
```
my-project/
├── .claude/commands/
│   ├── planner.md
│   ├── architect.md
│   ├── frontend_developer.md
│   ├── backend_developer.md
│   └── devops_engineer.md
├── src/
├── docs/
├── tests/
├── README.md
└── .gitignore
```

## Phase 2: Planning & Architecture

### 2.1 Requirements Analysis
```bash
.claude/commands/planner.md
```

**Use the planner to:**
- Analyze project requirements
- Create user stories and acceptance criteria
- Identify technical challenges and risks
- Plan development timeline and milestones
- Coordinate with stakeholders

**Expected outputs:**
- Project Charter
- Requirements Document
- Risk Assessment
- Development Timeline

### 2.2 System Architecture
```bash
.claude/commands/architect.md
```

**Use the architect to:**
- Design system architecture
- Make technology decisions
- Create technical specifications
- Plan database schema and API design
- Document architecture decisions (ADRs)

**Expected outputs:**
- System Architecture Document
- Technical Specifications
- Database Schema Design
- API Design Document
- Architecture Decision Records (ADRs)

## Phase 3: Development

### 3.1 Frontend Development
```bash
.claude/commands/frontend_developer.md
```

**Use the frontend developer to:**
- Implement user interface components
- Set up frontend build pipeline
- Implement state management
- Create responsive designs
- Integrate with backend APIs

**Expected outputs:**
- React/Vue/Angular components
- Frontend build configuration
- State management setup
- UI/UX implementation
- API integration code

### 3.2 Backend Development
```bash
.claude/commands/backend_developer.md
```

**Use the backend developer to:**
- Implement REST/GraphQL APIs
- Set up database connections and models
- Implement authentication and authorization
- Create business logic and services
- Set up error handling and logging

**Expected outputs:**
- API endpoints and routes
- Database models and migrations
- Authentication system
- Business logic implementation
- Error handling middleware

### 3.3 Slack Integration (if applicable)
```bash
.claude/commands/slack_developer.md
```

**Use the slack developer to:**
- Create Slack app and bot configuration
- Implement slash commands and interactions
- Set up event listeners and workflows
- Design Block Kit user interfaces
- Handle OAuth and permissions

**Expected outputs:**
- Slack app manifest
- Bot command handlers
- Event listeners
- Block Kit interfaces
- OAuth implementation

## Phase 4: Operations & Security

### 4.1 Infrastructure & Deployment
```bash
.claude/commands/devops_engineer.md
```

**Use the devops engineer to:**
- Set up CI/CD pipelines
- Configure containerization (Docker)
- Implement infrastructure as code
- Set up monitoring and logging
- Configure deployment automation

**Expected outputs:**
- CI/CD pipeline configuration
- Docker containers and compose files
- Infrastructure as code (Terraform/ARM)
- Monitoring setup (Prometheus/Grafana)
- Deployment scripts and automation

### 4.2 Security Assessment
```bash
.claude/commands/security_engineer.md
```

**Use the security engineer to:**
- Conduct security assessments
- Implement authentication and authorization
- Set up security monitoring
- Ensure compliance requirements
- Perform vulnerability testing

**Expected outputs:**
- Security Assessment Report
- Authentication/Authorization implementation
- Security monitoring setup
- Compliance documentation
- Vulnerability test results

## Phase 5: Quality Assurance

### 5.1 Cross-Agent Validation
Each agent includes validation checkpoints to ensure:
- Work is actually completed (not just claimed)
- Deliverables meet quality standards
- Integration points work correctly
- Documentation is complete and accurate

### 5.2 Project Validation
```bash
.claude/commands/validator.md --project-validation
```

**Use the validator to:**
- Verify all components are properly integrated
- Check that agents have completed their deliverables
- Validate project structure and documentation
- Ensure quality standards are met

## Agent Communication Patterns

### Handoff Protocols
Agents are designed to work together with clear handoff points:

```
planner → architect → developer → devops → security
   ↓         ↓           ↓         ↓        ↓
Project   System     Implementation  Deploy  Security
Charter   Design     & Testing       & Ops   Review
```

### Document-Based Communication
Agents communicate through standardized documents:
- **Project Charter** (planner → all agents)
- **System Design** (architect → developers)
- **API Documentation** (backend → frontend)
- **Deployment Guide** (devops → operations)
- **Security Report** (security → management)

### Cross-Agent Reviews
Agents can review each other's work:
```bash
# Architect reviews backend implementation
.claude/commands/architect.md "Review the API design and implementation"

# Security engineer reviews authentication
.claude/commands/security_engineer.md "Assess the authentication implementation"

# DevOps reviews deployment readiness
.claude/commands/devops_engineer.md "Validate deployment configuration"
```

## Common Workflows

### New Feature Development
1. **planner.md** - Analyze feature requirements
2. **architect.md** - Design feature architecture
3. **frontend_developer.md** - Implement UI components
4. **backend_developer.md** - Implement API endpoints
5. **devops_engineer.md** - Update deployment pipeline
6. **security_engineer.md** - Security review

### Bug Investigation and Fix
1. **Any relevant agent** - Investigate and diagnose
2. **developer.md** - Implement fix
3. **validator.md** - Verify fix quality
4. **devops_engineer.md** - Deploy fix

### Performance Optimization
1. **architect.md** - Analyze performance bottlenecks
2. **backend_developer.md** - Optimize API performance
3. **frontend_developer.md** - Optimize client performance
4. **devops_engineer.md** - Optimize infrastructure
5. **validator.md** - Validate improvements

### Security Incident Response
1. **security_engineer.md** - Assess security incident
2. **developer.md** - Implement security fixes
3. **devops_engineer.md** - Deploy emergency fixes
4. **planner.md** - Plan preventive measures

## Best Practices

### Start with Planning
Always begin new work with the planner to:
- Clarify requirements and objectives
- Identify potential issues early
- Coordinate across team members
- Set clear success criteria

### Document Decisions
Use agents to create proper documentation:
- Architecture decisions (architect)
- Implementation notes (developers)
- Deployment procedures (devops)
- Security protocols (security)

### Regular Validation
Use validation checkpoints throughout development:
- After major milestones
- Before deployments
- During code reviews
- When integrating components

### Cross-Agent Collaboration
Encourage agents to review each other's work:
- Architecture reviews by multiple agents
- Security reviews for all implementations
- Deployment readiness checks
- Quality assurance across the board

## Troubleshooting

### Agent Not Understanding Context
**Problem**: Agent doesn't seem to understand project specifics
**Solution**: Check that `.claude/project_config.yaml` exists and contains correct project information

### Missing Agent Commands
**Problem**: `.claude/commands/` directory is empty
**Solution**: Run `agent_selector.md --interactive` to generate project-specific agents

### Inconsistent Recommendations
**Problem**: Different agents providing conflicting advice
**Solution**: Use `planner.md` to coordinate and resolve conflicts, update project requirements

### Quality Issues
**Problem**: Agent outputs don't meet quality standards
**Solution**: Use `validator.md` to check quality and provide specific feedback for improvement

## Advanced Usage

### Custom Agent Creation
For specialized needs, you can create custom agents using the component system.

### Integration with Existing Projects
Use `extractor.md` to analyze existing prompts and migrate to the modular system.

### Team Collaboration
Multiple team members can use the same agents with consistent project context and standards.

### Continuous Improvement
Use `interaction_history_analyzer.md` to analyze usage patterns and optimize the system.

This workflow ensures systematic, high-quality development with clear accountability and validation at every step.