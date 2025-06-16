# Prompter - Modular Prompt Composition System

A system for creating and managing AI agent prompts using reusable, modular components instead of monolithic files.

## Problem Solved

Traditional AI agent prompts suffer from:
- **60-70% content duplication** across agent definitions
- **Maintenance overhead** requiring updates to multiple files for shared changes
- **Inconsistency** when patterns diverge between agents over time
- **Complexity** with 400-500 line monolithic prompt files

## Solution

Prompter provides a modular composition system that:
- **Eliminates duplication** through shared components
- **Ensures consistency** via single-source-of-truth components
- **Simplifies maintenance** with component-based updates
- **Enables rapid iteration** through configurable composition

## Architecture

```
prompter/
├── .claude/
│   └── commands/        # Meta-agents (Composer, Extractor, Validator, Initializer)
├── components/          # Reusable prompt components
│   ├── core/           # Universal components (thinking, tools, docs)
│   ├── specialized/    # Domain-specific components  
│   └── meta/           # Meta-agent components
├── agents/             # Base agent definitions
├── compositions/       # Agent composition configurations
└── examples/           # Usage examples and validation cases
```

## Available Commands

### Meta-Agent Commands
- **`.claude/commands/agent_selector.md`** - Interactive agent selection and project setup
- **`.claude/commands/composer.md`** - Assembles components into complete prompts
- **`.claude/commands/extractor.md`** - Analyzes existing prompts to extract components  
- **`.claude/commands/validator.md`** - Ensures quality, completeness, and validation protocols
- **`.claude/commands/initializer.md`** - Sets up new projects with modular system
- **`.claude/commands/meta/interaction_history_analyzer.md`** - Analyzes Claude interaction patterns for system improvements

## Core Components

### Core Components (80%+ reuse)
- **thinking.md** - Structured reasoning with think tool
- **mcp_tools.md** - MCP filesystem tool patterns
- **document_creation.md** - Cross-agent document protocols
- **tool_usage.md** - Permission and efficiency guidelines
- **agent_validation_checkpoints.md** - Success verification protocols

### Specialized Components (40-60% reuse)
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

### Meta Components (Role-specific)
- **interaction_history_analyzer.md** - System optimization and pattern analysis

## Available Agent Compositions

### Development Team Agents
- **planner.yaml** - Project planning and requirements analysis
- **architect.yaml** - System design and architecture planning  
- **frontend_developer.yaml** - Frontend development and UI/UX implementation
- **backend_developer.yaml** - Backend development and API implementation
- **slack_developer.yaml** - Slack application development and bot implementation

### Operations Team Agents  
- **devops_engineer.yaml** - DevOps automation and infrastructure management
- **security_engineer.yaml** - Security assessment and implementation
- **developer.yaml** - General implementation and coding (legacy)

## Quick Start

### Simple 3-Step Workflow (Recommended)
```bash
# Step 1: Initialize project structure and setup
.claude/commands/initializer.md --template web_app --name "my-ecommerce"
# Creates: project structure, git repo, configuration files
# Output: "✅ Project initialized! Next: .claude/commands/agent_selector.md --interactive"

# Step 2: Select your development agents
.claude/commands/agent_selector.md --interactive
# Reads: project config, provides smart recommendations
# Creates: specialized .claude/commands/ agents for your project
# Output: "✅ Agents ready! Start with: .claude/commands/planner.md"

# Step 3: Start development with your agents
.claude/commands/planner.md
# Your project-specific agents are ready to help!
```

### Quick Project Templates
```bash
# Web application (React + Node.js + PostgreSQL)
.claude/commands/initializer.md --template web_app --name "my-web-app"

# API service (Backend + Database)
.claude/commands/initializer.md --template api_service --name "my-api"

# Slack application (Bot + Integrations)
.claude/commands/initializer.md --template slack_app --name "team-bot"

# Enterprise application (Full stack + Security + Compliance)
.claude/commands/initializer.md --template enterprise --name "customer-portal"
```

### Advanced: Manual Component Assembly

For advanced users who want to create custom agents or analyze existing prompts:

#### 1. Extract from Existing Project
```bash
# Analyze existing prompts and extract components
.claude/commands/extractor.md --source .claude/commands/ --output components/
```

#### 2. Compose New Agent
```yaml
# Create composition config (compositions/architect.yaml)
agent_name: "architect"
components:
  core: [thinking.md, mcp_tools.md, document_creation.md, agent_validation_checkpoints.md]
  specialized: [architecture_patterns.md, quality_standards.md]
parameters:
  AGENT_NAME: "Architect"
  PRIMARY_DOCS: "ADR, System Design"
  VALIDATION_LEVEL: "High"
```

#### 3. Generate Agent Prompt
```bash
# Compose final prompt from components
.claude/commands/composer.md --config compositions/architect.yaml --output .claude/commands/architect.md
```

