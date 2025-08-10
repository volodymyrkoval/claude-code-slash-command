# Claude Code Slash Commands

A curated collection of workflow-optimized slash commands for [Claude Code](https://claude.ai/code) using intuitive namespace-style naming (`type:command`) to streamline development workflows through structured automation.

## Overview

This repository contains 16 workflow-optimized slash commands with namespace-style naming designed to accelerate development tasks:

- **Planning** (`plan:*`) - Requirements analysis and strategic planning
- **Analysis** (`analyze:*`) - Deep analysis of project, security, and performance
- **Implementation** (`exec:*`) - Execution of planned changes and improvements  
- **Quality** (`quality:*`) - Testing, cleanup, and quality assurance
- **Documentation** (`docs:*`) - Documentation generation and maintenance
- **Meta/Workflow** (`meta:*`) - Git workflow and command suggestions

Each command follows a namespace pattern (`type:command`) with standardized `Usage: target[:name] [options] [--help]` syntax for intuitive discovery and quick execution.

## Quick Start

### Installation

1. Clone this repository to your Claude Code commands directory:
```bash
git clone https://github.com/volodymyrkoval/claude-code-slash-command.git ~/.claude/commands
```

2. Restart Claude Code to load the new commands

### Basic Usage

Commands follow this namespace pattern:
```bash
/type:command [target] [options]
```

**Examples:**
```bash
/analyze:performance api:users speed --analyze-only  # Analyze API performance
/quality:cleanup module:auth unused --dry-run       # Preview unused code cleanup
/docs:explain function:calculateTotal               # Explain specific function
/meta:discuss patterns:error-handling               # Discuss error handling approaches
/meta:commit "fix: resolve user validation bug"     # Commit with message
```

## Available Commands

### 📋 Planning Phase (`plan:*`)
- **`/plan:feature`** - Create detailed feature implementation plans
- **`/plan:refactor`** - Identify refactoring opportunities and technical debt

### 🔍 Analysis Phase (`analyze:*`)  
- **`/analyze:project`** - Generate comprehensive project health dashboard
- **`/analyze:security`** - Perform security vulnerability analysis and fixes
- **`/analyze:performance`** - Identify and resolve performance bottlenecks

### ⚡ Implementation Phase (`exec:*`)
- **`/exec:feature`** - Execute feature plans with phase-based implementation
- **`/exec:refactor`** - Implement refactoring recommendations

### 🧪 Quality Phase (`quality:*`)
- **`/quality:test`** - Generate comprehensive test suites (unit, integration, e2e)
- **`/quality:cleanup`** - Remove unused code and technical debt
- **`/quality:validate`** - Validate implementation for bugs and errors

### 📚 Documentation Phase (`docs:*`)
- **`/docs:explain`** - Generate clear code and architecture explanations
- **`/docs:readme`** - Update project README.md with current features and setup
- **`/docs:update-context`** - Keep CLAUDE.md synchronized with code changes

### 🔧 Meta/Workflow Phase (`meta:*`)
- **`/meta:commit`** - Streamlined linting, formatting, and git commits
- **`/meta:discuss`** - Discuss code and project topics without making changes
- **`/meta:suggest`** - Get contextual command recommendations

## Command Examples

### Feature Development Workflow
```bash
# 1. Plan the feature
/plan:feature "add user authentication with OAuth"

# 2. Execute the implementation
/exec:feature user-auth

# 3. Generate tests and validate
/quality:test module:auth
/quality:validate module:auth

# 4. Commit changes
/meta:commit "feat: add OAuth authentication system"
```

### Code Quality Workflow
```bash
# 1. Security analysis
/analyze:security all --fix

# 2. Performance optimization
/analyze:performance module:api speed --benchmark

# 3. Code cleanup
/quality:cleanup all unused --aggressive

# 4. Update documentation  
/docs:readme features
/docs:update-context
```

### Analysis & Documentation
```bash
# Explain complex code
/docs:explain function:processPayment

# Discuss architecture decisions
/meta:discuss architecture:payment-flow

# Project health overview
/analyze:project --detailed

# Analyze refactoring needs
/plan:refactor module:legacy
```

## Generated Files

Commands create structured output files for tracking and reference:

- `FEATURE_PLAN-{title}.md` - Detailed implementation roadmaps
- `OPTIMIZATION_REPORT.md` - Performance analysis and improvements
- `SECURITY_REPORT.md` - Vulnerability assessments and fixes
- `CLEANUP_REPORT.md` - Code quality issues and resolutions
- `VALIDATION_REPORT.md` - Bug analysis and implementation validation
- `PROJECT_OVERVIEW.md` - Comprehensive project health dashboard
- `EXPLANATION.md` - Code and architecture documentation

## Key Features

### ⚡ **Laconic Design**
Commands use a compact, standardized format that reduces cognitive load while maintaining precision:
- 58% average line reduction from verbose templates
- Standardized `Usage:` syntax across all commands
- Condensed steps into numbered bullet points

### 🎯 **Workflow-Optimized**
- Commands organized by development lifecycle phase
- Namespace-style naming (type:command) for clear categorization
- Intuitive command structure enables quick discovery
- Support various testing frameworks and linting tools

### 🔄 **Workflow Integration** 
- Phase-based execution with checkpoints
- Progress tracking and status updates
- Automatic rollback and error recovery
- Subagent delegation for complex tasks

### 📊 **Comprehensive Output**
- Structured reports with severity levels
- Before/after comparisons
- Actionable recommendations
- Performance metrics and trends

## Advanced Usage

### Help System
Every command supports detailed help:
```bash
/command-name --help
```

### Targeting Options
Commands support flexible targeting:
```bash
/analyze:performance api:users           # Specific API endpoint
/analyze:performance file:src/utils.js   # Individual file
/analyze:performance module:payment      # Entire module
/analyze:performance all                 # Whole project (default)
```

### Execution Modes
Many commands offer execution control:
```bash
/analyze:security --fix           # Apply fixes automatically
/quality:cleanup --dry-run        # Preview changes only
/analyze:performance --analyze-only # Analysis without changes
/exec:feature --phase 1           # Execute specific phase
```

## Architecture

### Command Structure
- **Template-based**: Standardized markdown format for consistency
- **Argument parsing**: `$ARGUMENTS` placeholder with flexible option handling  
- **Progressive execution**: Step-by-step implementation with validation
- **Error handling**: Comprehensive error recovery and rollback mechanisms

### Integration Patterns
- **Subagent delegation** for complex algorithmic tasks
- **Phase-based execution** for large operations
- **Status tracking** in generated plan files
- **Cross-command workflows** for comprehensive development cycles

## Contributing

1. Fork the repository
2. Create commands following the established laconic format
3. Include comprehensive help documentation
4. Add usage examples to this README
5. Update CLAUDE.md with architectural changes

## License

MIT License - feel free to adapt these commands for your development workflows.

---

**Optimized for efficiency. Built for Claude Code.**