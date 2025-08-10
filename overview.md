Please provide a comprehensive project overview: $ARGUMENTS.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Parse Overview Type**:
   - Scope: `health`, `plans`, `metrics`, `history`, `all` (default)
   - Options: `--detailed`, `--summary`, `--recent`

2. **Gather Project Information**:
   
   Project Structure:
   - Primary language and framework
   - Number of files and directories
   - Total lines of code
   - Repository age and size
   
   Code Quality Metrics:
   - Test coverage percentage
   - Linting issues count
   - Code complexity metrics
   - Technical debt indicators

3. **Check Pending Work**:
   
   Active Plans:
   - FEATURE_PLAN-*.md files (status: pending/in-progress/completed)
   - REFACTORING_PLAN.md items (completed vs remaining)
   - OPTIMIZATION_REPORT.md recommendations
   - SECURITY_REPORT.md unresolved issues
   
   Recent Activity:
   - Last 10 slash commands executed
   - Recent file modifications
   - Latest test results
   - Recent commits

4. **Analyze Code Health**:
   - Outdated dependencies count
   - Security vulnerabilities
   - Performance bottlenecks identified
   - Test failures or skipped tests
   - Build warnings

5. **Generate PROJECT_OVERVIEW.md**:
   
   Include sections for:
   - Executive Summary (health score, main concerns)
   - Project Statistics
   - Code Quality Metrics
   - Pending Tasks and Plans
   - Recent Activity Log
   - Recommendations for Next Actions
   - Progress Trends (if historical data available)

6. **Create Dashboard View**:
    ### Project Overview
        Health Score: [A/B/C/D/F] based on metrics
   
    #### 📊 Metrics:

        - Coverage: X%
        - Dependencies: Y outdated, Z vulnerable
        - Tech Debt: N hours estimated
        - Open Tasks: M items

    #### 📋 Active Plans:

        - Feature Plans: X pending, Y in-progress
        - Refactoring: Z items remaining
        - Security: N critical issues

    #### 🏃 Recent Activity:

        - Last command: [command] [time ago]
        - Last commit: [message] [time ago]
        - Last test run: [pass/fail] [time ago]

    #### ⚠️ Attention Needed:

        - [Critical security issue]
        - [Failing tests]
        - [Outdated dependencies]

    #### ✨ Suggested Actions:

        - [Most impactful next step]
        - [Second priority]
        - [Third priority]

7. **Check Documentation Status**:
- README.md last updated
- CLAUDE.md synchronization status
- Missing documentation areas
- Outdated documentation sections

8. **Performance Baseline**:
- Current performance metrics
- Optimization opportunities
- Bundle size trends
- Load time statistics

9. **Team Workflow Insights**:
- Most used slash commands
- Common refactoring patterns
- Typical workflow sequences
- Productivity metrics

10. **Output Summary**:
 Provide actionable overview with health score, key metrics, and prioritized recommendations.

Gives a bird's-eye view of project health and guides next development actions.
