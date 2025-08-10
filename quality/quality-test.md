Please generate comprehensive tests for the specified scope: $ARGUMENTS.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Parse and Understand Scope**:
   Analyze $ARGUMENTS to determine testing scope:
   
   - **File-specific**:
     * "file:path/to/file.js" → Test specific file
     * "src/utils/helper.ts" → Test this exact file
     * "current file" → Test currently open/modified file
   
   - **Module/Component**:
     * "module:auth" → Test entire auth module
     * "component:UserProfile" → Test UserProfile component
     * "service:payment" → Test payment service
   
   - **Directory/Feature**:
     * "dir:src/controllers" → Test all controllers
     * "feature:checkout" → Test checkout feature
     * "api:v2" → Test API v2 endpoints
   
   - **Test Types**:
     * "unit" → Unit tests only (default)
     * "integration" → Integration tests
     * "e2e" → End-to-end tests
     * "all" → Generate all applicable test types
   
   - **Coverage Goals**:
     * "critical" → Test critical paths only
     * "full" → Comprehensive test coverage
     * "missing" → Only generate missing tests
     * "edge-cases" → Focus on edge cases and error handling

2. **Analyze Existing Test Setup**:
   - Check for test framework (Jest, Mocha, Pytest, RSpec, etc.)
   - Find test configuration files
   - Identify test file naming convention (*.test.js, *.spec.ts, test_*.py)
   - Check existing test coverage if available
   - Locate test directories structure
   - Identify mocking libraries in use

3. **Scan Target Code**:
   Based on scope, analyze the code to be tested:
   - List all functions/methods that need testing
   - Identify public APIs and interfaces
   - Find dependencies that need mocking
   - Detect edge cases and error conditions
   - Note any existing tests to avoid duplication
   - Understand business logic and requirements

4. **Generate Test Plan**:
   Create a structured plan of what will be tested:
