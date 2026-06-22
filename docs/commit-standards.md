# Commit Standards

All commits must follow the [Conventional Commits](https://www.conventionalcommits.org/) specification.

## Format

```text
<type>(<scope>): <subject>

[optional body]

[optional footer]
```

## Types

| Type       | When to use                                             |
| ---------- | ------------------------------------------------------- |
| `feat`     | A new feature                                           |
| `fix`      | A bug fix                                               |
| `chore`    | Maintenance tasks, dependency updates, build changes    |
| `refactor` | Code change that neither fixes a bug nor adds a feature |
| `style`    | Formatting, whitespace — no logic change                |
| `test`     | Adding or updating tests                                |
| `docs`     | Documentation only changes                              |
| `perf`     | Performance improvements                                |
| `revert`   | Reverting a previous commit                             |

## Rules

- **Subject**: lowercase, no trailing period, imperative mood (e.g., `add user login` not `added user login`)
- **Subject length**: 72 characters max
- **Body**: omit the body for small, self-explanatory changes. Only include a body when additional context is necessary to understand the motivation or impact of the change.
- **Scope**: optional, lowercase, refers to the affected module or area (e.g., `auth`, `router`, `query`)
- **Breaking changes**: append `!` after the type/scope (e.g., `feat!:`) and describe in the footer with `BREAKING CHANGE: <description>`
- **Language**: English only

## Examples

```text
feat(auth): add JWT refresh token support
fix(query): handle 401 response in query client
chore: upgrade react-query to v5
refactor(router): simplify lazy loading setup
test(utils): add unit tests for formatDate
docs: update commit standards
feat!: replace axios with fetch

BREAKING CHANGE: axios instance is no longer exported
```
