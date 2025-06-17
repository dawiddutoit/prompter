# Prompter

Creates specialized AI agents for your development projects.

## What This Does

Instead of generic AI prompts, Prompter generates project-specific AI agents that understand your technology stack, requirements, and codebase.

## Quick Start

### New Project
```bash
# Create a web application project with specialized AI agents
.claude/commands/create_new_project.md --template web_app --name "my-shop"

# Start developing with your AI team
cd /Users/dawiddutoit/projects/play/my-shop
.claude/commands/planner.md           # Plan features and requirements
.claude/commands/frontend_developer.md  # Build React components
.claude/commands/backend_developer.md   # Create APIs and database
```

### Existing Project  
```bash
# Add AI agents to your existing project
.claude/commands/add_agents_to_project.md --analyze-current

# Use your new AI agents
.claude/commands/planner.md          # Analyze current project and plan next steps
```

### Not Sure What You Need?
```bash
# Interactive guide
.claude/commands/prompter.md
```

### Working on Prompter Itself?
```bash
# System navigation and architecture guide
components/core/prompter_system_navigation.md
```

## Available Project Types

| Template | Description | AI Agents Generated |
|----------|-------------|-------------------|
| `web_app` | Frontend + Backend web application | planner, architect, frontend_developer, backend_developer, devops_engineer |
| `api_service` | Backend API service | planner, architect, backend_developer, devops_engineer |
| `slack_app` | Slack bot/integration | planner, slack_developer, backend_developer, security_engineer |
| `enterprise` | Full enterprise stack | planner, architect, frontend_developer, backend_developer, devops_engineer, security_engineer |

## What You Get

After running a command, you'll have:

- **Complete project structure** (src/, docs/, tests/)
- **Specialized AI agents** that understand your specific project
- **MCP server references** for enhanced development capabilities
- **Git repository** with initial commit
- **Documentation** with clear next steps

### Example AI Agents

Each agent knows about your specific project:

- **planner.md** - Plans features for your e-commerce site
- **frontend_developer.md** - Builds React components for your shop
- **backend_developer.md** - Creates APIs for your product catalog
- **devops_engineer.md** - Sets up deployment for your specific stack

## Commands

| Command | Purpose |
|---------|---------|
| `prompter.md` | Interactive guide - start here if unsure |
| `create_new_project.md` | Create new project with AI agents |
| `add_agents_to_project.md` | Add AI agents to existing project |
| `build_custom_agent.md` | Create specialized AI agent |
| `improve_agent_quality.md` | Validate and improve agents |

## Examples

### E-commerce Site
```bash
.claude/commands/create_new_project.md --template web_app --name "online-store"
cd /Users/dawiddutoit/projects/play/online-store
.claude/commands/planner.md  # "Help me plan user authentication and product catalog"
```

### API Service
```bash
.claude/commands/create_new_project.md --template api_service --name "user-api"
cd /Users/dawiddutoit/projects/play/user-api  
.claude/commands/backend_developer.md  # "Create REST endpoints for user management"
```

### Slack Bot
```bash
.claude/commands/create_new_project.md --template slack_app --name "team-bot"
cd /Users/dawiddutoit/projects/play/team-bot
.claude/commands/slack_developer.md  # "Create a bot that tracks team standup responses"
```

### Custom Technology Stack
```bash
.claude/commands/create_new_project.md --template web_app --name "vue-app" --frontend Vue --backend Python
cd /Users/dawiddutoit/projects/play/vue-app
.claude/commands/frontend_developer.md  # Now knows Vue.js instead of React
```

## MCP Server Setup

If you need to set up or troubleshoot MCP servers, use the dedicated management project:

```bash
cd ~/projects/play/mcp_management/ && ./setup-mcp.sh
```

## That's It

Run a command, get a project with AI agents that understand your specific needs. No configuration, no setup - just start building.