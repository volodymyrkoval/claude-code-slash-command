# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This repository contains a collection of Claude Code slash commands implemented as structured Markdown files. Each command follows a detailed template-based approach for executing complex development workflows.

## Architecture

### Command Structure
- All commands are stored as `.md` files in the root directory
- Commands use a standardized laconic format with compact usage syntax
- Each command follows the pattern: `Action for: $ARGUMENTS` followed by `Usage: target[:name] [options] [--help]`
- Commands support help flags (`--help` or `-h`) for documentation
- Arguments are passed via `$ARGUMENTS` placeholder and parsed within each command
- Steps are condensed into numbered bullet points for quick comprehension

### Command Categories

**Planning & Analysis:**
- `plan.md` - Analyzes requirements and creates detailed feature implementation plans
- `overview.md` - Provides comprehensive project health and metrics overview
- `refactor-analyze.md` - Analyzes code for refactoring opportunities

**Execution:**
- `plan-execute.md` - Executes feature plans created by the planning commands
- `refactor-execute.md` - Implements refactoring recommendations
- `commit.md` - Streamlined linting, formatting, and committing workflow

**Testing & Quality:**
- `tests-generate.md` - Generates comprehensive test suites with multiple test types
- `security-scan.md` - Performs security vulnerability analysis and fixes
- `optimize.md` - Streamlined performance bottleneck identification and optimization
- `cleanup.md` - Concise code cleanup and technical debt removal

**Documentation & Maintenance:**
- `claude-md-update.md` - Updates CLAUDE.md based on recent code changes
- `suggest-commands.md` - Suggests relevant slash commands for current context
- `explain.md` - Laconic code and architecture explanation generator

### Key Patterns

**Subagent Integration:** Commands frequently delegate complex logic to specialized agents:
```markdown
Use Subagent for Complex Implementation (if needed):
- "Implement the algorithm described in step X.Y"
- "Generate the optimized query for requirement Z"
```

**Phase-Based Execution:** Large operations are broken into phases with checkpoints:
```markdown
Phase 1: Foundation
Phase 2: Core Implementation  
Phase 3: Integration
Phase 4: Testing & Validation
```

**Progress Tracking:** Commands update plan status and maintain execution logs in generated files like `FEATURE_PLAN-*.md`.

**Error Handling:** Structured error recovery with rollback options and automatic retry mechanisms.

## Command Usage

### Basic Command Pattern
```bash
/command-name [arguments] [--flags]
```

### Common Workflows
1. **Feature Development**: `/plan feature-name` → `/plan-execute feature-name` → `/commit`
2. **Code Quality**: `/security-scan` → `/tests-generate` → `/optimize`  
3. **Maintenance**: `/overview` → `/cleanup` → `/claude-md-update`

### Generated Files
Commands create structured output files:
- `FEATURE_PLAN-{title}.md` - Detailed implementation plans
- `SECURITY_REPORT.md` - Security analysis results
- `PROJECT_OVERVIEW.md` - Project health dashboard

## Development Notes

- No package.json or build system detected - this is a documentation/command repository
- Commands are designed to work across different project types and tech stacks
- Recent optimization focused on laconic, precise command structure (58% average line reduction)
- Commands maintain full functionality while using standardized compact format
- Each command includes comprehensive error handling and validation
- Commands maintain compatibility with various testing frameworks and linting tools