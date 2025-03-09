# UI Gradient Picker Component

## Initialize

### Basic Usage

```html
<ui-gradient-picker></ui-gradient-picker>
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
<ui-gradient-picker
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
></ui-gradient-picker>
```

#### Vanilla JavaScript
```html
<ui-gradient-picker id="ui-gradient-picker"></ui-gradient-picker>
```

```typescript
const element = document.getElementById('#ui-gradient-picker');

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
const element = document.getElementById('#ui-gradient-picker');
// set value
element.value = 'value';

// get value
const gradientValue = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a gradient picker interface for creating and editing color gradients with support for multiple color stops and opacity. 