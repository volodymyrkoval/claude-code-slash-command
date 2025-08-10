Prepare and commit current changes: $ARGUMENTS

Usage: [message] [--help]

1. **Run Quality Checks**: Linter, formatter, type checker
2. **Auto-Fix**: Apply linter/formatter fixes (style only, NO business logic changes)  
3. **Review**: Ensure only formatting/style changes applied
4. **Stage**: `git add -A`, review with `git diff --staged`
5. **Commit**: Create conventional commit message (<50 chars), execute `git commit`
6. **Verify**: Check with `git log -1`

Important constraints:
- NEVER modify business logic, only fix style/formatting issues
- If linting reveals actual bugs or logic issues, report them but don't fix
- If no linting/formatting issues exist, create a commit with existing changes
- Respect project-specific linter configurations (.eslintrc, .prettierrc, etc.)

Context from user (if provided): $ARGUMENTS
