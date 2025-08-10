Please execute the feature plan from FEATURE_PLAN-$ARGUMENTS.md file.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Locate and Load Plan**:
   - If $ARGUMENTS provided: Look for `FEATURE_PLAN-$ARGUMENTS.md`
   - If no arguments: List all available FEATURE_PLAN-*.md files
   - Read the entire plan file
   - Parse all phases, steps, and code snippets
   - Check plan status (PENDING/IN_PROGRESS/COMPLETED)

2. **Validate Prerequisites**:
   - Verify all mentioned files exist (for modifications)
   - Check if required dependencies are available
   - Ensure no conflicting changes in progress
   - Validate that the plan is complete and executable
   - If issues found, report and ask for confirmation to proceed

3. **Display Execution Overview**:
    ```
    Feature Plan Execution
    Plan: FEATURE_PLAN-{feature-title}.md
    Feature: [Feature Name]
    Total Phases: [N]
    Total Steps: [N]
    Files to Create: [N]
    Files to Modify: [N]
    Execution Strategy: [Sequential/Parallel where safe]
    Proceeding with execution...
    ```
4. **Execute Plan Phases**:

For each phase in the plan:

a. **Announce Phase**:
   ```
   ========================================
   PHASE [N]: [Phase Name]
   Steps to execute: [N]
   ========================================
   ```

b. **Execute Each Step**:
   
   For each step in the phase:
   
   i. **Announce Step**:
      ```
      → Executing Step [N.M]: [Step Name]
        File: [path/to/file]
        Action: [CREATE/MODIFY/DELETE]
      ```
   
   ii. **Implement Changes**:
      - Open/Create the specified file
      - Apply the exact code changes from the plan
      - If code snippets are provided, use them exactly
      - If logic needs adaptation, use subagent for complex parts
   
   iii. **Use Subagent for Complex Implementation** (if needed):
      ```
      When the plan specifies complex logic without full implementation:
      - "Implement the algorithm described in step X.Y"
      - "Generate the optimized query for requirement Z"
      - "Create the state machine based on specifications"
      ```
   
   iv. **Validate Step**:
      - Check syntax (compile/parse)
      - Run relevant unit tests if they exist
      - Verify no breaking changes introduced
   
   v. **Report Step Completion**:
      ```
      ✓ Step [N.M] completed successfully
        Changes applied to: [file]
      ```

c. **Phase Checkpoint**:
   - After each phase, validate the system still works
   - Run tests if specified in the plan
   - Option to pause for review if risk is high
   - Update plan status to track progress

5. **Handle Dependencies & Configuration**:

When the plan specifies new dependencies:

a. **Install Dependencies**:
   ```bash
   npm install [packages]  # for Node.js
   pip install [packages]  # for Python
   bundle add [gems]       # for Ruby
   ```

b. **Update Configuration**:
   - Apply configuration changes as specified
   - Update environment variable templates
   - Modify config files

6. **Execute Testing Phase**:

If the plan includes a testing phase:

a. **Generate Tests**:
   - Create test files as specified in plan
   - Implement test cases from the plan

b. **Run Tests**:
   - Execute unit tests
   - Run integration tests
   - Report test results

c. **Use Subagent for Test Generation** (if needed):
   ```
   For complex test scenarios:
   - "Generate comprehensive test cases for [feature]"
   - "Create mock data for [test scenario]"
   ```

7. **Documentation Updates**:

As specified in the plan:
- Update README.md
- Update CLAUDE.md
- Add API documentation
- Update configuration docs

8. **Progress Tracking**:

Throughout execution:
- Mark completed steps in memory
- Track which files were modified
- Log any deviations from the plan
- Note any errors or warnings

9. **Error Handling**:

If an error occurs:

a. **Capture Error Details**:
   - Which step failed
   - Error message
   - Current state

b. **Attempt Recovery**:
   - Try alternative approach if available
   - Use subagent to solve unexpected issues
   - Skip non-critical steps if appropriate

c. **Rollback Option**:
   ```
   Error in Step [N.M]: [Error description]
   
   Options:
   1. Retry step with modifications
   2. Skip this step (if non-critical)
   3. Rollback all changes
   4. Pause for manual intervention
   
   Attempting automatic recovery...
   ```

10. **Update Plan Status**:
 
 After execution:
 - Update plan file with execution status
 - Mark completed steps with [x]
 - Add execution timestamp
 - Log any deviations or issues
 
 ```markdown
 ## Execution Log
 
 Execution Date: [Date]
 Status: COMPLETED/PARTIAL/FAILED
 
 Completed Steps:
 - [x] Step 1.1: [Result]
 - [x] Step 1.2: [Result]
 
 Issues Encountered:
 - [Any problems and resolutions]
 
 Deviations from Plan:
 - [Any changes made during execution]
 ```

11. **Final Validation**:
 
 - Run full test suite
 - Check that feature works as expected
 - Verify no regressions introduced
 - Validate performance impact

12. **Execution Summary**:
 ```
 Feature Plan Execution Complete
 ================================
 Plan: FEATURE_PLAN-{feature-title}.md
 Status: SUCCESS/PARTIAL/FAILED
 
 Execution Results:
 ✓ Phases Completed: [N/N]
 ✓ Steps Executed: [N/N]
 ✓ Files Created: [N]
 ✓ Files Modified: [N]
 ✓ Tests Passing: [N/N]
 
 Changes Made:
 - [Summary of key changes]
 
 Feature Status:
 - [Feature is now functional/partially functional/needs fixes]
 
 Next Steps:
 1. Review changes: git diff
 2. Run tests: [test command]
 3. Update docs: /update-claude-md
 4. Commit: /commit feat: [feature name]
 
 Warnings/Notes:
 - [Any important notes for the developer]
 ```

13. **Cleanup**:
 - Remove temporary files if any
 - Update plan status to COMPLETED
 - Suggest next actions

Execution Modes (via $ARGUMENTS):
- `{feature-title}` - Execute specific plan
- `{feature-title} --phase 1` - Execute only phase 1
- `{feature-title} --dry-run` - Show what would be done
- `{feature-title} --continue` - Continue from last failure
- No arguments - List available plans to execute

Subagent Usage During Execution:
- For implementing complex algorithms
- For generating optimal code
- For solving unexpected problems
- For creating test data
- For optimizing performance-critical sections
