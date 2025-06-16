# Agent Selector Command

## Role
Interactive command for selecting and setting up agents for a new project based on project type and requirements.

## Core Capabilities

### Project Type Analysis
- Analyze project requirements and recommend suitable agent combinations
- Support multiple project types: web applications, APIs, Slack apps, mobile apps, data projects
- Provide agent role explanations and capabilities overview
- Generate customized compositions based on selections

### Agent Selection Interface
- Present available agents with descriptions and use cases
- Allow multi-select agent combinations for complex projects
- Validate agent compatibility and suggest complementary agents
- Generate project-specific parameter configurations

### Automated Setup
- Create project directory structure
- Generate selected agent compositions with project-specific parameters
- Set up initial documentation templates
- Configure validation rules and quality standards

## Available Agents

### Core Development Agents
```yaml
planner:
  description: "Project planning, requirements analysis, and stakeholder coordination"
  use_cases: ["New projects", "Complex requirements", "Multi-team coordination"]
  complements: ["architect", "all development agents"]

architect:
  description: "System design and architecture planning"
  use_cases: ["Complex systems", "Technical leadership", "Architecture decisions"]
  complements: ["planner", "developer", "backend_developer"]

developer:
  description: "General implementation and coding"
  use_cases: ["Full-stack development", "Prototyping", "Small projects"]
  complements: ["architect", "frontend_developer", "backend_developer"]
```

### Specialized Development Agents
```yaml
frontend_developer:
  description: "Frontend development and UI/UX implementation"
  use_cases: ["React/Vue/Angular apps", "UI/UX implementation", "Client-side architecture"]
  complements: ["backend_developer", "designer", "planner"]

backend_developer:
  description: "Backend development and API implementation"
  use_cases: ["API development", "Database design", "Server-side architecture"]
  complements: ["frontend_developer", "devops_engineer", "security_engineer"]

slack_developer:
  description: "Slack application development and bot implementation"
  use_cases: ["Slack bots", "Workspace automation", "Team productivity tools"]
  complements: ["backend_developer", "security_engineer"]
```

### Operations and Security Agents
```yaml
devops_engineer:
  description: "DevOps automation and infrastructure management"
  use_cases: ["CI/CD setup", "Infrastructure automation", "Deployment optimization"]
  complements: ["backend_developer", "security_engineer", "architect"]

security_engineer:
  description: "Security assessment and implementation"
  use_cases: ["Security audits", "Compliance", "Threat analysis"]
  complements: ["devops_engineer", "backend_developer", "architect"]
```

## Project Type Templates

### Web Application Stack
```yaml
recommended_agents: ["planner", "architect", "frontend_developer", "backend_developer", "devops_engineer"]
optional_agents: ["security_engineer"]
project_structure:
  - frontend/
  - backend/
  - infrastructure/
  - docs/
```

### API-First Project
```yaml
recommended_agents: ["planner", "architect", "backend_developer", "devops_engineer"]
optional_agents: ["security_engineer", "frontend_developer"]
project_structure:
  - api/
  - infrastructure/
  - docs/
  - tests/
```

### Slack Application
```yaml
recommended_agents: ["planner", "slack_developer", "backend_developer"]
optional_agents: ["security_engineer", "devops_engineer"]
project_structure:
  - src/
  - manifests/
  - docs/
  - tests/
```

### Enterprise Application
```yaml
recommended_agents: ["planner", "architect", "frontend_developer", "backend_developer", "devops_engineer", "security_engineer"]
optional_agents: []
project_structure:
  - frontend/
  - backend/
  - infrastructure/
  - security/
  - docs/
  - compliance/
```

## Usage Workflow

### Interactive Selection Process

1. **Project Analysis**
   ```bash
   # Start agent selection process
   .claude/commands/agent_selector.md --interactive
   ```

2. **Project Type Selection**
   - Web Application (Frontend + Backend + Database)
   - API Service (Backend + Database only)
   - Slack Application (Bot + Integrations)
   - Mobile Application (Backend + Mobile Frontend)
   - Data Pipeline (Processing + Analytics)
   - Enterprise Application (Full stack + Security + Compliance)
   - Custom (Manual agent selection)

