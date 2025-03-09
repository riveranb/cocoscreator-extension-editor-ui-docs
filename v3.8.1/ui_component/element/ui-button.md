# UI Button Component

## Initialize

### Basic Usage

Basic button:
```html
<ui-button>Button</ui-button>
```

### Types

Primary button:
```html
<ui-button class="primary">Primary Button</ui-button>
```

Success button:
```html
<ui-button class="success">Success Button</ui-button>
```

Warning button:
```html
<ui-button class="warning">Warning Button</ui-button>
```

Danger button:
```html
<ui-button class="danger">Danger Button</ui-button>
```

### States

Disabled button:
```html
<ui-button disabled>Disabled Button</ui-button>
```

Loading button:
```html
<ui-button loading>Loading Button</ui-button>
```

## Parameters

### Attributes
```typescript
disabled; // statement
loading; // statement
```

## Events

### Available Events
```typescript
confirm // click event
```

### Usage Examples

#### Vue.js
```html
<ui-button @confirm="onClick">Click Me</ui-button>
```

#### Vanilla JavaScript
```html
<ui-button id="button">Click Me</ui-button>
```

```javascript
const element = document.getElementById('#button');

// addEventListener
element.addEventListener('confirm', () => {
    console.log('onClick');
});
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a customizable button element with various states and styles. 