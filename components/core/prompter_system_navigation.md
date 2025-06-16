# Prompter System Navigation Component

## Purpose
Provides comprehensive navigation and architectural understanding for agents working within the prompter system itself, preventing stochastic decay as the system grows.

## System Architecture Overview

### Core System Structure
```
prompter/
├── components/           # Reusable prompt building blocks
│   ├── core/            # Universal components (80%+ reuse)
│   ├── specialized/     # Domain-specific (40-60% reuse)
│   ├── meta/           # System-level capabilities
│   └── project/        # Project-specific templates
├── archetypes/         # Agent composition configurations (YAML)
├── .claude/commands/   # Prompter's own operational agents
├── examples/          # Reference implementations
└── projects/          # Generated/managed projects
```

### How Prompter Works (Component Composition System)
1. **Components** = Reusable prompt building blocks with specific purposes
2. **Archetypes** = YAML configurations that define how to combine components
3. **Composition Process** = Archetype + Components → Complete Agent Prompt
4. **Deployment** = Composed agents deployed to target project's `.claude/commands/`

## Component System Navigation

### Core Components (`components/core/`)
**Universal patterns used by 80%+ of agents:**
- `thinking.md` - Structured reasoning with think tool
- `mcp_tools.md` - MCP filesystem server integration patterns
- `document_creation.md` - Standardized document creation protocols
- `tool_usage.md` - General tool usage patterns and protocols
- `agent_validation_checkpoints.md` - Success verification and trust building
- `prompter_system_navigation.md` - This navigation guide (self-referencing)

### Specialized Components (`components/specialized/`)
**Domain-specific patterns for 40-60% reuse:**
- `architecture_patterns.md` - System design and technical architecture
- `backend_development.md` - Server-side development patterns
- `frontend_development.md` - UI/UX development patterns
- `devops_engineering.md` - Infrastructure and deployment patterns
- `testing_strategies.md` - Quality assurance and testing approaches
- `security_operations.md` - Security practices and compliance
- `research_methodologies.md` - Investigation and analysis patterns
- `project_planning.md` - Strategic planning and requirements analysis
- `quality_standards.md` - Quality management and standards enforcement

### Meta Components (`components/meta/`)
**System-level capabilities:**
- `interaction_history_analyzer.md` - Analyzes Claude usage patterns for optimization
- `meta_developer.md` - System evolution and improvement

### Project Components (`components/project/`)
**Project lifecycle templates:**
- `project.idea.md` - Initial project concept and requirements template
- `project.plan.md` - Comprehensive project configuration and planning template

## Archetype System Navigation

### Archetype Structure (YAML Configuration)
Each archetype defines:
```yaml
agent_name: "role_name"
description: "Agent purpose"
output_path: ".claude/commands/agent.md"

components:
  core: [list of core components]
  specialized: [list of specialized components]
  meta: [list of meta components]

parameters:
  AGENT_NAME: "Human-readable name"
  ROLE_DESCRIPTION: "What this agent does"
  # ... role-specific parameters

validation_rules:
  required_sections: [must-have sections]
  quality_standards: [quality requirements]
```

### Available Archetypes
- `architect.yaml` - System architecture and technical design
- `backend_developer.yaml` - Server-side development
- `frontend_developer.yaml` - UI/UX development
- `devops_engineer.yaml` - Infrastructure and deployment
- `planner.yaml` - Project planning and requirements
- `security_engineer.yaml` - Security practices and compliance
- `developer.yaml` - General development (backend + frontend)
- `maintainer.yaml` - Long-term maintenance and support
- `slack_developer.yaml` - Slack bot development

## Prompter's Internal Agents (`.claude/commands/`)

### System Management Agents
**These agents operate ON the prompter system itself:**

- `prompter.md` - Main entry point and user interface
- `create_new_project.md` - Project initialization and setup
- `add_agents_to_project.md` - Agent deployment to existing projects
- `build_custom_agent.md` - Custom agent composition
- `improve_agent_quality.md` - Quality assurance and validation
- `system/analyze.md` - System analysis and optimization
- `system/compose.md` - Agent composition from archetypes
- `system/extract.md` - Component extraction from existing prompts
- `system/validate.md` - System validation and quality checks

### Agent Operational Workflow
1. **User Interaction** → `prompter.md` (main interface)
2. **Project Creation** → `create_new_project.md` → calls `system/compose.md`
3. **Agent Addition** → `add_agents_to_project.md` → calls `system/compose.md`
4. **Custom Building** → `build_custom_agent.md` → calls `system/compose.md`
5. **Quality Assurance** → `improve_agent_quality.md` → calls `system/validate.md`

## How to Work Within Prompter System

### For Prompter System Development
**When working on prompter itself (not deployed agents):**

1. **Always Reference This Guide** - Include this component in your context
2. **Understand Component vs Archetype** - Modify components for functionality, archetypes for composition
3. **Use MCP Discovery Patterns** - Find existing components before creating new ones
4. **Follow Composition Rules** - Understand how components assemble into agents
5. **Validate System Changes** - Use `improve_agent_quality.md` after modifications

