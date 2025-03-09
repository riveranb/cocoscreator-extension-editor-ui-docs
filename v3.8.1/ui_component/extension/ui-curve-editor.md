# UI Curve Editor Component

## Initialize

### Basic Usage

```html
<ui-curve-editor></ui-curve-editor>
```

## Parameters

### Attributes
```typescript
value
disabled
readonly
invalid
hidden
```

## Events

### Available Events
```typescript
change
confirm
```

### Usage Examples

#### Vue.js
```html
<ui-curve-editor
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
></ui-curve-editor>
```

#### Vanilla JavaScript
```html
<ui-curve-editor id="ui-curve-editor"></ui-curve-editor>
```

```typescript
const element = document.getElementById('#ui-curve-editor');

// addEventListener
element.addEventListener('change', (event) => {
    // changed value
    console.log(event.target.value)
});
element.addEventListener('confirm', (event) => {
    // confirm value
    console.log(event.target.value)
});
```

## Methods

### Get/Set Value
```typescript
const element = document.getElementById('#ui-curve-editor');
// set value
element.value = 'value';

// get value
const curveValue = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a curve editor interface for creating and editing animation curves and other curve-based data. 