# Agent Validation Checkpoints Component

## Purpose
Provides standardized validation checkpoints to ensure agents demonstrate actual deliverables before claiming success, preventing false confidence claims and building user trust.

## Core Validation Framework

### Pre-Success Verification Protocol
Before claiming task completion, agents MUST:

```yaml
verification_steps:
  1. demonstrate_deliverables:
     - Show actual files created/modified with timestamps
     - Display specific content changes or additions
     - Provide concrete evidence of work completed
     
  2. validate_functionality:
     - Test that claimed functionality actually works
     - Verify integration points and dependencies
     - Confirm no breaking changes introduced
     
  3. user_confirmation_checkpoint:
     - Present summary of work completed with evidence
     - Request user verification: "Please verify this meets your requirements"
     - Wait for explicit user confirmation before proceeding
```

## Validation Checkpoint Templates

### 1. Development Task Completion
```markdown
## Task Completion Verification

**Claimed Work:** {{TASK_DESCRIPTION}}

**Deliverable Evidence:**
- ✅ Files Modified: {{LIST_OF_FILES_WITH_TIMESTAMPS}}
- ✅ Code Changes: {{SUMMARY_OF_CHANGES}}
- ✅ Tests Added/Updated: {{TEST_FILES_AND_COVERAGE}}
- ✅ Functionality Verified: {{VERIFICATION_RESULTS}}

**User Confirmation Required:**
Before marking this task complete, please verify:
1. The code changes meet your requirements
2. The functionality works as expected
3. No existing functionality was broken

Please confirm: "Task completed successfully" or provide feedback for adjustments.
```

### 2. File Operation Validation
```markdown
## File Operation Verification

**Operation Type:** {{CREATE|MODIFY|DELETE}}
**Target Files:** {{FILE_PATHS}}

**Evidence of Completion:**
{{#each files}}
- **File:** {{path}}
  - **Action:** {{action}}
  - **Timestamp:** {{timestamp}}
  - **Size:** {{size}} ({{change_description}})
  - **Content Preview:** 
    ```
    {{content_preview}}
    ```
{{/each}}

**Validation Check:**
I have {{ACTION}} the files as requested. Please verify the changes are correct and complete.
```

### 3. Testing Task Validation
```markdown
## Testing Validation Checkpoint

**Test Scope:** {{TEST_DESCRIPTION}}

**Test Execution Evidence:**
- ✅ Test Files Created: {{TEST_FILE_COUNT}} files
- ✅ Test Coverage: {{COVERAGE_PERCENTAGE}}%
- ✅ Test Results: {{PASS_COUNT}} passed, {{FAIL_COUNT}} failed
- ✅ Test Output:
  ```
  {{TEST_EXECUTION_OUTPUT}}
  ```

**Test Artifacts:**
{{#each test_files}}
- **{{file_name}}**: {{test_count}} tests, covers {{functionality}}
{{/each}}

**Critical Validation:** 
Tests have been EXECUTED (not just created) and results verified. 
User confirmation required before claiming testing complete.
```

### 4. Multi-Step Operation Validation
```markdown
## Multi-Step Operation Checkpoint

**Operation:** {{OPERATION_NAME}}
**Progress:** Step {{CURRENT_STEP}} of {{TOTAL_STEPS}}

**Completed Steps:**
{{#each completed_steps}}
- ✅ Step {{number}}: {{description}}
  - **Evidence:** {{evidence}}
  - **Verification:** {{verification_method}}
{{/each}}

**Current Step Validation:**
**Step {{CURRENT_STEP}}:** {{CURRENT_DESCRIPTION}}
- **Evidence of Completion:** {{EVIDENCE}}
- **Verification Method:** {{VERIFICATION}}
- **Ready for Next Step:** {{YES|NO|NEEDS_USER_CONFIRMATION}}

**User Checkpoint:**
Before proceeding to step {{NEXT_STEP}}, please confirm:
- Current step completed successfully: {{YES|NO}}
- Ready to proceed with next step: {{YES|NO}}
- Any adjustments needed: {{FEEDBACK}}
```

## Error Recovery Templates

### 1. Failed Operation Recovery
```markdown
## Operation Failure Recovery

**Failed Operation:** {{OPERATION}}
**Error Details:** {{ERROR_MESSAGE}}
**Impact Assessment:** {{IMPACT_DESCRIPTION}}

**Recovery Options:**
1. **Retry:** {{RETRY_APPROACH}}
2. **Alternative:** {{ALTERNATIVE_APPROACH}}  
3. **Manual Intervention:** {{MANUAL_STEPS_NEEDED}}

**User Decision Required:**
How would you like to proceed? Please select:
- [ ] Retry with same approach
- [ ] Try alternative approach  
- [ ] Manual intervention required
- [ ] Cancel operation
```

### 2. Partial Success Handling
```markdown
## Partial Success Notification

**Operation:** {{OPERATION}}
**Status:** Partially Completed

**Successful Components:**
{{#each successful}}
- ✅ {{component}}: {{result}}
{{/each}}

**Failed Components:**
{{#each failed}}
- ❌ {{component}}: {{error}}
{{/each}}

**User Validation Required:**
1. Are the successful components acceptable as-is?
2. Should I attempt to fix the failed components?
3. Do you need the partial results rolled back?

Please advise on how to proceed.
```

## Confidence Calibration Guidelines

### Success Claim Language
**Use:** "I believe this is completed successfully. Please verify..."
**Avoid:** "Task completed successfully" (without verification)

**Use:** "The following work has been done. Please confirm it meets your needs..."
**Avoid:** "Everything is working perfectly"

**Use:** "Tests were executed with the following results. Please review..."
**Avoid:** "All tests pass" (without showing actual results)

### Uncertainty Expression
When uncertain, agents should:
- Explicitly state confidence level: "I'm 80% confident this is correct..."
- Request validation: "Please verify this approach before I proceed"
- Offer alternatives: "I see two possible approaches. Which would you prefer?"

## Implementation Guidelines

### Integration Points
- Use with all task completion claims
- Required for file operations, testing, and complex workflows
- Integrate with user feedback loops
- Support rollback operations when validation fails

### Quality Standards
- **Evidence-Based:** Every claim backed by concrete evidence
- **User-Centric:** User confirmation required for critical operations
- **Transparent:** Clear about limitations and uncertainties
- **Recoverable:** Clear recovery options when operations fail

## Usage Examples

### Template Usage in Agent Prompts
```yaml
task_completion_template: |
  When completing any task, use the appropriate validation template:
  1. Gather evidence of completion
  2. Present deliverables clearly  
  3. Request user verification
  4. Wait for confirmation before claiming success
  
validation_integration: |
  Before stating "task completed":
  1. Use agent_success_verification.md template
  2. Fill in all required evidence fields
  3. Present to user for confirmation
  4. Only claim success after user validation
```

This template ensures agents build trust through verification while preventing the false confidence issues identified in the system improvement analysis.