### Component Development Workflow
```bash
# 1. Discover existing components
mcp__filesystem__search_files(path="/prompter/components", pattern="*.md")

# 2. Analyze component structure
mcp__filesystem__read_multiple_files(paths=["components/core/*.md"])

# 3. Understand integration points
mcp__filesystem__search_files(path="/prompter/archetypes", pattern="*.yaml")

# 4. Create/modify components following patterns
# 5. Update archetype configurations if needed
# 6. Test composition process
# 7. Validate with improve_agent_quality.md
```

### Archetype Development Workflow
```bash
# 1. Understand target agent requirements
# 2. Select appropriate components (core + specialized + meta)
# 3. Configure parameters for role
# 4. Define validation rules
# 5. Test composition process
# 6. Validate output agent quality
```

## Anti-Decay Protocols

### Preventing Stochastic Decay
**As the system grows, maintain coherence through:**

1. **Mandatory Navigation Reference** - This component included in all prompter agents
2. **Regular System Validation** - Use `improve_agent_quality.md` for health checks
3. **Component Consistency Checks** - Ensure integration points remain valid
4. **Archetype Validation** - Verify compositions produce quality agents
5. **Documentation Synchronization** - Keep this guide updated with system changes

### Quality Gates for System Changes
**Before modifying prompter system:**
- [ ] Understand current architecture using this guide
- [ ] Identify affected components and archetypes
- [ ] Test composition process still works
- [ ] Update this navigation guide if structure changes
- [ ] Validate with `improve_agent_quality.md`
- [ ] Update integration documentation

### Change Management Protocol
1. **Impact Analysis** - What components/archetypes are affected?
2. **Backward Compatibility** - Will existing compositions still work?
3. **Testing** - Verify composition and deployment processes
4. **Documentation** - Update this guide and related docs
5. **Validation** - System-wide quality check

## Integration Discovery Patterns

### Finding System Components
```bash
# Core component discovery
mcp__filesystem__directory_tree(path="/prompter/components/core")
mcp__filesystem__search_files(path="/prompter/components/core", pattern="*.md")

# Specialized component discovery
mcp__filesystem__directory_tree(path="/prompter/components/specialized")
mcp__filesystem__search_files(path="/prompter/components/specialized", pattern="*.md")

# Archetype discovery
mcp__filesystem__directory_tree(path="/prompter/archetypes")
mcp__filesystem__search_files(path="/prompter/archetypes", pattern="*.yaml")

# System agent discovery
mcp__filesystem__directory_tree(path="/prompter/.claude/commands")
mcp__filesystem__search_files(path="/prompter/.claude/commands", pattern="*.md")
```

### Understanding Component Dependencies
```bash
# Find which archetypes use a component
mcp__filesystem__search_files(path="/prompter/archetypes", pattern="*.yaml")
# Read archetype files to see component usage

# Find component integration points
mcp__filesystem__search_files(path="/prompter/components", pattern="*.md")
# Look for "Integration Points" sections
```

## Extension Patterns

### Adding New Components
1. **Identify Need** - What capability is missing?
2. **Choose Category** - Core, specialized, meta, or project?
3. **Follow Template** - Use existing components as patterns
4. **Define Integration Points** - How does it work with other components?
5. **Update Archetypes** - Which agent types need this component?
6. **Test Composition** - Verify it works in practice
7. **Update Navigation** - Add to this guide

### Adding New Archetypes
1. **Define Role** - What type of agent is needed?
2. **Select Components** - Which existing components apply?
3. **Configure Parameters** - Role-specific customization
4. **Set Validation Rules** - Quality requirements
5. **Test Composition** - Generate and validate agent
6. **Document Usage** - When to use this archetype

### Adding New System Agents
1. **Identify System Need** - What prompter operation is missing?
2. **Follow Agent Patterns** - Use existing system agents as templates
3. **Include Navigation Component** - Always include this guide
4. **Define Clear Purpose** - Single responsibility principle
5. **Test Integration** - Works with other system agents
6. **Update Main Interface** - Add to `prompter.md` if user-facing

## Emergency Recovery Procedures

### If System Navigation is Lost
1. **This File Location**: `/prompter/components/core/prompter_system_navigation.md`
2. **Auto-Discovery**: Search for "*navigation*" in components directory
3. **Rebuild Understanding**: Read this file completely
4. **Validate System**: Run `improve_agent_quality.md`
5. **Check Integration**: Verify this component is included in system agents

### If Component Structure Changes
1. **Reference This Guide** - Current architecture overview
2. **Map Changes** - What's different from this description?
3. **Update Guide** - Modify this file to reflect new reality
4. **Test System** - Verify composition still works
5. **Validate Quality** - Run full system quality check

## Success Metrics

### System Coherence Indicators
- All prompter agents can navigate system structure
- Component composition process works reliably
- System modifications don't break existing functionality
- New team members can understand and extend system
- Documentation stays synchronized with reality

### Anti-Decay Validation
- Regular system health checks pass
- Component integration points remain valid
- Archetype compositions produce quality agents
- System knowledge doesn't get lost or fragmented
- Evolution maintains backward compatibility

This navigation guide ensures prompter system agents always understand where they are, what they're working with, and how to make changes without breaking the system architecture.