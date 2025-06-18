# Project Setup Component

## Purpose
Provides standardized setup patterns for new projects, including MCP configuration and initial knowledge graph establishment.

## MCP Configuration Verification

### Filesystem Access Setup
```
# Verify current project directory is accessible
mcp__filesystem__list_allowed_directories()

# Should include current project: {{PROJECT_ROOT}}
# If not included, request filesystem MCP configuration update
```

**Common Issue**: New projects often have filesystem MCP configured with limited directory access, missing the current project directory.

**Solution**: When starting work on a new project, always verify and request filesystem access configuration if needed.

### Memory System Initialization  
```
# Review existing knowledge for project context
mcp__memory__read_graph()

# Initialize project root entity if starting fresh
mcp__memory__create_entities([{
  "name": "{{PROJECT_NAME}}",
  "entityType": "Project",
  "observations": ["Project scope, objectives, key stakeholders, initial requirements"]
}])
```

## Project Discovery Workflow

### Step 1: Environment Verification
- Check filesystem MCP directory access
- Review existing memory graph for project context
- Verify project structure and documentation

### Step 2: Context Establishment
- Create or update project root entity in memory
- Establish key project relationships
- Document initial understanding and constraints

### Step 3: Tool Configuration
- Ensure all necessary MCP tools are available
- Verify project-specific configuration needs
- Set up recurring patterns for knowledge maintenance

## Integration Points
- Essential foundation for all project work
- Used by all agent archetypes for consistent setup
- Enables effective cross-agent communication and context sharing
- Supports memory.md patterns for long-term knowledge management