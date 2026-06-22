---
name: validate
description: 'Validate files against code standards. Use when: checking code quality, validating file compliance, reviewing files against project standards, running code standard checks. Trigger phrases: validate, check standards, code review, lint files, validate file.'
argument-hint: 'One or more file paths to validate, e.g. src/components/Foo.tsx src/utils/bar.ts'
---

# Validate

Delegates to the **Code Validator** subagent to check one or more files against the project's code standards defined in `AGENTS.md`.

## When to Use

- Checking whether a file or set of files complies with project code standards
- Pre-commit or pre-review quality checks
- Reviewing newly written code against documented rules

## Procedure

1. Collect the file paths the user wants to validate (from the argument or conversation).
2. Invoke the **Code Validator** subagent, passing the file paths as the argument.
3. Return the subagent's validation report directly to the user without modification.