#### 4. Validate Quality and Reliability
```bash
# Validate components and compositions for quality and validation protocols
.claude/commands/validator.md --components components/ --compositions compositions/ --report validation_report.yaml
```

## Complete Project Examples

### Example 1: E-commerce Platform
```bash
# Step 1: Initialize with web app template
.claude/commands/initializer.md --template web_app --name "ecommerce-platform"

# Step 2: Agent selector will recommend:
# planner + architect + frontend_developer + backend_developer + devops_engineer
.claude/commands/agent_selector.md --interactive

# Step 3: Start development
.claude/commands/planner.md  # Begin with requirements and planning
```

### Example 2: Enterprise API Platform  
```bash
# Step 1: Initialize with enterprise template (includes security focus)
.claude/commands/initializer.md --template enterprise --name "customer-api"

# Step 2: Agent selector will recommend:
# planner + architect + backend_developer + devops_engineer + security_engineer
.claude/commands/agent_selector.md --interactive

# Step 3: Start development
.claude/commands/planner.md  # Begin with security-focused planning
```

### Example 3: Slack Bot for Team Productivity
```bash
# Step 1: Initialize with Slack app template
.claude/commands/initializer.md --template slack_app --name "productivity-bot"

# Step 2: Agent selector will recommend:
# planner + slack_developer + backend_developer + security_engineer
.claude/commands/agent_selector.md --interactive

# Step 3: Start development
.claude/commands/planner.md  # Begin with bot requirements and workflows
```

### Example 4: Custom Integration Project
```bash
# Step 1: Use the closest template as starting point
.claude/commands/initializer.md --template api_service --name "custom-integration"

# Step 2: Customize agent selection during interactive process
.claude/commands/agent_selector.md --interactive
# Can add/remove agents based on specific needs

# Step 3: Start development
.claude/commands/planner.md  # Begin with custom requirements analysis
```

## Benefits

- **90% Less Duplication**: Shared components eliminate redundancy
- **Faster Updates**: Change once, update everywhere
- **Consistent Quality**: Standardized patterns across all agents
- **Rapid Prototyping**: Quick agent creation from proven components
- **Easy Validation**: Automated quality checks and compliance

## Validation

Uses the Dreamwork project as a validation case study:
- 5 existing agents with 60-70% duplication
- Successful extraction into 4 core + 5 specialized components
- Maintains 100% functionality while reducing maintenance overhead

## Command Orchestration Examples

### Example 1: New Web Development Project
```bash
# 1. Initialize new project structure
.claude/commands/initializer.md --template web_development --name "my_web_app"

# 2. Create developer agent composition
cat > compositions/developer.yaml << EOF
agent_name: "developer"
components:
  core: [thinking.md, mcp_tools.md, tool_usage.md, agent_validation_checkpoints.md]
  specialized: [development_workflows.md, testing_strategies.md]
parameters:
  AGENT_NAME: "Full-Stack Developer"
  TECH_STACK: "React, Node.js, PostgreSQL"
  VALIDATION_REQUIRED: "true"
EOF

# 3. Generate developer agent
.claude/commands/composer.md --config compositions/developer.yaml --output .claude/commands/developer.md

# 4. Validate the composition
.claude/commands/validator.md --composition compositions/developer.yaml --check-validation
```

### Example 2: Legacy System Migration
```bash
# 1. Extract components from existing project
.claude/commands/extractor.md --source /path/to/legacy/.claude/commands/ --output components/ --analyze-patterns

# 2. Create modernized architect composition
cat > compositions/modernization_architect.yaml << EOF
agent_name: "modernization_architect"
components:
  core: [thinking.md, mcp_tools.md, document_creation.md, agent_validation_checkpoints.md]
  specialized: [architecture_patterns.md, development_workflows.md, quality_standards.md]
parameters:
  AGENT_NAME: "Modernization Architect"
  FOCUS_AREAS: "Legacy Migration, System Design, Risk Assessment"
  VALIDATION_CHECKPOINTS: "Architecture Review, Migration Plan, Risk Mitigation"
EOF

# 3. Generate architect agent
.claude/commands/composer.md --config compositions/modernization_architect.yaml --output .claude/commands/architect.md

# 4. Create testing specialist
cat > compositions/migration_tester.yaml << EOF
agent_name: "migration_tester"
components:
  core: [thinking.md, mcp_tools.md, agent_validation_checkpoints.md]
  specialized: [testing_strategies.md, quality_standards.md]
parameters:
  AGENT_NAME: "Migration Tester"
  TEST_TYPES: "Integration, Regression, Performance, Data Migration"
  VALIDATION_REQUIRED: "true"
EOF

# 5. Generate tester agent
.claude/commands/composer.md --config compositions/migration_tester.yaml --output .claude/commands/tester.md

# 6. Validate entire agent suite
.claude/commands/validator.md --components components/ --compositions compositions/ --check-validation --report migration_validation.yaml
```

