Please analyze the project and generate a comprehensive refactoring plan: $ARGUMENTS.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Project Discovery & Analysis**:
   - Run `find . -type f -name "*.{js,ts,py,rb,go,java,cs,php,rs}" | head -50` to understand project languages
   - Check for configuration files (package.json, tsconfig.json, .eslintrc, etc.)
   - Run `tree -L 3 -I 'node_modules|vendor|.git|dist|build'` or equivalent to understand structure
   - Identify the tech stack, frameworks, and architecture patterns in use
   - Check test coverage if available (`npm test -- --coverage`, `pytest --cov`, etc.)

2. **Code Quality Analysis**:
   - **Complexity Issues**:
     * Find functions/methods that are too long (>50 lines)
     * Identify deeply nested code (>3 levels)
     * Detect high cyclomatic complexity
   - **Code Duplication**:
     * Look for repeated code patterns
     * Identify copy-paste programming
     * Find similar functions that could be consolidated
   - **Code Smells**:
     * Large classes/modules doing too much
     * Long parameter lists
     * Dead code and unused variables
     * Magic numbers and hardcoded values
     * Inconsistent naming conventions
   - **Dependency Issues**:
     * Circular dependencies
     * Tightly coupled modules
     * Missing abstractions

3. **Architecture Analysis**:
   - **Structural Issues**:
     * Violations of separation of concerns
     * Missing or incorrect design patterns
     * Improper layering (e.g., business logic in controllers)
     * Lack of proper abstractions/interfaces
   - **Scalability Concerns**:
     * Bottlenecks in current architecture
     * Single points of failure
     * Missing caching strategies
     * Database query optimization needs
   - **Maintainability Issues**:
     * Lack of modularity
     * Poor component boundaries
     * Missing or inadequate error handling
     * Insufficient logging/monitoring points
   - **Security Considerations**:
     * Input validation gaps
     * Authentication/authorization improvements
     * Sensitive data handling

4. **Performance Analysis**:
   - Check for obvious performance anti-patterns
   - Identify N+1 query problems (if applicable)
   - Find synchronous operations that could be async
   - Detect inefficient algorithms or data structures

5. **Generate REFACTORING_PLAN.md**:
   Create a structured markdown file with the following sections:

   ```markdown
   # Refactoring Plan
   
   Generated: [Current Date]
   Project: [Project Name]
   
   ## Executive Summary
   [Brief overview of main findings and recommended priorities]
   
   ## Code Quality Improvements
   
   ### High Priority
   - [ ] **[Issue Name]**
     - Location: `path/to/file.ext`
     - Problem: [Description]
     - Solution: [Proposed fix]
     - Estimated effort: [S/M/L]
     - Impact: [High/Medium/Low]
   
   ### Medium Priority
   [Similar structure]
   
   ### Low Priority
   [Similar structure]
   
   ## Architecture Improvements
   
   ### Critical Changes
   - [ ] **[Improvement Name]**
     - Current state: [Description]
     - Proposed state: [Description]
     - Benefits: [List benefits]
     - Migration strategy: [Steps]
     - Estimated effort: [S/M/L/XL]
   
   ### Recommended Enhancements
   [Similar structure]
   
   ## Performance Optimizations
   - [ ] **[Optimization Name]**
     - Current bottleneck: [Description]
     - Proposed solution: [Description]
     - Expected improvement: [Metrics if possible]
   
   ## Technical Debt Items
   - [ ] **[Debt Item]**
     - Type: [Code/Design/Documentation/Testing]
     - Description: [What needs fixing]
     - Business impact: [Why it matters]
   
   ## Quick Wins
   [List of improvements that can be done in <1 hour each]
   
   ## Implementation Roadmap
   
   ### Phase 1: Foundation
   [Critical fixes and prerequisites]
   
   ### Phase 2: Core Refactoring
   [Main architectural changes]
   
   ### Phase 3: Optimization
   [Performance and quality improvements]
   
   ## Metrics for Success
   - [ ] Code coverage increased to X%
   - [ ] Cyclomatic complexity reduced by Y%
   - [ ] Response time improved by Z%
   - [ ] [Other measurable goals]
   
   ## Risks and Mitigations
   | Risk | Impact | Mitigation |
   |------|--------|------------|
   | [Risk description] | [H/M/L] | [Strategy] |
