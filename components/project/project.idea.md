# Project Idea Template Component

## Purpose
Provides a simple, user-friendly template for project.idea.md files that captures essential project vision and requirements for use by the planner agent.

## Core Capabilities

### User-Focused Structure
- **Project Overview**: What are you building and why?
- **Key Features**: What should this project do?
- **Technical Preferences**: Any specific technologies or constraints?
- **Success Criteria**: How will you know it's working?

### Integration with Planning
- **Planner Input**: Clear project vision for context-aware planning
- **Requirement Capture**: Essential features and goals
- **Constraint Documentation**: Technical and business limitations
- **Success Definition**: Measurable outcomes

## Template Structure

### Standard project.idea.md Format
```markdown
# {{PROJECT_NAME}}

## What are you building?
<!-- Describe your project in 1-2 sentences -->

## Why does this project matter?
<!-- What problem does it solve? Who benefits? -->

## What should it do?
<!-- List the main features/capabilities you want -->
- 
- 
- 

## Any technical preferences?
<!-- Specific technologies, frameworks, or constraints -->
- Programming language: 
- Framework/Platform: 
- Database: 
- Hosting/Deployment: 

## How will you know it's successful?
<!-- What does "done" look like? -->
- 
- 
- 

## Anything else important?
<!-- Special considerations, constraints, or context -->
```

## Usage Pattern

### For New Project Creation
1. Generate project.idea.md using this template
2. Fill in project-specific information based on user requirements
3. Place in project root directory
4. Reference from planner.md for context-aware planning

### For Project Planning Integration
1. Check if project.idea.md exists in project root
2. Parse structured information for planning context
3. Use requirements and tasks as planning input
4. Reference timeline and priorities for task organization

## Integration Points

### With Planner Component
- Provides structured project context for planning decisions
- Supplies requirements list for comprehensive coverage
- Offers priority framework for task organization
- Includes timeline constraints for realistic planning

### With Initializer Meta-agent
- Template instantiation for new projects
- Smart defaults based on project type
- Integration with project setup workflow
- Customization based on user specifications

### With Project Management
- Task tracking and progress updates
- Requirement validation and coverage
- Timeline monitoring and adjustment
- Risk assessment and mitigation tracking

## Parameter Definitions

### Project Information
- `{{PROJECT_NAME}}`: Clear, descriptive project name
- `{{PROJECT_DESCRIPTION}}`: Concise explanation of project purpose
- `{{PROJECT_TYPE}}`: Category of project (web app, CLI, library, etc.)
- `{{TARGET_USERS}}`: Intended audience or user base

### Status Tracking
- `{{PHASE}}`: Current development phase
- `{{CURRENT_DATE}}`: Last update timestamp
- `{{PRIORITY}}`: Overall project priority level
- `{{COMPLETION_PERCENTAGE}}`: Progress indicator

### Requirements
- `{{FUNCTIONAL_REQ_*}}`: What the system should do
- `{{TECH_STACK}}`: Technologies to be used
- `{{PERFORMANCE_REQUIREMENTS}}`: Speed, efficiency targets
- `{{SECURITY_REQUIREMENTS}}`: Safety and access controls

### Architecture
- `{{COMPONENT_*}}`: Major system components
- `{{DATA_FLOW_DESCRIPTION}}`: How information moves through system
- `{{INTEGRATION_POINT_*}}`: External system connections

### Timeline
- `{{IMMEDIATE_GOAL_*}}`: This week's objectives
- `{{SHORT_TERM_GOAL_*}}`: This month's objectives
- `{{LONG_TERM_GOAL_*}}`: This quarter's objectives

## Quality Standards
- **Completeness**: All sections filled with relevant information
- **Specificity**: Concrete, actionable requirements and tasks
- **Realism**: Achievable goals and reasonable timelines
- **Clarity**: Clear, unambiguous descriptions and criteria
- **Traceability**: Tasks linked to requirements and goals