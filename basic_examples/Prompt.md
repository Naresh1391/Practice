Before creating a new utility, search the project for any existing log sanitization, encoding, escaping, or security utility that can safely handle CWE-117.

If one exists, reuse it.

If none exists, propose the smallest reusable LogSanitizer needed for CR/LF log-injection protection.

Do not modify files yet.
Keep the response concise.
Fix only the first 5 CWE-117 findings using the approved/common sanitization pattern.
Rules:
No business-logic changes.
No unrelated refactoring.
Preserve existing logger levels/messages.
Modify only required files.
Do not analyze unrelated vulnerabilities.
After editing, give only:
files changed
findings fixed
tests run/results
