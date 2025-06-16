# Create New Project

## Role
Creates complete new projects with directory structure, configuration, and project-specific AI agents tailored to your technology stack and requirements.

## Core Capabilities

### Project Setup
- Create complete directory structure for new projects
- Generate initial component library from templates
- Set up project-specific configuration files
- **Prepare for agent selection workflow**

### Configuration Management
- Generate project-specific parameter files
- Create composition templates for different project types
- Set up validation rules and quality standards
- Initialize version control and documentation structure

### Agent Selection Preparation
- Create project metadata for agent_selector consumption
- Set up project context and requirements
- Generate clear handoff instructions for next steps

## Enhanced Initialization Workflow

1. **Project Analysis**: Understand project type, team structure, requirements
2. **Template Selection**: Choose appropriate base templates and components
3. **Directory Creation**: Set up complete project structure (src/, docs/, tests/)
4. **Configuration Generation**: Create project_config.yaml for agent_selector
5. **Git Repository Setup**: Initialize git with initial commit
6. **Documentation**: Generate README with clear next steps
7. **User Guidance**: Provide explicit command for agent selection
8. **Handoff**: Prepare project context for agent_selector workflow

**Key Output**: Complete project with specialized AI agents ready for development

## Project Templates

### Web Application Stack
```yaml
template: "web_app"
project_type: "web_application"
recommended_agents:
  core: ["planner", "architect"]
  development: ["frontend_developer", "backend_developer"]
  operations: ["devops_engineer"]
  optional: ["security_engineer"]
project_structure:
  - src/
  - docs/
  - tests/
  - infrastructure/
technology_defaults:
  frontend: "React"
  backend: "Node.js"
  database: "PostgreSQL"
  deployment: "AWS"
```

### API-First Project
```yaml
template: "api_service"
project_type: "api_service"
recommended_agents:
  core: ["planner", "architect"]
  development: ["backend_developer"]
  operations: ["devops_engineer"]
  optional: ["security_engineer", "frontend_developer"]
project_structure:
  - api/
  - docs/
  - tests/
  - infrastructure/
technology_defaults:
  backend: "Node.js"
  database: "PostgreSQL"
  deployment: "AWS"
```

### Slack Application
```yaml
template: "slack_app"
project_type: "slack_application"
recommended_agents:
  core: ["planner"]
  development: ["slack_developer", "backend_developer"]
  optional: ["security_engineer", "devops_engineer"]
project_structure:
  - src/
  - manifests/
  - docs/
  - tests/
technology_defaults:
  platform: "Slack Bolt Framework"
  backend: "Node.js"
  database: "PostgreSQL"
```

### Enterprise Application
```yaml
template: "enterprise"
project_type: "enterprise_application"
recommended_agents:
  core: ["planner", "architect"]
  development: ["frontend_developer", "backend_developer"]
  operations: ["devops_engineer", "security_engineer"]
  optional: []
project_structure:
  - frontend/
  - backend/
  - infrastructure/
  - security/
  - docs/
  - compliance/
technology_defaults:
  frontend: "React"
  backend: "Node.js"
  database: "PostgreSQL"
  deployment: "AWS"
  security: "SOC2"
```

## Generated Project Structure
```
my-project/
├── .claude/
│   ├── commands/           # Empty - populated by agent_selector
│   └── project_config.yaml # Project metadata for agent selection
├── src/                    # Application source code
├── docs/                   # Project documentation
├── tests/                  # Test directories
├── package.json           # Basic project configuration
├── README.md              # Setup guide + next steps
└── .gitignore             # Standard ignores
```

## Project Configuration Format
```yaml
# .claude/project_config.yaml
project:
  name: "my-project"
  type: "web_application"
  template: "web_app"
  created: "2025-01-16T10:30:00Z"
  status: "initialized"

recommended_agents:
  core: ["planner", "architect"]
  development: ["frontend_developer", "backend_developer"]
  operations: ["devops_engineer"]
  optional: ["security_engineer"]

technology_preferences:
  frontend: "React"
  backend: "Node.js"
  database: "PostgreSQL"
  deployment: "AWS"

project_requirements:
  - "Web application functionality"
  - "User authentication"
  - "Database integration"
  - "API development"

next_steps:
  command: "cd my-project && .claude/commands/planner.md"
  description: "Start development with your project-specific AI agents"
```

## Usage Examples

