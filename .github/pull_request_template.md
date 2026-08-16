## Pull Request Description

### Summary of Changes
<!-- Describe the changes introduced by this pull request. Be concise and precise. -->

### Checklist for Contributors & Copilot Agents
<!-- Please ensure all items are completed before merging. -->
- [ ] No syntax errors in PHP/JavaScript/HTML.
- [ ] Code adheres to the style guide and conventions defined in `.github/copilot-instructions.md`.
- [ ] All inputs are strictly sanitized and outputs are properly escaped.
- [ ] CSRF nonces are used for any form submission or dynamic links.
- [ ] No credentials, secret keys, or private environment variables are committed.

---

## 🤖 Instructions for Specialized Copilot Agents

When reviewing or executing tasks on this Pull Request, specialized agents must follow these instructions:

### 🔍 Copilot Code-Review Agent (`@copilot code-review`)
- Analyze the diff carefully.
- Ensure that no unused global variables, shadowed functions, or redundant dependencies are introduced.
- Verify that custom class, function, or variable names are properly prefixed to avoid namespace collisions.
- Check that the UI/layout changes render perfectly across responsive breakpoints.

### 🛡️ Copilot Security-Review Agent (`@copilot security-review`)
- Perform a thorough audit of the code changes for common web vulnerabilities (OWASP Top 10, WordPress-specific security issues).
- Ensure all PHP query manipulations use prepared statements (`$wpdb->prepare` or equivalent PDO preparation).
- Ensure zero Cross-Site Scripting (XSS) opportunities exist; verify output escaping matches context (`esc_html`, `esc_attr`, `esc_url`, etc.).
- Ensure authorization checks (`current_user_can()` or similar) are performed prior to execution of sensitive actions.
