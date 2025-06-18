# Tool Usage Component

## Purpose
Provides guidelines for effective tool usage patterns and permission management across all agent roles.

## Permission Strategy
```
## Tool use
When you want to use a tool that you have to ask for permission first:
- Figure out if there is a more generic permission you can request, so that we do not fill up the conversation with too many permission requests.
- For instance, if you want to use a bash command to list files, you can ask for permission to use the bash tool in general, instead of asking for permission to run a specific command.
```

## Standard Tool Categories

### File Operations
- **Read Operations**: mcp__filesystem__read_file, mcp__filesystem__read_multiple_files
- **Write Operations**: mcp__filesystem__write_file, mcp__filesystem__edit_file  
- **Discovery Operations**: mcp__filesystem__search_files, mcp__filesystem__directory_tree
- **Permission Level**: Generally safe, minimal permission required

### System Operations  
- **Bash Commands**: For build, test, install operations
- **Git Operations**: For version control tasks
- **Permission Level**: Request generic permission upfront

### Memory Operations
- **Knowledge Graph**: mcp__memory__create_entities, mcp__memory__read_graph, mcp__memory__search_nodes
- **Context Management**: mcp__memory__add_observations, mcp__memory__create_relations
- **Permission Level**: Generally safe, helps maintain context across conversations

### External Operations
- **Web Fetch**: For research and documentation lookup
- **API Calls**: For external service integration
- **Permission Level**: Specific permission per operation type

## Efficiency Patterns

### Batch Operations
```
# Good: Batch multiple file reads
mcp__filesystem__read_multiple_files(paths=[...])

# Avoid: Sequential single reads  
mcp__filesystem__read_file(path="file1")
mcp__filesystem__read_file(path="file2")
```

### Parallel Tool Calls
```
# Use multiple tool calls in single message for independent operations
- Read configuration files
- Check project structure  
- Search for existing implementations
```

### Memory Management Patterns
```
# Proactive context capture for complex projects
mcp__memory__create_entities([{
  "name": "ProjectRequirements", 
  "entityType": "Document",
  "observations": ["Key requirements and constraints discovered"]
}])

# Build knowledge graph of project relationships
mcp__memory__create_relations([{
  "from": "Frontend", "to": "API", "relationType": "depends_on"
}])

# Regular memory review for context continuity
mcp__memory__search_nodes(query="architecture decisions")
```

## Error Handling
- Always verify tool results before proceeding
- Use thinking.md component to analyze unexpected results
- Provide fallback strategies for tool failures

## Proactive Memory Usage

### When to Use Memory Tools
- **Complex Projects**: Track architecture decisions, requirements, and constraints
- **Multi-Session Work**: Maintain context across conversations  
- **Knowledge Discovery**: Build understanding of project relationships
- **Cross-Agent Communication**: Share insights between different agent roles
- **Decision Tracking**: Record rationale for future reference

### Memory Tool Workflow
1. **Session Start**: Review existing knowledge graph with mcp__memory__read_graph
2. **Discovery Phase**: Create entities for key findings and decisions
3. **Analysis Phase**: Build relationships between discovered concepts
4. **Documentation Phase**: Add observations to enrich entity understanding
5. **Session End**: Search and verify important knowledge is captured

## Integration Points
- Essential foundation for all other components
- Combines with mcp_tools.md for specific MCP patterns
- Supports thinking.md analysis workflows
- Enables memory.md patterns for knowledge persistence