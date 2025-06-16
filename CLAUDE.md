# Prompter Project - Modular Prompt Composition System

## Project Purpose
This project implements a modular prompt composition system for AI agents. Instead of monolithic prompt files with 60-70% duplication, prompts are assembled from reusable components.

## How This System Works

### Component-Based Architecture
- **Core Components** (`components/core/`): Universal patterns used by 80%+ of agents
- **Specialized Components** (`components/specialized/`): Domain-specific patterns for 40-60% reuse
- **Role-Specific Components** (`components/meta/`): Unique patterns for specific agent types

### Composition Process
1. **Configuration** - Define agent requirements in YAML composition files
2. **Assembly** - Use Composer meta-agent to merge components into complete prompts
3. **Validation** - Use Validator meta-agent to ensure quality and completeness
4. **Deployment** - Generated prompts ready for use in `.claude/commands/`

## Working with Components

### Creating New Components
- Follow the standard structure: Purpose, Usage Pattern/Core Capabilities, Integration Points
- Use parameter placeholders: `{{VARIABLE_NAME}}`
- Document integration points with other components
- Keep components focused and reusable

### Editing Existing Components  
- **Impact Analysis**: Changes to core components affect multiple agents
- **Validation Required**: Always run Validator after component changes
- **Regeneration Needed**: Update all composed prompts using modified components

### Component Dependencies
- Core components have no dependencies
- Specialized components may reference core components
- Role-specific components build on both core and specialized

## Meta-Agent Usage

### Composer
Use to generate agent prompts from component configurations:
```bash
# Generate architect prompt from composition config
tools/composer.md --config compositions/architect.yaml --output .claude/commands/architect.md
```

### Extractor  
Use to analyze existing monolithic prompts and extract reusable components:
```bash
# Extract components from existing project
tools/extractor.md --source /path/to/existing/.claude/commands/ --output components/
```

### Validator
Use to ensure component and prompt quality:
```bash
# Validate all components and compositions
tools/validator.md --components components/ --compositions compositions/
```

### Initializer
Use to set up new projects with modular prompt system:
```bash
# Initialize new project with modular prompts
tools/initializer.md --template web_development --name "new_project"
```

## Quality Standards

### Component Quality Requirements
- **Purpose Section**: Clear statement of component function
- **Usage Pattern**: Concrete examples of component usage
- **Integration Points**: Documentation of how component works with others
- **Parameter Documentation**: All `{{VARIABLES}}` explained

### Prompt Quality Requirements
- **Completeness**: All referenced components successfully merged
- **Coherence**: Logical flow from component assembly
- **Functionality**: Clear agent instructions and capabilities
- **Standards Compliance**: Follows project conventions

## Development Workflow

### Adding New Agent Role
1. Identify required components (core + specialized + role-specific)
2. Create composition configuration file
3. Generate prompt using Composer
4. Validate using Validator
5. Test functionality and iterate

### Modifying Agent Behavior
1. Identify which component contains the target behavior
2. Edit component (consider impact on other agents)
3. Regenerate affected agent prompts using Composer
4. Validate all changes using Validator
5. Test affected agents

### Maintaining System Quality
- Regular validation runs on all components and compositions
- Component impact analysis before modifications
- Systematic regeneration of prompts after core component changes
- Quality metrics tracking (duplication reduction, consistency scores)

## Guidelines for This Project

### When Working on Prompter
- **Think First**: Use the thinking tool for complex analysis and planning
- **Component Focus**: Prefer editing components over generated prompts
- **Validation Always**: Run validation after any component changes
- **Impact Awareness**: Consider downstream effects of component modifications
- **Documentation**: Keep component integration points current

### File Management
- **Components**: The source of truth for all prompt content
- **Compositions**: Configuration files defining how components assemble
- **Generated Prompts**: Output files, should not be manually edited
- **Examples**: Reference implementations and validation cases

This modular approach transforms prompt engineering from manual duplication management into systematic component-based development.