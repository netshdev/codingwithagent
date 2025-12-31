---
trigger: always_on
---

# React Component Basics

## Component Structure

- Use functional components with hooks (not class components)
- Destructure props at function signature
- Keep components under 200 lines
- One component per file

## Props

````javascript
// Good: Destructure props
const UserCard = ({name, email, onEdit}) => (
  <div>
    <h2>{name}</h2>
    <p>{email}</p>
    <button onClick={onEdit}>Edit</button>
  </div>
);

// Bad: Using props object
const UserCard = (props) => (
  <div>
    <h2>{props.name}</h2>
    <p>{props.email}</p>
    <button onClick={props.onEdit}>Edit</button>
  </div>
);

## Hooks Basic

### useState
Use for local UI state only (modals, toggles, input values)
```javascript
const [isOpen, setIsOpen] = useState(false);
const [count, setCount] = useState(0);
````

### useEffect

Use for side effects (API calls, subscriptions, timers)

```javascript
useEffect(() => {
  // Do something
  fetchData();

  // Cleanup (optional)
  return () => cleanup();
}, [dependencies]); // Don't forget dependencies!
```

### useCallback

Prevent function recreation on every render

```javascript
const handleClick = useCallback(() => {
  doSomething();
}, [dependencies]);
```

## JSX Best Practices

- Use semantic HTML (button, nav, header, footer)
- No anonymous functions in JSX: onClick={handleClick} not onClick={() => handleClick()}
- Keys must be from data, not array index: key={item.id} not key={index}
- Use fragments <></> instead of unnecessary divs
- Conditional rendering: use boolean values only

## Common Patterns

### Event Handlers

```javascript
// Good: Named function
const handleSubmit = (e) => {
  e.preventDefault();
  submitForm();
};

<form onSubmit={handleSubmit}>

// Bad: Anonymous function
<form onSubmit={(e) => {
  e.preventDefault();
  submitForm();
}}>
```

### Conditional Rendering

```javascript
// Good: Boolean condition
{
  isLoggedIn && <Dashboard />;
}

// Good: Ternary for two states
{
  isLoading ? <Spinner /> : <Content />;
}

// Bad: Can accidentally render "0"
{
  count && <Display />;
}
```

### Lists

```javascript
// Good: Key from data
{
  users.map((user) => <UserCard key={user.id} {...user} />);
}

// Bad: Index as key
{
  users.map((user, index) => <UserCard key={index} {...user} />);
}
```

### Component Organization

```javascript
const MyComponent = ({ prop1, prop2 }) => {
  // 1. Hooks
  const [state, setState] = useState();

  // 2. Event handlers
  const handleClick = () => {
    // handle click
  };

  // 3. Early returns
  if (!prop1) return null;

  // 4. Render
  return <div>{/* JSX here */}</div>;
};
```

## Avoid

- Class components (use functional components)
- Direct DOM manipulation (use refs sparingly)
- Inline styles (use CSS/styled-components)
- Prop drilling beyond 3 levels (use context or Redux)
- Components over 200 lines (break them down)

## Quick Checklist

- [] Using functional components?
- [] Props destructured?
- [] Event handlers named?
- [] Keys from data, not index?
- [] Component under 200 lines?
- [] useEffect has dependencies?
