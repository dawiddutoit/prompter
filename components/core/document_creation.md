# Document Creation Component

## Purpose
Provides standardized protocols for creating documents with proper audience targeting and cross-agent communication.

## Document Header Template
```markdown
---
**Document Type**: {{DOCUMENT_TYPE}}
**Created By**: {{AGENT_NAME}} Agent  
**Primary Audience**: {{PRIMARY_AUDIENCE}}
**Secondary Audience**: {{SECONDARY_AUDIENCE}}
**Purpose**: {{PURPOSE_STATEMENT}}
**Action Items**: {{ACTION_ITEMS}}
---
```

## Document Types by Agent Role

### Architecture Documents (Architect → Developer/Researcher)
- **Types**: ADR, System Design, Technical Specification
- **Purpose**: Enable implementation and further research
- **Action Items**: Implementation tasks, research questions

### Implementation Guides (Developer → All Agents)  
- **Types**: Setup Guide, Implementation Notes, Code Documentation
- **Purpose**: Enable code understanding and quality validation
- **Action Items**: Review tasks, testing requirements

### Research Reports (Researcher → Architect/Developer)
- **Types**: Technology Evaluation, Analysis Report, Recommendation
- **Purpose**: Inform architectural decisions and implementation choices  
- **Action Items**: Decision points, implementation considerations

### Quality Reports (Reviewer → Developer/Architect)
- **Types**: Code Review, Quality Assessment, Standards Compliance
- **Purpose**: Enable quality improvements and standard adherence
- **Action Items**: Specific fixes, improvement recommendations

### Testing Documentation (Tester → Developer/Reviewer)
- **Types**: Test Plan, Quality Validation, Test Results
- **Purpose**: Enable quality assurance and validation processes
- **Action Items**: Test execution, quality gates

## Standard Creation Protocol

1. **Discovery Phase**: Use MCP tools to find related documents
2. **Audience Analysis**: Identify primary and secondary audiences  
3. **Template Application**: Apply appropriate document header
4. **Content Creation**: Follow role-specific content patterns
5. **Cross-Reference**: Link to related documents and dependencies
6. **Action Items**: Specify clear next steps for target audience

## Integration Points
- Must be combined with mcp_tools.md for document discovery
- Works with thinking.md for complex audience analysis
- Essential for all agent role definitions