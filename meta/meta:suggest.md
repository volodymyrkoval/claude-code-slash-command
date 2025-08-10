Please analyze my session history and suggest custom slash commands for repetitive tasks: $ARGUMENTS.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Collect Session History**:
   - Gather all prompts from current session
   - Include recent file operations
   - Note command sequences used
   - Track time spent on similar tasks
   - Options: --last-n 50, --all, --today

2. **Identify Patterns**:
   
   Analyze for:
   - Repeated prompt templates
   - Common file operation sequences
   - Frequent code generation requests
   - Recurring debugging patterns
   - Similar refactoring requests
   - Repeated explanation queries
   - Common workflow combinations

3. **Categorize Repetitive Tasks**:
   
   Group by type:
   - Code Generation (similar components/functions)
   - Debugging (same error types)
   - Refactoring (consistent patterns)
   - Documentation (repeated updates)
   - Testing (similar test scenarios)
   - Integration (API/service patterns)
   - Configuration (setup tasks)

4. **Generate Command Suggestions**:
   
   Create SUGGESTED_COMMANDS.md with:
   - Command name and purpose
   - Frequency detected in session
   - Estimated time savings
   - Pattern that triggered suggestion
   - Full command definition
   - Usage examples
   - Integration with existing workflow

5. **Analyze Workflow Sequences**:
   
   Identify command chains:
   - Common command combinations
   - Typical workflow patterns
   - Suggest macro commands for sequences
   
   Example: If you frequently update API, then tests, then docs, then commit,
   suggest a combined /api-change command

6. **Smart Suggestions**:
   
   Prioritize by:
   - Frequency of repetition
   - Time-saving potential
   - Complexity reduction
   - Error prevention value
   
   Categories:
   - High Value (>5 uses, >10 min saved)
   - Good Value (3-5 uses, 5-10 min saved)
   - Consider (potential future value)

7. **Generate Custom Commands**:
   
   For top suggestions, create ready-to-use definitions:
   - Complete command structure
   - Parameter handling
   - Integration with existing commands
   - Error handling
   - Validation steps

8. **Workflow Optimization Tips**:
   - Suggest command aliases for long commands
   - Recommend parameter defaults
   - Propose command templates
   - Identify missing commands in workflow

9. **Output Summary**:
   Show analysis results with:
   - Number of prompts analyzed
   - Patterns found
   - Top command suggestions with time savings
   - Workflow profile summary
   - Quick wins for immediate improvement

10. **Learning Mode**:
    Store patterns for future suggestions:
    - Track which suggestions were implemented
    - Monitor usage of new commands
    - Refine suggestions over time

Auto-discovers your development patterns and suggests personalized automation.