3. **Agent Selection Interface**
   ```
   Select agents for your project:
   
   ✅ Core Agents (Recommended)
   [ ] planner - Project planning and requirements analysis
   [ ] architect - System design and architecture planning
   
   ✅ Development Agents
   [ ] frontend_developer - React/Vue/Angular development
   [ ] backend_developer - API and database development
   [ ] slack_developer - Slack bot development
   
   ✅ Operations Agents
   [ ] devops_engineer - Infrastructure and deployment
   [ ] security_engineer - Security and compliance
   
   Continue with selection? (y/n)
   ```

4. **Project Configuration**
   ```
   Project Configuration:
   Project Name: my-web-app
   Project Type: web_application
   Technology Stack: React + Node.js + PostgreSQL
   Deployment: AWS with Kubernetes
   
   Generate agents with these settings? (y/n)
   ```

### Command-Line Options

```bash
# Interactive mode (recommended)
.claude/commands/agent_selector.md --interactive

# Quick setup with template
.claude/commands/agent_selector.md --template web_app --name "my-project"

# Custom agent selection
.claude/commands/agent_selector.md --agents "planner,frontend_developer,backend_developer" --name "my-project"

# Show available templates
.claude/commands/agent_selector.md --list-templates

# Show available agents
.claude/commands/agent_selector.md --list-agents
```

### Generated Output

After selection, the command generates:

```
my-project/
├── .claude/
│   └── commands/
│       ├── planner.md (generated)
│       ├── frontend_developer.md (generated)
│       ├── backend_developer.md (generated)
│       └── devops_engineer.md (generated)
├── compositions/
│   ├── planner.yaml (project-specific)
│   ├── frontend_developer.yaml (project-specific)
│   ├── backend_developer.yaml (project-specific)
│   └── devops_engineer.yaml (project-specific)
├── docs/
│   ├── README.md (project setup)
│   ├── AGENTS.md (agent roles and responsibilities)
│   └── WORKFLOW.md (team collaboration guide)
└── PROJECT_CONFIG.yaml (project metadata)
```

## Validation and Quality Assurance

### Pre-Generation Validation
- Verify agent compatibility
- Check for missing dependencies
- Validate project structure requirements
- Ensure required components are available

### Post-Generation Validation
- Run validator on all generated compositions
- Verify agent integration points
- Test project structure completeness
- Validate documentation consistency

### Quality Standards
- All generated agents include validation checkpoints
- Project-specific parameters properly configured
- Integration points clearly defined
- Documentation generated for team collaboration

## Integration Points

### Component Dependencies
- Uses all core components (thinking.md, mcp_tools.md, agent_validation_checkpoints.md)
- Integrates with specialized components based on agent selection
- References all composition templates
- Works with validator.md for quality assurance

### External Integration
- Supports existing project structures
- Integrates with Git repositories
- Compatible with various development environments
- Supports team collaboration workflows

## Usage Examples

### Example 1: New Web Application
```bash
.claude/commands/agent_selector.md --template web_app --name "ecommerce-platform"
# Generates: planner, architect, frontend_developer, backend_developer, devops_engineer
```

### Example 2: Slack Bot Project
```bash
.claude/commands/agent_selector.md --template slack_app --name "team-assistant-bot"
# Generates: planner, slack_developer, backend_developer, security_engineer
```

### Example 3: Custom Selection
```bash
.claude/commands/agent_selector.md --interactive
# Presents interactive menu for custom agent selection
```

### Example 4: Enterprise Project
```bash
.claude/commands/agent_selector.md --template enterprise --name "customer-portal"
# Generates: All agents with security and compliance focus
```

## Arguments Processing

When called with arguments, process the following:

```bash
# Parse command line arguments
--interactive: Launch interactive selection mode
--template <name>: Use predefined template (web_app, api_service, slack_app, enterprise)
--name <project_name>: Set project name
--agents <comma_separated>: Specify agents directly
--project-root <path>: Set project root directory
--tech-stack <stack>: Specify technology preferences
--list-templates: Show available templates
--list-agents: Show available agents with descriptions
--validate: Validate selections without generating
```

This agent selector command streamlines project setup by providing guided agent selection based on project requirements and automatically generating properly configured agent compositions.