### Basic Project Creation
```bash
# Create new web application with AI agents
.claude/commands/create_new_project.md --template web_app --name "my-ecommerce"
# Output: "✅ Project created with specialized agents! Start: cd my-ecommerce && .claude/commands/planner.md"

# Create API service with AI agents
.claude/commands/create_new_project.md --template api_service --name "user-api"
# Output: "✅ API project created! Start: cd user-api && .claude/commands/planner.md"

# Create Slack application with AI agents
.claude/commands/create_new_project.md --template slack_app --name "team-assistant-bot"
# Output: "✅ Slack project created! Start: cd team-assistant-bot && .claude/commands/planner.md"
```

### With Technology Preferences
```bash
# Specify tech stack preferences
.claude/commands/initializer.md --template web_app --name "blog-platform" --frontend Vue --backend Python --database MongoDB
# Creates project_config.yaml with specified preferences
```

### Complete Workflow
```bash
# Step 1: Initialize project structure
.claude/commands/initializer.md --template web_app --name "blog-platform"

# Step 2: Select your development agents  
.claude/commands/agent_selector.md --interactive

# Step 3: Start development
.claude/commands/planner.md
```

## Command-Line Options

```bash
# Basic usage
.claude/commands/initializer.md --template <template_name> --name <project_name>

# Available templates
--template web_app           # Web application with frontend + backend
--template api_service       # Backend API service only
--template slack_app         # Slack bot/application
--template enterprise        # Full enterprise stack with security

# Optional customizations
--frontend <framework>       # React, Vue, Angular
--backend <framework>        # Node.js, Python, Java
--database <system>          # PostgreSQL, MongoDB, MySQL
--deployment <platform>      # AWS, Azure, GCP

# Advanced options
--path <custom_path>         # Custom project directory
--validation-level <level>   # standard, strict, minimal
```

## Generated README Template
```markdown
# {PROJECT_NAME}

## Project Status: Initialized ✅

Your project structure has been created successfully!

## Next Step: Select Your Development Agents

Run the following command to choose which AI agents you need for your project:

```bash
.claude/commands/agent_selector.md --interactive
```

This will analyze your project and help you select the right combination of agents for:
- Project planning and architecture
- {Frontend/Backend} development  
- DevOps and deployment
- Security and testing

## Project Structure

- `src/` - Your application source code
- `docs/` - Project documentation
- `tests/` - Test files
- `.claude/` - AI agent configurations (populated after agent selection)

## After Agent Selection

Once you've selected your agents, you'll have specialized AI assistants ready to help with:
- Requirements analysis and planning
- Code implementation and review
- Infrastructure setup and deployment
- Security assessment and testing

Start with: `.claude/commands/planner.md` (available after agent selection)
```

## Post-Initialization Output
```markdown
✅ Project "{PROJECT_NAME}" initialized successfully!

📁 Created:
- Complete project structure (src/, docs/, tests/)
- Git repository with initial commit
- Project configuration (.claude/project_config.yaml)
- Setup documentation (README.md)

🚀 Next Step:
.claude/commands/agent_selector.md --interactive

This will help you select the right AI agents for your {PROJECT_TYPE} project.

Template used: {TEMPLATE}
Technology preferences: {TECH_STACK}
```

## Integration Points

### With Agent Selector
- **Output**: Project structure + project_config.yaml
- **Handoff**: Clear instruction to run agent_selector
- **Context**: Project metadata for intelligent agent recommendations
- **Documentation**: Generated README with workflow guidance

### With Meta-Agents
- Uses Composer to generate initial templates
- Leverages Validator to ensure setup quality
- Provides foundation for Extractor to analyze existing projects

### Version Control
- Initializes git repository automatically
- Creates initial commit with descriptive message
- Sets up .gitignore with standard exclusions

## Quality Standards

### Initialization Validation
- ✅ Complete directory structure created
- ✅ Project configuration files generated
- ✅ Git repository initialized with initial commit
- ✅ Clear next-step instructions provided
- ✅ Project metadata ready for agent_selector

### User Experience
- ✅ Single command project setup
- ✅ Clear progress indicators
- ✅ Obvious next steps
- ✅ No ambiguity about workflow
- ✅ Seamless handoff to agent selection

### Template Quality
- ✅ Comprehensive project types covered
- ✅ Technology-specific defaults provided
- ✅ Scalable template system
- ✅ Consistent project structure

This initializer ensures users always know their next step and creates a smooth transition to agent selection and development.