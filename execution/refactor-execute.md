Please execute specific refactoring tasks from REFACTORING_PLAN.md: $ARGUMENTS.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Read and Parse REFACTORING_PLAN.md**:
   - Open and read the entire REFACTORING_PLAN.md file
   - Parse all sections and identify actionable items (marked with checkboxes [ ])
   - Create an indexed list of all refactoring tasks with their details
   - Note the priority, effort estimate, and location for each task

2. **Interpret Execution Request**:
   Analyze $ARGUMENTS to determine what to execute:
   
   - **If specific item mentioned**: 
     * Match by task name, section, or description
     * Examples: "execute high priority items", "fix the user service complexity"
   
   - **If priority specified**:
     * "high priority" → Execute all High Priority items
     * "quick wins" → Execute all Quick Wins section items
     * "low effort" → Execute all items marked as effort: S
   
   - **If phase specified**:
     * "phase 1" → Execute Phase 1 from Implementation Roadmap
     * "foundation" → Execute foundation phase items
   
   - **If category specified**:
     * "code quality" → Execute Code Quality Improvements
     * "architecture" → Execute Architecture Improvements
     * "performance" → Execute Performance Optimizations
     * "testing" → Execute Testing Improvements
   
   - **If number specified**:
     * "first 3" → Execute first 3 items by priority
     * "top 5" → Execute top 5 highest priority items
   
   - **If no specification or unclear**:
     * List all available sections and counts
     * Ask which specific items to execute
     * Provide examples of valid commands

3. **Confirm Selection**:
   - Display the selected refactoring items to be executed
   - Show their descriptions, locations, and estimated effort
   - List them with numbers for reference
   - State: "Ready to execute [N] refactoring tasks. Proceeding..."

4. **Execute Selected Refactoring Tasks**:
   For each selected task:
   
   a. **Announce current task**:
      - Print: "Executing: [Task Name]"
      - Show the file/location being modified
   
   b. **Implement the refactoring**:
      - Open the specified files
      - Make the described changes
      - Follow the solution/proposed fix from the plan
      - Maintain existing functionality (refactoring, not changing behavior)
   
   c. **Validate changes**:
      - Run relevant tests if they exist
      - Check that the code still compiles/runs
      - Verify no functionality was broken
   
   d. **Update task status**:
      - Mark the task as completed in memory
      - Track what was changed for summary

5. **Run Tests and Validation**:
   - Execute the project's test suite if available
   - Run linters to ensure code quality
   - Check for any introduced issues
   - If tests fail, note which refactoring might have caused it

6. **Update REFACTORING_PLAN.md**:
   - Mark completed items with [x] instead of [ ]
   - Add completion date next to executed items
   - Add a "## Execution Log" section if it doesn't exist
   - Log: "[Date] - Executed: [list of completed items]"
   - Update any metrics if measurable

7. **Generate Execution Summary**:
