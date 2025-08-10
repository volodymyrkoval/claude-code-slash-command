Please analyze the codebase and create a comprehensive plan for implementing: $ARGUMENTS.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Parse Feature Requirements**:
   - Extract the feature description from $ARGUMENTS
   - Identify key requirements and constraints
   - Generate a short feature title (kebab-case) for the filename
   - Example: "add oauth authentication" → "oauth-auth"

2. **Deep Code Analysis Phase**:
   
   a. **Understand Current Architecture**:
      - Map the current project structure
      - Identify relevant modules, services, and components
      - Understand data flow and dependencies
      - Find similar existing patterns to follow
   
   b. **Impact Analysis**:
      - Identify all files that will need changes
      - Find integration points
      - Detect potential breaking changes
      - List affected tests
      - Identify configuration changes needed
   
   c. **Research Phase** (use subagent if needed):
      ```
      If the problem is complex, delegate research to a subagent:
      - "Research best practices for [technology/pattern]"
      - "Analyze security implications of [approach]"
      - "Find optimal algorithm for [problem]"
      - "Review similar implementations in the codebase"
      ```

3. **Solution Design**:
   
   a. **Consider Multiple Approaches**:
      - Generate 2-3 different implementation strategies
      - Evaluate pros/cons of each approach
      - Consider performance, maintainability, and scalability
      - Select the optimal approach with justification
   
   b. **Technical Decisions**:
      - Choose design patterns to use
      - Decide on data structures
      - Plan error handling strategy
      - Define interfaces/contracts
      - Plan for backwards compatibility
   
   c. **Use Subagent for Complex Logic** (if needed):
      ```
      For complex algorithmic problems:
      - "Design algorithm for [specific problem]"
      - "Optimize database schema for [use case]"
      - "Create state machine for [workflow]"
      ```

4. **Create Detailed Implementation Plan**:
   
   Generate `FEATURE_PLAN-{short-feature-title}.md`:
   
   ```markdown
   # Feature Plan: [Feature Name]
   
   Generated: [Date]
   Status: PENDING
   Estimated Effort: [S/M/L/XL]
   Risk Level: [Low/Medium/High]
   
   ## Overview
   **Objective**: [Clear description of what we're building]
   **User Story**: As a [user], I want [feature] so that [benefit]
   **Success Criteria**: 
   - [ ] [Measurable outcome 1]
   - [ ] [Measurable outcome 2]
   
   ## Technical Analysis
   
   ### Current State
   - [Description of current implementation]
   - Key files involved: [list]
   - Current limitations: [list]
   
   ### Proposed Solution
   [Detailed description of the chosen approach]
   
   ### Alternative Approaches Considered
   1. **[Approach 1]**: [Description]
      - Pros: [list]
      - Cons: [list]
      - Reason not chosen: [explanation]
   
   ## Implementation Steps
   
   ### Phase 1: Foundation
   #### Step 1.1: [Task Name]
   - **File**: `path/to/file.ext`
   - **Action**: CREATE/MODIFY/DELETE
   - **Changes**:
     ```[language]
     // Specific code to add/modify
     function newFeature() {
       // Implementation details
     }
     ```
   - **Rationale**: [Why this change is needed]
   
   #### Step 1.2: [Task Name]
   [Similar structure...]
   
   ### Phase 2: Core Implementation
   [Detailed steps with code snippets...]
   
   ### Phase 3: Integration
   [Steps for integrating with existing code...]
   
   ### Phase 4: Testing & Validation
   [Test cases to implement...]
   
   ## File Changes Summary
   
   ### Files to Create:
   - `path/to/new/file1.ext` - [Purpose]
   - `path/to/new/file2.ext` - [Purpose]
   
   ### Files to Modify:
   - `path/to/existing/file1.ext` - [What changes]
   - `path/to/existing/file2.ext` - [What changes]
   
   ### Files to Delete:
   - `path/to/deprecated/file.ext` - [Why removing]
   
   ## Dependencies & Configuration
   
   ### New Dependencies:
   ```json
   {
     "package-name": "^1.0.0"
   }
