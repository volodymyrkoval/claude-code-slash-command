Analyze and optimize performance for: $ARGUMENTS

Usage: target[:name] [type] [--analyze-only] [--benchmark] [--help]
- Target: api, file, module, all (default)
- Type: speed, memory, database, bundle

1. **Find Bottlenecks**: O(n²)→O(n), N+1 queries, memory leaks, large dependencies, unnecessary loops, missing cache
2. **Generate OPTIMIZATION_REPORT.md**: List by severity (Critical >100ms, Major 10-100ms, Minor <10ms), show improvements
3. **Apply Optimizations**: Replace slow algorithms, add caching, fix N+1 queries, lazy loading, indexes, lighter dependencies
4. **Add Performance Tests**: Benchmarks, assertions, monitoring
5. **Output Summary**: Show gains and next steps

Focus on user-perceivable improvements and maintain code readability.
