# UI Grid Component

## Initialize

### Basic Usage

```html
<ui-grid></ui-grid>
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
<ui-grid
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
></ui-grid>
```

#### Vanilla JavaScript
```html
<ui-grid id="ui-grid"></ui-grid>
```

```typescript
const element = document.getElementById('#ui-grid');

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
const element = document.getElementById('#ui-grid');
// set value
element.value = 'value';

// get value
const gridValue = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a grid layout system for organizing and arranging UI elements in a structured manner. 