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
- **Permission Level**: Request generic bash/git permission upfront

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

## Error Handling
- Always verify tool results before proceeding
- Use thinking.md component to analyze unexpected results
- Provide fallback strategies for tool failures

## Integration Points
- Essential foundation for all other components
- Combines with mcp_tools.md for specific MCP patterns
- Supports thinking.md analysis workflows