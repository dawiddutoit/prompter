# Prompter Quick Start Guide

## TL;DR - 2 Commands to Get Started

```bash
# 1. Create your project with AI agents
.claude/commands/create_new_project.md --template web_app --name "my-project"

# 2. Start developing
cd my-project && .claude/commands/planner.md
```

That's it! You now have a complete project with specialized AI agents ready to help.

## Alternative: Guided Experience

```bash
# If you're not sure what you need
.claude/commands/prompter.md
```

## What Just Happened?

### Step 1: Project Initialization
The **initializer** created:
- 📁 Complete project structure (src/, docs/, tests/)
- 🔧 Basic configuration files (package.json, .gitignore)
- 📋 Project metadata (`.claude/project_config.yaml`)
- 📝 README with next steps
- 🔗 Git repository with initial commit

### Step 2: Agent Selection
The **agent_selector** created:
- 🤖 Specialized AI agents tailored to your project
- 📊 Smart recommendations based on project type
- 🎯 Project-specific knowledge and context
- 📚 Agent documentation and workflows

### Step 3: Development Ready
You now have:
- ✅ Project structure ready for development
- ✅ AI agents with project-specific expertise
- ✅ Clear workflow and documentation
- ✅ No additional setup required

## Available Project Templates

### Web Application (`web_app`)
**Best for**: Frontend + backend web applications
**Technology Stack**: React + Node.js + PostgreSQL
**Recommended Agents**: planner, architect, frontend_developer, backend_developer, devops_engineer

```bash
.claude/commands/initializer.md --template web_app --name "ecommerce-site"
```

### API Service (`api_service`)  
**Best for**: Backend APIs and microservices
**Technology Stack**: Node.js + PostgreSQL
**Recommended Agents**: planner, architect, backend_developer, devops_engineer

```bash
.claude/commands/initializer.md --template api_service --name "user-api"
```

### Slack Application (`slack_app`)
**Best for**: Slack bots and workspace integrations
**Technology Stack**: Slack Bolt Framework + Node.js
**Recommended Agents**: planner, slack_developer, backend_developer, security_engineer

```bash
.claude/commands/initializer.md --template slack_app --name "team-bot"
```

### Enterprise Application (`enterprise`)
**Best for**: Large-scale applications with security/compliance needs
**Technology Stack**: React + Node.js + PostgreSQL + Security
**Recommended Agents**: planner, architect, frontend_developer, backend_developer, devops_engineer, security_engineer

```bash
.claude/commands/initializer.md --template enterprise --name "customer-portal"
```

## Customizing Technology Preferences

You can specify technology preferences during initialization:

```bash
# Custom frontend framework
.claude/commands/initializer.md --template web_app --name "vue-app" --frontend Vue

# Custom backend language
.claude/commands/initializer.md --template web_app --name "python-app" --backend Python

# Custom database
.claude/commands/initializer.md --template web_app --name "mongo-app" --database MongoDB

# Multiple customizations
.claude/commands/initializer.md --template web_app --name "custom-app" --frontend Angular --backend Java --database MySQL
```

## Agent Selection Process

When you run `agent_selector.md --interactive`, you'll see:

```
📁 Project: my-project (web_application)

Based on your project type, here are recommended agents:

✅ Core Agents (Recommended)
[✓] planner - Project planning and requirements analysis
[✓] architect - System design and architecture planning

✅ Development Agents (Recommended)
[✓] frontend_developer - React development
[✓] backend_developer - Node.js API development

✅ Operations Agents
[ ] devops_engineer - Infrastructure and deployment

✅ Optional Agents
[ ] security_engineer - Security and compliance

Continue with these selections? (y/n)
```

## Your Generated Agents

After agent selection, you'll have specialized AI assistants:

### Core Agents
- **planner.md** - Project planning, requirements analysis, stakeholder coordination
- **architect.md** - System design, architecture decisions, technical leadership

### Development Agents  
- **frontend_developer.md** - React/Vue/Angular development, UI/UX implementation
- **backend_developer.md** - API development, database design, server-side architecture
- **slack_developer.md** - Slack bot development, workspace automation

### Operations Agents
- **devops_engineer.md** - Infrastructure automation, CI/CD, deployment
- **security_engineer.md** - Security assessment, compliance, threat analysis

## Starting Development

### Recommended Workflow

1. **Start with Planning**
   ```bash
   .claude/commands/planner.md
   ```
   - Analyze requirements
   - Create project roadmap
   - Identify technical challenges

2. **Design Architecture**
   ```bash
   .claude/commands/architect.md
   ```
   - System design
   - Technology decisions
   - Architecture documentation

3. **Begin Implementation**
   ```bash
   .claude/commands/frontend_developer.md  # For UI development
   .claude/commands/backend_developer.md   # For API development
   .claude/commands/slack_developer.md     # For Slack integration
   ```

4. **Setup Infrastructure**
   ```bash
   .claude/commands/devops_engineer.md
   ```
   - Deployment automation
   - CI/CD pipelines
   - Monitoring setup

5. **Security Review**
   ```bash
   .claude/commands/security_engineer.md
   ```
   - Security assessment
   - Compliance verification
   - Threat analysis

## What Makes This Different?

### Traditional Approach
- ❌ Generic AI prompts
- ❌ No project context
- ❌ Manual setup and configuration
- ❌ Inconsistent guidance

### Prompter Approach
- ✅ **Project-Specific**: Agents know your tech stack and requirements
- ✅ **Smart Recommendations**: Based on project type and best practices
- ✅ **Complete Setup**: Everything configured and ready to use
- ✅ **Consistent Quality**: Standardized patterns and validation

## Need Help?

- **Documentation**: Check `docs/` directory for detailed guides
- **Examples**: See complete project examples in the main README
- **Advanced Usage**: Learn about manual component assembly and customization
- **Troubleshooting**: Common issues and solutions in project documentation

## Next Steps

Once you're comfortable with the basic workflow:
- Explore advanced agent customization
- Learn about component assembly
- Use the validator for quality assurance
- Analyze interaction history for optimization

Welcome to systematic prompt engineering! 🚀