# MCP Tools Component

## Purpose
Provides standardized patterns for using MCP (Model Context Protocol) tools effectively across different agent roles.

## Core MCP Tools

### Filesystem Tools
- `mcp__filesystem__search_files` - Search for files by pattern
- `mcp__filesystem__directory_tree` - Get directory structure
- `mcp__filesystem__read_file` - Read file contents  
- `mcp__filesystem__read_multiple_files` - Read multiple files efficiently
- `mcp__filesystem__write_file` - Create/overwrite files
- `mcp__filesystem__edit_file` - Make targeted edits

### Memory Tools
- `mcp__memory__read_graph` - Review existing knowledge graph
- `mcp__memory__create_entities` - Create project entities and observations
- `mcp__memory__create_relations` - Build relationships between entities
- `mcp__memory__add_observations` - Enrich entities with new insights
- `mcp__memory__search_nodes` - Search knowledge graph for specific information
- `mcp__memory__open_nodes` - Retrieve detailed entity information

## Standard Usage Patterns

### Document Discovery Pattern
```
# Before starting work, discover relevant documents
mcp__filesystem__search_files(path="{{PROJECT_ROOT}}/docs", pattern="*.md")
mcp__filesystem__directory_tree(path="{{PROJECT_ROOT}}/.claude")
```

### Multi-File Analysis Pattern  
```
# Read multiple related files efficiently
mcp__filesystem__read_multiple_files(paths=[
    "{{PROJECT_ROOT}}/package.json",
    "{{PROJECT_ROOT}}/README.md", 
    "{{PROJECT_ROOT}}/docs/architecture.md"
])
```

### Safe File Operations Pattern
```
# Always read before editing
mcp__filesystem__read_file(path="{{TARGET_FILE}}")
# Then make targeted edits
mcp__filesystem__edit_file(path="{{TARGET_FILE}}", edits=[...])
```

### Memory Context Management Pattern
```
# Start session by reviewing existing knowledge
mcp__memory__read_graph()

# Create entities for key project discoveries
mcp__memory__create_entities([{
  "name": "{{PROJECT_NAME}}_Architecture",
  "entityType": "Design",
  "observations": ["Architecture decisions and rationale"]
}])

# Build understanding through relationships
mcp__memory__create_relations([{
  "from": "{{COMPONENT_A}}", 
  "to": "{{COMPONENT_B}}", 
  "relationType": "{{RELATIONSHIP_TYPE}}"
}])
```

### Memory-Enhanced Discovery Pattern
```
# Combine filesystem discovery with memory context
mcp__memory__search_nodes(query="{{SEARCH_TERM}}")
mcp__filesystem__search_files(path="{{PROJECT_ROOT}}", pattern="{{PATTERN}}")
# Cross-reference findings to build comprehensive understanding
```

## Role-Specific Adaptations

### Filesystem Focus
- **Architect**: Focus on design docs, ADRs, system overviews
- **Developer**: Focus on source code, config files, implementation guides  
- **Researcher**: Focus on research docs, technology evaluations, analysis
- **Reviewer**: Focus on code quality, documentation standards
- **Tester**: Focus on test files, quality validation docs

### Memory Management Focus
- **Architect**: Track system design decisions, component relationships, technology choices
- **Developer**: Record implementation patterns, bug fixes, code decisions
- **Planner**: Maintain project requirements, stakeholder feedback, timeline constraints
- **Researcher**: Build knowledge graphs of findings, technology comparisons, recommendations
- **Reviewer**: Track quality standards, review patterns, improvement suggestions
- **Tester**: Document test strategies, quality metrics, defect patterns

## Project Configuration Considerations

### Filesystem MCP Directory Access
For new projects, ensure the filesystem MCP is configured to include your project directory:
```
# Current project should be added to allowed directories
# Check: mcp__filesystem__list_allowed_directories() 
# Should include: {{PROJECT_ROOT}}
```

When starting work on a new project, verify filesystem access and request configuration updates if needed.

### Memory Graph Initialization
```
# Start new projects by establishing baseline knowledge
mcp__memory__read_graph()  # Review existing knowledge
# Create project root entity if needed
mcp__memory__create_entities([{
  "name": "{{PROJECT_NAME}}",
  "entityType": "Project", 
  "observations": ["Project scope, objectives, and key stakeholders"]
}])
```

## Integration Points
- Combine with document_creation.md for comprehensive workflows
- Use with thinking.md for complex discovery operations
- Essential for cross-agent communication patterns
- Memory tools enable context persistence across agent interactions
- Filesystem tools provide project exploration and modification capabilities