# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This repository contains a collection of Claude Code slash commands implemented as structured Markdown files. Each command follows a detailed template-based approach for executing complex development workflows.

## Architecture

### Command Structure
- Commands are organized in purpose-based directories for better maintainability
- Commands use a standardized laconic format with compact usage syntax
- Each command follows the pattern: `Action for: $ARGUMENTS` followed by `Usage: target[:name] [options] [--help]`
- Commands support help flags (`--help` or `-h`) for documentation
- Arguments are passed via `$ARGUMENTS` placeholder and parsed within each command
- Steps are condensed into numbered bullet points for quick comprehension

### Directory Structure

Commands are organized by development workflow phase with namespace-style naming:

```
/commands/
├── plan/           # plan:*
│   ├── feature.md - Analyzes requirements and creates detailed feature implementation plans
│   └── refactor.md - Analyzes code for refactoring opportunities
├── analyze/        # analyze:*  
│   ├── project.md - Provides comprehensive project health and metrics overview
│   ├── security.md - Performs security vulnerability analysis and fixes
│   └── performance.md - Performance bottleneck identification and optimization
├── exec/           # exec:*
│   ├── feature.md - Executes feature plans created by the planning commands
│   └── refactor.md - Implements refactoring recommendations
├── quality/        # quality:*
│   ├── test.md - Generates comprehensive test suites with multiple test types
│   ├── cleanup.md - Concise code cleanup and technical debt removal
│   └── validate.md - Validates implementation for bugs and errors
├── docs/           # docs:*
│   ├── explain.md - Laconic code and architecture explanation generator
│   ├── readme.md - Updates project README.md with current features and setup
│   └── update-context.md - Updates CLAUDE.md based on recent code changes
└── meta/           # meta:*
    ├── commit.md - Streamlined linting, formatting, and committing workflow
    └── suggest.md - Suggests relevant slash commands for current context
```

### Command Categories

**Planning Phase** (`plan:*`): Strategic planning and requirement analysis
**Analysis Phase** (`analyze:*`): Deep analysis of project, security, and performance
**Implementation Phase** (`exec:*`): Execution of planned changes and improvements
**Quality Phase** (`quality:*`): Testing, cleanup, and quality assurance
**Documentation Phase** (`docs:*`): Documentation generation and maintenance
**Meta/Workflow Phase** (`meta:*`): Git workflow and command suggestions

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
/type:command [arguments] [--flags]
```

### Common Workflows
1. **Feature Development**: `/plan:feature feature-name` → `/exec:feature feature-name` → `/meta:commit`
2. **Code Quality**: `/analyze:security` → `/quality:test` → `/analyze:performance`  
3. **Project Health**: `/analyze:project` → `/quality:cleanup` → `/docs:update-context`
4. **Refactoring**: `/plan:refactor` → `/exec:refactor` → `/quality:test` → `/meta:commit`

### Generated Files
Commands create structured output files:
- `FEATURE_PLAN-{title}.md` - Detailed implementation plans
- `SECURITY_REPORT.md` - Security analysis results
- `PROJECT_OVERVIEW.md` - Project health dashboard

## Development Notes

- No package.json or build system detected - this is a documentation/command repository
- Commands follow workflow-phase organization with namespace-style naming for easy discovery
- Commands are designed to work across different project types and tech stacks
- Recent optimization focused on laconic, precise command structure (58% average line reduction)
- Commands maintain full functionality while using standardized compact format
- Each command includes comprehensive error handling and validation
- Commands maintain compatibility with various testing frameworks and linting tools
- Namespace-style naming (type:command) enables intuitive command discovery by development phase