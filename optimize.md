Please analyze and optimize performance for: $ARGUMENTS.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Parse Scope**:
   - Target: `api:name`, `file:path`, `module:name`, or `all` (default)
   - Type: `speed`, `memory`, `database`, `bundle`
   - Options: `--analyze-only`, `--benchmark`

2. **Find Bottlenecks**:
   - Algorithm complexity (O(n²) → O(n))
   - N+1 database queries
   - Memory leaks and excessive allocation
   - Large bundle dependencies
   - Unnecessary loops and computations
   - Missing caching opportunities

3. **Generate OPTIMIZATION_REPORT.md**:
   - List bottlenecks by severity (Critical >100ms, Major 10-100ms, Minor <10ms)
   - Include current vs optimized code for each issue
   - Show expected performance improvements
   - Categorize as quick wins vs long-term improvements

4. **Apply Optimizations** (unless --analyze-only):
   - Replace slow algorithms with efficient ones
   - Add caching and memoization where beneficial
   - Fix N+1 queries with eager loading
   - Implement lazy loading for heavy components
   - Add database indexes if needed
   - Replace heavy dependencies with lighter alternatives

5. **Add Performance Tests**:
   - Create benchmarks for critical paths
   - Add performance assertions
   - Set up monitoring hooks

6. **Output Summary**:
   Show applied optimizations, performance gains, and next steps.

Focus on user-perceivable improvements and maintain code readability.
