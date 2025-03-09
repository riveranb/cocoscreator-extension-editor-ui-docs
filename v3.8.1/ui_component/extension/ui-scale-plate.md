# UI Scale Plate Component

## Initialize

### Basic Usage

```html
<ui-scale-plate></ui-scale-plate>
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
<ui-scale-plate
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
></ui-scale-plate>
```

#### Vanilla JavaScript
```html
<ui-scale-plate id="ui-scale-plate"></ui-scale-plate>
```

```typescript
const element = document.getElementById('#ui-scale-plate');

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
const element = document.getElementById('#ui-scale-plate');
// set value
element.value = 'value';

// get value
const scaleValue = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a scale plate interface for precise scaling and measurement operations. 