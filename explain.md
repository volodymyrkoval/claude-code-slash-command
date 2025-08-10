Please explain the specified code or architecture: $ARGUMENTS.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Parse Explanation Target**:
   - `file:path` - Explain specific file
   - `function:name` - Explain function/method
   - `module:name` - Explain module architecture
   - `architecture` - Explain overall system design
   - `flow:feature` - Explain feature workflow
   - `current` - Explain recent changes

2. **Analyze Target**:
   - Read and understand the code/structure
   - Identify key patterns and dependencies
   - Trace data flow and execution paths
   - Note complex logic or algorithms

3. **Generate Explanation**:
   
   Create EXPLANATION.md with:
   - Purpose and responsibility
   - How it works (step-by-step)
   - Key algorithms and logic
   - Dependencies and interactions
   - Input/output specifications
   - Edge cases and error handling
   - Usage examples
   - Potential improvements

4. **Add Visual Aids** (where helpful):
   - Flow diagrams in Mermaid format
   - ASCII diagrams for simple structures
   - Sequence diagrams for interactions
   - Component relationship maps

5. **Explain Complexity**:
   - Break down complex algorithms
   - Clarify business logic
   - Document design decisions
   - Explain performance considerations

6. **Output Summary**:
   Provide clear, concise explanation tailored to the target's complexity level.

Makes complex code understandable and documents institutional knowledge.