### Example 3: System Reliability Improvement
```bash
# 1. Analyze interaction history for improvement opportunities
.claude/commands/meta/interaction_history_analyzer.md "analyze system reliability patterns and recommend improvements"

# 2. Update existing compositions with validation checkpoints
# Edit existing compositions to include agent_validation_checkpoints.md

# 3. Create quality assurance specialist
cat > compositions/qa_specialist.yaml << EOF
agent_name: "qa_specialist"
components:
  core: [thinking.md, mcp_tools.md, document_creation.md, agent_validation_checkpoints.md]
  specialized: [quality_standards.md, testing_strategies.md, development_workflows.md]
parameters:
  AGENT_NAME: "Quality Assurance Specialist"
  FOCUS: "Validation Protocols, Test Execution, Evidence Verification"
  VALIDATION_LEVEL: "Maximum"
EOF

# 4. Generate QA agent
.claude/commands/composer.md --config compositions/qa_specialist.yaml --output .claude/commands/qa_specialist.md

# 5. Validate all agents have proper validation protocols
.claude/commands/validator.md --components components/ --compositions compositions/ --focus validation --report reliability_assessment.yaml
```

### Example 4: Multi-Agent Workflow Orchestration
```bash
# 1. Create coordinated agent suite for complex project

# Planning Agent
cat > compositions/planner.yaml << EOF
agent_name: "planner"
components:
  core: [thinking.md, mcp_tools.md, document_creation.md, agent_validation_checkpoints.md]
  specialized: [architecture_patterns.md, development_workflows.md]
parameters:
  AGENT_NAME: "Project Planner"
  ROLE: "Requirement Analysis, Task Breakdown, Risk Assessment"
  HANDOFF_TO: "architect, developer"
EOF

# Architect Agent
cat > compositions/architect.yaml << EOF
agent_name: "architect"
components:
  core: [thinking.md, mcp_tools.md, document_creation.md, agent_validation_checkpoints.md]
  specialized: [architecture_patterns.md, quality_standards.md]
parameters:
  AGENT_NAME: "System Architect"
  ROLE: "System Design, Architecture Decisions, Technical Leadership"
  RECEIVES_FROM: "planner"
  HANDOFF_TO: "developer"
EOF

# Developer Agent
cat > compositions/developer.yaml << EOF
agent_name: "developer"
components:
  core: [thinking.md, mcp_tools.md, tool_usage.md, agent_validation_checkpoints.md]
  specialized: [development_workflows.md, testing_strategies.md]
parameters:
  AGENT_NAME: "Lead Developer"
  ROLE: "Implementation, Unit Testing, Code Review"
  RECEIVES_FROM: "architect"
  HANDOFF_TO: "tester"
EOF

# Generate all agents
.claude/commands/composer.md --config compositions/planner.yaml --output .claude/commands/planner.md
.claude/commands/composer.md --config compositions/architect.yaml --output .claude/commands/architect.md
.claude/commands/composer.md --config compositions/developer.yaml --output .claude/commands/developer.md

# Validate the entire workflow
.claude/commands/validator.md --compositions compositions/ --check-handoffs --check-validation --report workflow_validation.yaml
```

## Getting Started

### For New Projects (Most Common)
1. **Initialize Project**: `.claude/commands/initializer.md --template <type> --name "project"`
2. **Select Agents**: `.claude/commands/agent_selector.md --interactive`
3. **Start Development**: `.claude/commands/planner.md` (or your preferred starting agent)

### For Advanced Users
1. **Extract Components**: Use Extractor for existing prompts  
2. **Compose Agents**: Use Composer for modular assembly
3. **Validate Quality**: Use Validator for compliance and reliability checks
4. **Monitor Performance**: Use Interaction History Analyzer for continuous improvement

### What You Get

After the 3-step setup, you'll have:
- ✅ **Complete Project Structure**: src/, docs/, tests/, infrastructure/
- ✅ **Git Repository**: Initialized with proper .gitignore
- ✅ **Project-Specific Agents**: Tailored to your technology stack and requirements
- ✅ **Clear Documentation**: README with workflow and agent responsibilities
- ✅ **Ready to Develop**: No configuration needed, start coding immediately

The modular approach transforms prompt engineering from artisanal craft to systematic engineering practice with built-in reliability and validation protocols.

## Documentation

- **[Quick Start Guide](docs/QUICK_START.md)** - Get started in 3 commands
- **[Workflow Guide](docs/WORKFLOW_GUIDE.md)** - Complete development workflow with agents
- **[Component Reference](components/)** - Detailed component documentation
- **[Agent Compositions](compositions/)** - Pre-configured agent examples

## Support

- **Issues**: Report bugs and feature requests in the GitHub issues
- **Documentation**: Comprehensive guides in the `docs/` directory
- **Examples**: Working examples in the `examples/` directory
- **Validation**: Use the built-in validator for quality assurance