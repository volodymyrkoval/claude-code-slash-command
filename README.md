# Claude Code Slash Commands

A curated collection of optimized slash commands for [Claude Code](https://claude.ai/code) that streamline development workflows through structured, template-based automation.

## Overview

This repository contains 13 laconic slash commands designed to accelerate common development tasks:

- **Planning & Analysis** - Requirements analysis, project overview, refactoring assessment
- **Execution** - Feature implementation, refactoring execution, code commits
- **Testing & Quality** - Test generation, security scanning, performance optimization
- **Documentation & Maintenance** - Code explanation, cleanup, documentation updates

Each command follows a standardized compact format with `Usage: target[:name] [options] [--help]` syntax for quick comprehension and execution.

## Quick Start

### Installation

1. Clone this repository to your Claude Code commands directory:
```bash
git clone https://github.com/volodymyrkoval/claude-code-slash-command.git ~/.claude/commands
```

2. Restart Claude Code to load the new commands

### Basic Usage

Commands follow this pattern:
```bash
/command-name [target] [options]
```

**Examples:**
```bash
/optimize api:users speed --analyze-only     # Analyze API performance
/cleanup module:auth unused --dry-run        # Preview unused code cleanup
/explain function:calculateTotal             # Explain specific function
/commit "fix: resolve user validation bug"   # Commit with message
```

## Available Commands

### 📋 Planning & Analysis
- **`/plan`** - Create detailed feature implementation plans
- **`/overview`** - Generate comprehensive project health dashboard
- **`/refactor-analyze`** - Identify refactoring opportunities and technical debt

### ⚡ Execution  
- **`/plan-execute`** - Execute feature plans with phase-based implementation
- **`/refactor-execute`** - Implement refactoring recommendations
- **`/commit`** - Streamlined linting, formatting, and git commits

### 🧪 Testing & Quality
- **`/tests-generate`** - Generate comprehensive test suites (unit, integration, e2e)
- **`/security-scan`** - Perform security vulnerability analysis and fixes
- **`/optimize`** - Identify and resolve performance bottlenecks
- **`/cleanup`** - Remove unused code and technical debt

### 📚 Documentation & Maintenance
- **`/explain`** - Generate clear code and architecture explanations
- **`/claude-md-update`** - Keep CLAUDE.md synchronized with code changes
- **`/suggest-commands`** - Get contextual command recommendations

## Command Examples

### Feature Development Workflow
```bash
# 1. Plan the feature
/plan "add user authentication with OAuth"

# 2. Execute the implementation
/plan-execute user-auth

# 3. Generate tests
/tests-generate module:auth

# 4. Commit changes
/commit "feat: add OAuth authentication system"
```

### Code Quality Workflow
```bash
# 1. Security analysis
/security-scan all --fix

# 2. Performance optimization
/optimize module:api speed --benchmark

# 3. Code cleanup
/cleanup all unused --aggressive

# 4. Update documentation
/claude-md-update
```

### Analysis & Documentation
```bash
# Explain complex code
/explain function:processPayment

# Project health overview
/overview --detailed

# Analyze refactoring needs
/refactor-analyze module:legacy
```

## Generated Files

Commands create structured output files for tracking and reference:

- `FEATURE_PLAN-{title}.md` - Detailed implementation roadmaps
- `OPTIMIZATION_REPORT.md` - Performance analysis and improvements
- `SECURITY_REPORT.md` - Vulnerability assessments and fixes
- `CLEANUP_REPORT.md` - Code quality issues and resolutions
- `PROJECT_OVERVIEW.md` - Comprehensive project health dashboard
- `EXPLANATION.md` - Code and architecture documentation

## Key Features

### ⚡ **Laconic Design**
Commands use a compact, standardized format that reduces cognitive load while maintaining precision:
- 58% average line reduction from verbose templates
- Standardized `Usage:` syntax across all commands
- Condensed steps into numbered bullet points

### 🎯 **Context-Aware**
- Commands adapt to different project types and tech stacks
- Support various testing frameworks and linting tools
- Progressive disclosure from basic to advanced options

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
/optimize api:users           # Specific API endpoint
/optimize file:src/utils.js   # Individual file
/optimize module:payment      # Entire module
/optimize all                 # Whole project (default)
```

### Execution Modes
Many commands offer execution control:
```bash
/security-scan --fix          # Apply fixes automatically
/cleanup --dry-run            # Preview changes only
/optimize --analyze-only      # Analysis without changes
/plan-execute --phase 1       # Execute specific phase
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