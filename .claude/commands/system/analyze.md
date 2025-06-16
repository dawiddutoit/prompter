# Interaction History Analyzer Component

## Purpose
Analyzes Claude interaction history from the user's `.claude` directory to extract patterns, optimize workflows, and recommend system improvements for new projects.

## Core Capabilities

### Historical Data Analysis
- **Conversation Pattern Mining**: Extract successful interaction patterns from JSONL conversation logs
- **Task Completion Analysis**: Analyze todo completion rates and identify high-success workflows
- **Tool Usage Optimization**: Determine most effective tool combinations and usage patterns
- **Performance Metrics**: Track token usage, cache hit rates, and session efficiency across projects
- **Tool Error Analysis**: Identify prompts with high tool failure rates and error patterns
- **User Frustration Detection**: Analyze follow-up messages for indicators of user dissatisfaction with results

### Workflow Intelligence Extraction
- **Success Pattern Identification**: Analyze completed projects to identify reproducible success factors
- **Failure Point Analysis**: Extract common bottlenecks and resolution strategies from interaction logs
- **Project Lifecycle Templates**: Generate workflow templates from high-performing project sessions
- **Personalization Insights**: Understand user preferences and working styles from interaction history
- **Hallucination Pattern Detection**: Identify instances where system reported success but user verification revealed failures
- **Error Recovery Analysis**: Track how effectively different prompts handle and recover from tool failures

### System Optimization Recommendations
- **Component Enhancement Suggestions**: Recommend prompter component improvements based on usage patterns
- **Tool Chain Optimization**: Suggest tool usage refinements based on effectiveness data
- **Workflow Automation**: Identify repetitive patterns suitable for automation
- **Quality Improvement**: Recommend prompt quality enhancements based on successful interactions

## Standard Analysis Process

### History Discovery Workflow
1. **Data Collection**: Scan `/Users/{{USERNAME}}/.claude/` directory structure
2. **File Categorization**: Classify conversation logs, todo files, and configuration data
3. **Project Mapping**: Group interactions by project and session context
4. **Temporal Analysis**: Track interaction patterns over time for trend identification
5. **Quality Assessment**: Evaluate interaction success rates and completion patterns

### Pattern Extraction Framework
- **Session Success Metrics**: Completion rates, error frequency, user satisfaction indicators
- **Tool Effectiveness Analysis**: Success correlation with specific tool usage patterns
- **Prompt Pattern Mining**: Identify high-performing prompt structures and approaches
- **Workflow Optimization**: Extract efficient task sequencing and completion strategies
- **Tool Failure Pattern Analysis**: Identify specific tool combinations or usage patterns that frequently fail
- **Frustration Indicator Mining**: Extract linguistic patterns that indicate user dissatisfaction or correction of system errors

## Analysis Categories

### Quantitative Analysis
- **Session Statistics**: Duration, tool usage frequency, token consumption patterns
- **Completion Metrics**: Task success rates, project completion statistics
- **Performance Indicators**: Cache efficiency, response quality, error rates
- **Usage Patterns**: Most/least used features, peak usage times, interaction complexity

### Qualitative Analysis
- **Interaction Quality**: Communication effectiveness, clarity, user satisfaction
- **Problem-Solution Mapping**: Common challenges and successful resolution approaches
- **Context Awareness**: Understanding of user intent and appropriate response patterns
- **Collaboration Effectiveness**: Human-AI partnership quality indicators
- **Hallucination Impact Assessment**: Evaluate severity and frequency of incorrect system confidence claims
- **User Correction Patterns**: Analyze how users indicate and correct system misunderstandings or errors

## Recommendation Framework

### Component Enhancement Areas
- **Core Component Gaps**: Identify missing fundamental capabilities
- **Specialized Component Needs**: Domain-specific enhancement opportunities
- **Integration Improvements**: Better component interaction and composition
- **Quality Standards**: Elevated standards based on successful pattern analysis

### Workflow Optimization Suggestions
- **Automation Opportunities**: Repetitive tasks suitable for streamlining
- **Tool Chain Improvements**: More effective tool combinations and sequences  
- **Performance Enhancements**: Faster execution paths and efficiency gains
- **User Experience**: Improved interaction patterns and reduced friction

## Output Formats

### Analysis Report Structure
```markdown
# Claude Interaction History Analysis

## Executive Summary
- {{TOTAL_SESSIONS}} sessions analyzed across {{PROJECT_COUNT}} projects
- {{SUCCESS_RATE}}% task completion rate
- {{KEY_INSIGHTS}} key optimization opportunities identified

## Usage Patterns
- Most effective tools: {{TOP_TOOLS}}
- Highest success workflows: {{SUCCESS_PATTERNS}}
- Common failure points: {{FAILURE_PATTERNS}}
- Tool error hotspots: {{ERROR_PRONE_TOOLS}}
- Hallucination incidents: {{HALLUCINATION_PATTERNS}}
- User frustration triggers: {{FRUSTRATION_INDICATORS}}

## Recommendations
### Immediate Improvements
- {{URGENT_RECOMMENDATIONS}}

### Component Enhancements
- {{COMPONENT_SUGGESTIONS}}

### Workflow Optimizations
- {{WORKFLOW_IMPROVEMENTS}}

### Error Prevention
- {{ERROR_MITIGATION_STRATEGIES}}

### Reliability Improvements
- {{HALLUCINATION_PREVENTION_MEASURES}}
```

