# Antigravity - Strict Profile

Maximum enforcement with zero tolerance for violations.

## What's Included

6 comprehensive rule files:

- `accessibility.md` - WCAG 2.1 AAA standards
- `code-quality.md` - 90% coverage, TypeScript mandatory
- `react-components.md` - 100% component coverage, strict hooks
- `testing.md` - 90% minimum, zero flaky tests
- `pull-request-review.md` - 2+ approvals, strict SLA
- `security.md` - OWASP compliance, zero vulnerabilities

## Installation

```bash
npx codingwithagent init
# Select tool: 3. Antigravity
# Select profile: 3. Strict
```

## Files created

```
.agent/rules/
├── accessibility.md
├── code-quality.md
├── react-components.md
├── testing.md
├── pull-request-review.md
└── security.md
```

## Requirements

- TypeScript (no `any` type)
- Components max 150 lines
- Lighthouse accessibility: 100
- Security vulnerabilities: 0
- Performance score: >90

## Warning

Only use if committed to maximum quality.
