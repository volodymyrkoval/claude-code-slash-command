Please prepare and commit the current changes: $ARGUMENTS.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Run linters and formatters** to check code quality:
   - Run the project's linter (e.g., `npm run lint`, `eslint .`, `pylint`, `rubocop`, etc.)
   - Run code formatters (e.g., `prettier`, `black`, `gofmt`, etc.)
   - Check for type errors if applicable (e.g., `tsc --noEmit`, `mypy`)

2. **Fix all auto-fixable issues** without changing business logic:
   - Apply automatic linter fixes (e.g., `eslint --fix`, `rubocop -a`)
   - Apply formatter fixes (e.g., `prettier --write`, `black .`)
   - Only fix style, formatting, and non-functional issues
   - DO NOT modify any business logic, algorithms, or functional behavior

3. **Review the changes** to ensure:
   - No business logic was altered
   - Only formatting, style, and linting issues were addressed
   - All files are properly formatted

4. **Stage the changes**:
   - Use `git add -A` or selectively stage files with `git add <files>`
   - Review staged changes with `git diff --staged`

5. **Create an expressive but concise commit message**:
   - Analyze the changes to understand what was modified
   - Follow conventional commit format if applicable (e.g., `fix:`, `feat:`, `chore:`)
   - Keep the message clear and under 50 characters for the subject line
   - Add a body if needed to explain why (not what)
   - Example: "chore: fix linting errors and format code"

6. **Commit the changes**:
   - Execute `git commit -m "<message>"`
   - Verify the commit with `git log -1`

Important constraints:
- NEVER modify business logic, only fix style/formatting issues
- If linting reveals actual bugs or logic issues, report them but don't fix
- If no linting/formatting issues exist, create a commit with existing changes
- Respect project-specific linter configurations (.eslintrc, .prettierrc, etc.)

Context from user (if provided): $ARGUMENTS
