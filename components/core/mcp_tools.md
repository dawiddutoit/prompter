# MCP Tools Component

## Purpose
Provides standardized patterns for using MCP (Model Context Protocol) tools effectively across different agent roles.

## Core MCP Tools
- `mcp__filesystem__search_files` - Search for files by pattern
- `mcp__filesystem__directory_tree` - Get directory structure
- `mcp__filesystem__read_file` - Read file contents  
- `mcp__filesystem__read_multiple_files` - Read multiple files efficiently
- `mcp__filesystem__write_file` - Create/overwrite files
- `mcp__filesystem__edit_file` - Make targeted edits

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

## Role-Specific Adaptations
- **Architect**: Focus on design docs, ADRs, system overviews
- **Developer**: Focus on source code, config files, implementation guides  
- **Researcher**: Focus on research docs, technology evaluations, analysis
- **Reviewer**: Focus on code quality, documentation standards
- **Tester**: Focus on test files, quality validation docs

## Integration Points
- Combine with document_creation.md for comprehensive workflows
- Use with thinking.md for complex discovery operations
- Essential for cross-agent communication patterns