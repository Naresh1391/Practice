For the 154 through-wrapper findings:
Implement CR/LF neutralization at the appropriate central logging boundary in MessageLoggerImpl.
Reuse an existing project sanitizer if one exists; otherwise create the smallest appropriate reusable sanitizer.
Preserve existing log levels, messages, and application behavior.
Do not modify business logic.
For the 8 bypass findings:
Fix them individually using the same validated CR/LF neutralization approach where appropriate.
Do not blindly change unrelated logger statements.
If any bypass requires different handling, leave it unchanged and report why.
Keep the changes minimal:
