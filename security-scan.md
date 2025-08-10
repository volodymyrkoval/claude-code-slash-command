Please perform security analysis for: $ARGUMENTS.

Follow these steps:

0. Check for Help Flag:
   If $ARGUMENTS contains --help or -h:
   - Display command documentation
   - Exit without executing

1. **Parse Scan Scope**:
   - Target: `file:path`, `module:name`, `api`, `auth`, or `all` (default)
   - Level: `critical`, `high`, `medium`, `low`, `all`
   - Options: `--fix`, `--owasp`, `--dependencies`

2. **Scan for Security Vulnerabilities**:
   
   Critical Issues:
   - Hardcoded secrets, API keys, passwords
   - SQL injection vulnerabilities
   - Command injection risks
   - Path traversal vulnerabilities
   - Unsafe deserialization
   - Missing authentication/authorization
   
   High Priority:
   - Cross-site scripting (XSS) risks
   - Insecure direct object references
   - Weak cryptography or hashing
   - Missing input validation
   - Exposed sensitive data in logs
   - CORS misconfigurations
   
   Medium Priority:
   - Missing rate limiting
   - Insufficient logging
   - Weak session management
   - Missing CSRF protection
   - Outdated dependencies with CVEs
   - Missing security headers
   
   Low Priority:
   - Information disclosure in errors
   - Missing HTTPS enforcement
   - Verbose error messages
   - Development code in production

3. **Check Dependencies**:
   - Scan for known vulnerabilities (CVE database)
   - Check dependency licenses for issues
   - Identify outdated security-critical packages
   - Find packages with security advisories

4. **Analyze Authentication & Authorization**:
   - Password storage methods
   - Token generation and validation
   - Session management
   - Permission checks
   - Multi-factor authentication

5. **Review Data Handling**:
   - Input sanitization practices
   - Output encoding
   - Database query construction
   - File upload validation
   - API response filtering

6. **Generate SECURITY_REPORT.md**:
   - Vulnerabilities by severity with CVSS scores
   - Affected files and line numbers
   - Exploitation scenarios
   - Recommended fixes with code examples
   - Compliance check results (OWASP Top 10)

7. **Apply Fixes** (if --fix flag):
   
   Automatic fixes:
   - Add input validation
   - Escape output properly
   - Update vulnerable dependencies
   - Add security headers
   - Remove exposed secrets
   - Implement rate limiting
   
   Manual review required:
   - Authentication flow changes
   - Authorization logic updates
   - Cryptography implementation
   - Database query restructuring

8. **Add Security Tests**:
   - Create tests for input validation
   - Add authentication/authorization tests
   - Test for injection vulnerabilities
   - Verify security headers

9. **Generate Security Configuration**:
   - Create/update security headers config
   - Add rate limiting rules
   - Set up CSP policies
   - Configure CORS properly

10. **Output Summary**:
    Report vulnerabilities found, fixes applied, remaining risks, and compliance status.

Prioritizes fixing exploitable vulnerabilities while maintaining functionality.
