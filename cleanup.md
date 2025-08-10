Please perform code cleanup and maintenance for: $ARGUMENTS.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Parse Cleanup Scope**:
   - Target: `file:path`, `module:name`, `dir:path`, or `all` (default)
   - Type: `unused`, `imports`, `console`, `formatting`, `deprecated`, `all`
   - Options: `--dry-run`, `--aggressive`

2. **Scan for Cleanup Opportunities**:
   - Unused variables, functions, and imports
   - Console.log/debug statements
   - Commented-out code blocks
   - Dead code paths (unreachable code)
   - Duplicate code segments
   - Inconsistent formatting
   - Deprecated API usage
   - Empty files and directories
   - Unnecessary type assertions
   - Redundant conditions and expressions

3. **Analyze Dependencies**:
   - Find unused dependencies in package.json
   - Identify duplicate packages
   - Check for deprecated packages
   - Find dev dependencies in production

4. **Generate CLEANUP_REPORT.md**:
   - List all issues found by category
   - Show file paths and line numbers
   - Indicate risk level for each cleanup
   - Estimate impact on bundle size

5. **Apply Cleanup** (unless --dry-run):
   
   Safe cleanups (always apply):
   - Remove unused imports
   - Delete console statements
   - Remove trailing whitespace
   - Fix inconsistent indentation
   - Remove empty comment blocks
   - Delete unnecessary blank lines
   
   Moderate cleanups (apply with care):
   - Remove unused variables and functions
   - Delete commented-out code
   - Simplify redundant conditions
   - Consolidate duplicate imports
   
   Aggressive cleanups (only with --aggressive):
   - Remove entire unused files
   - Delete unused dependencies
   - Refactor duplicate code
   - Remove all TODO/FIXME comments

6. **Organize Code Structure**:
   - Sort imports (external, internal, relative)
   - Group related functions together
   - Order class methods consistently
   - Arrange exports at appropriate locations

7. **Update Configuration**:
   - Clean .gitignore duplicates
   - Remove obsolete config entries
   - Update deprecated settings

8. **Validation**:
   - Run linter to verify no syntax errors
   - Execute tests to ensure functionality
   - Check that build still succeeds

9. **Output Summary**:
   Report files cleaned, lines removed, size reduction, and any warnings.

Maintains functionality while improving code cleanliness and reducing technical debt.
