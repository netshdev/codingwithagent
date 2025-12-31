---
trigger: always_on
---

# Code Quality Essentials

## Naming Conventions

- Variables & functions: `camelCase` (getUserData, isValid)
- Components: `PascalCase` (UserProfile, Button)
- Constants: `UPPER_SNAKE_CASE` (MAX_RETRIES, API_URL)
- Be descriptive: `isUserAuthenticated` not `isAuth`

## JavaScript Basics

- Use `const` by default, `let` only when reassigning
- Never use `var`
- Use arrow functions for callbacks
- Remove `console.log` before committing
- Use template literals: \`Hello ${name}\` not "Hello " + name

## Functions

- Keep functions small (under 50 lines)
- Functions should do one thing
- Use descriptive names that explain what they do
- Avoid deeply nested code (max 3 levels)

## Code Organization

- One component per file
- Group related files in folders
- Import order: React, libraries, local files
- Remove unused imports and code

## Common Patterns

### Good Practices

```javascript
// Destructure props
const Button = ({ onClick, label }) => (
  <button onClick={onClick}>{label}</button>
);

// Use early returns
const getStatus = (user) => {
  if (!user) return "guest";
  if (user.isPremium) return "premium";
  return "standard";
};

// Named functions for handlers
const handleClick = () => {
  console.log("clicked");
};
```

### Avoid

```javascript
// Don't access props directly
const Button = (props) => (
  <button onClick={props.onClick}>{props.label}</button>
);

// Don't use anonymous functions in JSX
<button onClick={() => handleClick()}>Click</button>;

// Don't nest too deeply
if (condition1) {
  if (condition2) {
    if (condition3) {
      // too deep!
    }
  }
}
```

## Quick Checklist

- [] Descriptive variable name?
- [] Functions under 50 lines?
- [] No console.log statements?
- [] Imports organized?
- [] Dead code removed?
