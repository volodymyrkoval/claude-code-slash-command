Please analyze recent changes and update the CLAUDE.md file if needed: $ARGUMENTS.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Analyze recent changes** in the project:
   - Run `git diff` to see uncommitted changes
   - Run `git diff --staged` to see staged changes
   - Run `git log --oneline -10` to see recent commits context
   - Identify what has been modified (new features, removed code, refactoring, dependencies, etc.)

2. **Read the current CLAUDE.md file**:
   - Open and read the entire CLAUDE.md file
   - Understand its current structure and content
   - Note what sections exist (architecture, features, setup, API docs, etc.)

3. **Determine what needs updating** based on the changes:
   - New features or functionality → Update feature list/documentation
   - New files or modules → Update project structure section
   - New dependencies → Update dependencies/requirements section
   - New APIs or endpoints → Update API documentation
   - Configuration changes → Update setup/configuration section
   - Removed features → Remove outdated documentation
   - Refactoring → Update architecture or implementation details
   - New environment variables → Update configuration section
   - New scripts or commands → Update usage/scripts section
   - Bug fixes worth noting → Update known issues or changelog

4. **Update CLAUDE.md** if changes are relevant:
   - Maintain the existing file structure and formatting style
   - Add new sections only if necessary
   - Keep descriptions clear and concise
   - Update code examples if they've changed
   - Ensure technical accuracy
   - Update the last modified date if the file has one
   - DO NOT remove existing valid information unless it's outdated
   - DO NOT make trivial updates for minor code style changes

5. **Review the updates**:
   - Show a diff of CLAUDE.md changes
   - Ensure updates accurately reflect the code changes
   - Verify no important information was accidentally removed

6. **Stage the updated file**:
   - If changes were made: `git add CLAUDE.md`
   - If no changes needed: Report that CLAUDE.md is already up to date

7. **Provide a summary** of what was updated or why no updates were needed

Decision criteria for updates:
- ✅ Update for: structural changes, new features, API changes, new dependencies
- ✅ Update for: significant refactoring, new configuration options
- ❌ Skip for: code formatting, minor bug fixes, internal refactoring
- ❌ Skip for: changes that don't affect usage or understanding

Context from user (if provided): $ARGUMENTS
