# Build Custom Agent

## Role
Interactive command for building custom AI agents using the modular component system.

## Purpose
When standard agent templates don't meet your specific needs, this command helps you:
- Compose agents from individual components
- Create domain-specific expertise
- Customize agent behaviors and knowledge
- Build agents for unique workflows or technologies

## When to Use This Command

### Perfect For:
- **Specialized Domains**: DevSecOps, Data Science, Mobile Development, Game Development
- **Unique Technology Stacks**: Less common frameworks or languages
- **Custom Workflows**: Specific organizational processes or methodologies
- **Role Combinations**: Agents that blend multiple specialties

### Examples:
- Data Science agent with ML + Python + Cloud expertise
- DevSecOps agent combining DevOps + Security + Compliance
- Mobile developer with React Native + iOS + Android knowledge
- Game developer with Unity + C# + Graphics programming

## Available Components

### Core Components (Foundation)
- **thinking.md** - Structured reasoning with think tool
- **mcp_tools.md** - MCP filesystem tool patterns
- **document_creation.md** - Cross-agent document protocols
- **tool_usage.md** - Permission and efficiency guidelines
- **agent_validation_checkpoints.md** - Success verification protocols

### Specialized Components (Domain Expertise)
- **architecture_patterns.md** - System design and architecture guidance
- **development_workflows.md** - Implementation patterns and coding workflows
- **quality_standards.md** - Review processes and quality assessment
- **testing_strategies.md** - Testing methodologies and validation frameworks
- **research_methodologies.md** - Research and analysis approaches
- **frontend_development.md** - Frontend frameworks and UI/UX implementation
- **backend_development.md** - API design and server-side architecture
- **slack_integration.md** - Slack app development and bot implementation
- **security_operations.md** - Security assessment and implementation
- **devops_engineering.md** - Infrastructure automation and deployment
- **project_planning.md** - Project management and requirements analysis

## Interactive Agent Builder

### Step 1: Define Agent Purpose
```bash
.claude/commands/build_custom_agent.md --interactive
```

**You'll be prompted for:**
- Agent name and role description
- Primary domain or technology focus
- Target audience for agent outputs
- Specific expertise requirements

### Step 2: Component Selection
```
Building Custom Agent: Data Science Engineer

Select components for your agent:

✅ Core Components (Required)
[✓] thinking.md - Structured reasoning
[✓] mcp_tools.md - File system tools
[✓] document_creation.md - Documentation standards
[✓] agent_validation_checkpoints.md - Quality verification

✅ Specialized Components
[ ] backend_development.md - API and server-side development
[ ] research_methodologies.md - Research and analysis techniques
[ ] testing_strategies.md - Testing and validation approaches
[ ] quality_standards.md - Quality assessment processes

Custom Components Needed:
[ ] Create new: data_science_workflows.md
[ ] Create new: machine_learning_patterns.md
[ ] Create new: cloud_platforms.md

Continue with selection? (y/n)
```

### Step 3: Parameter Customization
```yaml
# Agent configuration
agent_name: "data_science_engineer"
role_description: "Data science development with ML pipeline expertise"

parameters:
  AGENT_NAME: "Data Science Engineer"
  ROLE_DESCRIPTION: "Machine learning pipeline development, data analysis, and model deployment"
  PRIMARY_TECHNOLOGIES: "Python, Jupyter, scikit-learn, TensorFlow, AWS SageMaker"
  VALIDATION_FOCUS: "Model accuracy, data quality, pipeline reliability"
  DOCUMENT_TYPES: "Data Analysis Report, Model Documentation, Pipeline Guide"
```

## Command Options

### Quick Custom Agent
```bash
# Specify components directly
.claude/commands/build_custom_agent.md \
  --name "mobile_developer" \
  --components "thinking.md,mcp_tools.md,frontend_development.md" \
  --role "React Native and native mobile development"
```

### Domain-Specific Templates
```bash
# Start with domain template
.claude/commands/build_custom_agent.md --template data_science --name "ml_engineer"
.claude/commands/build_custom_agent.md --template devops_security --name "devsecops"
```

## Generated Output

## Completion Message Template

When custom agent creation is complete, provide this exact message to the user:

```markdown
✅ Custom agent "{AGENT_NAME}" created successfully!

🎯 Your Specialized Agent:
- {AGENT_NAME}.md - {ROLE_DESCRIPTION}
- Domain expertise: {SPECIALIZED_DOMAINS}
- Technology focus: {TECHNOLOGY_STACK}
- Custom components: {CUSTOM_COMPONENTS}

📁 Files Created:
- .claude/commands/{AGENT_NAME}.md - Your custom agent
- compositions/{AGENT_NAME}.yaml - Agent configuration
- components/custom/{CUSTOM_COMPONENTS} - New domain components (if created)

🚀 Next Steps:
1. Test your custom agent:
   .claude/commands/{AGENT_NAME}.md

2. Use in projects:
   .claude/commands/add_agents_to_project.md --custom {AGENT_NAME}

3. Share with team:
   - Copy .claude/commands/{AGENT_NAME}.md to project directories at /Users/dawiddutoit/projects/play/{PROJECT_NAME}
   - Share compositions/{AGENT_NAME}.yaml for reuse
   - Use in new projects: .claude/commands/create_new_project.md --custom-agents {AGENT_NAME}

💡 Your custom agent has specialized knowledge that isn't available in standard templates, tailored to your specific domain and workflow.

Ready to use your specialized AI agent!
```

**Important**: Always provide clear next steps for testing and using the custom agent.

Your custom agent will have deep expertise in your specific domain while maintaining the quality and validation standards of the prompter system.