### Prompter Enhancement Suggestions
- **New Component Proposals**: Components addressing identified gaps
- **Existing Component Improvements**: Enhancement suggestions for current components
- **Composition Refinements**: Better component integration patterns
- **Quality Standard Updates**: Elevated standards based on successful interactions

## Integration Points
- Works with thinking.md for complex analysis and reasoning processes
- Uses research_methodologies.md for systematic data analysis approaches
- Supports architecture_patterns.md for system design recommendations
- Integrates with quality_standards.md for recommendation validation

## Quality Standards
- **Data-Driven**: All recommendations backed by quantitative analysis from interaction logs
- **Actionable**: Specific, implementable suggestions with clear success criteria
- **Personalized**: Tailored to user's specific interaction patterns and preferences
- **Continuous**: Designed for ongoing analysis and iterative improvement

## Report Generation Instructions

### File Management
- **Report Directory**: Save all reports to `/Users/{{USERNAME}}/projects/play/prompter/docs/analysis/system_improvement_reports/`
- **Filename Format**: `YYYY-MM-DD_HH-MM-SS_Claude_System_Improvement_Report.md` (includes date AND time to prevent overwrites)
- **Directory Creation**: Ensure directory structure exists before saving

### Error and Frustration Analysis Requirements

#### Tool Error Analysis
- **Error Rate Calculation**: Count tool failures per prompt/session and identify patterns
- **Error Type Classification**: Categorize errors (permission, syntax, timeout, invalid parameters)
- **Tool Combination Analysis**: Identify problematic tool usage sequences
- **Recovery Success Rate**: Track how well different prompts handle tool failures

#### User Frustration Detection
- **Linguistic Indicators**: Look for phrases like "that didn't work", "still failing", "you said it passed but..."
- **Correction Patterns**: Identify when users provide corrective information after system claims success
- **Verification Failures**: Track instances where user verification contradicts system reporting
- **Retry Patterns**: Count how often users ask to repeat or fix the same task

#### Hallucination Pattern Analysis
- **False Success Claims**: Identify cases where system reports success but user verification reveals failures
- **Overconfidence Indicators**: Track instances of definitive claims without proper verification
- **Testing Discrepancies**: Compare system test reports with user-run verification results
- **Status Misrepresentation**: Cases where system incorrectly describes current state or results

### Enhanced Report Structure
```markdown
# Claude System Improvement Report
*Analysis of {{TOTAL_SESSIONS}} sessions from {{DATE_RANGE}}*

## Executive Summary
- Success rate: {{SUCCESS_RATE}}%
- Tool error rate: {{TOOL_ERROR_RATE}}%
- Hallucination incidents: {{HALLUCINATION_COUNT}}
- User frustration events: {{FRUSTRATION_COUNT}}

## Error Analysis
### Tool Failure Patterns
- {{HIGH_ERROR_TOOLS}} tools with highest failure rates
- {{ERROR_PATTERNS}} common error scenarios
- {{RECOVERY_STRATEGIES}} successful recovery approaches

### Hallucination Analysis
- {{HALLUCINATION_TYPES}} types of false confidence claims
- {{VERIFICATION_GAPS}} areas where verification is insufficient
- {{RELIABILITY_ISSUES}} prompts with highest hallucination rates

### User Frustration Indicators
- {{FRUSTRATION_TRIGGERS}} most common causes of user dissatisfaction
- {{CORRECTION_PATTERNS}} how users typically indicate system errors
- {{TRUST_IMPACT}} effect on user confidence and workflow

## Reliability Recommendations
### Error Prevention
- {{ERROR_MITIGATION}} strategies to reduce tool failures
- {{VERIFICATION_IMPROVEMENTS}} better success validation methods
- {{ROBUSTNESS_ENHANCEMENTS}} prompt modifications for error handling

### Hallucination Mitigation
- {{CONFIDENCE_CALIBRATION}} appropriate confidence expression guidelines
- {{VERIFICATION_REQUIREMENTS}} mandatory verification steps for critical operations
- {{UNCERTAINTY_HANDLING}} better approaches for ambiguous situations
```

## Usage Pattern
```
When generating system improvement reports:
1. Analyze historical interaction data from {{USER_CLAUDE_DIR}}
2. Calculate error rates and identify failure patterns
3. Detect user frustration and hallucination incidents
4. Extract successful error recovery strategies
5. Generate comprehensive recommendations for system reliability
6. Save report with datetime filename to prevent overwrites
7. Include specific, actionable suggestions for prompt improvements
```